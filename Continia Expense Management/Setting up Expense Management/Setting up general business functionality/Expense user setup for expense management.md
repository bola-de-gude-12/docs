---
title: Expense user setup for Expense Management
date: 11-09-2025
description: Learn how to add users to Expense Management. 
id: EM-36
lang: en
---
# Expense user setup for Expense Management

To add expense users and to initiate expense workflows in Expense Management, you must configure them on the **Continia User Setup** page. This page allows you to specify key settings for each expense user, such as their expense user group and document visibility.

> [!NOTE]
> The **Continia User Setup** is also relevant for Continia Document Capture. For more information, see [Continia User Setup for Approvals](@DC-23).

To create an expense user for Expense Management:

1. Search for {{search}} **Continia User Setup**.
2. On the **Continia User Setup Card**, on the action bar, click **New**.

3. Under **General**, fill in the following fields:

   | Field                     | Description                                                  |
   | ------------------------- | ------------------------------------------------------------ |
   | Continia User ID          | Select the user. All approvers must be Business Central users. You can access a list of them using the lookup button in this field. |
   | Name                      | Expense users who are not approvers do not need to log in to Business Central. If the user is not already a Business Central user, the system will prompt you to confirm adding them. |
   | Email                     | Enter the email address for the expense user if it's not filled out automatically. |
   | Allow Force  Registration | Determines whether the  user can override errors and warnings to force the registration of a document. |
   | Approval Administrator    | Indicates whether the user is an approval administrator responsible for managing approval processes. |

4. Under **Web Approval**, enter information for the Approval Client field. Specifies the client which the user will be using for approving documents. Used when sending out approval status e-mail with documents to approve which includes a hyperlink to access the documents for approval in the selected client. Only users with the approval client set to Continia web approval will be able to access the web approval portal.

5. Under **Expense Management**, fill in the following fields:

   | Field                         | Description                                                  |
   | ----------------------------- | ------------------------------------------------------------ |
   | Expense User                  | When this is enabled, users can create expenses and related documents as defined in the Expense Management setup. |
   | Expense Management Login Type | Defines how the user signs in. The options are **Continia Online** or **Microsoft 365**. If **Microsoft 365** is selected, users will be required to log in using their Microsoft 365 credentials, and new users will receive a welcome email with instructions on how to sign in. |
   | Can Edit Approved Documents   | Determines if the user can edit documents that are pending approval or have already been released. |
   | Limit Document Visibility     | When enabled, restricts the user to viewing only their own documents. |
   | Vendor No.                    | Here you set up a vendor for expense users. You can choose the vendor you have created for the employee by using the lookup button. The vendor number is used for posting, and when the user is reimbursed, the balance can be seen on this vendor. |
   | Employee No.                  | The employee number is used for posting. If both **Employee No.** and **Vendor No.** have been filled in, **Employee No.** will be used. |
   | Expense User Group            | Defines the group that the expense user belongs to.          |
   | Expense Reminder Code         | Specifies the code used for sending reminders to expense users. |
   | Approver Name                 | Assigns a designated person to be the approver for the expense user's expenses. |
   | Approval Limit Unlimited      | Indicates that the approver has no set limit to the expense amount that they're approving. |
   | Amount                        | Defines the maximum amount for an expense that an approver can approve for the expense user. |

6. After you've finished entering the user's details, go back to the **Continia User Setup** page, and on the action bar, click **Export Users**. This generates and sends welcome emails to newly created expense users. These emails contain a link to activating their role and creating a password as well as links to downloading the Expense Mobile App and the Expense Portal.

