---
title: Continia Banking Demo Script DK
date: 20-03-2025
description: A detailed description of how to make a complete demonstration of the standard features in Continia Banking.
id: CB-184
lang: en
---

# Continia Banking demo script

> [!IMPORTANT]
>
> The Continia Banking demo script is still in progress and will be updated as development continues.

This demo script provides a detailed description of how to demo the basic features in Continia Banking. The purpose of the Continia demo systems is to give Continia partners an environment to educate end customers and to present and test the latest versions of Continia Banking. 

This demo environment is already set up and ready to use, and it's always up-to-date with the latest version of Continia Banking. Working with the demo script requires basic knowledge of Continia Banking.

## To suggest vendor payments in Standard mode

In the standard setup of Continia Banking, payments are managed in a simple and efficient workflow. The procedure described here explains how to identify and validate vendor payments that are due for processing. 

> [!IMPORTANT] 
>
> If you already demoed suggesting vendor payments in Standard mode, there will be no suggestions for you to work with when you demo the Advanced Payment Suggestion. 

To set up the payment journal and suggest vendor payments:

1. Search for **Payment Journals**, then select the related link.
2. In the **Batch Name** field, select the PMT.JNL. journal.
3. On the action bar, select **Prepare** > **Payment Journal Setup**. Check the setup: 
   - The **Required Posting Status** field is set to "Paid."
   - The **Last Payment Date Calculation** field is set to "30D".
4. Return to the payment journal, and on the action bar, select **Home** > **Suggest Vendor Payments**. 
5. On the **Suggest Vendor Payments** page, use the default settings, enable **Summarize per Vendor** and select **OK**. The payment lines will now be created.
6. Go through the payment status of each line and show how they are validated. Use the following FactBoxes to assist in the process:
   - **Line Information FactBox** – displays the next steps and any approval details related to the transaction. Review this section to understand what actions are required and check for any approval information.
   - **Payment Journal Errors FactBox** – provides guided assistance to correct errors. Click on the suggested fields or areas to make corrections directly.
   - **Recipient Bank Details** – verifies the bank account for a selected transaction line that requires validation. Ensure that the correct bank details are assigned before proceeding.
   - **Applied Entries FactBox** – summarizes applied entries and allows direct access to related posted purchase invoices for easy cross-referencing.
   - **Remittance Information FactBox** – displays the generated remittance text, particularly useful for summarized transactions. Verify the details to ensure accurate payment communication.
7. To export the payments to the bank, select **Home** > **Export/Send payments**. In the **Do you want to export** dialog box, select **All Lines**.
8. Explain and show that the line's status has changed to **Sent to Online**.
9. On the action menu, select **Home** > **Update Status** and show that the line status changes to **Processing**.
10. Select **Home** > **Update Status** again and show that the line status changes to **Paid**.
11. To post the journal, select **Home** > **Post**, and select **Yes**.


## To suggest vendor payments in Advanced mode

The **Advanced Payment Suggestion** setup in Continia Banking offers more flexibility and control over payments. Unlike the standard setup, payment suggestions remain on the **Payment Suggestions** page, allowing users to review and adjust recipient information before transferring payments to the Payment Journal. This section explains how to find and validate vendor payments in Advanced mode.

> [!IMPORTANT]
>
> If you already demoed suggesting vendor payments in Standard mode, there will be no suggestions for you to work with.  

### Enable Advanced mode

Before you enable the **Advanced Payment Suggestion** mode, explain that it's important to check that the **Payment Journal** has no existing lines. The system will not allow you to proceed if any lines are open.

1. Search for and open the **Banking Export Setup** page.
2. On the **General** FastTab, enable **Advanced Payment Suggestion**.

### To create and review a payment suggestion

1. Search for and open **Payment Suggestion**.
2. Select **Suggest Vendor Payments** to generate a payment suggestion containing multiple payments.
3. In the overview, highlight how the FactBox provides additional details.
4. Click the number to open the payment suggestion.
5. View the payments and select the payment suggestion status to open the **Payment Card**.

### The advantages of the Payment card

Explain how the **Payment card** provides:
- **Summarized payment information**, including payment methods, currency, and bank details.
- **Detailed payment overview**, with amounts per payment, recipient and sender bank account details, and applied payment methods.
- **Quick access to vendor and customer information** at the payment level.
- **Easy handling of partial payments and payment discounts** for each transaction.
- **Payments for Associations**, integrating **Continia Banking** with **Continia Finance** to manage vendor or customer association payments efficiently while maintaining standard checks.
- **Payment Suggestion Templates**, allowing predefined filter settings for faster recurring payment processes.

### To finalize payments

Once all lines are reviewed, transfer the payment lines to the **Payment Journal** by selecting Create Gen. Journal Lines.

### To complete the Payment Journal

After transferring, complete the process by:
1. Sending payments to the bank.
2. Updating payment statuses.
3. Posting transactions, following the standard workflow.

## To set up search rules

