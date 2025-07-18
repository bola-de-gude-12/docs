# Continia Payment Management Demo Script

This demo script provides a detailed description of how to demo the standard features in Continia Payment Management. The purpose of the Continia demo systems is to give Continia partners an environment to educate end customers and to present and test the latest versions of Continia Payment Management. 

This demo environment is already set up and ready to use, and it's always up-to-date with the latest version of Payment Management. Working with the demo script requires basic knowledge of Payment Management.

The demo script covers the following processes:

| Process                                                      | Description                                                  |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [To create a purchase invoice](#to-create-a-purchase-invoice) | How to create and validate a purchase invoice.               |
| [To suggest vendor payments](#to-suggest-vendor-payments)    | How to set up the payment journal and suggest vendor payments. |
| [To enable bank account verification](#to-enable-bank-account-verification) | How to add the extra level of security by incorporating bank account verification. |
| [To approve and send payments to the bank](#to-approve-and-send-payments-to-the-bank) | How to approve the suggested vendor payments and send them to the bank to be paid. |
| [To set up bank account reconciliation rules](#to-set-up-bank-account-reconciliation-rules) | How to use rules to improve the matching rate in the reconciliation. |
| [To perform a bank account reconciliation](#to-perform-a-bank-account-reconciliation) | How to match the bank statement lines with the bank account ledger entries. |
| [To view and post the journals](#to-view-and-post-the-journals) | How to post the journals after the reconciliation.           |
| [To undo a bank account reconciliation](#to-undo-a-bank-account-reconciliation) | How to undo the reconciliation in situations where you need to correct or adjust a match. |
| [To include payment data from Payment Service Providers](#to-include-payment-data-from-a-payment-service-provider) | How to include real-time updated payment data from third-party payment service providers. |
| [To run the assisted setup guides](#to-run-the-assisted-setup-guides) | How to set up the basics of Payment Management by running the assisted setup guides. |
| [To customize payment information on a vendor](#to-customize-payment-information-on-a-vendor) | How to adjust the default payment information settings on a vendor. |
| [To customize Statement Intelligence](#to-customize-statement-intelligence) | How to set up Statement Intelligence on a bank account card. |
| [To create the scenario data](#to-create-the-scenario-data)  | How to recreate the scenario data and bank account statement if you want to run the demo script a second time. |

## Users in the demo environment

The following user roles are available for the demo environment. Please find the sign-in information for these user roles in your email about the demo environment.

| User role  | Description                                                  |
| ---------- | ------------------------------------------------------------ |
| Controller | This user is the person that typically performs day-to-day accounting in Microsoft Dynamics 365 Business Central related to invoice management, vendor payment suggestions, etc. |
| Approver   | This user is the person that approves invoices, credit memos, vendor payments, etc. The demo environment is set up with Payment Approval, meaning that all payments must be approved before they can be sent to the bank. |



## To create a purchase invoice

This section covers how to create a purchase invoice for vendor 90000. 

1. Sign in to Business Central as the controller. You can find the sign-in information for the controller user role in the email you received about the demo environment.

2. Open the vendor card of vendor 90000, and in the action menu, select **New Document** > **Purchase Invoice**. 

3. In the **General** FastTab, in the **Vendor Invoice No.** field, enter "1001". 

4. In the **Lines** section, fill in the fields with the following values:

   * No: 1896-S 

   * Quantity: 1 

5. On the action bar, select **Post** > **Post** and select **Yes**.

6. Select **No** when prompted to open the posted invoice.

Feel free to make more purchase invoices.



## To suggest vendor payments

This section describes finding and validating the vendor payments that must be paid. 

To set up the payment journal and suggest vendor payments:

1. Search for **Payment Journals**, then select the related link.
1. In the **Batch Name** field, select the "PMT.JNL." journal.
1. On the action bar, select **Prepare** > **Payment Journal Setup**. Check the setup: 
   - The **Required Posting Status** field. It is set to "Paid."
   - The **Last Due Date Calculation** field. It is set to "28D".
   - **Summarize Per Vendor**. It is enabled by default. 
1. Return to the payment journal, and on the action bar, select **Home** > **Suggest Vendor Payments**. 
1. Use the default settings and select **OK**.  The purchase invoice you made earlier now appears in the payment journal with status "Valid." 
1. Go through the payment status of each line and show how they are validated.

   - Explain how users can use the **Payment File Errors** FactBox.
   - Explain how users can use the information in the **Payment Notification** FactBox.
1. Before selecting all lines and sending them for approval, briefly mention the the Bank Account Verification feature by navigating to the **Recipient Bank Details** FactBox, and the **Verification Status** field.
1. Select all lines in the payment journal, and on the action menu, select **Request Approval** > **Send Approval Request** > **Selected Journal Lines**. The status of the journal lines changes to **Pending Approval**.

## To enable bank account verification

1. Explain that you can enable Bank Account Verification on the main **Payment Management Setup** page.

   * On the **Purchase and Payments** FastTab, go to **Approval** and enable **Bank Account Verification**.
   * Explain what happens when you select Yes and that the verification status can be revoked if any of the following fields is modified: Bank Branch No., Bank Account No., IBAN, Swift Code, Transit No., Bank Clearing Code.

1. Explain how to verify a new bank account. Open the 20000 Vendor bank account card on the action bar and select **Verify account**. 

   * Explain that if you trust the bank account, and want to assign the Verified status, you can use the **Verification Method** field to indicate how the bank account was verified: by Email, Phone, or Other.

1. On the Payment Journal page, navigate to the **Recipient Bank Details** FactBox, and select the value in the **Verification Status** field to initiate the verification process for the vendor's bank account. 

   * Explain that if a line includes a bank account status other than *Verified*, attempting to send the payment suggestion will result in an error message. 

   * Point out that the bottom line is not verified when making the payment suggestion, and will therefore cause an error when trying to send it. 
   
     

## To approve and send payments to the bank

1. Sign in to Business Central as the approver. You can find the sign-in information for the approver user role in the email you received about the demo environment.

1. In the Role Center, navigate to the **Payment Approvals Cue** group and select the **Requests to Approve** action tile.

1. On the **Requests to Approve** page, select all lines, select **Approve**, and close the page.

1. Open the payment journal "PMT.JNL." and highlight how the status has changed to "Approved."

1. To export the payments to the bank, select **Home** > **Export/Send payments**. 

1. In the **Do you want to export** dialog box, select **All Lines** and .

1. Explain and show that the line's status has changed to "Sent."

1. On the action menu, select **Home** > **Update Status** and show that the line status changes to "Processing."

1. Select **Home** > **Update Status** again and show that the line status changes to "Paid."

1. To post the journal, select **Home** > **Post**, and select **Yes**.



## To set up bank account reconciliation rules

Before doing the bank account reconciliation, show how the reconciliation rules can ease the process.  

1. Search for and open **Bank Account Reconciliations**.
1. On the action bar, select **New**. 
1. In the **Bank Account No.** field, select {param1}. 
1. In the action menu, select **Rules** and the type of rule you want to create:
   * **General reconciliation rules** - you can set up general reconciliation rules, for example, Fee and Interest, so that Statement Intelligence automatically reconciles, transfers, and enters the appropriate lines in the journal. This demo environment is set up with rules for fees and interests. If you want to change this, ensure the account has direct posting.
   * **Customer, vendor, and employee reconciliation rules** - you can set up customer, vendor, or employee reconciliation rules to improve the match rate in the reconciliation. For example, if a customer doesn’t send any helpful information in the posting text, notification, or customer name. This demo environment is set up so that if a customer writes {param2} in the posting text, the line will match customer 90040.
   * **Merge rules** - with merge rules, you can define rules that combine several account statement lines into one or more entries, for example, one entry per day or one entry per credit card terminal. In the demo environment, an account statement has been imported into the reconciliation journal. The payment description in the file is {param3}. In the description, the date is placed in positions 7-10 (0102), the credit card terminal number is 4015711, and the rest is a slip number.
     On the **Merge rules** page, a rule is set up to create one account statement line per day per terminal. The **Text** field includes a wildcard (*) that indicates the credit card terminal number. Positions 7-10 in the **Merge by positions** field indicate the date you want to merge. 



## To perform a bank account reconciliation

The following describes how Statement Intelligence can reconcile and transfer not yet posted lines to the general and cash recipient journals.

1. From the Role Center, open **Bank Account Reconciliations**.

2. Select {param1}.

3. In the action bar, select **Home** > **Import Bank Statement**. The statement will load and search for rules and various setups and then match and reconcile the lines.  

   The possible statuses of the bank statement lines:	

   - **OK** - a bank post has been found, and the reconciliation of this line is OK.
   - **Unsolved** - a direct match hasn't been found, and the line needs to be reconciled.
   - **Awaiting Cash Rcpt. Jnl**. - a match has been found, and the line has been transferred to the cash receipt journal – ready to be posted.
   - **Awaiting G/L Jnl.** - the line has been moved to the G/L Journal and is ready to be posted.
   - **Awaiting Payment Jnl**.: - the line has been moved to a payment journal and is ready to be posted.

Now take a look at the lines that you've imported. Some of the lines are OK and do not need any attention, but if there are any unsolved lines, you will need to resolve them. Let’s run down the list and look at all the unsolved lines.

### The 1st unsolved line

If you look at the first unsolved line, you can see that a bank account ledger entry matches the amount, and the invoice number is also the same. The thing that prevents a match is the date requirement in our setup, which also requires the dates to match. 

> [!TIP]
> To avoid this in the future, you can change this to allow the dates to deviate from each other. To do this, search for **Manual Setup**, search for **Banks** and open the bank card. Navigate to the **Statement Intelligence** FastTab and specify the allowed deviation in the fields **Tolerance Days - Before** and **Tolerance Days - After**. 

For now, you can do a manual match by selecting the two lines - one on each side, and then, in the action bar, select **Matching** > **Match Manually**. 

The lines will now have the status OK. 

### The 2nd unsolved line

For this line, you can see that there is a reconciliation suggestion. Select the number in the **No. of Reconciliation Suggestions** field to see that the suggested match is based on the document number found in the **Additional Info** field. 

The match wasn't created automatically because the original invoice is for a larger amount than the customer has paid. In the column **Original PMT. Disc.** Possibly, you can see that they had the option to receive a discount, and from the amount that they paid, you can tell that they opted for it. However, the payment didn't fall within the time limit, so the amounts do not match. 

Select **OK** to create the line in the cash receipt journal. In the reconciliation overview, note that the status changed to Awaiting Cash Receipt Journal.

> [!NOTE]
> You'll come across this line again later on in the journals. 

### The 3rd unsolved line

Further down the page, you find another unsolved line: a payment from the account that has not yet been registered in the internal system. 

When you have confirmed that this is an intentional payment, you can select the **Manual Handling** box and, in the action bar, select **Home** > **Create Journal Lines**. 

> [!NOTE]
> When you take a look at the general journal, later on, you'll be able to see this line.

### The 4th unsolved line

On the last unsolved line, there's a reconciliation suggestion in the **No. of Reconciliation Suggestions** column. 

Open the reconciliation suggestion to see that this has been made based on the document number found in **Additional Information**. You'll also notice a slight difference in the amount, which could be because of rounding. 

To accept the difference, select **OK**. The line is then created in the cash receipt journal.   

That's all for the unsolved lines. Other lines that you should point out are:

- Payment from headquarters: 2 payments were handled by Statement Intelligence, and the lines will be visible in the cash receipt journal.
- Merged lines: 2 lines that were handled by the merge rule.

## To view and post the journals

In this setup, if a bank account ledger entry doesn't match a bank statement line, journal lines will automatically be generated as reconciliation suggestions if the open ledger entries can be identified based on customer-, vendor-, or employee number, payment ID, or document no. If any reconciliation rules have been defined, these will also be used to generate reconciliation suggestions.

In the following journals, you can look through the suggestions and the lines you created.

- From the **Bank Account Reconciliation** page, select **Journals** in the action bar and then the relevant journal. 



### The cash receipt journal

The cash receipt journal is for incoming payments, and when you open it, you get notified that there are a few entries with differences. You already know this because you accepted the differences when solving the lines. 

- The first two lines are simply regular payments with sufficient information to match an open ledger entry. 
- The following line was matched due to the customer rule we saw earlier. The text 'Deperfinis Ltd.' in the description defines which customer number to use, and this line was then automatically created in the journal.
- The following line was created because of the customer number, which was located in the description.
- The following three consist of a joint payment from the headquarters and two lines where the amounts were distributed on the correct invoices. This was done based on the document number in the additional information.
- The following line is the line with the previously accepted payment discount.
- The last line is the line with the difference in the amount which you also accepted. 

Now post the journal. When you select **OK**, the bank account ledger entries are created, and the status on the bank statement lines changes to OK.

### The general journal

If there are any differences in the amount on the bank statement lines caused by missing ledger entries, you can specify a general journal to be used by Statement Intelligence for creating general ledger posting suggestions. 

Examples of missing ledger entries are coverings, interests, and fees. In this case, amount differences will be created as ledger entries in a general ledger journal and are ready to be posted. 

- The first two lines in the general journal are created based on the rules you created for incoming payments with the words Fee or Interest. You can see that they've been posted with the correct balance account, which was also set up in the rules.

- The following line, you created from one of the unsolved lines, and it doesn't have an account. To be able to post the journal, you must first select the account you want to post this line to. 

  > [!TIP]
  >
  > The following G/L accounts are suitable in the context, depending on your localization. 
  >
  > **DK: 05650, GB: 10330, NL: 3930, NO: 8210, SE: 6230**

Select **Home** > **Post** to create the bank account ledger entries. Note that the status of the bank statement lines has been updated to OK. 

> [!NOTE]
> There are no lines in the payment journal or the employee payment journal.

Now, go back to the bank account reconciliation and post it by selecting **Home** > **Post** in the action bar.     



## To undo a bank account reconciliation

Explain how it's possible to undo something after the reconciliation has been posted from the relevant bank account card. From the Role Center, open **Bank Accounts** from the action menu, select a bank, and select **Bank Account** > **Statements,** and then select the reconciliation. Here you can see all the lines in the statement and select **Undo**.

This will reopen the reconciliation where you select **Matching** > **Match Automatically** to perform a new reconciliation. All lines will match, and you can change the wrong match. 

After making all the appropriate corrections, you must post the reconciliation again.  

## To include payment data from a Payment Service Provider

Explain that Payment Management supports file imports from third-party Payment Service Providers (PSPs) such as Amazon, bol.com, Paypal, and Klarna). 

For this scenario, you can create scenario data: On the Role Center, open the **Welcome to the Continia Demo environment** notification and select **Next**. Select **Scenarios** > **Create PSP Klarna data**, then select **Create Scenario Data**. Once you execute this action, the Klarna demo settlement file will be downloaded to your designated download folder automatically.

1. Explain that before adding a PSP agreement, you must apply a few general settings. Go to **Payment Management Setup**, and on the **Payment Receipt Import** FastTab, in the **Update External Payment Reference** field, select **Using External Reference No.**.
2. Go through the process of adding an agreement for a payment service provider: use the search icon, and enter **PSP Agreement Setup**. Explain the Klarna agreement in the system, and how Continia adds default rules for fees and other charges to separate costs.
3. Explain that you can now import a Klarna statement. Go to **Cash Receipt Journals,** navigate to the KLARNA journal, and show how the **Payment Service Provider Journal** checkbox is selected for the journal.
4. Open the KLARNA journal, and on the action bar, select **Import Payments**. Add the Klarna statement.
5. Explain how the different transaction types are posted on G/L accounts automatically, based on the setup.

## To set up and customize Payment Management

In the demo environment, Payment Management is set up according to the settings in this section. You can use the step-by-step procedures below to show how to set up Payment Management and customize the basic settings.  



## To run the assisted setup guides

1. From the Role Center, search for Payment Management Setup and select the related link. The **Payment Management Setup** page opens and displays an overview of the general setup.

1. In the action menu, select **Assisted Setup** to access the assisted guides that help you run through all the basic setup. The assisted guides have already been run in the demo environment, but to explain what the different guides do, open and go through the guides.

   

## To adjust the Payment Management Setup

Go back to the **Payment Management Setup** page, and in the action menu, select **Manual Setup**. Select and go through each of the following setups.

| Setup                        | Description                                                  |
| ---------------------------- | ------------------------------------------------------------ |
| Banks                        | <ol><li>Select the bank: {param4} </li><li>On the bank card, scroll down to the **Statement Intelligence** FastTab. Go through the search principles and how to set up tolerance days to improve the match rate during the reconciliation process. </li><li>On the **Advanced** FastTab, explain how you set up the archive to store the communication between the bank and Business Central for a period. On the action menu, select **Archive** > **File Archive** to show where the files are stored. This is only used in the rare case that something doesn't go as planned. <li>Explain the **Update Payment Journal** field option to update the payment journal status automatically or manually on the Advanced FastTab. </li><li>In the action menu, select **Connection** and go through how users can import or export a certificate and allow other companies in the environment to use it.</li></ol> |
| Balance Account Setup        | In the **Balance Account Setup**, you set up from which banks, depending on the currency, payments should be made. If the currency code is blank, Payment Management will use the specified bank for all banks that are not set up with individual currency. |
| Bank Holiday Setup           | In the **Bank Holiday Setup**, bank holidays for several countries and years into the future are listed. If a payment falls on a bank holiday, you can set up Payment Management to move it forward or backward to an open bank day. |
| Currency Exchange Rate Setup | <ol><li>In the **Currency Exchange Rate Setup**, select ECB as the currency exchange rate provider, and enable **Automatic Import**. </li><li>If you want to change the import schedule, ensure the status under **Recurrence of Import** is set to On Hold. When completing the recurrence setup, change the status back to Ready by selecting **Ready/On Hold**. </li><li>The exchange rates will automatically be updated from ECB. You can also manually download the exchange rates using the **Import Currency Exchange Rates** button.</li></ol> |
| Payment Notification Setup   | <ol><li>In the **Notification setup**, show that the default notification is SHORT-TXT. To explain exactly what that means, show the **Recipient Reference Template** and the **Payment Notification Template** at the bottom of the page and a preview of how they will look. </li><li>Go back to the top of the page and go through the different default notification methods.</li><li>Explain the functionality of the **Limit Notification Size** toggle.</li><li>Explain how a person in the company can receive all payment notifications, by entering their email address in the **BCC Email for Payment Notifications** field.</li><li>Go through the three different email sending methods.</li><li>Go through the 4 buttons in the action menu:</li>    - **View Unsent Emails...**  <br />    - **Email Template Setup**:  Open and show how the content of the email notification is selected from different tables. View the email preview on the right side of the page. Show how you can enable or disable the company logo and the email signature. <br />    - **Update Payment Notification Templates** <br />    - **Foreign Notification Designations** |
| Statement Intelligence Setup | <ol><li>Explain how Statement Intelligence is helpful for bank account reconciliations.</li><li>On the **General** FastTab, show how you can set up Statement Intelligence to manage and create journal lines in the bank account reconciliation when you import bank account statements.</li><li>Go to the **Journals** FastTab, and go through the setup of the general, customer, vendor, and employee journals.</li><li>Explain how you can also set up the journals on the individual bank accounts and in which cases this is useful.</li> |


## 	To customize payment information on a vendor

The following section goes through the Payment Information Setup on a vendor. 

1. Search for Vendors, and choose the related link.

1. Select Vendor 90000, and scroll down to the **Payments** FastTab.
   - Explain how to set up the **Balance Account No.** and **Payment Method Code** fields.
   - Go through the **Notification** section that is based on the standard setup. Make sure to add the **Recipient Email**.
1. Under the **Alternative Vendor Information** FastTab, explain how to use and fill in the relevant information.
1. In the action bar, select **Vendor** > **Bank Accounts**. Select a bank and show the bank setup. 
   - Explain how users can update the vendor bank information and how it works based on the IBAN. Change the vendor address, select **Update Vendor Bank Account Info**, and show how the data is updated. 

## To customize Statement Intelligence

The setup of Statement Intelligence has already been set up. However, you should go through the following settings in your demonstration. 

- **The default setup**
  - To configure the default setup, navigate to **Payment Management Setup**, access **Manual Setup**, and select **Statement Intelligence Setup**. 
  - Here, you set up to which journals you want to post cash receipt journals, general journals, and payment journals.
- **The bank accounts setup**
  - To set up Statement Intelligence on the bank accounts, navigate to the list of bank accounts and select {param1}. 
  - On the bank account card, scroll down to the **Statement Intelligence** FastTab to configure the specific journal setup for this bank account and set up tolerance deviation.
  - Go through the details of the section **Multiple Bank Statements per Reconciliation**. 
  - Explain that you can add a job queue to import and reconcile bank account statements.

## To create the scenario data

When you've run a demo of Payment Management using this demo script, you can re-create the original scenario data and run the demo scripts from the beginning. 

To recreate the demo data:

1. On the Role Center, open the **Welcome to the Continia Demo environment** notification and select **Next**.
2. Select **Scenarios** and then **Create Scenario Data**. 
3. Navigate to the **Bank Account Reconciliations** page and import a new demo bank account statement. 