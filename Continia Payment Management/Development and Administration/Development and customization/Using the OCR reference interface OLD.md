---
title: Using the OCR reference interface
description: A guide on how to use the OCR reference
date: 18-02-2021
id:
lang: en
---

# Using the OCR reference interface

This page explains how you can use Payment Management's OCR reference interface to create OCR-strings for use with reports like for example invoices and reminders. The interface codeunit exposes functions which you can use to create the OCR-string.

For more information on how to create and use a dependency see the [Microsoft Docs](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-json-files) (search for **Dependencies**).

## OCR reference for sales invoices or reminders

The OCR interface is a code unit that exposes a couple of functions. This example shows how to use the interface with a posted sales invoice.

1. **Add a dependency to Payment Management 365.**
   In the App.json file of your app add a dependency to Payment Management 365. Use the following information:

   Appid: 14340ba6-5934-4145-8e14-dbf1846fef80

   Name: Continia Payment Management 365

   Publisher: Continia Software

   In the screenshot below is an example of how to insert the dependency:

![Dependency](/images/PM365/ocr dependency.png)

2. **Create a function to get an OCR reference**.

   In your app you are now able to call the functions from the interface.

   Create for instance a codeunit in your app where you create a function to call the interface from Payment.

   In the screenshot below is an example of a functions that calls the interface to generate a FIK reference with card type 71:

![Get reference](/images/PM365/get ocr reference.png)

3. **Call the procedure from a report.**

   The function created in step 2 can now be called from inside a report and placed on a RDLC or Word Layout.

   A. Create global variables to hold a label and the value of the OCR reference 

   ![Variables](/images/PM365/global variables.png)
   

   B. Add the global variables to the dataset of the report

   ![Add variables](/images/PM365/add global variables.png)
   

   C. Create a local function on the report that calls the function from step 2.

   ![Local function](/images/PM365/local function.png)

   D. The function could be called from inside the reports OnAfterGetRecord() trigger on the header dataitem to generate the OCR Reference:

   ![Call function](/images/PM365/call function.png)

4. **Add the label and the OCR reference to the layout of the report**

  The label and the reference can now be added to the report.

## OCR reference for reports

The OCR Reference interface provides the possibility to create OCR references intended for use with Reports. 

The interface contains a procedure which will return an OCR reference that can be added to the Invoice/Reminder Reports.

The procedure have two overloads that can be utilized: 

>  /// <summary>
>
>  /// Creates an OCR reference based On the Document No. and Document Type on the Header record.
>
> /// </summary>
>
> /// <param name="SalesHeader", Type="Record: Sales Header">The Sales Header for which the OCR reference will be created.</param>
>
>  /// <param name="OCRRefType", Type="Enum CPM OCR Reference Type">The type of OCR reference that will be created. Allowed values: 04, 15, 71, 75</param>
>
>   /// <returnvalue name="PaymentID", Type="Text">The OCR reference created based on the Header values and OCR Reference Type</returnvalue>
>
> procedure GenerateOcrReference(SalesHeader: Record "Sales Header"; OCRRefType: Enum "CPM OCR Reference Type") PaymentID: Text;

<br/>

> /// <summary>
>
>  /// Creates an OCR reference based On the Document No. and Document Type on the Header record.
>
> /// </summary>
>
> /// <param name="ReminderHeader", Type="Record: Reminder Header">The Reminder Header for which the OCR reference will be created.</param>
>
>  /// <param name="OCRRefType", Type="Enum CPM OCR Reference Type">The type of OCR reference that will be created. Allowed values: 04, 15, 71, 75</param>
>
>  /// <returnvalue name="PaymentID", Type="Text">The OCR reference created based on the Header values and OCR Reference Type</returnvalue>
>
> procedure GenerateOcrReference(ReminderHeader: Record "Reminder Header"; OCRRefType: Enum "CPM OCR Reference Type") PaymentID: Text;

In order to use the two procedures the "CPM OCR Reference Type" must be implemented.

