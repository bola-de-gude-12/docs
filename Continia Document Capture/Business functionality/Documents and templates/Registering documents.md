---
title: Registering documents in Document Capture
date: 27-05-2025
description: How to register documents in Document Capture.
id: DC-67
lang: en
---

# Registering documents

When you register a document in Continia Document Capture, you turn all of its recognized information into a real business entity in Microsoft Dynamics 365 Business Central. For example, by registering a purchase invoice that you’ve received from a vendor, you automatically create a Business Central purchase invoice.

Before you can register a document, all document fields must be captured and have valid values. In the document fields section (under **Document Header**), check if all fields are filled out correctly. If not, make sure this is done before you can register the document.

In the document list, you can also see if the overall document is ready to be registered. This is indicated with a checkmark in the **OK** column. If the document isn’t ready for registration, check the **Comments** section at the bottom to see what needs to be done.

When you register a document, Document Capture carries out additional validation that may stop the registration. If this happens, you’ll be informed about what to do to complete the registration.

## To register a document

1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – for example, **PURCHASE** – to open the document journal.
1. In the document list, select the document you want to register. Select the document line – not the number in the **No.** column, as this opens the document card. 
1. In the document fields section (under **Document Header**), check that all fields in the **OK** column have a check mark. If so, all fields are considered valid. If not, follow the field capturing guides in the [To capture fields](@DC-110#to-capture-fields) and [Training Document Capture to locate values](@DC-110#training-document-capture-to-locate-values) sections of [Capturing header fields in a document](@DC-110) to ensure that all fields are captured correctly and have valid values.
1. Not all field values are captured from the document – some must be added manually instead. The most important is the general ledger account number, which in most cases is mandatory. To add this value, go to **No.** and select the three dots in the **Value** column to open the **G/L Account List**. Choose a relevant account in the list by selecting its number in the **No.** column.
1. A dialog box appears, asking if you want to configure the selected account as the default. Select **Yes** if you want Document Capture to assign this account to all documents using the same source template – otherwise select **No**. Your response closes the dialog box and adds the selected value to the **No.** field.
1. In the document list, ensure that there's a check mark in the **OK** column for the selected document. If so, it's ready to be registered. If not, check the **Comments** section at the bottom of the document journal – and carry out any required actions specified there.
1. When there are no more comments and there's a check mark in the **OK** column for the selected document in the document list, go to the action bar, select **Home** and then **Register**.

The document is then registered as an actual Business Central document, and the document page opens automatically, unless you've somehow customized the setup – for example by setting Document Capture up to [register documents as general or purchase journal lines](#registering-documents-as-general-or-purchase-journal-lines).

> [!NOTE]
> Depending on your configuration, for example relating to your G/L accounts or VAT posting setup, you may receive certain warnings during the registration. Such warnings must be resolved for you to be able to register your documents. The same applies to duplicate transactions from Continia Expense Management, which is determined based on the document date (+/- 3 days), the currency code, and the amount including VAT.

If the registration of a document results in an update to an existing purchase order/purchase return order, Document Capture automatically archives the latter before applying the update. This allows you to view older versions of the purchase order/purchase return order via [the built-in archive functionality in Business Central](https://learn.microsoft.com/en-us/dynamics365/business-central/across-how-to-archive-documents) (Microsoft article).

Document Capture automatically archives updated purchase orders and purchase return orders in the following scenarios:

* **Purchase category** - registering a Document Capture document as an invoice or credit memo using the **Match & Update Order** or **Match & Update Return Order** registration options.
* **Purchase order category** - registering a Document Capture document using the **Create or Update Order**, **Update Order**, and **Update Order Receipt** registration options.

Additionally, a comment is added to the archived purchase order to indicate which document triggered the archiving – along with its **Document No.** and/or **Vendor Order No.**

### To enable automatic registration

To allow Document Capture to automatically register documents tied to a specific template, provided that there are no errors or warnings on the documents:

1. Search ({{search}}) for and select **Document Categories**.
2. Click the code of the relevant document category – for example, **PURCHASE** – to open the document journal.
3. In the document list, select a document tied to the template you want to enable automatic registrations for. Select the document line – not the number in the **No.** column, as this opens the document card.
4. On the action bar, click **Template** > **Template Card**.
5. On the **General** FastTab of the template card, enable the **Register Documents Automatically** setting.

## Registering documents as general or purchase journal lines

As an alternative to the standard registration setup, it's possible to register documents as either general journal lines or purchase journal lines, but without vendor names and other standard details. If you [set this up](@DC-112), Document Capture automatically creates lines directly in the general or purchase journal upon document registration – instead of creating invoices or credit memos.

This is particularly useful for businesses that don't require document approvals or detailed posting information for certain purchase documents. Some documents, often from one-time vendors, don't need to be registered in full in Document Capture because they contain so few details that they may as well be registered directly as lines in the general journal instead.

The flow is similar to the standard registration process, but there are some notable differences. Although the information below focuses on general journals, the same applies to purchase journals.

* Following registration, the **Edit - General Journals** page opens instead of the document page because no document is created.
   > [!NOTE]
   > This page opens if you've kept the default settings on the **Template Card** – that is, if **Show Document After Register** is set to **Always** and if **Invoice Reg. Step 2** and **Credit Memo Reg. Step 2** are left empty.
* In the document journal, when you select **Document** > **Find Entries** on the action bar, one of the following happens, depending on whether you've posted the general journal (for example, by setting **Invoice Reg. Step 2**/**Credit Memo Reg. Step 2** to **Post** in [the setup](@DC-112)):
   * **Journal posted** - the **Find entries** page opens, listing all related entries.
   * **Journal not posted** - the **General Journals** page opens.
* The following features aren't available when you register documents as general journal lines:
   * Document matching
   * Document approval
   * Purchase allocation
   * Invoices

>[!TIP]
>To see registered documents in their original form, use the document viewer on the **General Journals** page.

## To register prepayment invoices

As an automated extension of the standard Business Central prepayment functionality, Document Capture can automatically post any incoming invoice as a prepayment invoice linked to a purchase order, as long as the incoming invoice has been either identified as or marked as a prepayment invoice. If Document Capture recognizes certain terms in the document that indicate it's a prepayment invoice, it automatically marks it as such.

To register an invoice as a prepayment invoice:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** code to open the document journal.
1. In the document list, select the invoice you want to register as a prepayment invoice. Select the document line – not the number in the **No.** column. 
1. In the document fields section (under **Document Header**), go to **Our Order No.** and check that an order number is displayed in the **Value** column. If not, select the three dots on the right to open the **Purchase List**, and then select the order that you want to link to the invoice.
   > [!NOTE]
   > A purchase order number must be entered or captured for Document Capture to register the invoice as a prepayment invoice.
1. Go to **[I]nvoice / [C]r. Memo / [P]repayment**, and check that the letter **P** is displayed in the **Value** column. If not, enter it manually, and then select **Enter**.
1. [If something isn't correct, one or more error comments are displayed](#automatic-validation-and-updating-of-the-prepayment-percentage) in bold red in the **Comments** section at the bottom. Resolve these errors to enable document registration.
1. When no more error comments are displayed, register the invoice by selecting **Home** > **Register** on the action bar.

Document Capture will then post the invoice as a prepayment invoice linked to the purchase order specified in step 4 above.

### Automatic validation and updating of the prepayment percentage

As mentioned above, Document Capture may block the registration of a prepayment invoice if it encounters errors when validating it. Common causes of error are that no related purchase order exists, or that the amount of the prepayment invoice exceeds that of the purchase order. Such errors must be resolved for you to be able to register the prepayment invoice.

Other comments relating to prepayments don't prevent you from registering the invoice, but notify you of important details that you need to be aware of. For example, this is the case for the following warning:

*No prepayments have been processed on purchase order [order number]. The current prepayment invoice will increase the prepaid percentage and amount to [percentage (amount)]*.

> [!TIP]
> Although this comment doesn't by default prevent registration, you can configure it to do so by changing it from a warning to an error. For more information, see [Configuring comment types and importance](@DC-72).

The basis of these comments is the purchase order header field **Prepayment %**, which is located on the **Prepayment** FastTab of the purchase order. For example, if this field has been set to 10% in a purchase order with a total amount of $5,000 excluding tax, and the amount of the prepayment invoice is higher than $500 (10% of $5,000), the warning mentioned above is displayed in the document journal for the prepayment invoice, and the prepayment percentage of the purchase order is automatically changed to the new, actual percentage when the invoice is registered:

<br>

| Document<br></br>  | Amount excl. tax |                         Prepayment %                         | Comments<br></br> |
| ------------------ | :--------------: | :----------------------------------------------------------: | ----------------- |
| Purchase order     |      $5,000      | 10% <br>(original) <td rowspan="2">As the amount of the invoice is one fifth of the purchase order amount – corresponding to 20% –, the original prepayment percentage of 10% is adjusted accordingly. A warning about the mismatch is displayed in the document journal before document registration. After registration, Document Capture changes **Prepayment %** to 20% for the purchase order.</td> |                   |
| Prepayment invoice |      $1,000      |                     20% <br>(equivalent)                     |                   |

Note that if the amount of the prepayment invoice is lower than $500 (10% of $5,000), the line amounts are changed accordingly, but the prepayment percentage remains unchanged at both header and line level. In such cases, a similar warning is displayed in the document journal for the prepayment invoice.

If the amount of the prepayment invoice is more than 100% of the purchase order amount, an error is displayed instead of a warning, and you won't be able to register the invoice:

<br>

| Document<br></br> | Amount excl. tax | Prepayment % | Comments<br></br> |
| --- | :-: | :-: | --- |
| Purchase order | $5,000 | 10% <br>(actual) <td rowspan="2">As the amount of the invoice exceeds the purchase order amount – corresponding to 120% – the original prepayment percentage of 10% won't be adjusted. An error message about the amount mismatch is displayed in the document journal, preventing the invoice from registration.</td> ||
| Prepayment invoice | $6,000 | 120% <br>(equivalent)  ||

> [!NOTE]
> All Document Capture prepayment functionality applies at header level, as **Prepayment %** is a purchase order header field. It's not possible to link prepayment invoices to purchase orders at line level.

## Related information

[Working with paper and PDF documents](Working with paper and PDF documents.md)  