Before doing the bank account reconciliation, show how the reconciliation rules can ease the process. Search rules streamline the bank account reconciliation process by automatically matching transactions to the correct accounts based on specific text criteria. Even when date and amount don’t match, these rules help identify and assign ledger entries to the right accounts, making reconciliation faster and more efficient.

1. Search for and open **Bank Account Reconciliations**.
1. On the action bar, select **New**. 
1. In the **Bank Account No.** field, select NORDEA721. 
1. In the action menu, select **Rules** and the type of rule you want to create:
   * **G/L Account Search Rules** - you can set up search rules, for example, Gebyr and Rente, so that Continia Banking automatically reconciles, transfers, and enters the appropriate lines in the journal. You can create a rule, when you encounter the lines in the Bank Account Reconciliation. Make sure to select the dedicated accounts with direct posting.
   * **Customer, vendor, and employee search rules** - you can set up customer, vendor, or employee search rules to improve the match rate in the reconciliation. For example, if a customer doesn’t send any helpful information in the posting text, notification, or customer name. You can even set up a search rule to post the payment automatically on the customer. 

## To perform a bank account reconciliation

The following describes how built-in logic reconciles and transfers unposted lines to the general, payment, employee, and cash recipient journals.

1. From the Role Center, open **Bank Account Reconciliation** and select NORDEA721.
2. In the action bar, select **Home** > **Import and Match Bank Statement**. The statement will load and search for rules and various setups and then match and reconcile the lines.  

   Explain (some of) the possible statuses of the bank statement lines:

   | **Status**                                | **Description**                                              |
   | ----------------------------------------- | ------------------------------------------------------------ |
   | **Unsolved** (Red, bold)                  | No direct match found. Requires manual review in the **Payment Application Review** page to identify and apply the correct ledger entry. |
   | **Pending** (Yellow)                      | A payment proposal is generated but not fully applied. Users must review and reconcile in on of the journals. |
   | **Related Party Matched** (Blue)          | A matching account (customer, vendor, or employee) was found, but no corresponding ledger entry. Manual application may be needed. |
   | **Review Proposals** (Yellow)             | A matching ledger entry exists, but the amounts differ. Users must review and manually apply the correct amount. |
   | **Completed** (Green, bold)               | The transaction has been successfully matched and reconciled. No further action needed. |
   | **Search Rule Invalid** (Yellow)          | There is a search rule, but it lacks information on what to do with the bank statement entry. For example, about where do you want it to be posted. Users must correct the rule and re-run reconciliation. |
   | **Search Rule Matched** (Yellow)          | A Search Rule successfully assigned values to the **Account Type** and **Account No.**. No further action required unless reviewing. |
   | **Pending Cash Receipt Journal** (Yellow) | A journal line was created and it must be posted before the payments can be reconciled. |
   | **Pending General Journal** (Yellow)      | A journal line was created using a **G/L Account** and requires posting. |
   | **Pending Payment Journal** (Yellow)      | A journal line was created using a **Vendor or Employee Ledger Entry** and requires posting. |
   | **Difference** (Red)                      | There is an unresolved amount discrepancy. Users can transfer, post, adjust, or check settings for handling differences. |
   | **Manual**                                | If a matching record cannot be found, the status remains *Unsolved*. You can then manually change the status to *Manual* to indicate that the user needs to manually manage the posting for a specific line, typically in cases where automatic rules, such as search rules, don't apply. |

   

Now, take a look at the lines you've imported. Some may not require any further action. However, any **Unsolved** lines must be reviewed and resolved. Let’s go through the list and examine each unresolved case.

### First unsolved line: bank fee

This transaction represents a bank fee. You can create a search rule to automatically post bank fees to the appropriate G/L account. When configuring search rules, you can set them to always apply, apply with a proposal, or apply without a proposal. To ensure the rule takes effect in the current reconciliation, consider using the **Create Journal Line Method** and selecting **Match Automatically**. Once the rule is activated, journal lines can either be created manually or generated automatically.

### Second unsolved line: bank interest

This transaction represents bank interest. Similar to bank fees, you can create a search rule to automatically post bank interest to the relevant G/L account. Look for the line with the description **Rente**, copy the word, and then add a search rule from the top menu. Use **G/L account 07110** for the posting. You can configure the rule to always apply, apply with a proposal, or apply without a proposal. Additionally, clarify that journal lines can be created manually or automatically once the rule is activated.

### Third unsolved line: customer payment

Further down the page, you encounter another unsolved line: a customer payment for a sales invoice that has not yet been registered in the system.

You can create a search rule to post this payment to the correct customer account. To do this, click **Details** in the third line to create the search rule, then delete everything except **Amazonia**. Set the search method to **From left** and choose **Without proposal** for the usage type. Ensure the **Create Journal Line Method** is set to **Always**. This configuration ensures the rule applies automatically without a proposal. After the rule is set, you can verify its effectiveness in the subsequent bank account reconciliation statement line.


### Final line: Related Party Match

The last line in the reconciliation is marked as **Related Party Match**. Open Proposals to show that a match has been identified based on IBAN and address. **Select Apply Entries**, then explain how the entries now belong solely to this related party match.

### Additional lines that you can show

