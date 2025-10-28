---
title: Expense Management permissions
date: 15-09-2025
description: List of the Continia Expense Management permission sets
id: EM-62
lang: en
---

# Expense Management permissions
{{include "permissions" "Expense Management"}}

## Standard Continia permission sets

| Permission set | Description |
| --- | --- |
| CSC BASIC | To ensure that all standard features work as intended, the CSC BASIC permission set is mandatory for all Business Central users, including those who don't use Expense Management directly, as they still need certain permissions to access and run objects that somehow interfere with the standard Business Central code. This permission set is added automatically, grants access to all Continia Core features, and enables you to obtain the Expense Management activation status. Overall, it's similar to the standard Dynamics NAV/Business Central BASIC permission set. |
| CSC APP SETUP | This permission set allows you to activate Continia products, including Continia Core. It's mainly used for product installation and – in Business Central online – when making changes to subscription agreements, such as selecting and deselecting subscribed modules. The permission set is mostly required in online deployments of Business Central, as users who set up on-premises environments typically use the CEM ADMIN permission set instead. |

## Expense Management-specific permission sets

| Permission set | Description |
| --- | --- |
| CEM BASIC | With this permission set, you can perform all basic Expense Management operations in Business Central. All users of Expense Management prior to, and including version 26, must be assigned the CSC BASIC set to ensure that all standard features work as intended. <br>The CEM BASIC permission set is necessary for users who don't use Expense Management on a system that has Expense Management installed and is active. Such users will then avoid receiving Expense Management permission errors when interacting with standard Business Central functionality. Expense Management traces standard Business Central tables for updating Field Type lookup values. This permission set offers access to update those lookup values, and also read-access to the Expense Management Setup table. |
| CEM APPROVE | Using this permission set, you can perform all basic approval operations when approving documents in either Business Central or the Continia Web Approval Portal: *approve*, *reject*, *put on hold*, *forward*, and *add comment*. The permission set isn't sufficient on its own but should be used together with either [CDC-APPROVE](/continia-document-capture/development-and-administration/document-capture-permissions#document-capture-specific-permission-sets), as Expense Management uses the overall Document Capture framework for approval. |
| CEM ADMIN | When you're assigned this permission set, you get full access to all Expense Management tables. This typically applies to users who set up Expense Management. |
| CEM DOC. EDIT | Expense users using Business Central to register expenses. |

> [!NOTE]
> To configure approval sharing and export users to the Web Approval Portal, you must have access to all companies.


## Permission sets for accounts payable clerks and similar
If your role is to process invoices and other business documents (for example as an admin or an accounts payable clerk), you must as a minimum be assigned the following permission sets for the companies that are relevant to you:

* CSC BASIC (this role is automatically included in CEM ADMIN)
* CEM ADMIN
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

* CSC BASIC (this role is automatically included in CEM APPROVE)
* CDC BASIC (this role is automatically included in CEM APPROVE)
* CEM APPROVE
* CDC APPROVE (this role is automatically included in CEM APPROVE)
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
* CDC BASIC
* CDC APPROVE
* D365 BASIC<a href="#footnote-1.3"><sup>1

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.3">The name of the permission set depends on your version of NAV/Business Central.</li>
  </ol>
</div>
</small>

## Legacy permission sets (for older versions)

The following permission sets only apply to earlier versions of Expense Management (prior to 27.0) and are retained here for reference.

| Permission set | Description |
| --- | --- |
| CSC-BASIC | Access to all Continia Core features and the Expense Management activation status. Ensures all standard features work as intended, it is mandatory for all Business Central users. |
| CSC-APP SETUP | Used for activating Continia products, product installation, and managing subscriptions. |
| CEM-ALL | Perform all basic Expense Management operations in Business Central. All users of Expense Management prior to, and including version 26, must be assigned the CSC BASIC set to ensure that all standard features work as intended. |
| CEM-APPROVE. | Perform all basic approval operations when approving documents in either Business Central or the Continia Web Approval Portal. This set should be used together with either [CDC-APPROVE](https://docs.continia.com/en-us/continia-document-capture/development-and-administration/document-capture-permissions/#document-capture-specific-permission-sets), as Expense Management uses the overall Document Capture framework for approval. |
| CEM-SUPER | Gives you full access to all Expense Management tables. This typically applies to users who set up Expense Management. |
| CEM-NAVUSER | Expense users using Business Central to register expenses. |
| D365-BASIC | The name of the permission set depends on your version of NAV/Business Central. |



<style>
  .content table tr td:nth-child(1) {
    width: 90px;
  }
  .content table tr td:nth-child(2) {
    width: 640px;
  }  
</style>