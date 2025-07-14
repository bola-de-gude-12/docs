---
title: Applying rounding amounts when working with different currencies
date: 31-03-2025
description: Applying rounding amounts when working with different currencies. 
id: CB-212
lang: en
---

# Applying rounding amounts when working with different currencies

Managing payments and reconciliations across different currencies can lead to rounding discrepancies when applying entries. Business Central provides configuration options to automatically manage these differences. This article explains how these settings apply in Bank Account Reconciliation and Payment Reconciliation Journal, and how rounding amounts are handled when using Continia Banking. 

Continia Banking can automatically match ledger entries for all currencies independently of the bank account’s currency, based on the settings in the Sales & Receivables Setup and the Purchase & Payables Setup. The standard matching routine in Business Central, only finds entries in the same currency and does not match entries in different currencies.

> [!IMPORTANT]
>
> Make sure that the G/L account used for posting the rounding amounts allows direct posting.

## General settings in Business Central

Continia Banking follows the general settings in Business Central, based on the Appln. Rounding Precision field in the General Ledger Setup and the Appln between Currencies in the Sales & Receivables Setup and the Purchase & Payables Setup: 

- **Appln. Rounding Precision** (**General Ledger Setup** page > **Application** FastTab) - specifies the rounding difference that will be allowed when you apply entries in LCY to entries in a different currency. If the rounding discrepancy falls within the specified tolerance, it is automatically adjusted. If it exceeds the threshold, the difference is transferred to the **Rounding Precision G/L Account**. 
- **Application between Currencies** (**Sales & Receivables Setup** page > **Purchase & Payables Setup** page > **General** FastTab) - controls whether cross-currency applications are allowed. The options are: 
  - **None** – no cross-currency applications are permitted. 
  - **EMU** – only cross-currency applications between EMU European Monetary Union) currencies are allowed. 
  - **All** – cross-currency applications between all currencies are allowed. 
* **Debit Curr. Appln. Rndg. Acc.** (**Customer/Vendor Posting Group Card**) - specifies the general ledger account to post rounding differences to. 

## To handle rounding differences in multi-currency transactions on the bank account reconciliation page 

The bank account reconciliation process ensures that bank transactions match the corresponding customer and vendor ledger entries. When dealing with foreign currency (FCY) bank accounts, reconciliation is limited to entries in the same currency. However, local currency (LCY) bank accounts allow payments in multiple currencies, depending on [system settings](#general-settings-in-business-central). 

### To handle rounding amounts within the tolerance settings

If the rounding amount falls within the tolerance specified in the **Appln. Rounding Precision** field, the system retrieves the relevant data in the Bank Account Reconciliation. When a Payment Application Proposal is applied: 

- If the difference is within the rounding tolerance, Continia Banking treats it as a rounding adjustment and posts it to the designated rounding G/L account. 
- A rounding difference generates an additional journal line. 
- Once posted, the process is complete. 

### To handle rounding amounts that exceed the tolerance settings 

If the rounding amount exceeds the tolerance set in the **Appln. Rounding Precision** field, the line in the bank account reconciliation displays with status *Difference*, indicating an unresolved discrepancy. 

To resolve differences: 
- **Transfer the difference** – select **Transfer Difference to Account**. This creates an additional line. 
- **Post the difference** – use **Post All Journal Lines** to process both the regular entries and the difference in one step. Alternatively, post lines individually in separate journals using the Post Journals option on the Payment Application Review page. 
- **Review and adjust** – modify the transaction or apply the difference manually to a specific ledger entry. 

  

## To handle rounding differences in multi-currency transactions in the payment reconciliation journal

The payment reconciliation journal automates the matching of payments to open customer or vendor ledger entries. It ensures that the **Amount to Apply** is in the currency of the entry, which may differ from the bank account’s currency. 

The system follows the **Application Between Currencies** field setting from **Sales & Receivables Setup** and **Purchase & Payables** Setup. The bank account currency is the default for application. 

### To handle rounding amounts within the tolerance settings

Rounding differences are generated during posting and displayed in the posting preview. If the difference falls within the rounding threshold, the system automatically applies the payment. The system posts rounding differences to the G/L account associated with the customer’s or vendor's posting group. 

For example, a company with an LCY set to GBP processes a bank statement in GBP. A customer payment is matched to an invoice in USD, resulting in a rounding difference. The system automatically generates a rounding journal entry, which is visible on the Preview Posting page, ensuring the rounding amount is applied correctly. 

### To handle rounding amounts that exceed tolerance settings

If the rounding amount exceeds the tolerance: 

Possible actions: 
* **Transfer the difference** – on the Payment Journal Reconciliation, select Transfer Difference to Account. This creates an indented line below the original entry. 
* **Review and adjust** – modify the transaction or apply the difference manually to a specific ledger entry. 

