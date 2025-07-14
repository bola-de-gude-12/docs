---
title: To set up KID payments
date: 14-07-2023
description: 
id: DO-119
lang: en
---

# Setting up KID payments 

This article describes a scenario where you can set up KID payments in Peppol documents. 

> [!IMPORTANT]
>
> The code examples provided in this guide are meant for inspiration and testing purposes only. They should not be used in production solutions.

## Prerequisites

This scenario only works for:

* Continia Delivery Network version 2.0.0.1 or higher
* App Extension that uses the following Continia apps: 
  * Continia Core version 5.0.0.0
  * Continia Delivery Network version 2.0.0.1

## Event

In the context of setting up KID (Kundeidentifikation) payments in PEPPOL documents, you can utilize the following event:

*OnBeforePaymentMeans*



## Code sample

```al
/ Event Subscriber for setting up KID Payments in PEPPOL documents
[EventSubscriber(ObjectType::Codeunit, Codeunit::"CTS-CDN PEPPOL BIS3 Inv.", 'OnBeforePaymentMeans', '', true, true)]
procedure OnBeforePaymentMeansKID(
    SalesInvoiceHeader: Record "Sales Invoice Header";
    var RootNode: Codeunit "CSC XML Node";
    var PaymentType: Option Bank, KID, FIK;
    var PaymentID: Text[1024];
    var AccountID: Code[50];
    var FinancialInstitutionBranchID: Text[1024];
    var Handled: Boolean)
begin
    PaymentType := PaymentType::KID;
    // Set the KID Payment information here
    // ...
end;
```

