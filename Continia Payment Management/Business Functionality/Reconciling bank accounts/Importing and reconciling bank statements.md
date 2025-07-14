---
title: Importing and reconciling bank statements
description: How to import and reconcile bank account statements
date: 22-09-2022
id: PM-48
lang: en
---

# Importing and Reconciling Bank Statements

You can import your bank account statements: by file or directly from the bank using direct communication. Once imported, the bank's file format is converted, and all the information is automatically used to reconcile your bank account.

When you import the bank account statement, Statement Intelligence automatically matches the statement lines with your bank account's ledger entries. It will also prepare accounts receivable for matching or generate proposals for matches.

## To import a bank statement manually

Manually importing a bank account statement allows you to update your financial records and reconcile your accounts. 

To import a bank statement file:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Account Reconciliations**, then select the related link. This opens the list of bank account reconciliations.
1. Open the bank account reconciliation for which you want to import account statement lines or create a new bank account reconciliation by selecting **New** in the action bar. Statement Intelligence will automatically be activated for the reconciliation if the bank account is set up to use Payment Management.
1. On the bank account reconciliation, navigate to the action bar and select **Bank** > **Import and Match**. It will now start reconciling, finding customer ledger entries, and vendor ledger entries, and looking for all data that can be matched. 
1. If the bank account is set up to use direct communication, available bank account files will automatically be imported into the journal directly from the bank. If, on the other hand, the bank account is not set up for direct communication, you must manually select the file to be imported into the journal.

During import, the account statement will be processed for reconciliation, after which you can use **Status** on the account statement lines to get an overview of the reconciliation. Possible statuses are:

* **Ok** - a direct match is found.
* **Unsolved** - no direct match found, but if the **No. of Reconciliation Suggestions** column contains a number, possible matches are suggested.
* **Awaiting Cash Receipt Jnl/General Jnl/Payment Jnl** - no direct match found. Bank statement lines with reconciliation suggestions based on open customer, vendor, or employee payments. 

If automatic matching has not been possible, Statement Intelligence will, in most cases, be able to generate matching suggestions. 

For more information on managing open payments , see the [Managing open payments from the bank account reconciliation](@PM-50) article.

## To import bank statements automatically

When new bank statements are available in the bank to be imported to Business Central with direct bank communication, you can automatically import these to the bank account reconciliation.

To import bank statements automatically:

* On the bank account card, on the action bar, select **Actions** > **Enable Account Statement Job Queue**. It will now automatically create a [job queue](@PM-324) to download bank statements automatically.

  > [!IMPORTANT]
  >
  > Before activating job queues related to import and reconcile bank statements, customers with Dutch and UK banks must import and reconcile the first bank account to enable the job queues.

## Automatic reconciliation by Statement Intelligence

After importing your statements, Statement Intelligence automatically identifies all receivables and generates corresponding entries in the appropriate journal. The following procedure describes how Statement Intelligence handles the imported statement lines during import:

1. Statement Intelligence utilizes the **Transaction ID** and **Sender Reference** fields to search for matching bank account ledger entries based on the bank statement lines. When payments are processed through Payment Management, a unique payment reference ID is automatically generated and filled in the **Transaction ID** field in the payment journal. This ID is used to locate the corresponding bank ledger entry, which is then be marked for reconciliation. If the bank does not support transaction ID in the bank account statement, Statement Intelligence will search for information in the sender reference that can be used for reconciliation. The field **Sender Reference** allows a custom setup specified on the bank account. For further details on sender reference, refer to the [Defining Sender Reference](@PM-194) article.
   
1. Statement Intelligence subsequently attempts to find closed payment receipt ledger entries that match the information on the account statement line. A match will be based on the customer payment ID, document no., external payment reference, amount, and date. <br>For example, if you have set up customer statements to include an external payment reference and the external payment reference appears in the description or among the information received from the bank, Statement Intelligence identifies the external payment reference. It creates a reconciliation suggestion, including all the related entries. For more information, see [Set up Customer Statements](@PM-258). 

   If no unique match is found, Statement Intelligence searches for bank account ledger entries using only the amount and date as a search key. A reconciliation suggestion will be generated if a potential match is identified, requiring manual validation to confirm its accuracy. For more information, refer to the [Reconciling bank statement lines manually](@PM-39) article.

1. If a bank account ledger entry is still not identified for reconciliation, Statement Intelligence will further investigate the open customer entries using the customer number, payment ID, and document number as search criteria. This step is taken to identify any open customer entries that have been paid but were not properly registered in Business Central.
   
   If there are open customer entries in the system that constitute a match according to the search keys, Statement Intelligence creates a reconciliation suggestion for the identified payments in the payment receipt journal, ready to post. After posting the open customer entries, the payments will thus be registered in Business Central, and the associated bank account ledger entries can be applied to the bank account statement line. For more information, refer to the [managing open payments from the bank account reconciliation](@PM-50) article.
   
1. Eventually, all non-reconciled account statement lines will be reviewed to see if a match can be found based on the [reconciliation rules](@PM-37) defined in the bank account. If a match is based on such a rule, reconciliation suggestions are created for payments and cash receipts in the ledger journal.
   The corresponding payment lines will be created when the ledger journal is posted. The associated bank account ledger entries will be applied to the related bank account statement lines.

1. The remaining bank account statement lines that Statement Intelligence can't automatically match must be handled manually using the function **Manual Match**. For more information about manual matching, refer to the [Manually match bank statement lines](@PM-49) article.
