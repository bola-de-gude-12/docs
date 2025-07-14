---
title: Modifying line values
date: 14-07-2023
description: 
id: DO-120
lang: en
---

# Modifying line values

This article describes a scenario where

> [!IMPORTANT]
>
> The code examples provided in this guide are meant for inspiration and testing purposes only. They should not be used in production solutions.

## Prerequisites

This scenario only works for

* Continia Delivery Network version 2.0.0.1 or higher
* App Extension that uses the following Continia apps: 
  * Continia Core version 5.0.0.0
  * Continia Delivery Network version 2.0.0.1

## Event

In this scenario, we can leverage the event "OnAfterCreateLines" to  modify XML values within the InvoiceLine. Specifically, we aim to ensure that the "PriceAmount" is always positive and the "InvoicedQuantity" is negative if the "PriceAmount" is negative.

## Code sample

```
[EventSubscriber(ObjectType::Codeunit, 6086240, 'OnAfterCreateLines', '', TRUE, true)]
local procedure OnAfterCreateLines(SalesInvoiceHeader: Record "Sales Invoice Header"; VAR XmlDoc: Codeunit "CSC XML Document"; VAR LineNodeList: Codeunit "CSC XML NodeList")
var
  LineList: Codeunit "CSC XML NodeList";
  LineNode: Codeunit "CSC XML Node";
  PriceNode: Codeunit "CSC XML Node";
  InvoicedQtyNode: Codeunit "CSC XML Node";
  PriceAmount: Decimal;
  i: Integer;
begin
  XmlDoc.CreateNamespaceManager();
  XmlDoc.SelectNodes(LineList, '/ns:Invoice/cac:InvoiceLine');
  for i := 0 to LineList.Count() - 1 do begin
    LineList.GetItem(LineNode, i);
    XmlDoc.SelectSingleNode(PriceNode, 			StrSubstNo('/ns:Invoice/cac:InvoiceLine[%1]/cac:Price/cbc:PriceAmount', i + 1));
    if Evaluate(PriceAmount, PriceNode.InnerText()) AND (PriceAmount< 0) then begin
      PriceAmount:= Abs(PriceAmount);
      PriceNode.SetInnerText(format(PriceAmount, 0, 9));
      XmlDoc.SelectSingleNode(InvoicedQtyNode, strSubstNo('/ns:Invoice/cac:InvoiceLine[%1]/cbc:InvoicedQuantity', i + 1));
      InvoicedQtyNode.SetInnerText('-' + InvoicedQtyNode.GetInnerText());
    end;
  end;
end;
```