* The completed lines are payments from the payment journal:
  * Select **Proposals** on one of the lines.
  * Verify that the match was found using the End-to-End ID.
* Customer payments with payment discounts. There are three lines with the description "Vedr. Fak.:…". These represent payments that showcase how customer payments with payment discounts are handled. All matches are found using the Document Number:
  * First payment: The customer paid within the due date. At the bottom of the page, verify that the payment is handled according to the General ledger setup.
  * Second payment: The customer paid after the due date but within the tolerance set in the general ledger. Verify at the bottom of the page that everything is handled correctly.
  * Third payment: The customer paid after the due date and within the tolerance setup in the general ledger. Additionally, the customer paid a slightly lower amount. This is also handled according to the General ledger setup, as shown at the bottom of the page.


* Payments covering multiple invoices. There is a line with five proposals:
  1. Select **Proposals** to see that this payment covers multiple invoices.
  1. Confirm that all customer ledger entries were matched and applied based on the details in the statement line.
  1. Verify that the matches were found using the document number.


* Payment with FIK reference. One line contains a FIK reference in the description. This payment is automatically matched with a customer ledger entry based on the payment reference rule for FIK references. This feature is still in Preview. You can view Payment Reference Rules in the top menu: **Rules** > **Payment Reference Rules**.

## To view and post the journals

In this setup, if a bank account ledger entry doesn't match a bank statement line, journal lines will automatically be generated as reconciliation suggestions if the open ledger entries can be identified based on customer-, vendor-, or employee number, payment ID, or document no. If any reconciliation rules have been defined, these will also be used to generate reconciliation suggestions.

In the following journals, you can look through the suggestions and the lines you created.

1. From the **Bank Account Reconciliation** page, select **Journals** in the action bar and then select the relevant journal. Alternatively, on the **General** FastTab, in the **Related Lines in Journal** section, select the number to open the journal. 
2. You can open the journals and post the lines from there or select **Journals** > **Post all Journal lines** to create the bank account ledger entries from all the journals in one go. Note that the status of the bank statement lines has been updated to **Completed**.
3. You can now post the Bank Account Reconciliation. 

## To undo a bank account reconciliation

Explain how it's possible to undo something after the reconciliation has been posted from the relevant bank account card. 

1. From the Role Center, open **Bank Accounts** from the action menu, select a bank, and select **Bank Account** > **Statements**, and then select the reconciliation. Here you can see all the lines in the statement and select **Undo**.
2. This will reopen the reconciliation. Select **Matching** > **Match Automatically** to initiate a new reconciliation. All lines will be matched, and you can adjust any incorrect matches.
3. Once all corrections are made, post the reconciliation again.



## To run the assisted setup guides

In the demo environment, Continia Banking is set up according to the settings described in this section. You can use the step-by-step procedures below to show how to set up Continia Banking and customize the basic settings

You can configure Continia Banking through guided assisted setups. These setups are available for various modules and the general setup. You can access the setups on the Continia Banking Setup page, through a direct search using the {{search}} icon, or on the dedicated Banking Import Setup and Banking Export Setup pages.

1. From the Role Center, search for Continia Banking Setup and select the related link. The **Continia Banking Setup** page opens and displays an overview of the general setup.
1. In the action menu, select **Assisted Setup** to access the assisted guides that help you run through all the basic setup. The assisted guides have already been run in the demo environment, but to explain what the different guides do, open and go through the guides.

## To run a manual setup

In addition to the assisted setup guides, Continia Banking offers Manual Setup pages that allow you to configure Continia Banking according to your specific requirements. You can access the setups on the Continia Banking Setup page, through a direct search using the {{search}} icon, or on the dedicated pages.

1. Go back to the **Continia Banking Setup** page, and in the action menu, select **Manual Setup** and go through each of the following setups. 
2. **Payment Balance Account Setup** – Define which banks should be used for payments based on currency. If the currency code is left blank, Continia Banking will use the specified bank for all transactions that do not have an individual currency setup.
3. **Bank Closing Days Setup** – Configure bank holidays for multiple countries and future years. If a payment date falls on a bank closing day, you can set Continia Banking to automatically move it forward or backward to the next available business day.
4. **Payment Suggestion Template** – Create and manage predefined templates for payment suggestions. These templates allow bookkeepers to efficiently process payments by applying customized filters, managing job queues for automation, and optimizing discounts.


## 	To customize payment information on a vendor

The following section goes through the payment information setup on a vendor. 

1. Search for Vendors, and select the related link.
1. Select Vendor CBA.C00003, and scroll down to the **Payments** FastTab.
   - Explain how to set up the **Balance Account No.** and **Payment Method Code** fields.
   - Go through the **Remittance Advice** section that is based on the standard setup. Make sure to add the **Recipient Email**.
1. Explain the field in the **Alternative Vendor Information** FastTab.
1. On the action bar, select **Vendor** > **Bank Accounts**. Select a bank and show the bank setup. 
1. Explain how users can update the vendor bank information and how it works based on the IBAN. Change the vendor address, select **Update Vendor Bank Account Info**, and show how the data is updated. 

