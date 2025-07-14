---
title: Using the OCR reference interface
description: A guide on how to use the OCR reference
date: 24-08-2021
id: PM-10
lang: en
---

# Using the OCR Reference Interface

Payment Management's OCR reference interface can create OCR strings for customer documents such as invoices and reminders. 

For more information on creating and using dependencies, see [Microsoft Docs](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-json-files) (search for **Dependencies**).

## Setting up an OCR interface

The procedure described in this article provides an example of how to set up an OCR interface in your payment solution. The procedure's outcome may vary depending on how the programming is done.

> [!TIP]
>
> To use the document type in the reference, use the following options: Invoice = 0, Account Statement = 1, Reminder = 2, Interest Note = 3

To set up an OCR interface:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Sales & Receivables Setup**.

2. On the **Sales & Receivables Setup** page under the FastTab **General**, ensure that the **OCR Reference Type** is defined.

3. Use the ![Search for page or report](/images/search_small.png) icon and search for **Company Information**.

4. On the **Company Information** under the FastTab **Payments**, ensure that the **Bank Creditor No.** is defined.

5. Create an app or add functionality to an existing app, having the following dependencies <br> <br> ![Dependencies](/images/PM365/ocr-app-dependencies.png) <br> <br> The dependency for Payment and Reconciliation Formats (DK) is needed to get the Bank Creditor No. from the Company Information. The dependency for Payment Management is needed to generate the payment ID. 

6. Add a procedure to the report (or any other place of your choice). To be able to print an OCR reference, you must add the functionality. You can add the procedure in the report directly. 

   The following example uses a posted sales invoice and the standard Word report layout from Business Central. 

   The procedure creates an OCR reference that consists of: <br>

   * The OCR Reference type from the Sales & Receivables Setup 

   - The OCR reference based on the Document No. 

   - The Bank Creditor No. from the Company Information <br><br>
       In the report add the following procedure: <br> <br> ![Procedure](/images/PM365/ocr-add-procedure-to-report.png) <br> 

       Please note that If you are using a version of Payment Management that does note contain the OCR Reference Type on the Sales & Receivables Setup you can hardcode the OCR Reference Type. <br>The procedure returns an OCR reference looking as the example below: <br> <br> **+71<000000010319200+12345678<**  <br> <br>The procedure can be modified according to customer requirements. 

7. Add a variable to the report of data type *text* to hold the OCR reference and call the procedure. 

8. Add a call to the procedure by assigning the new variable with the return value from the procedure.  <br>![Procedure](/images/PM365/ocr-add-call-to-procedure.png).

9. Add a new column to the dataset to be able to use the variable in the report layout.<br>![Procedure](/images/PM365/ocr-add-column-to-dataset.png).

10. Add the OCR reference to the layout. The OCR reference is a part of the reports dataset and can be added to the layout. This can be done regardless of the layout format (RDLC or Word). Identify the variable holding the OCR reference and place it in the layout.
    
11. Print the report and verify that the OCR reference is created. 



