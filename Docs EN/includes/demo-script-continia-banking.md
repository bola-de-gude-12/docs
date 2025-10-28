> [!IMPORTANT]
>
> The Continia Banking demo script will be updated as development progresses.

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
5. On the **Suggest Vendor Payments** page, use the default settings, enable **Summarize per Vendor** (use the **Show more** option if this field is not displayed) and select **OK**. The payment lines will now be created.
6. Go through the payment status of each line and show how they are validated. Use the following FactBoxes to assist in the process:
   - **Line Information FactBox** – displays the next steps and any approval details related to the transaction. Review this section to understand what actions are required and check for any approval information.
   - **Payment Journal Errors FactBox** – provides guided assistance to correct errors. Click on the suggested fields or areas to make corrections directly.
   - **Recipient Bank Details** – verifies the bank account for a selected transaction line that requires validation. Ensure that the correct bank details are assigned before proceeding.
   - **Applied Entries FactBox** – summarizes applied entries and allows direct access to related posted purchase invoices for easy cross-referencing.
   - **Remittance Information FactBox** – displays the generated remittance text, particularly useful for summarized transactions. Verify the details to ensure accurate payment communication.
7. If you want to show details from the lines:

   - **Line 1** – this is a summarized payment. Show the **Remittance Information**, then open one of the **Applied Entries** and display the **Posted Purchase Invoice**. Explain that with CEM and CDC installed, you can view the original document and see if it was previously approved.
   - **Line 3** – this is a payment with a {param1} reference. Show that the **Payment Reference** field contains the {param1} reference.
   - **Line 4** – this is an international payment. Show that the **Payment Method Code** is *BTI* and the **Cost Type** is *Shared*.

8. To send the payments for approval, export the payments to the bank by selecting **Prepare > Send Approval Request**.
9. Show that the line status changes to **Pending Approval**.
10. Navigate to the **Role Center** and open **Continia Banking Activities**. Select **Requests to Approve**.
11. Select the approval lines and on the action bar click **Approve**.
12. Return to the **Payment Journal**. All lines should now have the status **Approved**.
13. In the **Line Information FactBox**, show that the lines are now **Ready for Export** and the approval information is visible.
14. To export the payments to the bank, select **Home** > **Export/Send payments**. In the **Do you want to export** dialog box, select **All Lines**.
15. Explain and show that the line's status has changed to **Sent to Online**.
16. On the action menu, select **Home** > **Update Status** and show that the line status changes to **Processing**.
17. Select **Home** > **Update Status** again and show that the line status changes to **Paid**.
18. To post the journal, select **Home** > **Post**, and select **Yes**.


## To suggest vendor payments in Advanced mode

The **Advanced Payment Suggestion** setup in Continia Banking offers more flexibility and control over payments. Unlike the standard setup, payment suggestions remain on the **Payment Suggestions** page, allowing users to review and adjust recipient information before transferring payments to the Payment Journal. This section explains how to find and validate vendor payments in Advanced mode.

> [!IMPORTANT]
>
> If you already demoed suggesting vendor payments in Standard mode, there will be no suggestions for you to work with.  



### To create and review a payment suggestion

1. Search for and open **Payment Suggestion Templates**.
2. From the list, select the advanced payment suggestion.
3. Explain how payment suggestion templates function. Highlight that these templates offer more flexibility and automation compared to manually creating a payment suggestion - such as utilizing job queues for processing and different journal setups to manage payments efficiently.
4. On the action bar, click **Suggest Vendor Payments** to generate a payment suggestion containing multiple payments.
5. In the overview, highlight how the FactBox provides additional details.
6. Click the number to open the payment suggestion.
7. View the payments and select the payment suggestion status to open the **Payment Card**.

### The advantages of the Payment card

Explain how the **Payment card** provides:

- **Summarized payment information**, including payment methods, currency, and bank details.
- **Detailed payment overview**, with amounts per payment, recipient and sender bank account details, and applied payment methods.
- **Quick access to vendor and customer information** at the payment level.
- **Easy handling of partial payments and payment discounts** for each transaction.
- **Payments for Associations**, integrating **Continia Banking** with **Continia Finance** to manage vendor or customer association payments efficiently while maintaining standard checks.
- **Payment Suggestion Templates**, allowing predefined filter settings for faster recurring payment processes.

### To finalize payments

Once all lines are reviewed, transfer the payment lines to the **Payment Journal** by selecting **Create Gen. Journal Lines**.

### To complete the Payment Journal

After transferring, complete the process by:

1. Sending payments to the bank.
2. Updating payment statuses.
3. Posting transactions, following the standard workflow.

### To import a settlement file from a Payment Service Provider

1. Use the {{search}} icon to find and select **Cash Receipt Journals**.  
2. Go to the **Batch Name** field and from the dropdown list, select the **PSP JNL**.  
3. On the action bar, go to **Home > Import PSP Payments**.  
4. In the **Import Payments** dialog, enable **Create Balancing Account Lines Per Posting Date**, then select **OK** to continue.  
5. Explain the different statuses of the lines: some payments are applied directly to customer ledger entries, while others are posted to G/L accounts depending on the transaction type.  
6. To post the journal, select **Home > Post**, then confirm by selecting **Yes**.  

