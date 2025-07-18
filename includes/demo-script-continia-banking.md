# Continia Banking Demo Script

This demo script provides a structured walkthrough of how to demonstrate the standard features in Continia Banking. The Continia demo environment is designed for Continia partners to educate end customers and showcase the latest version of Continia Banking.

This demo environment is already set up and ready to use, and it's always up-to-date with the latest version of Continia Banking. Using this demo script requires a basic understanding of Continia Banking.

## Users in the demo environment

The following user roles are available in the demo environment. You can find the sign-in details in your email about the demo environment.

- **Controller** – Handles daily accounting tasks, such as processing invoices and generating payment suggestions.
- **Approver** – Reviews and approves invoices, credit memos, and vendor payments. Approval is required before payments can be processed.

## To suggest vendor payments in standard mode

This section explains how to identify and validate vendor payments that are due for processing. The standard mode provides a straightforward and efficient way to generate payment suggestions.

To set up the payment journal and suggest vendor payments:

1. Search for **Payment Journals**, then select the related link.

1. In the **Batch Name** field, select the PMT.JNL. journal.

1. On the action bar, select **Prepare** > **Payment Journal Setup**. Check the setup: 
   - The **Required Posting Status** field is set to "Paid."
   - The **Last Payment Date Calculation** field is set to "30D".

1. Return to the payment journal, and on the action bar, select **Home** > **Suggest Vendor Payments**. 

1. Use the default settings, make sure to check that it is setup to summarize and select **OK**. The payment lines will now be created.

1. Go through the payment status of each line and show how they are validated. Use the following FactBoxes to assist in the process:

   - **Line Information FactBox** – displays the next steps and any approval details related to the transaction. Review this section to understand what actions are required and check for any approval information.
   - **Payment Journal Errors FactBox** – provides guided assistance to correct errors. Click on the suggested fields or areas to make corrections directly.
   - **Recipient Bank Details** – verifies the bank account for a selected transaction line that requires validation. Ensure that the correct bank details are assigned before proceeding.
   - **Applied Entries FactBox** – summarizes applied entries and allows direct access to related posted purchase invoices for easy cross-referencing.
   - **Remittance Information FactBox** – displays the generated remittance text, particularly useful for summarized transactions. Verify the details to ensure accurate payment communication.

1. Select all lines in the payment journal, and on the action bar, select **Request Approval** > **Send Approval Request** > **Selected Journal Lines**. The status of the journal lines changes to **Pending Approval**. The **Payment Status** in the **Line Information** FactBox changes too.


## To enable bank account verification

1. Explain that you can enable Bank Account Verification on the main **Banking Export Setup** page:
   * On the **Approval** FastTab, enable **Use Bank Account Verification**.
1. Explain what happens when you get the prompt and you select **Yes** and that the verification status can be revoked if any of the following fields is modified: Bank Branch No., Bank Account No., IBAN, Swift Code, Transit No., Bank Clearing Code.
   * Show this on vendor CBA.C00003, navigate to bank account. Notice that it needs to be verified. 
1. Explain how to verify a new bank account. Open the CBA.C00003 Vendor bank account card on the action bar and select **Verify account**. 
1. Explain that if you trust the bank account, and want to assign the Verified status, you can use the **Verification Method** field to indicate how the bank account was verified: by Email, Phone, or Other:
   * On the **Payment Journal** page, navigate to the **Recipient Bank Details** FactBox, and select the value in the **Verification Status** field to initiate the verification process for the vendor's bank account. 
1. Explain that if a line includes a bank account status other than *Verified*, attempting to send the payment suggestion will result in an error message or the line being blocked. 

## To approve and send payments to the bank

1. Sign in to Business Central as the approver. You can find the sign-in information for the approver user role in the email you received about the demo environment.
1. In the Role Center, navigate to the **Payment Approvals Cue** group and select the **Requests to Approve** action tile.
1. On the **Requests to Approve** page, select all lines, select **Approve**, and close the page.
1. Open the payment journal "PMT.JNL." and highlight how the status has changed to **Approved**.
1. Show that the approval information and the next step is explained in the **Line Information** FactBox – **Ready for export**.
1. To export the payments to the bank, select **Home** > **Export/Send payments**. 
1. In the **Do you want to export** dialog box, select **All Lines**.
1. Explain and show that the line's status has changed to **Sent to online**.
1. On the action menu, select **Home** > **Update Status** and show that the line status changes to **Processing**.
1. Select **Home** > **Update Status** again and show that the line status changes to **Paid**.
1. To post the journal, select **Home** > **Post**, and select **Yes**.



## To suggest vendor payments in Advanced mode
This section explains how to find and validate vendor payments in **Advanced mode**.

