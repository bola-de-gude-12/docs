---
title: Configuring purchase documents in Document Capture
date: 01-10-2025
description: How to configure certain purchase document settings to better match the needs of your organization.
id: DC-139
lang: en
---

# Configuring purchase documents

It's possible to configure certain purchase document settings to better match the needs of your organization. The sections below provide details on how to do so.

Note that this article generally uses invoices for illustrative purposes, but the text applies equally well to credit memos.

## Automatic amount validation

When you receive an invoice from a vendor and convert it into a purchase invoice, Document Capture can automatically check if the total amount of the original invoice (often referred to as the imported amount) matches the amount you've entered in the purchase invoice.

If you enable this check and there’s a mismatch between the two amounts, an error is displayed when you try to post the purchase invoice because there must be an exact match between the two amounts.

However, it's possible to factor in differences in rounding accuracy if required. Document Capture allows for a discrepancy of 0.01 currency units, but this can be customized in the **General Ledger Setup** (for LCY) or on the **Currency Card** (for non-LCY).

You can either use the standard Microsoft Dynamics 365 Business Central fields **Invoice Rounding Precision (LCY) ** and **Invoice Rounding Type (LCY)**, or the Document Capture fields **Maximum Allowed Difference Incl. VAT** (app only) and **Maximum Allowed Difference Excl. VAT** (app only).

To set up amount validation:

1. Search ({{search}}) for and select **Document Capture Setup**.
1. On the **General** FastTab, under **Amount Validation on Post**, select which types of amounts must match, if any: amounts including VAT, amounts excluding VAT, both types, or neither (i.e.: **Not Required**).

>[!TIP]
>It’s also possible to allow Document Capture to handle the automatic update of minor rounding differences in VAT, provided that these differences are within the allowed limits set up as described above. To enable the automatic update of VAT amounts:
>1.	Search ({{search}}) for and select **General Ledger Setup**.
>2.	On the**General** FastTab, enable the Allow automatic update of VAT amount setting.

## Customization of imported amounts

When a vendor sends you an invoice, Document Capture automatically registers the total amount of this invoice and copies it to the corresponding purchase invoice that's created. However, this original invoice total – the imported amount – can be changed [by certain users](#users-capable-of-customizing-imported-amounts). A common reason for changing imported amounts is to avoid discrepancies caused by:

* VAT differences (if you post invoices using a different VAT rate than your vendor)
* The fact that VAT is calculated differently by different systems
* Rounding issues (if you use different rounding rules than your vendor)

> [!NOTE]
> The way you change the imported amounts of incoming documents depends on how the documents have been registered – [as standard documents](@DC-67#to-register-a-document) (the default method) or [as journal lines](@DC-67#registering-documents-as-general-journal-lines). Both procedures are described below, under [Documents registered using the standard method](#documents-registered-using-the-standard-method) and [Documents registered as journal lines](#documents-registered-as-journal-lines) respectively.

### Documents registered using the standard method

To change the imported amounts of documents (here exemplified by purchase invoices) that have been registered in the usual way as standard documents:

1. From the Role Center, in the **Continia Document Capture Activities** section, click **Open PIs**.
1. In the list of purchase invoices, select the one for which you want to configure the imported amounts by selecting its number in the **No.** column.
1. The selected purchase invoice opens. On the action bar, click **Invoice** > **Change Imported Amounts**.
1. In **New Amount Excl. VAT** and/or **New Amount Incl. VAT**, enter the amount(s) you want to apply to this invoice.
1. Click **OK** to close the **Change Document Amount** page.

The new amounts are applied to the purchase invoice and displayed on the **General** FastTab, under **Amount Excl. VAT (Imported)** and/or **Amount Incl. VAT (Imported)**.

### Documents registered as journal lines

To change the imported amounts of documents that have been registered as journal lines:

1. Search ({{search}}) for and select **General Journals** or **Purchase Journals**, depending on which of these types of journal the documents have been registered as lines in.
1. In the list of journal lines, select the one whose imported amounts you want to change.
1. On the action bar, click **Line** > **Change Imported Amounts**.
1. In **New Amount Excl. VAT** and/or **New Amount Incl. VAT**, enter the amount(s) you want to apply to the selected journal line.
1. Click **OK** to close the **Change Document Amount** page.

The new amounts are applied to the document represented by the selected journal line although they aren't immediately visible in the journal itself.

## Users capable of customizing imported amounts

To [change imported amounts](#customization-of-imported-amounts), you must meet one of the following criteria – depending on whether invoice approval has been set up for the current company.

### No invoice approval

When invoice approval has not been set up, you must be permitted to edit the **CDC Document** table. Two [permission sets](/Continia Document Capture/Development and Administration/Document Capture permissions.md) grant you this permission: CDC CAPTURE and CDC ADMIN. You must be assigned one of these permission sets by an admin.

### Invoice approval enabled

When invoice approval has been set up, you must be configured as an approval administrator. This can only be done by an admin and is done as follows:

1. Search ({{search}}) for and select **Continia User Setup**.
1. On the action bar, click **Edit** to open the **Continia User Setup Card**.
1. On the **General** FastTab, enable the **Approval Administrator** setting.

## Related information
[Setting up purchase documents](@DC-476)  
[Setting up the registration of documents as general journal lines](@DC-112)  