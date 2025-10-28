---
title: Continia Web Approval Portal
date: 15-05-2025
description: A description of the Continia Web Approval Portal, and how to use it.
id: DC-165
lang: en
---

# Continia Web Approval Portal

The [Continia Web Approval Portal](https://www.continiaonline.com/) is a website dedicated to the approval of purchase documents (including purchase contracts), expenses, and sales documents across the companies you have access to. The blue ribbon at the top of the portal features a tab for each of these areas – **Purchase**, **Expense Management**, **Contracts**, and **Sales**, provided that you have all relevant solutions/modules activated – but this article focuses exclusively on the **Purchase** tab and the approval and management of purchase documents.

There are two views available in the Web Approval Portal: classic and cross-company. The main focus of this article is the cross-company view.

> [!NOTE]
> To set up the Web Approval Portal and configure users for it, see [Setting up Web Approval](@DC-76). Note that users must also be [set up as approvers](@DC-23#to-set-up-users-as-approvers) in order to use the portal.

## Purchase approval

The landing page of the **Approvals** section is the **My Open Approvals** page. This page provides an overview of the various documents for approval, and allows you to carry out a number of commonly used approval actions.

To open other overview pages, select **My Open Approvals**. This opens a dropdown menu from where you can choose between the following:

<br>

| Page/section | Description |
| --- | --- |
| System View | A section header. This section of the dropdown menu contains a list of all available purchase approval overview pages. |
| Approvals On The Way | This page lists all documents for which you've been assigned as an approver who's not the first approver in the approval flow. No approval actions can be carried out from this page. |
| My Open Approvals | The main page that lists all documents pending your approval. From this page, you can approve, reject, or forward documents for approval, or put them on hold. |
| My Processed Approvals | A page that lists all approval documents that have been either approved or rejected. No approval actions can be carried out from this page. Once documents are posted, they're no longer available on this page – but can be found using the archive functionality. |
| All Shared Approvals | A page that lists all approval documents that have been shared with you by another approver. These are documents that you can approve even though they weren't originally yours to approve. From this page, you can approve, reject, forward for approval, or put documents on hold. |
| Shared Approvals | A section header. This section of the dropdown menu contains a list of all users that have shared approvals with you. When you select a name on the list, a filtered page opens, displaying only the documents that the selected user has shared with you. From each of the pages listed in this section, you can approve, reject, forward for approval, or put documents on hold. |

> [!TIP]
> To return to the **My Open Approvals** page, select either the home icon or the text **Continia Web Approval Portal**, both in the upper-left corner of the screen, on the blue ribbon at the top of the portal.

Most overview pages feature the same set of approval actions, and they all allow you to drill down to each individual document to get access to more document details and additional approval actions. In the following, **My Open Approvals** – the default landing page – is used as an illustrative example.

### My Open Approvals

The action bar of the **My Open Approvals** page features the following approval actions:

* Approve
* Reject
* Forward
* Put on Hold and Approve
* Put on Hold

These actions allow you to process documents straight from the landing page. They're described in detail below under [The detailed view](#the-detailed-view).

To narrow down the number of approval entries per page, use **Select Type** to filter on the type of document or **Select Company** to filter on the company.

The list of approval entries provides the most important details about each of the documents submitted for approval, including the company, type, name, latest approval comment, and amount. In addition, the **Actions** column allows you to view or download the original PDF or XML.

To carry out one of the above approval actions from this page:

1. In the list of approval entries, choose the one that you want to process by selecting the column on the far left – the one with a checkmark in the header – for the relevant entry. This highlights the entire entry.
1. On the action bar, click the action that you want to perform for the selected entry.
1. Do one of the following:
   1. If you select **Reject**, **Put on Hold and Approve**, or **Put on Hold**, a dialog opens. Select a reason code (if such codes have been set up) and add a comment, and then select **Continue** to confirm the action.
   1. If you select **Forward**, a different dialog opens. Select or enter the name of the user who you want to forward the approval request to, and then select the forwarding action you prefer. If necessary, add a comment at the bottom, and then select **Continue** to confirm the action. 

> [!TIP]
> In the list of approval entries, you can select multiple entries at the same time to carry out approval actions in bulk for all selected entries. To select all entries in one go, select the checkmark on the far left in the header. You can also use this checkmark to cancel the selection of all entries.

If you need more document details and/or additional approval actions for a given approval entry, select the entry to open the detailed view. This is described in the next section. 

### The detailed view

The detailed view includes more actions on the action bar, a document viewer on the right, access to more document details, a list of all approval comments and attachments, and the ability to add comments and files and to view or edit document lines – among other things.

The table below provides an overview of the various actions on the action bar, though not all are available across all document types:

<br>

| Action | Description |
| --- | --- |
| Approve | Approves the document of the open approval entry. Note that when you approve a document, the Web Approval Portal attempts to approve the next entry – provided that the **Approval Sharing** settings allow for it. |
| Reject | Rejects the document of the open approval entry. In the dialog that opens, select a reason code (if such codes have been set up) and add a free-text comment, and then select **Continue** to confirm the action. |
| Forward | Forwards the document of the open entry to a different user for approval. You have up to three forwarding options, [depending on your setup](@DC-164): <ul><li><b>Approve \& Forward</b>: Select this to first approve the document and then have it forwarded to a different user for further approval.</li><li><b>Forward without approval</b>: Select this to forward the document to a different user for approval without approving it yourself.</li><li><b>Forward and return to me for approval</b>: Select this to forward the document to a different user for approval and then have the document automatically returned to you for further approval.</li></ul> |
| Put on Hold and Approve | Puts the document on hold and approves it at the same time. |
| Put on Hold | Puts the document on hold if you're not ready to approve it yet – for example, if you expect to receive a related credit memo or need more time to gather necessary information. By putting the document on hold, you signal to other stakeholders that you've received the document but may struggle to meet the approval deadline. <br> <div class="alarm alarm-note"><p class="alert-title"><i class="icon icon-warning-2"></i><span>Note</span></p><p>When a document is on hold, it can't be finalized – for example, a purchase invoice can't be paid – even if it's approved. During approval, you can choose to remove the on-hold status of the document using the **Remove On Hold** dialog that's displayed. This is okay in some situations and undesirable in others, depending on your organizational setup. To prevent the **Remove On Hold** dialog from being displayed, see [To set up purchase approval](@DC-22#to-set-up-purchase-approval).</p></div> |
| Use Template | Distributes the amount of the document automatically between multiple lines using an amount distribution code. For more information, see [Using Amount Distribution Codes](@DC-118) in general and [To activate codes in the Web Approval Portal](@DC-118#to-activate-codes-in-the-web-approval-portal) specifically. |
| Previous | Goes to the previous approval entry in the list of entries on the **My Open Approvals** page. |
| Next | Goes to the next approval entry in the list of entries on the **My Open Approvals** page. |
| Download | Downloads the original PDF or XML. |
| Fullscreen | Views a full-screen image of the original PDF or XML. |

**The document viewer** on the right side of the page displays an OCR-processed version of the document to be approved. This document viewer is not interactive, as it is in the document journal or on the document card in Continia Document Capture.

**The main area of the detailed view**, to the left of the document viewer, has the name of the vendor as its header, and on the right side of this, the document currency and the total amount excluding VAT are displayed. Immediately below the header are a number of important document details, which also vary depending on the document type:

<br>

| Field | Description |
| --- | --- |
| Type | The type of purchase contract. For example, expense or purchase. |
| Number | The document number as registered in Document Capture (**Document No.**). |
| Vendor Name | The name of the vendor related to the document. |
| Description | The description of the document. |
| Cost Category | The description of the document. |
| Contract Start Date | The date from when the contract is valid. |
| Price Type | Defines if a purchase contract has a fixed or variable amount. |
| Invoicing Period | The invoicing period for a purchase contract. |
| Prices Including VAT | Specifies whether the amounts in the document include VAT. |
| Date | The date when the document was issued, as stated in the purchase document. |
| Due Date | The date when the document must be paid. |
| Approvers | A list of all approvers involved in the approval of the document. The approver whose name is written in bold is the one with whom the approval of the document currently resides. <br> <div class="alarm alarm-tip"><p class="alert-title"><i class="icon icon-tip"></i><span>Tip</span></p><p>If you select the circled i to the right of **Approvers**, a window is displayed, providing the approval history of the document, including the exact details of when the document was received and approved (date and time stamps) and by whom. </p></div> |

On the right side of the main area is a list of the comments and/or attachments that have been added to the document, including date and timestamps and the names of the approvers who added the comments or attachments. Using the filters **All**, **Comments**, and **Attachments**, you can filter the list accordingly.

To add a comment to the document, select the text field at the top of this section and enter the desired text. When you're done, select **Save** or press Enter to submit the comment. You can use the same field to add an attachment by selecting the paper clip icon, selecting the file that you want to attach, and then selecting **Open**. Alternatively, you can drag the relevant file to the comments and attachments section to add it. Any added comments and attachments are included in the list below the field.

In the **Invoice Lines** section, you can view the lines of the document as they've been captured by Document Capture or edited/entered by other users. If necessary, you can also edit the lines to correct any mistakes or even add lines, provided that **Can Edit Posting Lines** has been enabled for you as an approver. For more information, see [To set up users as approvers](@DC-23#to-set-up-users-as-approvers).

The **Total Amounts** section contains all relevant information about the amounts of the document, including both imported and assigned amounts, if applicable, as well as the difference between these.

> [!NOTE]
> When a vendor sends you a purchase document such as an invoice, Document Capture automatically registers the total amount of this invoice and copies it to the corresponding purchase invoice that's created in Microsoft Dynamics 365 Business Central. The original invoice total – known as the imported amount – is used to verify that the sum of all lines matches the amount of the imported document, but this amount can be changed by certain users if necessary. For more information, see [Customization of imported amounts](@DC-139#customization-of-imported-amounts).

## Archive

The **Archive** section allows you to search for purchase approval documents that have already been approved. To open the **Archive** section, select the **Archive** option from the **Purchase Menu** on the blue ribbon at the top of the portal.

You must fill out one or more of the following search criteria to search for archived documents:

<br>

| Field | Description |
| --- | --- |
| Search For | Specify what type of purchase documents you want to search for. You can choose between invoices and credit memos. |
| Vendor | Enter the name of a vendor to search for purchase documents sent by that particular vendor. |
| Posting Date | Enter or select start and end dates to search for documents with posting dates within the specified time range. |
| Our Invoice No. | Enter a document number to search for purchase documents whose **Document No.** field value matches the entered number. |
| Vendor Invoice No. | Enter a document number to search for purchase documents whose **Vendor Invoice No.** field value matches the entered number. |

The more search criteria you enter, the more precise your search is. When you've entered all relevant search criteria, select **Search** in the upper-left corner. The Web Approval Portal will then list all documents that match the entered search criteria.

## The company overview menu

>[!NOTE]
>This menu is only available if you've selected the classic view on the **Settings** page of the Web Approval Portal. By default, the cross-company dashboard is selected.

The company overview menu in the upper-right corner of the portal lists your companies, and displays how many documents for approval there are for each company. If you expand this by selecting **\[number\] [document type] for approval**, a breakdown of the distribution of these documents is displayed. For example, if the company overview menu indicates that one of your companies has a total of 10 documents for approval, you may find the following distribution when you expand the menu:

**Company name**  
10 documents for approval

* 5 purchases
* 3 expenses
* 2 per diems

This distribution is also reflected in the blue ribbon (where figures indicate the number of documents for approval per tab) and in the green options in the submenus (where figures indicate the number of documents for approval for each document type). In this case, the blue ribbon – including submenus – could look like this:

<br>

| Purchase (5) | Expense Management (5) | Sales (1) |
| --- | --- | --- |
| Purchase Menu <br> **Approvals (5)** | Expense Management Menu <br> **Expenses (3)** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **Mileage (0)** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **Per diems (2)** &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; **Expense reports (0)** | Sales Menu <br> **Orders (1)** |

The numbers in brackets – representing the number indicators – clearly indicate where to find the documents for approval. Together with the company overview menu, they provide you with a good overview of the distribution of your approval tasks.

If you select a specific document type in the expanded version of the company overview menu, the corresponding document list opens. You can also select the company name in either the expanded or the collapsed version of the menu to open the highest ranked document list that has documents for approval. Which document list to open is determined according to the following hierarchy:

1. Purchase Menu - Approvals
1. Expense Management Menu - Expenses
1. Expense Management Menu - Mileage
1. Expense Management Menu - Per diems
1. Expense Management Menu - Expense reports

If there are no documents for approval in the document lists higher in the hierarchy, the next one in the hierarchy is opened instead when you select the company name in the company overview menu. But even a single document for approval in a highly ranked list trumps a lower ranked list with more documents for approval. For example, if you have 25 expenses to approve but only one purchase document for approval, the Purchase Menu – Approvals list is opened because it's ranked higher in the hierarchy.

## To handle other types of document

Before you can process documents other those supported out-of-the-box in the Web Approval Portal (e.g.: purchase invoices, purchase contracts, purchase orders, and credit memos), you need to set up PDF reports and web menus.

>[!NOTE]
>Web menus are only available when the Web Approval Portal is set to Classic mode. If your portal is set to Cross-company, only the document types supported by default are shown.

This allows you to view and handle documents such as sales quotes, sales orders, and sales credit memos in the Web Approval Portal. However, note that it’s not possible to edit these documents in the Web Approval Portal – or see order line information that’s not shown in the report.

To create a PDF report setup and assign it to a web menu:

1. Search ({{search}}) for and select **Document Capture Setup**.

2. On the **Document Capture Setup** page, go to Setup and, on the action bar, click Web Approval.

3. On the **Document Capture Setup** / **Continia Web Approval** page, select **PDF Report Setup** on the action bar.

4. On the **PDF Report Setup** page, in a new line, enter the following details:

   * **Table ID** - the ID of the table that should use the PDF report specified.
   * **Document Type** – the type of document for which this report is generated in PDF.
   * **PDF Report ID** - the report for the approval entries, with the specified table ID and document type, used for the generation of a visual representation in PDF in the portal.

5. Return to the **Document Capture Setup / Continia Web Approval** page and, on the action bar, click **Web Menus**.

6. On the **Web Menu Card**, in a new line, enter the following details:

   * **Code** - the desired code of the web menu.
   * **Description** - a brief description of the web menu, which is visible in the portal.
   * **Sorting** - the order in which this web menu appears in the portal.

7. On the action bar, click **Edit** to open the new web menu.

8. On the **Web Menu Card**, enter the following details on the **Submenus** FastTab:

   * **Code** - the desired code of the submenu.
   * **Description** - a brief description of the submenu, which is visible in the portal.
   * **Approval Code Filter** - the approval workflow code, used by the Web Approval Portal to filter approval entries. E.g.: MS-SOAPW-01.
   * **Table ID Filter** - the ID of the table used by the Web Approval Portal to filter approval entries. This value should match the corresponding **Table ID** on the **PDF Report Setup** page.
   * **Document Type Filter** - the number value (e.g.: 0, 1, 2, etc.) of the option available in the Business Central table field (e.g.: quote, order, invoice, etc.).
   * **Sorting** - the order in which this submenu appears within the menu in the portal.

You can now log in to the Web Approval Portal and handle additional document types.

## Related information

[Overview of Purchase Approval](@DC-34)  
[Different approval clients](@DC-111)  