### Enable Advanced mode
To enable **Advanced Payment Suggestion**, explain it important to check that the **Payment Journal** has no existing lines. The system will not allow you to proceed if any lines are open.
1. Search for and open the **Banking Export Setup** page.
2. Enable **Advanced Payment Suggestion**.

### To create and review a payment suggestion
1. Search for and open **Payment Suggestion**.
2. Select **Suggest Vendor Payments** to generate a payment suggestion containing multiple payments.
3. In the overview, highlight how the FactBox provides additional details.
4. Click the number to open the payment suggestion.
5. View the  payments and select the payment suggestion status to open the **Payment Card**.
### Advantages of the Payment card
Explain how the **Payment card** provides:
- **Summarized payment information**, including payment methods, currency, and bank details.
- **Detailed payment overview**, with amounts per payment, recipient and sender bank account details, and applied payment methods.
- **Quick access to vendor and customer information** at the payment level.
- **Easy handling of partial payments and payment discounts** for each transaction.
- **Payments for Associations**, integrating **Continia Banking** with **Continia Finance** to manage vendor or customer association payments efficiently while maintaining standard checks.
- **Payment Suggestion Templates**, allowing predefined filter settings for faster recurring payment processes.

### To finalize payments
Once all lines are reviewed, transfer the payment lines to the **Payment Journal** by selecting Create journal lines?

### To complete the Payment Journal
After transferring, complete the process by:
1. Sending payments to the bank.
2. Updating payment statuses.
3. Posting transactions, following the standard workflow.

## To set up search rules

Before doing the bank account reconciliation, show how the reconciliation rules can ease the process.  
1. Search for and open **Bank Account Reconciliations**.
1. On the action bar, select **New**. 
1. In the **Bank Account No.** field, select NORDEA721. 
1. In the action menu, select **Rules** and the type of rule you want to create:
   * **G/L Account Search Rules** - you can set up search rules, for example, Gebyr and Rente, so that Continia Banking automatically reconciles, transfers, and enters the appropriate lines in the journal. You can create a rule, when you encounter the lines in the Bank Account Reconciliation. Make sure to select the dedicated accounts with direct posting.
   * **Customer, vendor, and employee search rules** - you can set up customer, vendor, or employee search rules to improve the match rate in the reconciliation. For example, if a customer doesn’t send any helpful information in the posting text, notification, or customer name. You can even set up a search rule to post the payment automatically on the customer. This demo environment is set up so that if a customer writes Defernis in the posting text, the line will match customer CBA.C00003.
   
## To perform a bank account reconciliation

The following describes how built-in logic reconciles and transfers unposted lines to the general, payment, employee, and cash recipient journals.
1. From the Role Center, open **Bank Account Reconciliations**.
2. Select NORDEA721.
3. In the action bar, select **Home** > **Import and Match Bank Statement**. The statement will load and search for rules and various setups and then match and reconcile the lines.  

   The possible statuses of the bank statement lines:

   | **Status**                                | **Description**                                              |
   | ----------------------------------------- | ------------------------------------------------------------ |
   | **Unsolved** (Red, bold)                  | No direct match found. Requires manual review in the **Payment Application Review** page to identify and apply the correct ledger entry. |
   | **Pending** (Yellow)                      | A payment proposal is generated but not fully applied. Users must review and reconcile in the **Cash Receipt Journal** or **Bank Account Reconciliation**. |
   | **Related Party Matched** (Blue)          | A matching account (customer, vendor, or employee) was found, but no corresponding ledger entry. Manual application may be needed. |
   | **Review Proposals** (Yellow)             | A matching ledger entry exists, but the amounts differ. Users must review and manually apply the correct amount. |
   | **Completed** (Green, bold)               | The transaction has been successfully matched and reconciled. No further action needed. |
   | **Search Rule Invalid** (Yellow)          | A matched Search Rule is missing an **Account No.**. Users must correct the rule and re-run reconciliation. |
   | **Search Rule Matched** (Yellow)          | A Search Rule successfully assigned values to the **Account Type** and **Account No.**. No further action required unless reviewing. |
   | **Pending Cash Receipt Journal** (Yellow) | A journal line was created and awaits posting to reconcile payments in the **Bank Account Reconciliation**. |
   | **Pending General Journal** (Yellow)      | A journal line was created using a **G/L Account** and requires posting. |
   | **Pending Payment Journal** (Yellow)      | A journal line was created using a **Vendor or Employee Ledger Entry** and requires posting. |
   | **Difference** (Red)                      | There is an unresolved amount discrepancy. Users can transfer, post, adjust, or check settings for handling differences. |
   | **Manual**                                | If a matching record cannot be found, the status remains *Unsolved*. You can then manually change the status to *Manual* to indicate that the user needs to manually manage the posting for a specific line, typically in cases where automatic rules, such as search rules, don't apply. |
   
   

