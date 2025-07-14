---
title: Adding the invoice period to a PEPPOL invoice document
date: 14-07-2023
description: 
id: DO-118 
lang: en
---

# Adding the invoice period to a PEPPOL invoice document



> [!IMPORTANT]
>
> The code examples provided in this guide are meant for inspiration and testing purposes only. They should not be used in production solutions.

Prerequisites:

* Continia Delivery Network version 2.0.0.1 or higher
* App Extension that uses the following Continia apps: 
  * Continia Core version 5.0.0.0
  * Continia Delivery Network version 2.0.0.1

In scenarios where there is no Event Publisher available to easily modify a value, you can use one of Continia's generic Event Publishers, such as *OnAfterCreateHeader*. This event is triggered immediately after all the Header fields have been created.

To make desired changes, you have the flexibility to utilize your own XML library or the Continia Core XML Codeunits. You can use the RootNode variable to add a new XML element.

```
```

```al
[EventSubscriber(ObjectType::Codeunit, 6086240, 'OnAfterCreateHeader', '', true, true)]
procedure OnAfterCreateHeaderPEPPOL(
    SalesInvoiceHeader: Record "Sales Invoice Header";
    var XmlDoc: Codeunit "CSC XML Document";
    var RootNode: Codeunit "CSC XML Node")
var
    InvoicePeriodNode: Codeunit "CSC XML Node";
    TempNode: Codeunit "CSC XML Node";
begin
    // Create the NamespaceManager based on the attributes of the root Node
    XmlDoc.CreateNamespaceManager;

    // Create the InvoicePeriod node. Elements containing undernodes must have the cac prefix (cac:InvoicePeriod) and the below namespace URL.
    XmlDoc.CreateNode(InvoicePeriodNode, 'element', 'cac:InvoicePeriod', 'urn:oasis:names:specification:ubl:schema:xsd:CommonAggregateComponents-2');

    // Create the child node of InvoicePeriod node. Elements containing values must have the cbc prefix (cac:InvoicePeriod) and the below namespace URL.
    XmlDoc.CreateNode(TempNode, 'element', 'cbc:StartDate', 'urn:oasis:names:specification:ubl:schema:xsd:CommonBasicComponents-2');
    // Set the desired value
    TempNode.SetInnerText(FORMAT(SalesInvoiceHeader."Posting Date", 0, 9));
    // Append the child node
    InvoicePeriodNode.AppendChild(TempNode);

    XmlDoc.CreateNode(TempNode, 'element', 'cbc:EndDate', 'urn:oasis:names:specification:ubl:schema:xsd:CommonBasicComponents-2');
    TempNode.SetInnerText(FORMAT(SalesInvoiceHeader."Posting Date", 0, 9));
    InvoicePeriodNode.AppendChild(TempNode);

    XmlDoc.CreateNode(TempNode, 'element', 'cbc:Description', 'urn:oasis:names:specification:ubl:schema:xsd:CommonBasicComponents-2');
    TempNode.SetInnerText('Invoice Period');
    InvoicePeriodNode.AppendChild(TempNode);

    // Append the InvoicePeriod node to the Root node.
    RootNode.AppendChild(InvoicePeriodNode);
end;
```

You can achieve the same level of customization by using our Codeunit CTS-CDN XML Library:

```
[EventSubscriber(ObjectType::Codeunit, Codeunit::"CTS-CDN PEPPOL BIS3 Inv.", 'OnAfterCreateHeader', '', true, true)]
local procedure OnAfterCreateHeaderPEPPOL(
    SalesInvoiceHeader: Record "Sales Invoice Header";
    var XmlDoc: Codeunit "CSC XML Document";
    var RootNode: Codeunit "CSC XML Node")
var
    CDNXMLLibrary: Codeunit "CTS-CDN XML Library";
    TempNode: Codeunit "CSC XML Node";
    TempNode2: Codeunit "CSC XML Node";
begin
    // Set the XML Doc to the XML library
    CDNXMLLibrary.SetXmlDoc(XmlDoc);

    // Create the Namespaces records, eliminating the need to know the Namespace 	URL later on
    CDNXMLLibrary.CreateNSRecordsFromXmlDoc();

    CDNXMLLibrary.AppendChildNodeTo(RootNode, TempNode, 'cac', 'InvoicePeriod', 	'', TRUE);
    // The function receives a Variant for the value, eliminating the need for 		value formatting
    CDNXMLLibrary.AppendChildNodeTo(TempNode, TempNode2, 'cbc', 'StartDate', 		SalesInvoiceHeader."Posting Date", TRUE);
    CDNXMLLibrary.AppendChildNodeTo(TempNode, TempNode2, 'cbc', 'EndDate', 			SalesInvoiceHeader."Posting Date", TRUE);
    CDNXMLLibrary.AppendChildNodeTo(TempNode, TempNode2, 'cbc', 'Description', 		'Invoice Period', TRUE);
    CDNXMLLibrary.GetXmlDoc(XmlDoc);
end;

```

