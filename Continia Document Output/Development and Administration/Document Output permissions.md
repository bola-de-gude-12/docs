---
title: Document Output Permissions
date: 13-05-2025
description:  
lang: en
---

# Document Output Permissions

To use Continia Document Output, assign one or more permission sets (also called roles) to each user. These permission sets grant access to features and enable users to complete specific tasks. Continia provides several predefined permission sets, each designed for a specific purpose. You can also create custom permission sets if needed, or add users to a security group that already includes the required permission sets. For more information, see [Assign permissions to users and groups](https://learn.microsoft.com/en-us/dynamics365/business-central/ui-define-granular-permissions) (Microsoft Learn article).

> [!NOTE]
> Make sure to assign the necessary Microsoft Dynamics 365 Business Central permission sets, along with the Continia ones, to make sure that all features function correctly.

## Standard Continia permission sets

| Permission set | Description |
| --- | --- |
| CSC BASIC | This permission set grants you access to all Continia Core features and enables you to obtain the Document Output activation status. All users of Document Output must be assigned the CSC BASIC and CDO-ALL permission sets to ensure that all standard features work as intended. |
| CSC APP SETUP | This permission set allows you to activate Continia products, including Continia Core. It's mainly used for product installation and – in Business Central online – when making changes to subscription agreements, such as selecting and deselecting subscribed modules. The permission set is mostly required in online deployments of Business Central, as users who set up on-premises environments typically use the CDO-SUPER permission set instead. |

## Document Output-specific permission sets

| Permission set | Description |
| --- | --- |
| CDO-ALL | With this permission set, you're able to perform all basic Document Output operations in Business Central (including editing email recipients), except viewing the log, editing templates, and modifying the setup. All users of Document Output must be assigned the CSC BASIC and CDO-ALL permission sets to ensure that all standard features work as intended. The CDO-ALL permission set may also be necessary for Business Central users that don't use Document Output, as they may still need certain permissions to access and run objects that somehow interfere with the standard Business Central code. |
| CDO-LOG | This permission set allows you to view the log in Document Output. |
| CDO-SUPER | When you're assigned this permission set, you get full access to all Document Output functionality. This is the only permission set that allows you to edit log settings. |

> [!NOTE]
> If you can’t locate any of the above roles, run codeunit 6192860 **CSC Create Core Roles** and codeunit 6175291 **CDO Create Roles**. These codeunits will then create all relevant roles for Continia Core and Document Output respectively.






<style>
  .content table tr td:nth-child(1) {
    width: 90px;
  }
  .content table tr td:nth-child(2) {
    width: 640px;
  }  
</style>