Now, take a look at the lines you've imported. Some are marked as **Completed** and require no further action. However, any **Unsolved** lines must be reviewed and resolved. Let’s go through the list and examine each unresolved case.

### First unsolved line: bank fee
This transaction represents a bank fee. You can create a search rule to automatically post bank fees to the appropriate G/L account. Explain how search rules can be configured to always apply, apply with a proposal, or apply without a proposal. Also, mention that once the rule is activated, journal lines can either be created manually or generated automatically.

### Second unsolved line: bank interest
This transaction represents bank interest. Similar to bank fees, you can create a search rule to automatically post bank interest to the relevant G/L account. Explain the available options for handling search rules: always apply, apply with a proposal, or apply without a proposal. Additionally, clarify that journal lines can be created manually or automatically once the rule is activated.

### Third unsolved line: customer payment
Further down the page, you encounter another unsolved line—a customer payment for a sales invoice that has not yet been registered in the system.

This payment originates from a webshop. You can create a search rule to post this payment to the correct customer account. Configure the rule to be used "without proposal", ensuring it only applies if no matching entry is found in the customer ledger entries. Point out how this can be verified in the following bank account reconciliation statement line.


### Final line: Related Party Match
The last line in the reconciliation is marked as **Related Party Match**. Open Proposals to show that a match has been identified based on IBAN and address. **Select Apply Entries**, then explain how the entries now belong solely to this related party match.

### Additional lines that you to show

* The first 12 completed lines are payments from the payment journal:

  * Select **Proposals** on one of the lines.

  *  Verify that the match was found using the End-to-End ID.


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

1. From the **Bank Account Reconciliation** page, select **Journals** in the action bar and then select the relevant journal. 
2. You can open the journals and post the lines from there or select **Home** > **Post all Journal lines** to create the bank account ledger entries from all the journals in one go. Note that the status of the bank statement lines has been updated to **Completed**.
3. You can now post the Bank Account Reconciliation. 

## To undo a bank account reconciliation
Explain how it's possible to undo something after the reconciliation has been posted from the relevant bank account card. 

1. From the Role Center, open **Bank Accounts** from the action menu, select a bank, and select **Bank Account** > **Statements**, and then select the reconciliation. Here you can see all the lines in the statement and select **Undo**.
2. This will reopen the reconciliation where you select **Matching** > **Match Automatically** to perform a new reconciliation. All lines will match, and you can change the wrong match. 
3. After making all the appropriate corrections, you must post the reconciliation again.  


## To set up and customize Continia Banking

In the demo environment, Continia Banking is set up according to the settings in this section. You can use the step-by-step procedures below to show how to set up Continia Banking and customize the basic settings.  

## To run the assisted setup guides

1. From the Role Center, search for Continia Banking Setup and select the related link. The **Continia Banking Setup** page opens and displays an overview of the general setup.
1. In the action menu, select **Assisted Setup** to access the assisted guides that help you run through all the basic setup. The assisted guides have already been run in the demo environment, but to explain what the different guides do, open and go through the guides.

## To adjust the Continia Banking Setup

1. Go back to the **Continia Banking Setup** page, and in the action menu, select **Manual Setup** and go through each of the following setups. 
2. **Payment Balance Account Setup** – Define which banks should be used for payments based on currency. If the currency code is left blank, Continia Banking will use the specified bank for all transactions that do not have an individual currency setup.
3. **Bank Closing Days Setup** – Configure bank holidays for multiple countries and future years. If a payment date falls on a bank closing day, you can set Continia Banking to automatically move it forward or backward to the next available business day.
4. **Payment Suggestion Template** – Create and manage predefined templates for payment suggestions. These templates allow bookkeepers to efficiently process payments by applying customized filters, managing job queues for automation, and optimizing discounts.


## 	To customize payment information on a vendor

The following section goes through the payment information setup on a vendor. 
1. Search for Vendors, and choose the related link.
1. Select Vendor CBA.C00003, and scroll down to the **Payments** FastTab.
   - Explain how to set up the **Balance Account No.** and **Payment Method Code** fields.
   - Go through the **Notification** section that is based on the standard setup. Make sure to add the **Recipient Email**.
1. Under the **Alternative Vendor Information** FastTab, explain how to use and fill in the relevant information.
1. On the action bar, select **Vendor** > **Bank Accounts**. Select a bank and show the bank setup. 
   - Explain how users can update the vendor bank information and how it works based on the IBAN. Change the vendor address, select **Update Vendor Bank Account Info**, and show how the data is updated. 