### To import a customer payment file into the Payment Reconciliation Journal

1. From the Role Center, open **Payment Reconciliations**.  
2. On the action bar, click **New Journal**.  
3. Select the journal {param9}.  
4. On the action bar, go to **Page > Show more actions**.  
5. Then select **Home > Import and apply payments**  
6. Explain how payment matches are made using **Payment Reference Rules** based on country-specific formats, such as KID payments, BG payments, and FIK payments.  
7. To post the journal, select **Home > Post Payments Only**, and confirm by selecting **Yes**.  

## To set up search rules

Before doing the bank account reconciliation, show how the reconciliation rules can ease the process. Search rules streamline the bank account reconciliation process by automatically matching transactions to the correct accounts based on specific text criteria. Even when date and amount don’t match, these rules help identify and assign ledger entries to the right accounts, making reconciliation faster and more efficient.

1. Search for and open **Bank Account Reconciliations**.
1. On the action bar, select **New**. 
1. In the **Bank Account No.** field, select {param9}. 
1. In the action menu, select **Rules** and the type of rule you want to create:
   * **G/L Account search rules** - the system has search rules set up for fee and interest, so that Continia Banking automatically reconciles, transfers, and enters the appropriate lines in the journal. You can create a rule, when you encounter the lines in the Bank Account Reconciliation. Make sure to select the dedicated accounts with direct posting.
   * **Customer, vendor, and employee search rules** - you can set up customer, vendor, or employee search rules to improve the match rate in the reconciliation. For example, to post the payment automatically on the customer. 

## To perform a bank account reconciliation

The following describes how built-in logic reconciles and transfers unposted lines to the general, payment, employee, and cash recipient journals.

1. From the Role Center, open **Bank Account Reconciliations** and select {param9}.

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

   

### Reviewing imported payment lines

Now, review the lines you’ve imported:  

- Some lines may not require any further action.  
- However, any **Unsolved** lines must be carefully reviewed and resolved. Unsolved lines usually appear if you haven’t posted the Payment Service Provider settlement or posted payments in the Payment Reconciliation Journal. These lines can be handled manually.

Explain how the first lines in the statement are matched with the bank account ledger entries created when posting the payment journal:  

- Select **Proposals** on one of the lines.  
- Verify the match by checking the **End-to-End ID** to confirm the connection between the payment and the bank transaction.  

#### 1. Bank fee line  

**Description:** {param2}

This transaction represents a bank fee. 
  - Explain that there is a search rule to automatically post bank fees to the appropriate G/L account.  
  - When configuring search rules, you can choose to:  
    - Always apply the rule  
    - Apply with a proposal  
    - Apply without a proposal  
  - Further explain how search rules can be set up. For example, show the **Create Journal Line Method** and select **Match Automatically**. Once activated, journal lines can be created either manually or automatically, depending on your configuration.

#### 2. Bank interest line  

**Description:** {param3}

This transaction represents bank interest. 
  - Similar to bank fees, a search rule automatically posts bank interest to the relevant G/L account.  

#### 3. Customer payment lines with discounts  

**Description:** {param4}:  102235, 102236, 102237  

These lines show payments applied to sales invoices with payment discounts.  
  - The line status is **Pending** in the cash receipt journal.  
  - The payments illustrate different scenarios based on payment discount dates and tolerances set in the General Ledger setup:  
    1. **First Payment** - paid within the due date. Verify at the bottom of the page that the payment follows the General Ledger setup.  
    2. **Second Payment** - paid after the due date but within the payment discount tolerance. Verify correctness at the bottom of the page.  
    3. **Third Payment** - paid after the due date, within tolerance, but slightly less than the invoice amount. The payment tolerance handles this, as per the General Ledger setup.

  - Explain that all matches are found using the **Document Number**.

#### 4. Webshop payments  

**Description**: {param5} 

  - The first payment is automatically matched to a sales invoice.  
  - The second payment is posted directly to the customer, based on a rule applied when no matching sales invoice exists.

#### 5. Multiple invoice payment  

**Description:** 102242, 102243, 102244, 102245, 102246  

  - One payment matching five different sales invoices or customer ledger entries.  
  - All applications are automatic.

#### 6. Payment reference match  

**Description:** {param6}

  - This payment is matched based on a payment reference rule.

#### 7. Related party match  

**Description:** {param7}

  - There is a related party match.  
  - By opening **Proposal**, you can select **Apply Entries** to link payments to customer ledger entries.  
  - If a difference arises, handle it by selecting **Home > Transfer Difference to Journal…**  
  - In the prompt, select the account where you want to post the difference.

#### 8. PSP and reference payments  

**Description:** Klarna 16626.65 and {param8}  

  - The first line matches the PSP posting in the cash receipt journal. 
  - The second line matches the reference payments posted in the Payment Reconciliation journal.  
  - Select **Proposal** on each line and verify the match by **Posting Date** and **Amount**.  
  - If you haven’t completed these steps, you can manually create a journal line to post them.

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
