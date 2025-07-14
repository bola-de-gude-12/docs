---
title: Applying ledger entries
description: A guide on how to apply ledger entries in the bank account reconciliation.
date: 29-07-2021
id: PM-163
lang: en
---

# Applying Ledger Entries

If the reference to the associated invoice or purchase document isn't available on the imported bank account statement lines, it will not be possible for Payment Management to do the automatic reconciliation. 

For example, if you're invoicing with an OCR-related ID, you may find that a customer makes an account-to-account transfer, without specifying either the invoice number or the OCR ID (payment ID). When looking at vendor payments, the case could be if payments are made through direct debit agreements with your vendor, allowing your vendor to withdraw money from your account. In both cases, Payment Management will miss the information needed to do the automatic reconciliation.

To help Payment Management identify the associated customer, vendor, or employee for an account statement line, you can set up reconciliation rules. When a reconciliation rule is met, the customer, vendor, or employee account number will be inserted on the statement line, after which you'll be able to apply the associated ledger entry.

> [!IMPORTANT]
>
> Due to a limitation in Business Central only bank accounts where the "Currency Code" field is blank are supported when reconciling employees. If the bank account does not have a blank currency code then the reconciliation is not executed and related page elements are hidden.


## Overview of lines created in journals

In the bank account reconciliation under the FastTab **General**, you have an overview of the number of lines transferred from the bank account reconciliation to a relevant cash receipt journal, payment journal, or payment employee journal due to line amount differences caused by missing posting of customer-, vendor-, or employee payments. The journal lines must be applied to reconcile the correspondent bank statement lines.
<br>You can access the journal lines from the action bar under **Journals**.

## To apply suggested ledger entries 

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Account Reconciliations**, then select the related link. This opens the list of bank account reconciliations.
1. Open the desired bank account reconciliation and select the bank statement line that must be applied. 
   > [!TIP] 
   > 
   > You can add more columns of information to the **Bank Statement Lines** from the action bar under **Related** > **Page** > **Show More Columns**. This will add **Account Type** and **Account No.** to the table in which you can see the customer, vendor, or employee number.   
1. Navigate to the action bar and select **Matching**
1. Depending on whether it is a customer, vendor, or employee statement line that needs to be applied select one of the following options to open a list of open ledger entries for the given customer, vendor, or employee.:
   - **Apply Customer Ledger Entries**
   - **Apply Vendor Ledger Entries**
   - **Apply Employee Ledger Entries**
1. Choose the ledger entries that must be applied to the bank statement line.
   > [!TIP]
   >
   > Use the reconciliation information at the bottom of the page, to see if the entire statement line amount has been applied, or if there is a difference that still needs to be applied. 
1. When you have marked the ledger entries to be applied, select **Close**. 


## Related information

[Setting up Vendor Reconciliation Rules](@PM-32)  
[Setting up Customer Reconciliation Rules](@PM-187)  
[Setting up Employee Reconciliation Rules](@PM-188)



