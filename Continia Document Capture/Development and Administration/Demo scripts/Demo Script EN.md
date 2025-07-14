---
title: Continia Document Capture demo script
date: 11-04-2025
id: DC-57
lang: en
description: A detailed description of how to demo standard Document Capture features.
---

# Continia Document Capture demo script

This script provides a step-by-step description of how to give a complete demonstration of the standard features in Continia Document Capture.

The purpose of the Continia demo systems is to give Continia partners an environment to educate end customers, and to present and test the latest versions of Document Capture. Previous knowledge of Document Capture is required.

This demo environment is already set up and ready to use, and it's always updated to the latest version of Document Capture.

The script covers the following processes:

\


| Process                                                                                                                                | Description                                                                                                                                          |
| -------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| [To register PDF invoices with total amount](<Demo Script EN.md#to-register-pdf-invoices-with-total-amount>)                           | How to register PDF invoices for which the full amount will be posted to a single G/L account.                                                       |
| [To register PDF invoices with lines](<Demo Script EN.md#to-register-pdf-invoices-with-lines>)                                         | How to recognize and register individual invoice lines for which the line amounts will be posted to different G/L accounts, as different items, etc. |
| [To register XML invoices with lines](<Demo Script EN.md#to-register-xml-invoices-with-lines>)                                         | How to add missing fields to XML templates and register XML invoices.                                                                                |
| [To match purchase invoices against orders/receipts](<Demo Script EN.md#to-match-purchase-invoices-against-ordersreceipts>)            | How to automatically match purchase invoices to their related purchase orders or purchase receipts.                                                  |
| [To approve invoices in the Continia Web Approval Portal](<Demo Script EN.md#to-approve-invoices-in-the-continia-web-approval-portal>) | How to carry out various approval actions and set up out-of-office approval sharing using the Continia Web Approval Portal.                          |
| [To approve invoices in the Business Central web client](<Demo Script EN.md#to-approve-invoices-in-the-business-central-web-client>)   | How to use Business Central to approve and post documents, including approving on behalf of other users.                                             |
| [To access the archive using **Find Entries**](<Demo Script EN.md#to-access-the-archive-using-find-entries>)                           | How to use the standard Business Central **Find Entries** functionality to navigate directly to archived PDF invoices.                               |
| [To access the archive from the vendor card](<Demo Script EN.md#to-access-the-archive-from-the-vendor-card>)                           | How to view recently received documents from the vendor card.                                                                                        |
| [To access the archive using full-text search](<Demo Script EN.md#to-access-the-archive-using-full-text-search>)                       | How to search for any content in archived PDF files, whether or not your search string was recognized during document registration.                  |
| [To add and process a custom document](<Demo Script EN.md#to-add-and-process-a-custom-document>)                                       | How to submit a custom PDF file to your demo environment, and import the PDF into the desired category.                                              |

## Users in the demo environment

The names of the users in your demo environment differ depending on the localization of the environment. In Document Capture, the following user roles are available:

\


| User role  | Description                                                                                                                                                                                                                                        |
| ---------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Controller | This user is the person that typically performs day-to-day accounting in Microsoft Dynamics 365 Business Central related to invoice management, purchase order matching, etc.                                                                      |
| Approver   | This user is the person that approves invoices, credit memos, etc. The demo environment is set up with approval sharing, meaning that all documents are sent to a group called Marketing, which has multiple approvers that can approve documents. |

The user names in the welcome email and the Continia Demo Portal are the actual names of the users in your environment.

> \[!NOTE] For ease of reference and understanding, this demo script refers to the actual names of the controller and the approver as they appear in the UK localization of Business Central:
>
> * Controller: Ester Henderson (EH)
> * Approver: Robin Bettencourt (RB)

## To register PDF invoices with total amount

1. Sign in to Business Central as the controller Ester Henderson (EH).
2. In the Role Center, select **Ready to Register**.
3.  Select the first invoice from vendor **20000** (First Up Consultants/AR Day Property Management).

    > \[!NOTE] Note that this invoice is an OCR-processed document (a PDF file). For the registration of XML documents, see [Purchase document registration – XML](<Demo Script EN.md#purchase-document-registration--xml>) below.
4. On the **Document Header** FastTab, select one of the value fields in the list to identify the location of the value in the document image, and to verify that it has been captured correctly.
5. Go through the remaining document header fields to confirm that the initial field recognition has been completed successfully.
6.  Under **No.**, add a suitable G/L account.

    > \[!TIP] The following G/L accounts are suitable in this context, depending on your localization:
    >
    > * **AT: 7610, AU: 6040, BE: 612500, CH: 6500, DE: 6815, DK: 05650, ES: 6290002, FI: 6851, FR: 618000, GB: 31010, NL: 3610, NO: 8210, NZ: 8210, SE: 6230, US: 64100**
7. In the dialog box that opens, select **Yes** to set up the template to use the selected account whenever you register future invoices from this vendor.
8. Select the **Posting Description** field value, and highlight the relevant text in the document image using your left mouse button.
9. The document has now been fully recognized. Select **Process** > **Register** to create the purchase invoice in Business Central.
10. The **Purchase Invoice** page opens automatically. Confirm that the recognized (imported) amount corresponds to the line total in the invoice line section, and then select **Request Approval** > **Send Approval Request** > **OK** to confirm. The **Document Status** changes to **Pending Approval**.
11. Close the **Purchase Invoice** page to return to the document journal.
12. Register the other two invoices from vendor **20000** (First Up Consultants/AR Day Property Management) in the document journal, and then send them for approval by selecting **Recognize Fields** > **Register** > **Send Approval Request** > **OK**.

## To register PDF invoices with lines

1. In the document journal, select the first invoice from vendor **50000** (Nod Publishers) or **10000** (London Postmaster) – invoice number 17777.
2. On the action bar, click **Document** > **Document Card**.
3. On the **Lines** FastTab, select the **No.** value field, and then capture the header **Item #** in the document image by drawing an orange box around it using the right mouse button.
4.  Repeat this process for the additional value fields:

    \


    | Line value field | Header text to capture in the document image |
    | ---------------- | -------------------------------------------- |
    | **Description**  | **Text**                                     |
    | **Quantity**     | **Quantity**                                 |
    | **Unit Cost**    | **Price**                                    |
    | **Line Amount**  | **Amount**                                   |

    \

5. On the action bar, click **Recognize Fields**. The values associated with the headers you've captured manually are then automatically recognized and added to the list on the **Lines** FastTab.
6.  Fill out the three line translations as follows:

    \


    | Line number | No.        | Translate to Type | Translate to No.                                  |
    | ----------- | ---------- | ----------------- | ------------------------------------------------- |
    | 1           | **C1908**  | **Item**          | **1908-S**                                        |
    | 2           | **C1900**  | **Item**          | **1900-S**                                        |
    | 3           | **MP1969** | **GL Account**    | Relevant office supplies account (see note below) |

    > \[!NOTE] For line 3 above, the **Translate to No.** account depends on your localization:
    >
    > * **AT: 7610, AU: 6040, BE: 612500, CH: 6500, DE: 6815, DK: 05650, ES: 6290002, FI: 6851, FR: 618000, GB: 31010, NL: 3610, NO: 8210, NZ: 8210, SE: 6230, US: 64100**
7. On the action bar, click **Register** to create the invoice in Business Central, and then select **Send Approval Request**.
8. Return to the document journal, and register the next invoice from vendor **50000** (Nod Publishers) or **10000** (London Postmaster), with invoice number 18888. Don't send this invoice for approval.
9. Recognize the last invoice from vendor **50000** (Nod Publishers) or **10000** (London Postmaster) – invoice number **19999**. As new item numbers are now recognized, several line errors are displayed. Don't register the invoice.

## To register XML invoices with lines

1.  In the document journal, select the first Peppol document from Nod Publishers/London Postmaster.

    > \[!NOTE] Note that this invoice is an XML document. For the registration of OCR-processed documents (PDF files), see [Purchase document registration – total amount](<Demo Script EN.md#purchase-document-registration--total-amount>) above.
2. Look at the **XML Path** column to see where the data is identified in the XML document.
3. Whenever an XML document is recognized, the line recognition feature is automatically activated, meaning that Document Capture automatically identifies all recognized item numbers based on **Item Reference**, **Purchase Line Translation, Description Translation**, and **Vendor Item**. On the action bar, click **Register** to create the purchase invoice in Business Central.
4. The Business Central **Purchase Invoice** page opens automatically. Close the page to return to the document journal.
5. Select the second Peppol invoice from Nod Publishers, and then select **Recognize Fields**. This invoice has a document embedded in the XML file, as evidenced by the number (**1**) that's displayed in the **Attachments** field of the **Document Header** section.
6. To view the attached file, simply select the **Document** field in the upper-left corner of the document viewer, and then select the file from the drop-down menu that opens.
7. The comments section displays a warning that needs attention. This warning appears because the XML document contains values that are currently not recognized in any template fields. Document Capture comes with built-in functionality to validate XML document amounts, and each validation results in a user notification. Select **Template** > **Add Template Field** to add the relevant fields to the template.
8. When asked if you'd like to review the list of missing fields, select **Yes**.
9. Select both fields (**95 – Discount** and **CG – Cleaning**), and then select **OK**.
10. When the fields have been added, the values are automatically recognized. In the comments section, a couple of new messages are displayed. In this demo scenario, the two newly recognized amounts must be assigned to a G/L account.
11. Select **Template** > **Accounts for Amounts** to open the posting setup for the recognized header amount fields.
12. Choose a suitable G/L account for both amounts, and select **OK** to confirm.

    > \[!TIP] The following G/L accounts are suitable in this context, depending on your localization:
    >
    > * **AT: 7610, AU: 6040, BE: 612500, CH: 6500, DE: 6815, DK: 05650, ES: 6290002, FI: 6851, FR: 618000, GB: 31010, NL: 3610, NO: 8210, NZ: 8210, SE: 6230, US: 64100**
13. Select **Recognize Fields** to check that everything has been recognized correctly. If so, select **Register** to create the purchase invoice in Business Central.
14. Once the invoice has been created, send it for approval by selecting **Send Approval Request** > **OK**.

## To match purchase invoices against orders/receipts

1. In the document journal, select the invoice from vendor **40000** (Wide World Importers) or **30000** (Schmeichel Møbler).
2. To match the invoice against a purchase order/receipt, select **Process** > **Match Lines** to open the matching page.
3. Select **Process** > **Perform Match**. Note that the purchase order receipt lines are automatically matched with the purchase invoice.
4. Close the page to return to the document journal.
5. In the comments section, a message informs you that the invoice has been fully matched with the purchase receipt.
6. On the action bar, click **Process** > **Register** to create the invoice in Business Central, and then select **Send Approval Request** > **OK**.
7. Close all pages to return to the Role Center.

## To approve invoices in the Continia Web Approval Portal

1. Sign in to the Continia Web Approval Portal as the approver Robin Bettencourt (RB).
2. On the **My Open Approvals** page, in the list of documents for approval, select the Nod Publishers invoice with a total amount of 797.00 excluding VAT (invoice number **17777**).
3. Under **Invoice Lines**, in the **Department** column, add the department codes you prefer.
4. To attach a document, open Windows File Explorer, and then drag the relevant document from your desktop to the drop area in the Web Approval Portal.
5. On the action bar, click **Approve** to approve the invoice.
6. Finalize and approve the second invoice (invoice number **100026**) from vendor **50000** (Nod Publishers) or **10000** (London Postmaster).
7. Select the invoice from Wide World Importers, and then select **Put on hold** on the action bar.
8. In the box that opens, select a reason code and enter a reason for putting the approval on hold, and then select **OK** to close the box.
9. As you're signed in as Robin Bettencourt, who's currently unavailable, you must adjust your out-of-office settings. Select the cogwheel in the upper-right corner, and specify that Robin will be away for the rest of the week.
10. Close the browser.

## To approve invoices in the Business Central web client

1. Sign in to Business Central as the controller Ester Henderson (EH).
2.  Navigate to the **Purchase Approval Entries** page.

    > \[!NOTE] Because Robin Bettencourt has limited approval rights, not all invoices are released. Robin has shared his approvals with Ester Henderson (EH), who's the next approver in this setup. The documents that have been submitted to Robin and which are still open are displayed in the list of purchase documents for approval, under the heading **Shared by Robin Bettencourt**.
3. In the list, under the heading **Shared by Robin Bettencourt**, select the first invoice from **First Up Consultants/AR Day Property Management** (invoice number **44444444**), and then select **Approve**.
4. Open the **Purchase Invoices** page. Note that all approved purchase invoices are written in green, have the status **Released**, and are ready to be posted. Invoices pending approval are written in black, whereas the red invoices haven't yet been sent for approval.
5. Go to the released invoice from Nod Publishers, select **No.** to open the **Purchase Invoice** card, and then select **Posting** > **Post**.
6. When asked if you'd like to view the posted invoice, select **Yes**. This will open the **Posted Purchase Invoice** card.

## To access the archive using 'Find Entries'

1.  On the **Posted Purchase Invoice** card, select **Home** > **Find Entries**.

    > \[!NOTE] You can also do this from the **Posted Purchase Invoices** list: Select the posted invoice from vendor **50000** (Nod Publishers) or **10000** (London Postmaster), and then select **Home** > **Find Entries**.
2. On the action bar, click **Show Related Entries** to view the PDF version of the original invoice or other attachments (**Document Capture File**).
3. Return to the Role Center.

## To access the archive from the vendor card

1. Open the **Vendors** page, and navigate to vendor **50000** (Nod Publishers) or **10000** (London Postmaster).
2. The FactBox on the right displays a list of the latest documents relating to this vendor and processed by Document Capture. Select one of the documents to view the original file.
3. On the vendor card, on the **General** FastTab, the field **No. of Documents** shows the number of attachments that have been archived for the vendor. Select the number to view the full list.
4. Return to the Role Center.

## To access the archive using full-text search

1. In the Role Center, select the **Document Search** action.
2.  Enter the text that you want to search for in the **Find What** field. On the action bar, click **Search** to activate the search.

    > \[!TIP] The text to search for depends on your localization:
    >
    > * **AT: Bernhard, AU: Robin, BE: Dale, CH: Bernhard, DE: Bernhard, DK: Lukas, ES: Sergio, FI: Antero, FR: Gérard, GB: Robin, NL: Dale, NO: Stein, NZ: Robin, SE: Viktor, US: Robin**
3.  You can narrow down the search by adding additional search terms or by choosing a category in the **Document Category** field. On the action bar, click **Search** to activate the search again.

    > \[!TIP] The category to choose depends on your localization:
    >
    > * **AT: London, AU: London, BE: London, CH: London, DE: London, DK: London, ES: Londres, FI: London, FR: Londres, GB: London, NL: London, NO: London, NZ: London, SE: London, US: London**
4. Select the first search result in the list, and then select **Show Document Card**, **Show File**, or **Find Entries** to view the document details.

The search functionality is based on the full content of all PDF and XML files and is therefore not dependent on information stored in the Business Central/NAV **Purchase Invoice** table.

The content of the search table is automatically generated whenever PDF documents are OCR-processed. This means that users can search for any text string in the original document – including serial numbers, item specifications, and terms/conditions – even though the text wasn't recognized in a field in the document journal during document registration. You can also search for part of a word or for combinations of multiple words and numbers.

## To add and process a custom document

1. Create an invoice for demonstration purposes using a word processor (such as Microsoft Word) or a different application. Make sure to add the elements you would like to recognize – such as order lines, if you want to test line recognition.
2. When you’re done creating the invoice, save it as PDF or print to a PDF file.
3. In the Role Center in Business Central, under **Continia Document Capture Activities**, select **Submit Document**.
4. In the dialog box that opens, select the email address by the document category you would like to send your PDF invoice to. E.g.: Purchase Invoices and Credit Memos.
5. A draft is created in your default email application. Attach your PDF invoice to the draft and send it.
6. In the Role Center in Business Central, under **Continia Document Capture Activities**, select **Import Files** when the value in the **Ready to Import** cue changes to indicate that a new file is available.
7. Select the **Ready to Register** cue to open the document journal. If you have imported documents from two or more different categories, selecting **Ready to Register** brings you to the **Document Categories** page. From there, select the code of the desired category. E.g.: **PURCHASE**.
8. In the document journal, select your document and start working with it.
