---
title: Using the Payment Management fields on the vendor card
date: 02-11-2023
description: A guide to PM fields for setting up a vendor.
id: PM-368
lang: en

---

# The Payment Management fields on the Vendor Card

This article describes the Payment Management-specific fields on the vendor card and how to benefit from them. On the Vendor card, navigate to the FastTab **Payments** to find the following fields:

| Field                                      | Description                                                  |
| ------------------------------------------ | ------------------------------------------------------------ |
| Skip payment                               | When switched on, all payments to this vendor are excluded when creating payment suggestions. This could be convenient if you made payments not sent directly from Business Central, for example, a direct withdrawal from a credit card. |
| Balance Account No.                        | A balance account must be applied to the payment journal lines for Payment Management to validate and process the payments. When you specify the balance account on the vendor card, a balance account is automatically applied to all purchase documents for the given vendor. For more information, see the [Setting up Balance Accounts](@PM-62) article. |
| Payment Method Code                        | The Payment Management Payment Method Code specifies how the payments are usually submitted, for example, via a bank transfer or check. If the bank changes something, Payment Management will notify you to update your settings. |
| Allow Summarizing Payments                 | When switched on, it summarizes payment lines in the payment journal and sends one payment line to the bank. This can be an advantage if, for example, the bank charges a fee per payment line. For more information, see the [Setup for Summarizing Payments](@PM-186) article. |
| Exclude Credit Memo When Summarizing       | Specifies if credit memos must be excluded when summarizing payments when using the suggested vendor payments action. This field on the vendor card makes it possible to enable the excludes when summarizing payments. When switched on, all vendor-specific credit memos are excluded. For more information, see the [Setup for Summarizing Payments](@PM-186) article. |
| Exclude Refunds When Summarizing           | Specifies if vendor ledger entry type refunds must be excluded when summarizing payments. For more information, see the [Setup for Summarizing Payments](@PM-186) article. |
| Exclude Payments When Summarizing Payments | Specifies if vendor ledger entry type *payments* must be excluded when summarizing payments. This can be convenient when an isolated payment entry is not balanced with an invoice. For more information, see the [Setup for Summarizing Payments](@PM-186) article. |
| Payment Reference Template Code            | Specifies the template used for building automatic payment references for this document. For more information, see the [Setting up Payment References](@PM-43) article. |
| Cost Type Code                             | Specifies the default cost type for the vendor. When making a payment that involves a fee, such as SEPA payments, the cost type code can define who should pay the fee. For more information, see the [Setting up Cost Types article](@PM-44) article. |
| Creditor No.                               | Specifies the number of the vendor. This field is convenient as some localizations have specific OCR-related fields. For example, FIK, BankGirot, and PlusGirot. |
| G-Account %                                | Specifies the percentage that should be paid to a G-Account. A G-account is a frozen account that you can only use to make payroll taxes or VAT payments to the Dutch Tax and Customs Administration. |
| G-Account Bank Account                     | Specifies the G-Account of the Vendor. A G-account is a frozen account that you can only use to make payroll taxes or VAT payments to the Dutch Tax and Customs Administration. The recipient deposits the estimated amount of payroll taxes or VAT payments into your G-account. You can use this amount solely to pay payroll taxes or VAT. |
| Recipient Email                            | Specifies the email address that will be used to notify the vendor when making payments to this vendor. |
| Limit Notification Size                    | Specifies whether to set limitations when summarizing payments. Summarized payments exceeding the allowed notification size for the payment method will be split into multiple payments. |
| Notification Template                      | Specifies the payment notification template that should be used as the default for this vendor. |
| Notification Method                        | Specifies the payment notification method that should be used as the default for this vendor. The options are *Bank only* and *Bank and Email*. |
| Name, Address, Address 2, Post Code, City  | On the **Alternative Vendor Information** FastTab, you can add the address if the name or address contains special characters. See the [Defining Alternate Payment Addresses](@PM-87) article for more information. |
| Tolerance Type                             | By setting up a tolerance for reconciliation suggestions, you can widen the search for ledger entries and improve matching and suggestion possibilities. You can select to set up the tolerance in percentage or amount. See the [Defining Allowed Tolerances for Reconciliation Suggestions](@PM-273) article for more information. |
| Tolerance Value                            | Specifies if the automatic bank account reconciliation function will suggest ledger entries with the amount incl. tolerance suggested by percentage or amount. See the [Defining Allowed Tolerances for Reconciliation Suggestions](@PM-273) article for more information. |
| Bank Giro No.                              | Specifies the vendor Bank Giro Number. Identifier for bank accounts in Sweden. |
| Plus Giro No.                              | Specifies the vendor Plus Giro Number. Identifier for bank accounts in Sweden. |

