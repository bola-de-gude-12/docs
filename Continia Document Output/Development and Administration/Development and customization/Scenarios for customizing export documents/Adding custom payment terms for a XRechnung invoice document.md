---
title: Adding custom payment terms for a XRechnung invoice document
date: 14-07-2023
description: 
id: DO-117  
lang: en
---

# Adding custom payment terms for a XRechnung invoice document

This article describes a scenario

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

The XRechnung format has specific rules concerning payment terms. In the Event Publisher, you can customize the value at the following path:

/Invoice/PaymentTerms/Note

The *OnBeforePaymentTerms* event handler is triggered before handling the payment terms in the PEPPOL process

## Code sample

```[EventSubscriber(ObjectType::Codeunit, 6086243, 'OnBeforePaymentTerms', '', true, true)]
procedure OnBeforePaymentTermsPEPPOL(
    SalesInvoiceHeader: Record "Sales Invoice Header";
    var RootNode: Codeunit "CSC XML Node";
    var PaymentTermsText: Text[1024];
    var Handled: Boolean)
begin
    // The desired value for the path '/Invoice/PaymentTerms/Note'
    PaymentTermsText := 'Test Payment Terms';

    // Handled means we added the XML Node to the RootNode, therefore false.
    Handled := false;
end;
```

If the *Handled* variable is set to true, the code in this example will not create the *PaymentTerms* node. In such cases, you must manually append this node to the Root node.

