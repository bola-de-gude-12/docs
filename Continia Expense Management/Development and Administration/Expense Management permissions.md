---
title: Expense Management Permissions
date: 15-05-2025
description:  
id: EM-62
lang: en
---

# Expense Management permissions
{{include "permissions" "Expense Management"}}

## Standard Continia permission sets

| Permission set | Description |
| --- | --- |
| CSC BASIC | This permission set grants access to all Continia Core features and enables you to obtain the Expense Management activation status. All users of Expense Management must be assigned the CSC BASIC permission set to ensure that all standard features work as intended. |
| CSC APP SETUP | This permission set allows you to activate Continia products, including Continia Core. It's mainly used for product installation and – in Business Central online – when making changes to subscription agreements, such as selecting and deselecting subscribed modules. The permission set is mostly required in online deployments of Business Central, as users who set up on-premises environments typically use the CEM-SUPER permission set instead. |

## Expense Management-specific permission sets

| Permission set | Description |
| --- | --- |
| CEM-ALL | With this permission set, you're able to perform all basic Expense Management operations in Business Central. All users of Expense Management must be assigned the CSC BASIC set to ensure that all standard features work as intended. The CEM-ALL permission set may also be necessary for Business Central users that don't use Expense Management, as they may still need certain permissions to access and run objects that somehow interfere with the standard Business Central code. |
| CEM-APPROVE | Using this permission set, you can perform all basic approval operations when approving documents in either Business Central or the Continia Web Approval Portal: *approve*, *reject*, *put on hold*, *forward*, and *add comment*. The permission set isn't sufficient on its own but should be used together with either [CDC-APPROVE](/continia-document-capture/development-and-administration/document-capture-permissions#document-capture-specific-permission-sets), as Expense Management uses the overall Document Capture framework for approval. |
| CEM-SUPER | When you're assigned this permission set, you get full access to all Expense Management tables. This typically applies to users who set up Expense Management. |
| CEM-NAVUSER | Expense users using Business Central to register expenses. |

> [!NOTE]
> In order to be able to configure approval sharing and export users to the Web Approval Portal, you must have access to all companies.

## Permission sets for accounts payable clerks and similar
If your role is to process invoices and other business documents (for example as an admin or an accounts payable clerk), you must as a minimum be assigned the following permission sets for the companies that are relevant to you:

* CSC BASIC
* CEM-SUPER
* D365 BASIC<a href="#footnote-1.1"><sup>1
* An account payable permission set of your choice from standard Business Central

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.1">The name of the permission set depends on your version of NAV/Business Central.</li>
  </ol>
</div>
</small>

## Permission sets for approvers
If you're an approver (whether in Microsoft Dynamics NAV/Business Central or in the Web Approval Portal), you must as a minimum be assigned the following permission sets for the companies that are relevant to you:

* CSC BASIC
* CDC-ALL
* CEM-APPROVE
* CDC-APPROVE
* D365 BASIC<a href="#footnote-1.2"><sup>1

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.2">The name of the permission set depends on your version of NAV/Business Central.</li>
  </ol>
</div>
</small>

## Permission sets for reviewers

If you're a purchase contract reviewer (whether in Microsoft Dynamics NAV/Business Central or in the Web Approval Portal), you must as a minimum be assigned the following permission sets for the companies that are relevant to you:
* CSC BASIC
* CDC-ALL
* CDC-APPROVE
* D365 BASIC<a href="#footnote-1.3"><sup>1

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.3">The name of the permission set depends on your version of NAV/Business Central.</li>
  </ol>
</div>
</small>

## Updating permissions when implementing service packs

When you upgrade Expense Management or implement a service pack in Business Central online or apps, permissions are always updated automatically.

However, when you implement a service pack in FOB-based versions of NAV/Business Central, you must manually run the following codeunit whenever permissions have been changed:

* 6086320 (**CEM Create EM Roles**) – to update the Expense Management-specific permission sets

Running this codeunit will only add or modify permissions – no permissions are deleted.

<style>
  .content table tr td:nth-child(1) {
    width: 90px;
  }
  .content table tr td:nth-child(2) {
    width: 640px;
  }  
</style>