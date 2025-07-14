---
title: Summarizing Payments in Payment Management
description: Information on summarizing payments in the payment journal.
date: 07-10-2021
id: PM-201
lang: en
---

# Summarizing Payments

You can summarize payment lines in the payment journal, which means sending only one payment line to the bank that covers multiple payments for the same vendor. This can be beneficial when the bank charges a fee per payment line.

If you activate the option to summarize payment lines on the vendor card and payment journal set up, the payment lines will be automatically summarized per vendor when suggesting payments in the payment journal. Additionally, you can manually summarize payment lines after creating them in the payment journal. For more information about managing the setup for summarizing payments, see [Setup for Summarizing Payments](@PM-186).

Payments can be summarized if:

- The functionality is activated on the vendor card and on the payment journal. See [To allow for vendor payments to be summarized](@PM-186#to-allow-for-vendor-payments-to-be-summarized).

- The payment information values are generic for the payments. These values include **Balance Account No., Creditor No. Payment Method Code** and **Recipient Bank Account**. 

  > [!NOTE]
  >
  > You can allow payment lines to be summarized even though the given values are not generic when manually summarizing the payment lines. For more information, see [To enable summarizing lines differing in value (only manual summation)](@PM-186#to-allow-summarizing-lines-differing-in-value-only-manual-summation).

- The bank supports receiving payments with long notifications. Payments using short notifications can't be summarized.

  > [!NOTE]
  >
  > If your bank charges a fee for payments with long notification, Payment Management will, in most cases, automatically send the payments with a short notification to avoid the fee. If your bank charges a fee for using a long notification method, the payments can't be summarized in the payment journal. 

## Manually summarizing payments

To manually summarize payment lines in the payment journal, you can select the lines and use the Summarize payments action.

To summarize payments manually:

* Select the lines you want to summarize, and on the action bar, select **Prepare** > **Summarize Payments**. This will analyze to determine any potential issues with the selected lines. If any issues are found, a page displaying a list of the identified errors will open. Once potential errors have been resolved for the selected lines, you can summarize them. 

  > [!NOTE]
  >
  > You can only summarize payments if the functionality is activated on the vendor card and the payment journal. See [To allow for vendor payments to be summarized](@PM-186#to-allow-for-vendor-payments-to-be-summarized).

## Related information

[Setup for Summarizing Payments](@PM-186)  
[To allow for vendor payments to be summarized](@PM-186#to-allow-for-vendor-payments-to-be-summarized)  
[To allow summarizing lines differing in value (only manual summation)](@PM-186#to-allow-summarizing-lines-differing-in-value-only-manual-summation)

