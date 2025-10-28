---
title: Approver Setup for Expense Management
date: 19-06-2025
description: 
id: EM-33
lang: en
---
# Approver setup for Expense Management

The first step is to set up designated approvers to enable workflows that involve document approval. This setup is done on the Continia User Setup page, where various settings for the approver are defined, including the approval limit and permissions related to editing approved documents. By configuring these parameters, you can effectively streamline your approval processes and make sure that documents are appropriately reviewed and authorized.

To add approval permissions to a user:

1. Search for {{search}} **Continia User Setup**.
2. On the action bar, click **New**.
3. Use the following fields to assign approval permissions to a user:
   | FastTab | Field | Description |
   | ---| --- | --- |
   | General | **Continia User ID** | Select the user. All approvers must be Business Central users. You can access a list of them using the lookup button in this field. |
   | General | **Name** | A user's name is automatically filled in when their email address is entered, which is utilized for welcome emails and notifications. |
   | General | **No. of Approval Forwarding** | Specifies the number of users to whom approval can be forwarded to. |
   | General | **Allow Force Registration** | Specifies if the user is allowed to force registration of a document, ignoring errors and warnings that would cause the registration to fail. |
   | General | **Approval Administrator** | Enable this option to grant the user the ability to force approve documents. Once activated, the user can reopen, edit, and force approve a document to bypass the standard approval flow. Note that enabling this option will also automatically enable the corresponding setting in the **Approval User Setup**, and that the user will be granted a number of standard approval administrator permissions in addition to the Continia-specific permissions. The specific permissions are described in [Expense Management Permissions](@EM-62). |
   | Web Approval | **Approval Client** | Choose the client for approving expense documents. If the Continia Web Approval Portal is selected, the user can approve documents using Business Central or the Continia Web Approval Portal.<br />The options are:<ul><li>**Blank** - no approval client </li><li>**Web client** - the approval request is processed within Business Central</li><li>**Continia Web Approval Portal** - through this portal, you have access to all documents pending approval from Continia Document Capture and Continia Expense Management.   </li></ul> |
   | Expense Management | **Can Edit Approved Documents** | Activate this option if you want the user to be able to edit documents that have already been approved. Users with this option enabled cannot modify any information related to the expense amount. To edit the amount on an approved expense document, users must undergo the regular approval process again. |
   | Expense Management | **Unlimited Amount** | Documents from a user with unlimited approval status automatically receive the approved status. Enabling this option is mandatory for at least one approver. |
   | Expense Management | **Approval Limit** | This field is for approvers who have a defined approval limit. Meaning that they can only approve expense documents up to a certain amount. If a document's expense amount exceeds this limit, it's either declined or forwarded to an approver who has a higher approval limit or unlimited approval authority. |
   
4. The last step in configuring approvers is to export them. To do this, on the action bar, click **Export Users**. This action automatically generates and sends welcome emails to the newly designated approvers. These emails include essential links, allowing them to activate their approver role, create a password, and conveniently access the Expense Mobile App and Expense Portal.

   > [!NOTE]
   > You can also sign in with your Microsoft 365 credentials. If you do so, creating a password isn't necessary. 

## Related information
[Setting up the Continia users default setup](Setting up the Continia Users Default Setup.md)

