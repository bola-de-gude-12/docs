---
title: Expense Management Permissions
date: 24-01-2022
description:  
id: EM-165
lang: en
---

# Expense Management Permissions
To use Continia Expense Management, you must have assigned permission sets, also known as "roles." These sets grant access and abilities for your tasks with specific permissions for different features and tasks.

If required, you can even [create custom permission sets](/continia-expense-management/development-and-administration/expense-management-permissions#creating-custom-permission-sets) to suit your specific needs. Alternatively, you can gain certain permissions by joining a user group that already has the necessary permissions applied. For more information, see the [Assigning permissions to users and user groups](/continia-expense-management/development-and-administration/expense-management-permissions#assigning-permissions-to-users-and-user-groups) article.

> [!NOTE]
> In addition to the Continia permission sets mentioned in this article, you must also be assigned the standard Microsoft Dynamics 365 Business Central permission sets in order for all permitted operations to work as intended.

## Overview of predefined permissions
There are two types of predefined permission sets relevant to users of Expense Management: the standard Continia permission set and the Expense Management-specific permission set. The Expense Management permission set supplements the standard Continia permission sets and works in conjunction with them.

The standard Continia permissions are:

> [!IMPORTANT]
>
> The CSC BASIC and CSC APP SETUP sets described below are complementary. Therefore, you should only be assigned one of them.

| Permission set | Description |
| --- | --- |
| CSC BASIC | This permission set grants access to all Continia Core features and enables you to obtain the Expense Management activation status. All users of Expense Management must be assigned the CSC BASIC and CEM-ALL permission sets to ensure that all standard features work as intended. |
| CSC APP SETUP | This permission set allows you to activate Continia products, including Continia Core. It's mainly used for product installation and – in Business Central online – when making changes to subscription agreements, such as selecting and deselecting subscribed modules. The permission set is mainly required in online deployments of Business Central, as users who set up on-premises environments typically use the CEM-SUPER permission set instead. |

The Expense Management-specific permissions are:

| Permission set | Description |
| --- | --- |
| CEM-ALL | With this permission set, you can perform all basic Expense Management operations in Business Central. All users of Expense Management must be assigned the CSC BASIC and CEM-ALL permission sets to ensure that all standard features work as intended. The CEM-ALL permission set may also be necessary for Business Central users that don't use Expense Management, as they may still need specific permissions to access and run objects that somehow interfere with the standard Business Central code. |
| CEM-APPROVE | Using this permission set, you can perform all basic approval operations when approving documents in either Business Central or the Continia Web Approval Portal: *approve*, *reject*, *put on hold*, *forward*, and *add comment*. The permission set isn't sufficient on its own but should be used together with either [CDC-APPROVE or CDC-WEB](/continia-document-capture/development-and-administration/document-capture-permissions#document-capture-specific-permission-sets), as Expense Management uses the overall Document Capture framework for approval. |
| CEM-SUPER | When you're assigned this permission set, you get full access to all Expense Management tables. This typically applies to users who set up Expense Management. |
| CEM-NAVUSER | Expense User using NAV to register expenses. |

## To assign permissions to users and user groups
Assigning Expense Management permissions to users and user groups is a standard Business Central process. For more information, see Microsoft's article [Assign Permissions to Users and User Groups](https://docs.microsoft.com/en-us/dynamics365/business-central/ui-define-granular-permissions).

## To assign permissions to approvers

If you're an approver, you must, as a minimum, be assigned the following permission sets for the companies that are relevant to you:

| Permission set | Description                                           |
| -------------- | ----------------------------------------------------- |
| CEM-APPROVE    | Requires CDC-APPROVE.<br />Used by the approver role. |
| CDC-APPROVE    |                                                       |

## To assign permissions to bookkeepers

If you're a bookkeeper, you must, as a minimum, be assigned the following permission sets for the companies that are relevant to you:

| Permission set | Description                                         |
| -------------- | --------------------------------------------------- |
| CEM-SUPER      | Used by the bookkeeper role and EM super user role. |

## To assign permissions to administrators

If you're an administrator, you must, as a minimum, be assigned the following permission sets for the companies that are relevant to you:

| Permission set | Description                                         |
| -------------- | --------------------------------------------------- |
| CEM-SUPER      | Used by the bookkeeper role and EM super user role. |

## See also

[Assign Permissions to Users and User Groups](https://docs.microsoft.com/en-us/dynamics365/business-central/ui-define-granular-permissions) (Microsoft article)  




<style>
  .content table tr td:nth-child(1) {
    width: 90px;
  }
  .content table tr td:nth-child(2) {
    width: 640px;
  }  
</style>