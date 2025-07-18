---
title: Continia Expense Management Demo Script
date: 30-05-2022
id: EM-88
lang: en
---

# Continia Expense Management Demo Script

This demo script provides a step-by-step description of how to make a complete demonstration of the standard features in Continia Expense Management.

The purpose of the Continia demo systems is to give Continia partners an environment to educate end customers, and to present and test the latest versions of Expense Management. Previous knowledge of Expense Management is required.

This demo environment is already set up and ready to use, and it's always updated to the latest version of Expense Management.

The script covers the following processes:

\


| Processes                                                                                                                                                                              | Description                                                                                |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------ |
| [To submit expenses using the Expense App](<Demo Script EN.md#to-submit-expenses-using-the-expense-app>)                                                                               | How to register expenses with images of receipts.                                          |
| [To submit expenses with allocations using the Expense App](<Demo Script EN.md#to-submit-expenses-with-allocations-using-the-expense-app>)                                             | How to split expenses into several lines.                                                  |
| [To start working with expenses and credit card transactions in Business Central](<Demo Script EN.md#to-start-working-with-expenses-and-credit-card-transactions-in-business-central>) | How to process expenses and credit card transactions.                                      |
| [To submit receipts for credit card transactions using the Expense App](<Demo Script EN.md#to-submit-receipts-for-credit-card-transactions-using-the-expense-app>)                     | How to process credit card expenses.                                                       |
| [To approve expenses using the Continia Web Approval Portal](<Demo Script EN.md#to-approve-expenses-using-the-continia-web-approval-portal>)                                           | How to approve from outside of Business Central.                                           |
| [To preview posting of expenses before final posting](<Demo Script EN.md#to-preview-posting-of-expenses-before-final-posting>)                                                         | How to verify that posting is correct before final posting.                                |
| [To submit per diems using the Expense App](<Demo Script EN.md#to-submit-per-diems-using-the-expense-app>)                                                                             | How to register per diems.                                                                 |
| [To approve and post per diems](<Demo Script EN.md#to-approving-and-post-per-diems>)                                                                                                   | How to approve and post per diems using both the Web Approval Portal and Business Central. |
| [To submit mileages using the Expense App](<Demo Script EN.md#to-submit-mileages-using-the-expense-app>)                                                                               | How to register mileages.                                                                  |
| [To approve and post mileages](<Demo Script EN.md#to-approve-and-post-mileages>)                                                                                                       | How to approve and post mileages using both the Web Approval Portal and Business Central.  |
| [The Expense Portal](<Demo Script EN.md#the-expense-portal>)                                                                                                                           | How to register expenses, mileages, and per diems using the Expense Portal.                |
| [The Expense Management Status Report](<Demo Script EN.md#the-expense-management-status-report>)                                                                                       | How to run the Expense Management Status Report and review it.                             |

## Users in the demo environment

The names of the users in your demo environment will differ depending on the localization of the environment. You can find the user names in the email you receive when you start up a demo environment as well as on the demo portal page. In Expense Management, the following user roles are available:

\


| User role    | Description                                                                                                                                                                                                                                                                                                 |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Controller   | This user is the person that typically performs day-to-day accounting related to expenses, mileages, etc. in Microsoft Dynamics 365 Business Central.                                                                                                                                                       |
| Expense user | This user is the person travelling and/or submitting expenses, mileages, etc.                                                                                                                                                                                                                               |
| Approver     | This user is the person that approves expenses, mileages, etc. for the expense user. It might be the expense user's manager. The demo environment is set up with approval sharing, meaning that all expenses are sent to a group called Marketing, which has multiple approvers that can approve documents. |

The user names in the welcome email and the Continia Demo Portal will be the actual names of the users in your environment.

> \[!NOTE] For ease of reference and understanding, this demo script will refer to the actual names of the controller and the approver as they appear in the UK localization of Business Central:
>
> * Controller: Ester Henderson (EH)
> * Approver: Robin Bettencourt (RB)

## To submit expenses using the Expense App

1. Follow the link to the Expense App in the welcome email or from the demo environment page. In this environment, you will be automatically signed in as the expense user.
2. Select **New Expense**, and fill in all required details.
3. Add a picture of a receipt from the saved images. Choose the image called **Food Market**.
4. Submit the expense.

## To submit expenses with allocations using the Expense App

Allocation can be used if you need to split an expense into different expense types or other available fields, such as department, project, etc. A good example of a receipt that you might want to split is a hotel bill, where you want accommodation to go on one line and food and beverage on another line.

1. Follow the link to the Expense App in the welcome email or from the demo environment page.
2. Select **New Expense**, and then select **Add Saved Image** to add the image "Westin Hotel".
3. Fill out the required fields.
4. Select **Add allocation lines**.
5. Add a line by selecting the plus (+) button.
6. Fill in description, expense type, and amount for this line, and save. Now you see two lines.
7. Submit the expense.

## To start working with expenses and credit card transactions in Business Central

1. Sign in to Business Central as the controller.
2. In the Role Center, in the **Continia Expense Management Activities** FastTab, select **Synchronize**. This will download the expense you just submitted to the Expense App.

> \[!NOTE] Synchronizations can be scheduled in a job queue. Read more about setting up job queues [here](https://docs.continia.com/en-us/continia-expense-management/setting-up-expense-management/setting-up-general-business-functionality/setting-up-job-queues).

3. When you synchronize, you will get this warning: “_There are one or more entries in the Bank Transactions Inbox_”. These transactions are created for you so you can go through the process of handling imported credit card transactions in Expense Management.
4. Select **Unhandled Bank Transaction Inbox**. The card number is part of a bank transaction and has not yet been assigned to an expense user.
5. Select **Process**, and then select **Assign card to User**. Select the name of the expense user, and the select **Mastercard** as payment type. When you assign a card number to user, Expense Management will match any corporate credit card expenses that have already been submitted to these transactions. In this demo environment, no expenses will be matched because it doesn’t contain any submitted credit card expenses. Expense Management will automatically assign future transactions to the correct user.
6. In the Role Center, in the **Continia Expense Management Activities** FastTab, under **Expenses**, select **Pending**.
7. You will see six expenses: the two expenses you created in the app and four expenses which Expense Management creates from credit card transactions. The two expenses you created in the Expense App have the status **Pending Approval** while the four expenses from the credit card transactions have the status **Pending Expense User**.

## To submit receipts for credit card transactions using the Expense App

1. Follow the link the to the Expense App in the welcome email or from the demo environment page.
2. Select refresh, and notice that the **Open** action indicates that you have new documents.
3. Select **Open** to see the documents.
4. Select one of the four documents, attach a receipt, and submit.
5. Go back to Business Central, and select **Synchronize**. You will now see three expenses with the status **Pending Approval**.

## To approve expenses using the Continia Web Approval Portal

1. Follow the link to the Web Approval Portal in the welcome email or from the demo environment page. You will be automatically signed in as an approver. You will see the three expenses that haven’t been approved yet. One of these expenses is the one with allocation.
2. Choose the expense with allocation, and show that all detailed information for each line is visible to the approver.
3. Approve the expenses.
4. Go back to Business Central, and synchronize. In the Role Center, you will now see the status of the six expenses:
   * Three expenses have the status **Pending** – waiting for the expense user to submit.
   * The three last expenses have the status **Released**.

## To preview posting of expenses before final posting

1. In the Role Center, in the **Continia Expense Management Activities** FastTab, under **Expenses**, select **Ready to Post**.
2. Select **Actions** > **Posting** > **Preview Posting**.
3. Select **Show Related Entries** to see the entries that have been created.
4. Go back to the **Expenses** page.
5. Then select **Post** for each of them or **Post Batch** to post all released expenses.
6. Go to **Chart of Accounts** to see the expenses.
7. Select account **8252** – Food & Beverages.
8. Select **Account** > **Ledger Entries**.
9. Select **Entry** > **Find Entries**.
10. Select **Expense**.
11. The expense type **Food** is posted to account **8252**.
12. To show the setup behind the posting of the expense type **Food**, choose the \{{search\}} icon, enter **Expense Types**, and then choose the related link. Select the expense type **Food** and then **Setup**.

## To submit per diems using the Expense App

1. Follow the link to the Expense App in the welcome email or from the demo environment page.
2. Select **New Per Diem**.
3. Enter a **Departure Date Time**, **Return Date Time** and **Description**.
4. The amount is pending calculation. You set up calculation methods and rates in Business Central. After the first synchronization with Business Central, the amount will be displayed in the Expense App.
5. Select **Days (5)**, and the five days will be displayed.
6. When selecting a specific day, the expense user can select what is included for this specific day. Expense users can enable or disable details for all days.
7. Save the per diem.
8. Go to Business Central, and synchronize.
9. In the Expense App, select the three lines in the upper right corner, and then select **Synchronize**.
10. The per diem amount is now visible in the **Open**, the **Per Diem** and **Per Diem Days** views. Here users get an overview of the amount for each specific per diem day.
11. Open the per diem, and then submit it.

## To approve and post per diems

1. Sign in to Business Central as the controller.
2. Select **Synchronize**, and the per diems will be updated and will be awaiting approval.
3. Follow the link to the Web Approval Portal in the welcome email or from the demo environment page.
4. Select **Per Diems** from the **Expense Management** menu.
5. Select the first per diem, and approve it.
6. Go back to Business Central. Now the per diem is ready to post.
7. In the Role Center, in the **Continia Expense Management Activities** FastTab, under **Per Diem**, select **Ready to Post**.
8. Select **Process** > **Post** to post the per diem.
9. If you would like to show the posting result, choose the \{{search\}} icon, enter **Posted Per Diems**, and then choose the related link. Select **Process** > **Find Entries**.
10. If you would like to show the per diem posting group, choose the \{{search\}} icon, enter **Per Diem Groups**, and then choose the related link.
11. This demo environment has only one default group, but you can of course create more groups if needed.
    * Under **Code**, select **Default**. In the demo environment, **Accommodation** and **Meal Allowance** have been set up. If your country version requires the entertainment allowance, drinks allowance or transportation allowance to be enabled, you can do this on the **Expense Management Setup** page.
    * Navigate to allowance rates by selecting the **1**. Here you can see and modify the rates that are defined for the **Default** group.

## To submit mileages using the Expense App

1. Follow the link to the Expense App in the welcome email or from the demo environment page.
2. Select **New Mileage**.
3. Fill in the **From address** and **To address** fields.
4. Select one of the routes suggested by Google Maps.
5. Submit the mileage.
6. You now get three options:
   * **Send and create return** – If you would like to create a return trip. A new mileage will be created automatically with the reverse destination.
   * **Send and continue from** – If you are going to a new destination.
   * **Send** – Submit this mileage.

## To approve and post mileages

1. Sign in to Business Central as the controller.
2. In the Role Center, in the **Continia Expense Management Activities** FastTab, under **Actions**, select **Synchronize**.
3. In the Role Center, in the **Continia Expense Management Activities** FastTab, under **Mileage**, select **Pending**. You now see one mileage, or two if you selected to create a return trip. The mileage you created in the app has the status **Pending Approval**.
4. Follow the link to the Web Approval Portal in the welcome email or from the demo environment page.
5. Select **Mileage** from the **Expense Management** menu.
6. Approve all mileages.
7. Go back to Business Central, and in the Role Center, in the **Continia Expense Management Activities** FastTab, under **Mileage**, select **Ready to Post**.
8. Select **Process** > **Post** to post the mileage.
9. If you would like to show the posting result, choose the \{{search\}} icon, enter **Posted Mileage**, and then choose the related link. Select **Process** > **Find Entries**.
   * As with expenses and other documents in Expense Management, the user can select **Show Related Entries** to see all entries for a mileage.
   * Select the **G/L Entry** row and then **Show Related Entries**.
   * As with expenses, you can navigate from **Chart of Accounts** to a mileage.
   * Go to the **Vehicle List.**
   * Here customers can set up all the needed vehicle types, and by selecting **Setup**, they can define where mileages should be posted. In this setup, account 8270 is used.

## The Expense Portal

Expense users can use the Expense Portal to create expenses, mileages, and per diems.

1. Follow the link to the Expense Portal in the welcome email and/or on the demo environment page. In this environment, you will be automatically signed in as the expense user Linda Townsend.
2. You will see the three expenses to which Lina Townsend still needs to attach receipts.
3. Select the **Food Market** expense, and attach a receipt.
4. Select **Submit** to upload the expense.
5. Go back to Business Central, and synchronize. You will now see that the status has changed to **Pending Approval**.
6. Go back to the Expense Portal, and select **Mileage**.
7. Select **New Mileage** to create a new mileage, and then select **Send**. If you want to create a return trip, select **Send and create return**.
8. Go back to the **Mileage** page in Business Central, and synchronize. Now the mileage is ready for approval.
9. Go back to the Expense Portal, and select **Per Diem**.
10. Select **New Per Diem,** and create a new per diem by entering a period and description.
11. Select **Update Per Diem Days**.
12. Select a day, and remove one item, lunch for example.
13. Select **Save** to save the per diem.
14. Go back to Business Central as Ester Henderson, and synchronize.
15. Go back to the Expense Portal, and refresh your browser.

## The Expense Management Status Report

The status of documents in Expense Management can also be viewed in the **Expense Management Status Report**.

1. Choose the \{{search\}} icon, enter **Expense Management Status Report**, and then choose the related link.
2. Run the report, and review the pages.
