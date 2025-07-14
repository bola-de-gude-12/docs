---
title: Using amount distribution codes in Document Capture
date: 07-07-2025
description: How to use amount distribution codes in Document Capture.
id: DC-118
lang: en
---

# Using amount distribution codes

An amount distribution code is a code that automatically distributes the amount of a document between multiple lines when the document is created in Microsoft Dynamics 365 Business Central, according to your specifications. Using these codes, you can determine how the amount of an incoming invoice or credit memo should be split into lines upon document creation – and which accounts, amounts, and dimensions should be applied to each newly created document line. The amount of each document line can be either a fixed amount or a percentage of the recognized document amount, as defined by you.

> [!NOTE]
> Amount distribution codes are typically applied to the total amount of the document (when line recognition isn't enabled). If relevant, you can also apply them to any other amount field.

To set up amount distribution codes, see [To create amount distribution codes](#to-create-amount-distribution-codes) below.

Once you've set up one or more amount distribution codes, they must be applied to a document to take effect. To apply amount distribution codes, use one of the following methods:

* Set them up to be [applied automatically using a document template](#to-apply-amount-distribution-codes-using-a-template).
* [Apply them manually in the document journal](#to-apply-amount-distribution-codes-manually-during-registration) during document registration.
* [Activate them from the relevant document after registration](#activating-amount-distribution-codes-from-registered-documents), either directly in Business Central or from the Continia Web Approval Portal.

## To create amount distribution codes

1. Search {{search}} for and select **Standard Amount Distribution Codes**.
1. On the action bar, click **Edit List**.
1. In the table, select an empty line and then, in the **Code** column, enter the name of the code that you want to create.
1. **Optional**: In the **Description** column, enter a description of the code you're creating.
1. In the **Enabled for Purchase** column, select one of the following options:
   * **Yes - all vendors** - if you want the code to be applied to all incoming documents.
   * **Yes - selected vendors only** - if you only want the code be applied to documents from certain vendors.
1. If you selected **Yes - selected vendors only** in step 5 above, click **Vendors** on the action bar. On the page that opens, in the **Vendor No.** column of the table, select a vendor whose documents you want the code to be applied to. Go to a new line and repeat the process for any additional vendors, and then close the page to return to the **Standard Amount Distribution Codes** page. 
1. On the action bar, click **Edit** to open the **Standard Amount Distribution Code Card**.
1. **Optional**: On the **General** FastTab, enable **Distribute by Dimensions** if you want document amounts to be split into multiple lines according to dimensions while keeping the existing account number for all created lines.

   > [!IMPORTANT]
   > **This feature is available as of Document Capture 2023 R1 (11.00).**
   > 
   > When the document amount is split into multiple lines, the account number that was originally assigned to the document is automatically applied to the lines. For that reason, you can't edit the **Type** and **No.** fields when you enable **Distribute by Dimensions**, and you can only enable **Distribute by Dimensions** when you [activate amount distribution codes from the relevant document after registration](#activating-amount-distribution-codes-from-registered-documents) – the methods of applying them automatically using a document template or manually in the document journal will both fail.

1. On the **Lines** FastTab, select a line in the table, and then fill out the table fields as needed.
   * **Type** - select the type of account you want this line's amount posted to.
   * **No.** - select the number of the account you want this line's amount posted to.
   * **Description** - enter a free-text description of the line.
   * **Distribution %** - enter the amount you want to assign to this line, as a percentage of the recognized document amount.
   * **Unit Cost** - enter the fixed amount you want to assign to this line.
   * **[Global dimensions 1 and 2]** - enter the dimension value(s) you want to assign to this line.

   > [!NOTE]
   > Only the two preconfigured global dimensions are displayed as columns in the table, and you can only add and view values for these two dimensions directly in the table. However, you can add other dimensions and values as follows: Select the relevant line, click **Line** > **Dimensions** to open the **Standard Amount Distribution Dimensions** page, and then select a dimension code and a dimension value code in the table. Add as many dimensions as you like by creating lines in the table on the **Edit** page, and then click **Close** to return to the **Standard Amount Distribution Code Card**. Your dimension codes and values are assigned to the selected line, even though they aren't visible in the table.

1. To add another document line, select a new line in the table, and then fill out the fields as needed. Repeat this process until you've set up all the lines you want to be automatically created when the document is created in Business Central.

   > [!TIP]
   > For each line, you can only fill out either **Distribution %** or **Unit Cost** – not both at the same time. If you choose to fill out **Distribution %**, the values you've entered for each of the lines should add up to a total of 100%. If the values add up to less (or more) than 100%, this different percentage is applied to the relevant document – overriding the original document amount. For more information, see [Amount distribution code values differing from the document amount](#amount-distribution-code-values-differing-from-the-document-amount).

You've now set up an amount distribution code with the name that you specified in step 3. Once this code is applied to an imported document and that document is created in Business Central, the amount of the document is split into the number of lines that you specified on the **Standard Amount Distribution Code Card** in steps 9-10. Also, the accounts and dimension values that you specified are automatically applied on document creation. 

For a number of examples of how various code setups are implemented when applied, see [Examples of applied amount distribution codes](#examples-of-applied-amount-distribution-codes) below.

## To apply amount distribution codes using a template

1. Search ({{search}}) for and select **Document Categories**.
1. To open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself), and then click **Edit** on the action bar to open the **Document Category** card.
1. On the **Templates** FastTab, in the list of templates, select the template you want to configure, and then click **Edit** to open the template card.
1. **Optional**: On the **Fields** FastTab, click **Create new Template Field** to start the **Assisted Template Field Setup Guide**, and then select the amount field you want to apply an amount distribution code to. 
1. On the action bar, click **Related** > **Template** > **Translations** > **Accounts for Amounts** to open the **Accounts for Amounts** page.
1. In the list of fields, select the one that you want to apply an amount distribution code to (typically **Amount Excl. VAT** or similar, but not necessarily).
1. In the **Type** column, select **Amount Distribution Code**.
1. In the **No.** column, select the amount distribution code you want to apply.

The selected amount distribution code is applied to all documents using this template.

## To apply amount distribution codes manually during registration

1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – for example, **PURCHASE** – to open the document journal.
1. In the list of documents, select the one you want to apply an amount distribution code to.
1. Under **Document Header**, click the three dots on the right of the **Type** field to open the **Account Types** page.
1. In the list of account types, select **Amount Distribution Code**, and then click **Close** to return to the document journal.
1. Under **Document Header**, click the three dots on the right of the **No.** field to open the **Standard Amount Distribution Codes** page.
1. In the list of codes, select the one that you want to apply, and then click **OK** to return to the document journal.
1. A dialog appears, asking if you want to configure the code as the default account for the primary amount field. Click **Yes** or **No** – depending on your preference – to close the dialog.

The selected amount distribution code is now applied to the document and will take effect once you register the document in Business Central.

## Activating amount distribution codes from registered documents

You can activate an amount distribution code for a document even after the document has been registered. This can be done either in Business Central or in the Web Approval Portal. Both methods are described below, using invoices as an illustrative example.

> [!NOTE]
> You must use one of these two methods if you enable **Distribute by Dimensions** [in the setup](#to-create-amount-distribution-codes) (available as of Document Capture 2023 R1). 

### To activate codes in Business Central

1. From the Role Center, in the navigation menu at the top, click **Purchasing** > **Purchase Invoices**.
1. In the list of open invoices, select the one you want to activate an amount distribution code for. The **Purchase Invoice** page opens.
1. On the action bar, click **Actions** > **Functions** > **Get Std. Amount Distribution Codes**.
1. On the page that opens, under **Distribution Code**, select the code you want to apply.
1. Under **Lines**, specify whether you want to replace the existing invoice lines with the ones added by the amount distribution code, or if you want to keep the existing invoice lines and add the amount distribution code lines on top.
1. The **Amount to Distribute** field is auto-populated based on data from the selected invoice, but you can edit the displayed amount, if necessary.
1. Click **OK** when you're done

The invoice is then updated with the changes specified by the applied amount distribution code.

### To activate codes in the Web Approval Portal

1. In the list of documents, select the one you want to activate an amount distribution code for. The document page opens.
1. On the action bar, click **Use Template** to open the **Use Template** page.
1. In the dropdown menu at the top, select the code you want to apply.
1. Below the dropdown menu, specify whether you want to replace the existing invoice lines with the ones added by the amount distribution code, or if you want to keep the existing invoice lines and add the amount distribution code lines on top.
1. The **Amount to Distribute** field is auto-populated based on data from the selected document, but you can edit the displayed amount, if necessary.
1. Click **Continue** when you're done.

The invoice is then updated with the changes specified by the applied amount distribution code.

## Examples of applied amount distribution codes

Once an amount distribution code has been applied to a document, no matter which of the above methods is used, the document amount is split into lines as specified by you. The following examples illustrate how this can be implemented in practice.

> [!NOTE]
> Any discrepancies between imported and assigned amounts trigger a dialog notifying you of the mismatch – provided that you've enabled **Amount Validation** on the relevant template card, on the **Purchase Documents** FastTab, under **Approval**. In such cases, you must resolve the issue manually, for example by adding and/or adjusting lines to make the imported and assigned amounts match.

### Standard setup

Consider the following **Standard Amount Distribution Code Card** setup for an amount distribution code named **Office**:

<br>

| Type | No. | Description | Distribution % | Unit Cost | Department Code |
| --- | --- | --- | :-: | :-: | :-: |
| G/L Account | 31400 | Office expenses, admin | 50 | - | ADM |
| G/L Account | 31400 | Office expenses, sales | 30 | - | SALES |
| G/L Account | 40800 | Office expenses, production | 20 | - | PROD |

When this amount distribution code is applied to an invoice with an imported amount of EUR 200.00 excluding VAT, the following three lines are automatically added to the invoice:

<br>

| Type | No. | Description | Direct Unit Cost Excl. VAT | Department Code |
| --- | --- | --- | :-: | :-: |
| G/L Account | 31400 | Office expenses, admin | 100.00 | ADM |
| G/L Account | 31400 | Office expenses, sales | 60.00 | SALES |
| G/L Account | 40800 | Office expenses, production | 40.00 | PROD |

Note that the invoice amount has been distributed between the lines according to the specified percentages, and that the correct accounts and dimension values (in this case different department codes) have been applied to the lines – as specified in the setup.

### Amount distribution code values differing from the document amount

As mentioned under [To create amount distribution codes](#to-create-amount-distribution-codes), your entered values for **Distribution %** should add up to a total of 100% – as in the example above. However, if the values add up to less (or more) than 100%, this different percentage is applied to the relevant document, overriding the original document amount. For example, consider this setup:

<br>

| Type | No. | Description | Distribution % | Unit Cost | Department Code |
| --- | --- | --- | :-: | :-: | :-: |
| G/L Account | 31400 | Office expenses, admin | 30 | - | ADM |
| G/L Account | 31400 | Office expenses, sales | 30 | - | SALES |
| G/L Account | 40800 | Office expenses, production | 30 | - | PROD |

If this amount distribution code is applied to an invoice with an imported amount of EUR 200.00 excluding VAT, the following three lines are added to the invoice:

<br>

| Type | No. | Description | Direct Unit Cost Excl. VAT | Department Code |
| --- | --- | --- | :-: | :-: |
| G/L Account | 31400 | Office expenses, admin | 60.00 | ADM |
| G/L Account | 31400 | Office expenses, sales | 60.00 | SALES |
| G/L Account | 40800 | Office expenses, production | 60.00 | PROD |

Note that the total amount is now EUR 180.00 excluding VAT (exactly 90% of the imported amount of EUR 200.00), which has then been split into three lines, each with 30% of the total amount.

> [!NOTE]
> Similarly, if any entered **Unit Cost** values add up to less (or more) than the imported invoice amount, the **Unit Cost** total is applied to the invoice and overrides the original invoice amount. In both cases, you're notified that there's a discrepancy between the imported and the assigned amounts, and you must then take manual steps to resolve this issue.

### Mixed amount distribution code values

As mentioned in [To create amount distribution codes](#to-create-amount-distribution-codes), you can't fill out both **Distribution %** and **Unit Cost** for the same line when you set up amount distribution codes. However, if you set up multiple lines for a given code, you can in fact use both options across the different lines, as illustrated in the following setup:

<br>

| Type | No. | Description | Distribution % | Unit Cost | Department Code |
| --- | --- | --- | :-: | :-: | :-: |
| G/L Account | 31400 | Office expenses, admin | 25 | - | ADM |
| G/L Account | 31400 | Office expenses, sales | - | 50 | SALES |
| G/L Account | 40800 | Office expenses, production | - | 50 | PROD |

If this amount distribution code is applied to an invoice with an imported amount of EUR 200.00 excluding VAT, the following three lines are added to the invoice:

<br>

| Type | No. | Description | Direct Unit Cost Excl. VAT | Department Code |
| --- | --- | --- | :-: | :-: |
| G/L Account | 31400 | Office expenses, admin | 25.00 | ADM |
| G/L Account | 31400 | Office expenses, sales | 50.00 | SALES |
| G/L Account | 40800 | Office expenses, production | 50.00 | PROD |

Note that the percentage in **Distribution %** isn't applied until the two **Unit Cost** amounts have been deducted from the imported amount: (200 – 50 – 50) × 0.25 = 25.00.