---
title: Standard Purchase Approval
date: 13-01-2022
description: A description of standard purchase approval and how to initiate it for invoices
id: DC-32
lang: en
---

# Standard Purchase Approval

With standard purchase approval, the approval workflow of any document submitted for approval is determined by the total amount of the document and the purchaser code you apply to it.

The document is initially routed to the approver that is associated with the entered purchaser code, and if the document amount is within the approver's approval limit, the approver can approve the document and end the approval process. If, on the other hand, the document amount exceeds the approver's approval limit, the document is forwarded to the manager of the approver instead. In case the manager doesn't have sufficient approval limit either, the document is then routed to the manager's manager, and so on until an approver with sufficient approval limit has been identified.

Note that this article uses purchase invoices to describe the application of standard purchase approval, but the functionality is equally applicable to credit memos.

> [!IMPORTANT]
> [Purchase approval must be enabled](@DC-22) in the **Document Capture Setup** in order for this to work.
> 
> The default configuration of the Continia Document Capture **Purchase Invoice Approval Workflow** must remain as is. So for the **Approval of a purchase document is requested** event, the settings of the workflow response must be as follows under **Create an approval request for the record using approver type %1 and %2 (DC)**:
> * **Approver Type** must be **Salesperson/Purchaser**.
> * **Approver Limit Type** must be **Approver Chain**.
> 
> Also, all users in the chain of approval must be [set up as approvers](@DC-23). Otherwise, an error will be returned when you submit the document for approval.

## To initiate standard purchase approval for an invoice

You initiate standard purchase approval for an invoice simply by applying a purchaser code to it. This is typically done during the field-capturing process that follows after document scanning and import.

To apply a purchaser code to an invoice, do as follows:

1. Follow the usual procedure for capturing fields:
   1. Search ({{search}}) for and select **Document Categories**.
   1. Select the **PURCHASE** code to open the document journal for purchase documents.
   1. In the list of documents displayed in the document journal, select the invoice for which you want to [capture fields](/continia-document-capture/business-functionality/documents-and-templates/working-with-paper-and-pdf-documents#capturing-fields).
1. To apply a purchaser code, go to the **Document Header** section and locate the **Our Contact** field in the table.
1. For the **Our Contact** field, under **Value**, select the three dots on the right to open the **Salespeople/Purchaser** page.
1. In the list of purchaser codes, select the one you want to apply to the invoice, and then select **OK** to close the page.

The chosen purchaser code is now added to the **Our Contact** field and will be copied to the invoice during registration, thereby initiating standard purchase approval. When you submit the invoice for approval, it will be sent to the approver associated with the chosen purchaser code and, in case of insufficient approval limit, escalated to the approver's manager.

## Related information

[Document Capture Setup](@DC-22)  
[Continia User Setup for Approvals](@DC-23)  
[Capturing fields](/continia-document-capture/business-functionality/documents-and-templates/working-with-paper-and-pdf-documents#capturing-fields)  