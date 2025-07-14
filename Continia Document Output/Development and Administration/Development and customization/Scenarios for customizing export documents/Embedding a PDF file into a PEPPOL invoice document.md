---
title: Embedding a PDF file into a PEPPOL invoice document
date: 14-07-2023
description: 
id: DO-116
lang: en
---

# Embedding a PDF file into a PEPPOL invoice document

This article describes a scenario

> [!IMPORTANT]
>
> The code examples provided in this guide are meant for inspiration and testing purposes only. They should not be used in production solutions.

## Prerequisites

* Continia Delivery Network version 2.0.0.1 or higher
* App Extension that uses the following Continia apps: 
  * Continia Core version 5.0.0.0
  * Continia Delivery Network version 2.0.0.1

## Event

By subscribing to the "OnCreateAdditionalDocRef" event of Codeunit 6086240 "CTS-CDN PEPPOL BIS3 Inv.," you can include additional documents in PEPPOL invoice documents. For example, a PDF file.

To add a file to a PEPPOL invoice document:

* Load the file into the TempBlob variable and provide a filename. Optionally, you can also specify an ID value for reference purposes.

## Code sample

```
[EventSubscriber(ObjectType::Codeunit, 6086241, 'OnCreateAdditionalDocRef', '', true, true)]
procedure OnCreatedAdditionalDocRefPEPPOL(
	SalesInvoiceHeader: Record "Sales Invoice Header"; 
	var TempBlob: Record "CSC Temp Blob" temporary; 
	var Filename: Text[1024]; 
	var ID: Text[1024]; 
	var Handled: Boolean)
var
	SalesReport: Report "Standard Sales - Invoice";
	SalesInvFilter: Record "Sales Invoice Header";
	WriteStream: OutStream;
	Param: Text;
begin
	Clear(TempBlob);
	TempBlob.Blob.CreateOutStream(WriteStream);

	// Fill Write Stream with the required file ->>
	SalesInvFilter.SetRange("No.", SalesInvoiceHeader."No.");
	SalesReport.SetTableView(SalesInvFilter);
	Param := GetReportParam(SalesInvoiceHeader);
	SalesReport.SaveAs(Param, ReportFormat::Pdf, WriteStream);
	// <--

	// Filename with extension. The file extension will be used to generate the 	MimeCode value 
	Filename := StrSubstNo('Sales Invoice %1.pdf', SalesInvoiceHeader."No.");

	// The desired value for the path '/Invoice/AdditionalDocumentReference/ID'
	ID := SalesInvoiceHeader."No.";

	Handled := true;

end;
```

