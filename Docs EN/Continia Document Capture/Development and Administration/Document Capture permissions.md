---
title: Document Capture permissions
date: 15-09-2025
description: How permissions work in Document Capture.
id: DC-140
lang: en
---

# Document Capture permissions

{{include "permissions" "Document Capture"}}

## Standard Continia permission sets

| Permission set | Description |
| --- | --- |
| CSC BASIC | To ensure that all standard features work as intended, the CSC BASIC permission set is mandatory for all Business Central users, including those who don't use Document Capture directly, as they still need certain permissions to access and run objects that somehow interfere with the standard Business Central code. The permission set also enables you to obtain the Document Capture activation status. Overall, it's similar to the standard Dynamics NAV/Business Central BASIC permission set. |
| CSC APP SETUP | This permission set allows you to activate Continia products, including Continia Core. It's mainly used for product installation and – in Business Central online – when making changes to subscription agreements, such as selecting and deselecting subscribed modules. The permission set is mostly required in online deployments of Business Central, as users who set up on-premises environments typically use the CDC ADMIN permission set instead. |

## Document Capture-specific permission sets

| Permission set | Description |
| --- | --- |
| CDC BASIC | To ensure that all standard features work as intended, the CDC BASIC permission set is mandatory for all Business Central users, including those who don't use Document Capture directly, as they still need certain permissions to access and run objects that somehow interfere with the standard Business Central code. The permission set is similar to the standard Dynamics NAV/Business Central BASIC permission set. |
| CDC CAPTURE | This permission set allows you to import files, capture document values, and register documents in Business Central using Document Capture. Note that you must also be assigned certain standard Business Central permission sets in order to use Document Capture to capture and process documents, depending on what version of Business Central you're using. |
| CDC APPROVE | Using this permission set, you can perform all basic approval operations when approving documents in either Business Central or the Continia Web Approval Portal: approve, reject, put on hold, forward, and add comment. The permission set is applicable as of Business Central v14. |
| CDC ADMIN | When you're assigned this permission set, you get full access to all Document Capture tables. This typically applies to users who set up Document Capture in Business Central. |
| CDC WEB | This permission set enables you to approve documents in the Web Approval Portal. The permission set only applies up to and including Business Central v13. In Business Central v14 and later, this permission set is included in CDC APPROVE. |
| CDC EDIT | With this permission set, you can edit purchase invoice lines when approving documents. The permission set only applies up to and including Business Central v13. In Business Central v14 and later, this permission set is included in CDC APPROVE. |
| CDC ALLOCAT | This permission set is mandatory for customers using allocations. The permission set only applies up to and including Business Central v13. In Business Central v14 and later, this permission set is included in CDC BASIC. |
| CDC SENDEDOCS | Using this permission set, you can edit data in eDocuments. For more information, see [Continia eDocuments](@DC-177). |
| CDC PC ADMIN | This permission set allows you to configure the [Purchase Contracts](@DC-85) setup, create purchase contracts, and update the basic details of each contract. It also enables you to use the purchase contracts administrator review functionality, including the ability to start reviews, return contracts to reviewers, finish reviews, and cancel reviews. |

As indicated above, the CDC WEB, CDC EDIT, and CDC ALLOCAT permission sets were discontinued as of version 14 of Business Central. For version 14 and all subsequent versions of Business Central, the individual permissions of these three sets have instead been included in the other permission sets mentioned above. 

> [!NOTE]
> To configure approval sharing and export users to the Web Approval Portal, you must have access to all companies.

## Permission sets for accounts payable clerks and similar
If your role is to process invoices and other business documents (for example as a bookkeeper or an accounts payable clerk), you need at least the following permission sets for the companies that are relevant to you:

* CSC BASIC
* CDC BASIC
* CDC CAPTURE
* D365 BASIC<a href="#footnote-1.1"><sup>1
* D365 ACC. PAYABLE<a href="#footnote-1.1"><sup>1

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.1">The name of the permission set depends on your version of NAV/Business Central.</li>
  </ol>
</div>
</small>

## Permission sets for approvers
If you're an approver (whether in Microsoft Dynamics NAV/Business Central or in the Web Approval Portal), you need at least the following permission sets for the companies that are relevant to you:

* CSC BASIC
* CDC BASIC
* CDC APPROVE
* D365 BASIC<a href="#footnote-1.2"><sup>1
* D365 PURCH DOC, EDIT<a href="#footnote-1.2"><sup>1

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.2">The name of the permission set depends on your version of NAV/Business Central.</li>
  </ol>
</div>
</small>

> [!NOTE]
> In the Web Approval Portal, the account name of each document line is displayed in the **Account Name** column. In order for this to be visible, you must have direct access to the various types of accounts that can be displayed here (G/L accounts, items, resources, fixed assets, and item charges). Direct access to G/L accounts, items, resources, and item charges is included in the mandatory **D365 PURCH DOC, EDIT** and **D365 BASIC** permission sets mentioned above. If you're using fixed assets, you must be assigned a standard permission set that includes fixed assets.

## Permission sets for reviewers

If you're a purchase contract reviewer (whether in Microsoft Dynamics NAV/Business Central or in the Web Approval Portal), you need at least the following permission sets for the companies that are relevant to you:
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

The following permission sets only apply to earlier versions of Document Capture (prior to 27.0) and are retained here for reference.

| Permission set | Description |
| --- | --- |
| CDC-ALL | To ensure that all standard features work as intended, the CDC-ALL permission set is mandatory for all Business Central users, including those who don't use Document Capture directly, as they still need certain permissions to access and run objects that somehow interfere with the standard Business Central code. The permission set is similar to the standard Dynamics NAV/Business Central BASIC permission set. |
| CDC-CAPTURE | This permission set allows you to import files, capture document values, and register documents in Business Central using Document Capture. Note that you must also be assigned certain standard Business Central permission sets in order to use Document Capture to capture and process documents, depending on what version of Business Central you're using. |
| CDC-APPROVE | Using this permission set, you can perform all basic approval operations when approving documents in either Business Central or the Continia Web Approval Portal: *approve*, *reject*, *put on hold*, *forward*, and *add comment*. The permission set is applicable as of Business Central v14. |
| CDC-SUPER | When you're assigned this permission set, you get full access to all Document Capture tables. This typically applies to users who set up Document Capture in Business Central. |
| CDC-WEB | This permission set enables you to approve documents in the Web Approval Portal. The permission set only applies up to and including Business Central v13. In Business Central v14 and later, this permission set is included in CDC-APPROVE. |
| CDC-EDIT | With this permission set, you can edit purchase invoice lines when approving documents. The permission set only applies up to and including Business Central v13. In Business Central v14 and later, this permission set is included in CDC-APPROVE. |
| CDC-ALLOCAT | This permission set is mandatory for customers using allocations. The permission set only applies up to and including Business Central v13. In Business Central v14 and later, this permission set is included in CDC-ALL. |
| CDC-SENDEDOCS | Using this permission set, you can edit data in eDocuments. For more information, see [Continia eDocuments](@DC-177). |
| CDC-PC-ADMIN | This permission set allows you to configure the [Purchase Contracts](@DC-85) setup, create purchase contracts, and update the basic details of each contract. It also enables you to use the purchase contracts administrator review functionality, including the ability to start reviews, return contracts to reviewers, finish reviews, and cancel reviews. |

<style>
  .content table tr td:nth-child(1) {
    width: 120px;
  }
  .content table tr td:nth-child(2) {
    width: 610px;
  }  
</style>