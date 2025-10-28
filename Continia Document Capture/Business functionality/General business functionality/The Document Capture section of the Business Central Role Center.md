---
title: The Document Capture Section of the Business Central Role Center
date: 17-04-2025
description: An overview of the Document Capture functionality available within the Role Center.
id: DC-172
lang: en
---

# The Document Capture section of the Business Central Role Center

Continia Document Capture enhances the user interface and functionality of Microsoft Dynamics 365 Business Central by extending some of the standard Role Centers in Business Central. It does so by adding a section with a number of cues and action tiles, making it easier for you to process your incoming documents.

This section, **Continia Document Capture Activities**, is divided into several cue groups – each of which contains multiple relevant cues or action tiles. These are all described in more detail below, under [The Continia Document Capture Activities section](#the-continia-document-capture-activities-section).

The following standard Business Central Role Centers have been extended with this section:

* **Accountant**
* **Accounting Manager**
* **Accounts Payable Coordinator**
* **Bookkeeper**
* **Business Manager**

> [!NOTE]
> In addition to the above Role Centers, which have been extended by default, Continia partners can extend any additional Business Central Role Center with the **Continia Document Capture Activities** section as well. This is done using the page **6085573 CDC Doc. Capture Activities**. If this is relevant to you, please reach out to [your Continia partner](@DC-15).

## The Continia Document Capture Activities section

The **Continia Document Capture Activities** section of the Role Center includes five cue groups:

* [**Documents**](#the-documents-group)
* [**Purchase Approval - Invoices**](#the-purchase-approval---invoices-group)
* [**Purchase Approval - Credit Memos**](#the-purchase-approval---credit-memos-group)
* [**Purchase Contracts**](#the-purchase-contracts-group)
* [**Actions**](#the-actions-group)

Each of these cue groups contains multiple relevant cues or action tiles, as described in the sections below.

### The Documents group

The **Documents** cue group provides an overview of how many documents are pending OCR-processing, how many are ready to be imported, how many are ready to be registered, and how many are assigned to you.

Selecting **Pending OCR** or **Ready to Import** opens a corresponding page that lists all document categories. In the **Documents for OCR** column, you can see how many documents are pending OCR-processing for each category. When a document has been OCR-processed, it's moved to the **Documents for Import** column. If there was an issue with a document during the OCR-processing of it, it's moved to the **Documents with Error** column, from where you must then handle it manually.

> [!TIP]
> To view the details of the documents in any of the columns or carry out various actions for any of them, select the number in the relevant column for the relevant document category to open the **Display Documents** page, which lists all the documents in the selected column and category. From this page, you can search for a specific document in the list (**Search**), open a file to view it outside of Business Central (**Show File**), delete a file entirely (**Delete**), and import an OCR-processed file (**Import File**).
>
> Note that in the **From** column you can also view the email address of the original sender of a document (typically a vendor), rather than that of an intermediary mailbox or similar.

Selecting **Ready to Register** opens the document journal, which is where you process imported documents and capture the textual information that’s contained within them. For more information about the document journal and how to use it, see [Working with paper and PDF documents](@DC-71).

Selecting **Assigned to me** opens the **Assigned Documents** page, which enables you to view, process, unassign, or reassign documents that have been assigned to you. The documents displayed here have been assigned to you because you’re better equipped to handle them than the users who assigned them to you. They’re not documents for approval or in any other way related to document approval.

### The Purchase Approval - Invoices group

The **Purchase Approval - Invoices** cue group is dedicated to purchase invoices (PIs) and contains three cues: **Open PIs**, **PIs for Approval**, and **Released PIs**. These provide an overview of how many invoices are open, how many are ready to be approved, and how many have been released – respectively.

No matter which of the cues you select, the **Purchase Invoices** page opens. It's named and filtered differently according to your selection, though the overall layout is the same.

### The Purchase Approval - Credit Memos group

The **Purchase Approval - Credit Memos** cue group is dedicated to purchase credit memos (PCMs) and contains three cues: **Open PCMs**, **PCMs for Approval**, and **Released PCMs**. These provide an overview of how many credit memos are open, how many are ready to be approved, and how many have been released to the next stage of processing – respectively.

No matter which of the cues you select, the **Purchase Credit Memos** page opens. It's named and filtered differently according to your selection, though the overall layout is the same.

> [!NOTE]
> For more information about the standard Business Central purchase functionality relating to any of the pages above, see [Purchasing](https://learn.microsoft.com/en-nz/dynamics365/business-central/purchasing-manage-purchasing) (Microsoft article). <br><br>For more information about purchase approval, see [Overview of purchase approval](@DC-34).

### The Purchase Contracts group

The **Purchase Contracts** cue group is dedicated to purchase contracts and contains four cues: **All**, **Approval Due**, **Approval Needed**, and **Pending Approval**. These provide an overview of how many contracts there are in total, how many are due based on the next approval date, how many have the status **Approval Needed**, and how many have the status **Pending Approval** – respectively.

No matter which of the cues you select, the **Purchase Contracts** page opens. It's named and filtered differently according to your selection, though the overall layout is the same.

>[!NOTE]
>For more information about purchase contracts, see [Overview of purchase contracts](@DC-85).

### The Actions group

The **Actions** cue group contains five action tiles that allow you to perform different tasks and operations:

<br>

| Action | Description |
| --- | --- |
| **Submit Document** | Select this to open a page with a list of email addresses for each document category. To import a document into Document Capture, select an email addresses from the list (you may want to maximize the page), and then send an email to the selected email address with the relevant document attached. For more information, see [Importing documents](@DC-82#via-email). |
| **Import Files** | Select this to import all files from the **Ready to Import** cue in [the **Documents** cue group](#the-documents-group). The files will then be moved to the **Ready to Register** cue. For more information, see [Importing documents](@DC-82#via-email). |
| **Document Search** | Select this to search through your PDF and XML documents for any text. All textual content in the documents is checked, no matter if the text has been captured or not. Note that **Find entries** finds all entries related to the transaction you've searched for, even including unposted documents – such as invoices that are pending approval or haven't been registered yet. For more information, see [Search for any document](https://www.youtube.com/watch?v=if9Vjx_IeEg) (video). |
| **Send Status email to Approvers** | Select this to send an email notification to all approvers that have pending approval requests. For more information, see [To send status emails manually](@DC-26#to-send-status-emails-manually). |
| **Send Status email to Purchase Contract Approvers** | Select this to send an email notification to all purchase contract approvers that have contracts pending their approval. |

## Related information

[OCR-processing a document](@DC-145)  