---
title: Purchase VAT Next Month in Continia Finance
date: 11-10-2024
description: How to enable and use the Purchase VAT Next Month feature in Continia Finance.
id: CF-120
lang: en
---

# Purchase VAT Next Month

This article describes the **Purchase VAT Next Month** feature, which automatically allocates the VAT of your purchase invoices and credit notes to the correct period – provided that the received date in these documents is later than the last day of the month of the related posting date.

When **Enable VAT Correction** is turned on, the system automatically populates the **Document Received Date** (or **Document Receipt Date**) field of your purchase invoices and credit notes with the value from the **Posting Date** field – or from another date field defined by you. Although you can change this value before posting a purchase document, you must have a value in the received date field while **Enable VAT Correction** is on. Otherwise, you can't post the document.

## To enable VAT correction
To enable VAT correction in Continia Finance:

1. Choose the {{search}} icon, enter **Extended Financial Reports Setup**, and then choose the related link.
2. On the **Purch. VAT Next Month** FastTab, turn on the **Enable VAT correction** setting.
3. Select the desired values for the following options:
   * Bal. Account VAT Base - the default G/L account for the **Correct VAT Entries** report. A journal line is created based on the original posting date, and a balancing entry is created based on the document's received date.
   * Account VAT Base Next Month - the G/L account to which the net amount is posted on the original posting date.
   * Account VAT Amount Last Month - the G/L account to which the net amount is posted on the document's received date.
   * VAT Correction Jnl. Template Name - the default journal template name for the **Correct VAT Entries** report.
   * VAT Correction Jnl. Batch Name - the default journal batch name for the **Correct VAT Entries** report.
   * Source Code VAT Correction - the origin code for the **Correct VAT Entries** report. It's recommended to create a dedicated source code for this purpose.
   * Allow Doc. Receipt Date From - the earliest document received date on which posting to the company books is allowed, if you choose to run a plausibility check.
   * Allow Doc. Receipt Date To - the last document receipt date on which posting to the company books is allowed, if you choose to run a plausibility check.
   * Default Doc. Receipt Date - the default date of the document receipt date. If you select **None**, the field is left empty – and you must enter the date manually.

## To correct VAT entries
To run the **Correct VAT Entries** task:
1. Choose the {{search}} icon, enter **Correct VAT Entries**, and then choose the related link.
2. The **Journal Template Name** and **Journal Batch Name** should be pre-populated with the values defined on the **Extended Financial Reports Setup** page, but you can select different values if needed.
3. On the **Filter: G/L Entry** FastTab, add a single date or a period to the **Posting Date** field.
4. Select **OK**.

You're then presented with an overview of the invoices whose VATs are going to be transferred from one month to another. When you finish reviewing the corrections, select **Post** to process them.

>[!NOTE]
>To accommodate these corrections, make sure to set up the appropriate VAT product posting group – and extend the related VAT product posting group to it under the **Income Date VAT Posting Group** column on the **VAT Posting Setup** page. For example, the VAT 21% posting group could be extended with the VAT 21% (following month) posting group.