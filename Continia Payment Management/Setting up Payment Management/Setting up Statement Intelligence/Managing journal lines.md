---
title: Managing journal lines
description: Information on how to manage journal lines in the journals used for bank account reconciliation.
date: 26-06-2024
id: PM-36
lang: en
---

# Managing Journal Lines

Matching and applying bank account statement lines to ledger entries is crucial for successful reconciliation. The journal ledger entries can be created within various journals, including the general journal, the cash receipt journal, the payment journal, and the employee payment journal.  The employee payment journal is based on a standard payment journal created by Payment Management to separate the vendor ledger entries from the employee ledger entries. 

## To manage journal lines on import

You can choose how Statement Intelligence should manage and create journal lines in the bank account reconciliation when importing bank account statements for the customer, vendor, and employee payments.

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon to search for **Statement Intelligence Setup** and select the related link. This will open the Payment Management Setup page.
1. On the **Statement Intelligence Setup** page, navigate to the FastTab **General**.
1. Select how to manage journal lines when importing bank account statements. You can define this for the following setups: 
    - Handle Cash Receipt Journal Lines
    - Handle Payment Journal Lines
    - Handle Employee Payment Journal Lines
    - Handle Reversal Lines
	
	  For each of the above setups, you can choose between the following settings:
	
	  | Setting                    | Description                                                  |
	  | -------------------------- | ------------------------------------------------------------ |
	  | **Create Suggestion**      | Journal lines are automatically generated as reconciliation suggestions if open ledger entries can be identified based on customer-, vendor-, or employee number, payment ID, or document no. as search parameters. If reconciliation rules have been defined, these will also be used to generate potential reconciliation suggestions. |
	  | **None**                   | Journal entries will not be created. Instead, you can access the **No. of Reconciliation Suggestions** on the imported bank statement line and create the journal line suggestions from there. |
	  | **Create Lines on Import** | When importing a bank account statement, ledger entries will automatically be created, matching all the imported bank account statement lines 1:1. You must then manually validate and delete journal lines that are not created correctly. |
	  | **Create Lines Manually**  | This setting is very similar to the setting **Create Suggestion**; however, the journal line suggestions are not created automatically in the journals. Instead, it would be best to manually create the journal ledger entries using the action **Create journal lines**. |



## To update the payment journal line status

Keeping the status of payment journal lines up-to-date is essential for accurate transaction tracking. You can set this process to be manual or automatic, ensuring flexibility in how updates are managed. 

To configure your preferred setting for updating the payment journal lines:

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **Banks**, then select the related link. 
1. Select the bank, and on the bank card, navigate to the FastTab **Advanced**.
1. Go to the **Update Payment Journal Lines Status** field, and from the drop-down box, select *Automatic* or *Manual*.

   > [!NOTE]
   >
   > If you select to update the payment journal line status automatically, it will run the Job queue (codeunit 6216327 CPM update Pmt.Jnl.Line Status) on the selected time interval and update the status accordingly.



## To manage journal numbers

You can indicate whether you want to automatically renumber journal document numbers in journals used for bank account reconciliation before posting the journal lines. Automatically renumbering journal document numbers in bank account reconciliation journals before posting is convenient when you need to ensure unique, sequential identifiers for each entry. This helps prevent duplicates, simplifies audits, and maintains orderly records.

To manage the renumbering of journal document numbers:

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **Statement Intelligence Setup**, then select the related link. This will open the **Payment Management Setup** page.
1. On the **Statement Intelligence Setup** page, navigate to the FastTab **General**.
1. Go to the **Renumber Journal Document Nos.** field and select the option if you want document numbers in journals used for bank account reconciliation to be automatically renumbered before posting.



## To include the statement number in the journal line description

You have the option to specify whether the bank account statement number should be included in the description of journal lines created by Statement Intelligence. Including the bank account statement number in the description of journal lines created by Statement Intelligence is convenient when you need to quickly identify and reference specific statements during the reconciliation process. 

To include the statement number in the journal line description:

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **Statement Intelligence Setup**, then select the related link. This will open the Payment Management Setup page.
1. Navigate to the FastTab **General,** and enable the **Include Statement No. in the Journal Description** setting if you want to include the bank account reconciliation in the description of journal lines created by Statement Intelligence.



## To handle empty Ending No field 

You can control how to manage empty Ending No. fields in sales and purchase documents to ensure consistency and accuracy. The system offers options to either throw an error or skip matching based on No. Series when these fields are empty. 

To handle empty Ending No. field:

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **Statement Intelligence Setup**, then select the related link. This will open the Payment Management Setup page.
1. On the **Statement Intelligence Setup** page, navigate to the FastTab **General**.
1. In the **Handle No. Series empty Ending No.** field section, go to the **Sales Documents** field and select how you want to handle an empty Ending No field. The options are:
   * Throw error
   * Ignore No. Series matching
   * Guess empty Ending No
1. Do the same for the **Purchase Documents** field.



