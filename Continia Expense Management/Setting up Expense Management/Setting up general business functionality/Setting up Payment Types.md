---
title: Setting up payment types
date: 07-08-2025
description: Learn how to track various types of payments by creating payment types
id: EM-81  
lang: en
---
# Setting up payment types

Payment types in Expense Management offer a convenient way to categorize and track various types of expenses while being simple to configure and assign to users. You can assign multiple payment types to individual expense users or expense user groups, allowing for easy management of expenses from different credit cards or various types of cash payments.

Additionally, Expense Management comes with a collection of [unique icons](https://www.continia.com/expense-management-icons/) you can assign to your payment types, enhancing visual intuitiveness and user-friendliness for quick reference and recognition. If a specific icon you need is unavailable, you can request it by opening a support ticket. Note that the icons are currently limited to the Expense Mobile App.  

As an Expense admin, you can correct the Continia user credit card record if an incorrect user ID or payment type has been assigned, even when bank transactions are present. You can also change the setup on the payment type card, for example, Posting and Intermediate posting accounts.

<iframe src="https://player.vimeo.com/video/951415956?h=3ac6d99db8&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="9 Import credit card_Configure Payment Types"></iframe> 

## Create a payment type

To create a payment type:

1. Search for {{search}} **Payment Types**.
1. On the action bar, click **New**.
1. Enter information for the following fields:

   | Field                  | Description                                                  |
   | ---------------------- | ------------------------------------------------------------ |
   | Code                   | Specify the code to identify the payment type.               |
   | Description            | Provide a description for the payment type.                  |
   | Selectable             | Choose whether users can create expenses using this payment type. If set to "no," users must wait for expenses to be created and pushed to them. |
   | Submit Expenses in LCY | Specify if users are required to submit expenses in the local currency. |
   | Method                 | Select how to handle expenses for this payment type:<br /><ul><li>**Post on the Expense User's Account** - expenses will be posted on the expense user account, and the company will reimburse the user for the expense.</li><li>**Post on a business account** - expenses will be posted on a business account. If selected, provide the type and number of the account</li></ul> |
   | Posting Account       | This setup option is used when **Post at Import** on the **Expense Management Setup** page is enabled. <br /><br />Select how to post imported transactions for this payment type:<br /><ul><li>**Type** - imported transaction are posted to the selected account type. <br />It's recommended to select **Bank Account**, as it makes it easier to reconcile monthly statements from credit card providers.</li><li>**No.** - select the account on which imported transaction are posted.</li></ul> |
   | Intermediate Posting Account       | These are the setup options for the balancing account that's linked to the posting account setup.<br /><br />Select how to post imported transaction for this payment type to the balancing account:<br /><ul><li>**Type** - as default you can only select **G/L Account**.</li><li>**No.** - select the G/L account number.</li></ul><br /><br />When a credit card expense is posted, the intermediate posting account is balanced out, and the credit card expense is posted on the expense type posting account. |
   | Create Expense from Transaction | Specifies whether expenses are created automatically based on transactions. |
   | Matching Tolerance      | This is used if expense users create credit card expenses that are submitted right away without the credit card transaction having been imported. These credit card expenses will appear with the status **Open** in Business Central waiting to be matched with the credit card transactions. You can set a matching tolerance for both date (in number of days) and amount (in percent). From experience, and to automate the process as much as possible, it's recommended to set the matching tolerances to 2 days and 2 percent, as setting the matching tolerances too low, such as 0, will result in you having to match most of the expenses manually. |
   | Match to Expense       | Determine how to match expenses to transactions. The options are: <ul><li>**Never required** - use this option if the customer's bank cannot send transactions to Continia Expense Management. In such cases, manual import of transactions is necessary before approval and posting of expenses.</li><li>**Required from date** - choose this option if you expect to receive transactions starting from a specific date. Matching expenses and transactions will not be required until that date.</li><li>**Always required** - with this option, expenses using this payment type must be matched with a transaction before they can be approved and posted. This ensures all transactions are appropriately matched with expenses. |

## Assign a payment type to an expense user

To assign a payment type to an expense user:

1. Search for {{search}} **Continia User Setup**.
1. Select an expense user.
1. On the action bar, select **Payment Types**.
1. From here, you can assign payment types in two ways:  
   * On the action bar, click **Add Payment Types** and select a payment type to assign it to this expense user. You can add multiple payment types.
   * On the action bar, click **Edit Payment Type Assignment**.  In the **Payment Type** column, select a payment type in the first empty field to assign it to this expense user. You can add multiple payment types.
>[!TIP]
>When you create new expense users, you can also assign payment types to them from the **Continia User Setup Card** using the **Payment Types** action on the action bar.

## Assign a payment type to an expense user group

To assign a payment type to an expense user group:

1. Search for {{search}} **Expense User Groups**.
1. Select an expense user group.
1. On the action bar, click **Payment Types**.
1. Under **Payment Type**, select a payment type. Repeat this step in the next empty field for each payment type you want to add to a particular expense user group.

## Assign expense users or expense user groups to a payment type

To assign expense users or expense user groups to a payment type:

1. Search for {{search}} **Payment Types**.
1. Select a payment type.
1. On the action bar, click **Payment Type** > **Effective Users**.
1. On the **Continia Users** page, you can add as many expense users and expense user groups to a payment type as you want.

## Configure Posting

To set the posting method and posting account:

1. Search for {{search}} **Payment Types**.
1. Under **Posting** in the **Method** dropdown menu, choose **Post on a Business Account**.
3. Under **Posting Account**, choose from the **Type** dropdown menu. The options are as follows:
   * **G/L Account** - You can only reconcile with **Bank Account Reconciliation - Expense Management**.
   * **Vendor** - You can only reconcile with **Bank Account Reconciliation - Expense Management** and need to post invoices. Choosing this option means you cannot use Expense Reports.
   * **Bank Account** - You can reconcile using both the standard bank account reconciliation and **Bank account reconciliation - Expense Management**.


## Related information

[Expense User Group setup for Expense Management](@EM-35)  
[Expense User setup for Expense Management](@EM-36)



