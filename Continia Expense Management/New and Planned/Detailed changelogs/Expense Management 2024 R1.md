---
title: Detailed Changelog for Continia Expense Management 2024 R1
date: 11-07-2025
description:  
id: EM-217
lang: en
---
# Detailed Changelog for Continia Expense Management 2024 R1
This article lists all new features and bug fixes for each version of Continia Expense Management 2024 R1.

> [!TIP]
> As a Continia partner, you can be notified of new Expense Management versions and service packs whenever they're released. To sign up for this service, go to the [notifications page](https://continia.zendesk.com/hc/en-us/articles/360005316840-Receive-a-notification-upon-new-Expense-Management-releases) for Expense Management in the Continia PartnerZone (only available to partners).

> [!IMPORTANT]
> Currently, Expense Management supports BC v14 and the three latest versions of Business Central. This will change with the release of Expense Management 2025 R1 (26.00) in April, 2025. **Expense Management 2025 R1 (26.00) and all future versions from then on will only support the three latest versions of Business Central**.
> 
> **The next version of Expense Management – Expense Management 2024 R2 (25.00) – will be the last version with support for Business Central April 2019 (BC v14)**.

## Expense Management 2024 R1 Service Pack 4, Hotfix 0

*Release date online: June 27, 2025*  
*Release date, on-premises: June 27, 2025*  
*App version: 24.4*  
*Fob version: 24.04*  


### New or changed functionality

| Functional Area | Description | ID |
| --- | --- | --- |
| General | When posting an expense report, the general ledger entries of documents will retain the original **Document Date**, but the balancing entries (like vendor or employee ledger entries) will use the expense report **Posting Date**. Previously all document dates were falling back to the **Posting Date** of the expense report.<br>The following field is posted as the **Document Date** for each document type:<ul><li>Expense: **Document Date**</li><li>Mileage: **Registration Date**</li><li>Per Diem: **Return Date**</li></ul> | 65614 |
| Expenses | The <b>Post in Expense Currency</b> feature now ensures that expenses for users associated with an <b>Employee</b>, where the <b>Currency Code</b> is specified, are posted in their respective currencies—consistent with the behavior for users associated with a <b>Vendor</b>. This improvement ensures consistency in currency handling across different user types. | 62142 |
| Mileages | Expense: **Document Date** Mileage: **Registration Date** Per Diem: **Return Date**To improve clarity in the calculation of the 60-day rule in the Danish localization, the **60-Day Rule Day Count** and **60-Day Rule Destination** fields have been added to the mileage list.<ul><li><b>60-Day Rule Day Count</b> provides a count of how many days, within the past year, the employee has traveled to the same destination</li><li> <b>60-Day Rule Destination</b> displays the address text of the first recorded destination, which can be used for address lookups and filtering similar destinations. For example, if a construction site spans multiple streets, bookkeepers can use this field to easily filter and identify related mileage entries.</li></ul> | 61550 |
| Mileages | In the Danish localization, when the 60-day rule is enabled, a warning comment now appears if neither the <b>From Home</b> nor <b>To Home</b> checkboxes are selected, but there is a clear correlation to a previously used home address within the default range of 300 meters. | 62432 |
| Mileages | In the Danish localization, when the 60-day rule is enabled, a warning comment now appears if GPS coordinates are missing on a mileage.<br>GPS coordinates are used to the determine proximity to a destination address and validate home address checks. If GPS coordinates are missing, the system defaults to identifying similar destination addresses based solely on the address text, which may affect the accuracy of the 60-day rule calculation. | 62433 |
| Mileages | In the Danish localization, when the 60-day rule is enabled, you can now see a warning comment if a mileage has either <b>From Home</b> or <b>To Home</b> specified but the home address is outside the 300 meter range when compared to the previously used address. | 62467 |

### Bug fixes

| Functional Area | Description | ID |
| --- | --- | --- |
| Document Approval | Users with the CEM-APPROVE permission set can now attach files to an Expense Document in the Continia Web Approval Portal without receiving the following error:<ul><li><em>You do not have the following permissions on TableData CEM Attachment: Modify.</em></li></ul> | 62512 |
| Expenses | Expense allocations now self-correct decimal rounding differences, preventing the following error, at posting time:<ul><li><em> The transaction cannot be completed because will cause inconsistencies in the G/L Entry table. Check where and how the CONSISTENT function is used in the transaction to find the reason for the error. Contact your system administrator. Tables can be marked as inconsistent during comprehensive tasks, such as posting. This prevents data from being updated incorrectly.</em></li></ul> | 52524 |
| Expenses | Automatic allocations with **Distribution Codes** no longer add values in the **VAT Amount** field, preventing incorrect VAT calculations. This resolves the following the appearance of one of the following errors when trying to post an expense that had no VAT Amount specified:<ul><li><em> Allow VAT Difference must be equal to 'Yes' in Gen. Journal Batch: Journal Template Name=&lt;TEMPLATE_NAME&gt;, Name=EXPENSE. Current value is 'No'.</em></li><li><em>VAT % must have a value in Gen. Journal Line: &lt;TEMPLATE_NAME&gt;, Journal Batch Name=EXPENSE, Line No.=0. It cannot be zero or empty.</em></li></ul> | 64443 |
| General Application | One of the following errors could occur when attempting to directly or indirectly modify Expense Management documents that had never been synchronized with **Continia Online**, in a company where Expense Management was not activated: <ul><li><em>Excessive recursion has been detected in event subscriber function RunModify...</em></li><li><em>There is insufficient memory to execute this function. This can be caused by recursive function calls.</em></li></ul> | 66286 |
| Per Diem | The Per Diem taxable amount was not calculated correctly when a fixed amount was assigned to meals. | 64432 |

## Expense Management 2024 R1 Service Pack 3

*Release date: January 17, 2025*  
*App version: 24.3.0*  
*Fob version: 24.03*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Document Approval                                         | <span>In the Business Central client, when a document is rejected and sent back to the previous approver, the system will prompt the user to provide a comment.</span> | 60596 |
| Document Approval                                         | <span>The following event has been added to Codeunit&nbsp;CEM Approval Management:</span> <ul><li><span>OnBeforeGetNextApprover</span> </li> </ul> | 61006 |
| Expenses                                                  | <span>The following event has been added to</span><span>&nbsp;</span>R<span>eport</span><span>&nbsp;</span><span>CEM Export Attachments:</span> <ul><li><span>OnExportAttachmentsOnCreateFileName</span> </li> </ul> | 61796 |
| General Application                                       | Event Publisher has been added to Codeunit&nbsp;CEM Approval Functions (WS):<ul><li>OnBeforeForwardApprovalEntryWS </li> </ul> | 58646 |
| General Application                                       | <span>The following events were updated on Page 6086402 &quot;CEM Client Addin - Settlement&quot;:</span><ul><li><span><span>Added Event Publisher&nbsp;</span><span><span>OnHandleXmlCommandOnActiveRecordChanged</span>.</span></span> </li><li><span><span>Added Event Publisher&nbsp;<span>OnLoadImageFromRecIDOnAfterSetRecRef.</span></span></span> </li><li><span><span>Added Event Publisher&nbsp;<span>OnLoadImageFromRecIDOnAfterFilterAttachment.</span></span></span> </li> </ul> | 58788 |
| General Application                                       | A new field <b>Posted Document No.</b> has been added to the <b>Posted Expense Report </b>card and list pages. It shows the <b>Document No.</b> of the ledger entries created during Expense Report posting. The field is visible when <b>Post on multiple document numbers</b> is disabled on <b>Expense Management Setup</b> page. | 59765 |
| General Application                                       | Global Dimension fields have been added to the following pages:&nbsp;<span><b>CEM Per Diem Reimbursement Details,&nbsp;</b></span><span><b>CEM Expense Reimbursement Details</b>,&nbsp;</span><span><b>CEM Mileage Reimbursement Details</b></span> | 59766 |
| Mileages                                                  | <span>In the Danish localization, when the 60-day rule is enabled, a</span><span>n error comment is now generated if both the </span><b>From Home</b><span>&nbsp;and </span><b>To Home</b><span>&nbsp;fields are selected simultaneously. This ensures that only valid mileage data is processed and helps maintain accurate records.</span> | 61287 |
| Mileages                                                  | <span>The following event has been added to<span>&nbsp;</span></span><span>Table</span><span>&nbsp;</span><span>CEM Mileage Rate:</span> <ul><li>OnBeforeRecalcMilAcrossComp </li> </ul>The event enables filtering of companies for which mileage will be recalculated. | 61621 |


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Document Approval                                         | The hyperlink in the Expense Management Approval Status email now leads the user to settlements approval view on the Web Approval Portal page if <b>Expense Report</b>&nbsp;is set to <b>Mandatory</b> in Expense<span>&nbsp;Management Setup.</span> | 61197 |
| Expenses                                                  | When creating an invoice for a business vendor, allocations containing personal items will now be included on the invoice. Previously, personal items were excluded from business invoices; however, as these are now classified as company expenses, they will be reflected in the purchase document. | 52886 |
| Expenses                                                  | When creating an expense allocation, the default dimensions were inserted on the first line. The functionality has not changed, so the dimensions are copied from the main expense. Default dimensions will be triggered when changing relevant values on the allocation. | 58995 |
| General Application                                       | To prevent potential errors, users are no longer allowed to perform the following actions on an Expense Report if Expense Management Continia Online Synchronization is in progress: <ul><li>Reopen. </li><li>Send to Expense User. </li><li>Send for Approval. </li><li>Force Approval. </li> </ul> | 58511 |
| General Application                                       | When using the <b>CEM Tax Report</b>, the <b>Settlement No.</b> filter on the request page was not respected. | 58767 |
| General Application                                       | When posting expenses, ,mileage or per diems as separate documents, ledger entries will retain the original <b>Document Date</b>. Previously this date was falling back to the <b>Posting Date</b>. | 58912 |
| General Application                                       | When an expense report was reimbursed, it would have triggered a notification in the Expense App for each sub-document, instead of one notification for the whole document. | 59145 |
| General Application                                       | When downloading an update to an existing Per Diem or Expense, the Posting Date was previously reset, overwriting the original value. | 60597 |
| General Application                                       | Applying a <b>Fixed Filter</b> on the <b>Field Type Source Table</b> with a length exceeding 100 characters would have previously resulted in the following error: <ul><li><span><em>The length of the string is &lt;filter length&gt;, but it must be less than or equal to 100 characters. Value: &lt;filter value&gt;</em></span> </li> </ul> | 61230 |
| General Application                                       | The fields <span><b>Description</b> and <b>Autofill</b>&nbsp;on field types are no longer reset to default during the daily synchronizations.</span> | 61359 |
| General Application                                       | The Mileage Details page in the Mileage Reimbursement process now displays accurate field captions for &quot;Global Dimension 1 Code&quot; and &quot;Global Dimension 2 Code.&quot; | 62071 |
| General Application                                       | When upgrading a company where <b>Digital Sign Attachments</b> is enabled without having a <b>Company Code</b> specified in the <b>Continia Company Setup</b>, the following error would have been shown: <ul><li><span>&quot;The remote party closed the WebSocket connection without completing the close handshake.&quot;</span> </li> </ul> | 62215 |

## Expense Management 2024 R1 Service Pack 2

*Release date: August 23, 2024*  
*App version: 24.2.0*  
*Fob version: 24.02*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|The fields <b>Payment Type</b> and <b>Expense Type</b>&nbsp;are now enforced to have a value before allocating an expense. |52911|
| General Application|A new Event Publisher has been introduced in Codeunit&nbsp;6086373&nbsp;&quot;CEM Proxy Response Handling&quot; that allows setting show/hide parameter for the confirmation dialog when deleting Continia User Setup record: <ul><li><em>OnBeforeConfirmOnDeleteUserSetup.</em> </li> </ul> |55619|
| General Application|<span>The following events were updated in Codeunit&nbsp;6086319 &quot;<span>CEM NAV-version Mgt.</span></span><span>&quot;:<br></span> <span><ul><li><span>Added Event Publisher&nbsp;</span><span>OnAfterPostGenJnlLine.</span> </li> </ul></span>|57028|
| General Application|The following events have been added in the&nbsp;<span>codeunit CEM Settlement-Post, to facilitate integration with other payroll systems.</span>&nbsp; <ul><li><span>OnAfterTransferExpense</span> </li><li><span>OnAfterTransferMileage</span> </li><li><span>OnAfterTransferPerDiem</span> </li> </ul> |57039|
| General Application|The fields <b>Employee No.</b> and <b>Vendor No.</b>&nbsp;have been added to the following pages for easier sorting and filtering. The fields are hidden by default. <ul><li>6086315 &quot;CEM Expense Reimburse Matrix&quot; </li><li>6086322 &quot;CEM Mileage Reimburse Matrix&quot; </li><li>6086454 &quot;CEM Per Diem Reimburse Matrix&quot; </li> </ul> |57604|
| General Application|The following events were added in order to allow adding custom fields and functionality in the export to Excel functionality, on the reimbursement pages. <br> <span>Codeunit <span>CEM Export Expense Reimb. (</span>6086565)</span><br> <ul><li><span><span>OnAfterCreateRowWithColumnsCaptions</span></span> </li><li><span><span><span>OnAfterCreateDataSheetLine</span></span></span> </li> </ul> <span><span><span>Codeunit<span>&nbsp;</span></span>CEM Export Mileage Reimb. (6086566)</span><br></span> <span><span><ul><li><span><span>OnAfterCreateRowWithColumnsCaptions</span></span> </li><li><span><span><span>OnAfterCreateDataSheetLine</span></span></span> </li> </ul></span></span> <span><span><span><span>Codeunit<span>&nbsp;</span></span>Export Per Diem Reimb. (6086567)<span>&nbsp;</span></span><br></span></span> <span><span><span><span><ul><li><span><span>OnAfterCreateRowWithColumnsCaptions</span></span> </li><li><span><span><span>OnAfterCreateDataSheetLine</span></span></span> </li> </ul></span></span></span></span> |57813|
| General Application|The following event was added in order to allow additional posting before the preview stops the process and before the COMMIT.&nbsp; <br> <span>C</span><span>odeunit</span><span>&nbsp;</span><span>CEM Settlement-Post (6086338)</span><br>   <ul><li><span>OnAfterPostExpenseReportOnBeforeStopPreview</span><span>.</span> </li> </ul> |57955|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|When applying payments to purchase documents created by Expense Management, the expense was not marked as reimbursed. As a result, these expenses appeared as unpaid in both the Expense App and the Expense Portal. |57878|
| General Application|<span>General enhancements in the credit card field mapping were implemented.</span> |54232|
| General Application|The reimbursement dialog displayed an incorrect user count under certain conditions. |55288|
| General Application|When approving or rejecting a document on the <b>CEM Approval Entries</b> page, if shared approval is set up, the next document highlighted will be for the same approver. Previously, the selection would always move to the next entry in line, causing issues with shared approvals by jumping to a different approver's entry. |57912|

## Expense Management 2024 R1 Service Pack 1, Hotfix 4

*Release date: July 18, 2024*  
*App version: 24.1.4*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|When importing transactions via the Transaction Import Journal, it was possible to create duplicate transactions if another parallel process was handling the same bank transaction inbox entry. |57687|
| General Application|When batch posting allocated expenses, with a posting date replacement, the following error would have prevented the posting because the balancing lines currency calculation was not adjusted to the new posting date. <ul><li><em><span>The transaction cannot be completed because it will cause&nbsp;</span><span>inconsistencies in the G/L Entry table. Check where and how the&nbsp;</span><span><font><span>CONSISTENT function used in the<span>&nbsp;</span></span></font></span><span>transaction</span><span><font><span>&nbsp;to find the&nbsp;</span></font></span><span>reason for the error.</span></em> </li> </ul> |57785|

## Expense Management 2024 R1 Service Pack 1, Hotfix 2

*Release date: June 18, 2024*  
*App version: 24.1.2*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application| When running a synchronization process, the following error would sometimes appear and it would have stopped the synchronization. The issue would be logged in the job queues or would be shown as an error to the user.&nbsp;<span>The issue is affecting all the document types.</span> <ul><li>The changes to the Expense Report Inbox record cannot be saved because some information on the page is not up-to-date. Close the page, reopen it, and try again. </li> </ul> |56842|

## Expense Management 2024 R1 Service Pack 1, Hotfix 1

*Release date: June 11, 2024*  
*App version: 24.1.1*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|In certain situations, the following error was not necessary when processing inbox entries. Removing this error will make the system correct on itself with the next synchronization. <ul><li><span>&lt;Document&gt; Inbox &lt;Entry No.&gt; needs to be processed first.&nbsp;</span>Status must be equal to 'Open' in Document: Entry No.=&lt;Entry No&gt;. Current value is 'Pending Expense User'. </li> </ul> |56536|
| General Application|When running the Expense Management Status Report, the following error would have occurred for some specific documents. The issue is that the Expense Report deletion would have not deleted the sub-expenses. The issue was introduced in version 24. <ul><li><span>The Expense Report does not exist. Identification fields and values: Document Type='Expense Report',No.=&lt;Expense Report No.&gt;.</span> </li> </ul> |56872|

## Expense Management 2024 R1 Service Pack 1

*Release date: May 29, 2024*  
*App version: 24.1.0*  
*Fob version: 24.01*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|When the <b>Card No.</b><span><span>&nbsp;</span>is blank on transactions imported as .csv file through <b>Transaction template tool,</b> users will get an error when trying to&nbsp;</span><b>Approve and Transfer.&nbsp;</b> |54141|
| Document Approval|A new event was added in Codeunit CEM Approvals Mgt.: <ul><li><span>OnAfterInitializeApprovalEntry.</span><br> </li> </ul> <span>The event publisher will provide opportunity to modify Approval Entry and the ApprovalAmounts, which are used for limit checks.</span> <font color="#2f3941" face="system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Oxygen-Sans, Ubuntu, Cantarell, Helvetica Neue, Arial, sans-serif">This will be added in version 12.03, 24.01 and onwards.&nbsp;</font>  |54466|
| General Application|Procedure LockToSpecificDocumentNo() has been made externally available on all the relevant card pages.  |54658|
| General Application|Event Publisher has been added to Codeunit&nbsp;CEM Mileage Inbox-Transfer:<br> <ul><li>OnAfterMileageInboxTransfer</li> </ul> Event Publisher has been added to Codeunit&nbsp;CEM Settlement Inbox-Transfer:<br> <ul><li>OnAfterExpHeaderInboxTransfer </li> </ul> Event Publisher has been added to Codeunit&nbsp;CEM Per Diem Inb.-Transfer:<br> <ul><li>OnAfterPerDiemInboxTransfer </li> </ul>|55180|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|When matching expenses with transactions,&nbsp;<b>Credit Card No.</b> was not copied to the expenses.&nbsp; |54577|
| Expenses|When using distribution codes based on tax calculations, a fully non-taxable receipt will create a 100% allocation for the selected non-taxable expense type. |54920|
| Expenses|When updating the foreign currency on an allocated expense, the <b>Amount (LCY)</b> would have not been recalculated. |55645|
| General Application|When adding an expense in status <b>Pending Expense User</b> that had pending updates to be downloaded to an <b>Open</b> Expense Report, the user changes were no longer synchronized to that expense.  |48682|
| General Application|The&nbsp;<b>Expense Management</b>&nbsp;<b>Status Report </b>was<b>&nbsp;</b>failing when the <b>Corporate Language</b>&nbsp;was&nbsp;<b>ESP</b>. |54225|
| General Application|When having multiple attachments, only the first attachment was presented in the Roletailored Client. |54392|
| General Application|When posting expenses in foreign currencies where the <b>Amount Rounding Precision</b> allows more decimals than the local currency and&nbsp;<b>Post in Expense Currency</b><span><span>&nbsp;</span>was enabled. T</span>he following error message was stopping the process.&nbsp; <em><ul><li><span>Amount (LCY) &lt;Amount&gt; needs to be rounded in Gen. Journal Line Journal Template Name='',Journal Batch Name='',Line No.='0'.</span></em> </li> </ul> |54691|
| General Application|When upgrading from OnPrem to Cloud, the <b>Default Table Mappings</b> was not automatically calculated for Expense Management.&nbsp; |54723|
| General Application|The&nbsp;<b>CEM Pre-Cloud Migration Wizard </b>in the departments, was not searchable.&nbsp; |54838|
| General Application|When adding filters on a <b>Field Type</b>, in the <b>No. Of Source Table Filters</b>, the calculated <b>No. of Lookup Values</b> was not updated. The issue was only visually not updated. |55300|
| General Application|When previewing an unsupported attachment type, preview message was not downloading the file. |55309|
| General Application|When trying to open an approved document from the Approval Request Entries, it was not opening the document page or giving the error below. <br><em> <ul><li>Specify a filter for the &lt;Primary Key Field&gt; in the &lt;Table Name&gt; table. </em></li> </ul> |55676|
| General Application | When trying to open an approved document from the Approval Request Entries, it was not opening the document page or giving the error below:<br><ul><li><em>Specify a filter for the &lt;Primary Key Field&gt; in the &lt;Table Name&gt; table.</em></ul></li> | 55676 |
| Mileages|In the Spanish localization, when posting mileage, the&nbsp;<b>Bill-to/Pay-to No. </b>was not specified, resulting in a posting error. |54427|
| Mileages|When calculating mileage over a certain <b>Starting Distance</b>, the lower rate was not applied. Instead the next year rate was picked up, if this was specified. |55306|

## Expense Management 2024 R1
*Release date, online: April 2, 2024*  
*Release date, on-premises: April 11, 2024*  
*App version: 24.0.0*  
*Fob version: 24.00*  

> [!NOTE]
> With its 2024 spring release, Expense Management will make a version leap from 12.00 to 24.00, meaning that versions 13.00–23.00 don't exist and never will. This was done in order to align the versioning of Expense Management with that of Microsoft Dynamics 365 Business Central.

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|In the Belgian localization, an option to post an expense report by using multiple document numbers has been introduced. This is to ease the payment processing and is especially helpful for the EB Payment Journal. The functionality can be enabled in Expense Management Setup on the Expense Report tab: <b>Post on multiple document numbers.</b> |46157|
| Country and Regional|<span>With the introduction of Enforced Digital Vouchers in BC23.2, attaching documentation as incoming documents, prior to posting purchase document and journals, will in certain localizations become mandatory.</span><br> When using Expense Management in an environment where Enforced Digital Vouchers are configured to check for attached files prior to posting, Expense Management will transfer the underlying digital vouchers to the posted documents.<br> When posting an <b>Expense</b>, the digital voucher will be enforced, and the expense cannot be posted without providing an attachment, which becomes the digital voucher. <span>When posting </span><b>Mileage</b><span> and </span><b>Per Diem</b><span>,</span><b>&nbsp;</b><span>a tax report extract will be generated. This serves as a digital voucher for these documents.</span><br>How to enable the feature:<ul><li><span lang=EN-GB>All versions prior to BC23.2: The feature can be enabled in Expense Management Setup.</span> </li><li><span>BC23.2 and newer: The feature will be automatically enabled if “Digital Voucher Setup” and “Digital Voucher Entry Setup” are configured to check for attachments prior to posting.</span> </li><li>Specifically for Denmark: When using BC23.2 or newer, and the environment is a production environment in Cloud, the Digital Voucher functionality is forcedly enabled from July 1<sup>st</sup><span><span>&nbsp;</span>2024. Consequentially Expense Management will automatically create Digital Vouchers from that date and onwards.</span> </li> </ul> |50995|
| Credit Card Transactions|When using&nbsp;<b>Enable&nbsp;Multiple User per Card</b>&nbsp;on payment types, the credit card mapping fields (specified on Expense Management Setup) were shared across multiple payment types, making it difficult to use the functionality when having multiple payment types with different mapping rules.&nbsp; The functionality is now moved on a <b>Payment Type</b> level and it makes it possible to have different fields for different payment types. |53513|
| Credit Card Transactions|Transactions posted at import are no longer marked as <b>System-Created Entry</b> in the ledgers. |53759|
| Expenses|Expense Management now supports distribution codes, giving the possibility to automatically allocate expenses based on predefined rules on the expense types. The distribution codes can be added on the expense types and automatic allocations will be triggered when the document is sent for approval.&nbsp; In the Australian localization, the distribution codes can also allocate based on the GST percentage, once the AMOUNT INCLIDING TAX field is used. The allocation will also happen if the user changes expense types on the documents. |50042|
| Expenses|An EventPublisher &quot;OnBeforeValidateAttachments&quot; has been added in Codeunit&nbsp;<span>6086321</span><span>&nbsp;</span><span>&quot;CEM Expense-Validate&quot; to allow bypassing our standard Expense Attachments validation.</span> |51117|
| Expenses|The field&nbsp;<b>Matched to Bank Transaction</b>&nbsp;has been added&nbsp;<span>on Posted Expense List and Card pages.</span> |53354|
| General Application|The following events were updated in Codeunit&nbsp;6086338&nbsp;&quot;CEM Settlement-Post&quot;: <ul><li><span>Added Event Publisher </span><span>OnAfterExpensePostGenJnlLine2.</span> </li><li><span>Obsoleted&nbsp;</span><span>Event Publisher</span><span>&nbsp;<span>OnAfterExpensePostGenJnlLine (redundant).</span></span> </li><li><span>Obsoleted&nbsp;</span><span>Event Publisher</span><span>&nbsp;<span>OnBeforeExpensePostGenJnlLine</span><span><span><span>&nbsp;</span>(redundant).</span></span></span> </li> </ul>  |49134|
| General Application|<span>A new&nbsp;</span><b>GDPR Retention Period (Years)&nbsp;</b><span>field has been added to the<span>&nbsp;</span></span><b>Expense Management Setup</b><span><span>&nbsp;</span>page, to be used with the newly introduced<span>&nbsp;</span></span><b>Run GDPR Maintenance</b><span><span>&nbsp;</span>action on the<span>&nbsp;</span></span><b>Expense Management Setup</b><span><span>&nbsp;</span>page. This action deletes all data stored in Expense Management related to the posted<span>&nbsp;</span></span><span>documents<span>&nbsp;older than</span></span><span>&nbsp;the GDPR retention period (fiscal years) specified.&nbsp;</span> |49231|
| General Application|<b>Posting Date</b><span><span>&nbsp;</span>has been added to expenses and mileages.&nbsp;</span>  |50039|
| General Application|<b>Updated By Delegation User</b> was changed to <b>Submitted By Delegated User</b>. |50295|
| General Application|<span><b>Submitted By Delegated User</b> is added to Expense Report.</span> |50297|
| General Application|The following procedures on&nbsp;<span>Page 6086402 &quot;CEM Client Addin - Settlement&quot;</span> are now available for external access: <ul><li>ClearImage </li><li>LoadImageFromRecID </li> </ul> |50553|
| General Application| The column<span>&nbsp;</span><b>User ID</b>&nbsp;has been removed from the<span>&nbsp;</span><b>Document Log Entries</b>&nbsp;and<span>&nbsp;</span><b>System Log Entries<span>&nbsp;</span></b>pages.&nbsp;<span>The change has been made to comply with GDPR legislation in certain countries, such as Germany. To adhere to bookkeeping legislation in other countries, like Denmark, the value remains accessible via<span>&nbsp;</span></span><b>Page Inspection</b><span><span>&nbsp;</span>(zoom).</span> <span>A user with sufficient permissions is still able to inspect the user ID by using the<span>&nbsp;</span><b>Page Inspection</b>&nbsp;(zoom).</span>  |52236|
| General Application|Enabling the option&nbsp;<b>Check for attachment before posting of purchase document</b>&nbsp;in the<span>&nbsp;</span><b>Expense Management Setup</b><span>&nbsp;</span>page specifies if the system should display an error message if no incoming document or Expense Management file is associated with the document at the time of posting. The check is imposed both on purchase documents and purchase journals. <br> The option only applies to on-premises environments and Business Central versions 23.1 and earlier. |52927|
| General Application | Now the user export will only run if any changes necessitate a new export, reducing unnecessary excessive exports when configured in the Job Queue. If the export is run in a database where the data for export is unchanged since the last export, the following notification will be shown:<ul><li><em>Nothing is exported, because no changes have been done since the last export.</em></ul></li> |55687|
| Per Diem|<span>When users travel to the same destination for more than 3 months, the rate will be set to taxable in Per Diem. This is known as the &quot;3-months rule&quot; in Germany, and it's only available in this localization. The setting can be enabled from the Expense Management setup page under the Per Diem tab.&nbsp;</span> <span>This functionality relies on the <b>Address Code</b>&nbsp;to do the calculations.&nbsp;</span> |46291|
| Purchase Contracts|The system analyzes posted expenses and searches for recurring expenses, 3 in a row, to find possible purchase contracts.&nbsp; The users will get a notification on the&nbsp;<b>Expense Card </b>and the&nbsp;<b>Expense List</b>&nbsp;pages if, based on the analysis results, the selected expense is recurring. There are two different notifications:&nbsp; <ul><li>Suggestion to create a new purchase contract based on the expense. </li><li>Suggest linking the expense to an existing purchase contract if a suitable purchase contract can be found in the system.&nbsp; </li> </ul> |50208|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|The error message appearing when creating Bank Transactions where <b>Bank Country/Region</b>&nbsp;field is not in the Bank Country Mapping table, has been improved.&nbsp; |41048|
| Credit Card Transactions|When using the <b>EM Bank Reconciliations</b> with multiple bank accounts, the&nbsp; <b>Balance Last Statement</b> and <b>Statement No. </b>would have been&nbsp;incorrectly calculated. |53165|
| Document Approval|<span>Approvers are now able to modify Expense Allocations when Expense is part of an Expense Report in Pending Approval Status.</span> |54255|
| General Application|Following Event Publishers have been made public/external: <ul><li>Report 6086312 &quot;CEM Batch Post Expenses&quot; &quot;OnBeforeOnOpenPage&quot; </li><li><span>Report 6086313 &quot;CEM Batch Post Mileage&quot; &quot;OnBeforeOnOpenPage&quot;</span> </li><li><span><span>Report 6086314 &quot;CEM Batch Post Settlements&quot; &quot;OnBeforeOnOpenPage&quot;</span></span> </li><li><span><span><span>Report 6086315 &quot;CEM Batch Post Per Diems&quot; &quot;OnBeforeOnOpenPage&quot;</span></span></span> </li> </ul>   |49563|
| General Application|The RTC Client would have crashed if the first attachment file was not available. The issue was introduced in the version 12.01. |52792|
| Country and Regional|In the Australian localization, when using <b>distribution codes</b> and both the&nbsp;<b>AMOUNT INCLUDING TAX</b> and the&nbsp;<b>TAX AMOUNT</b> were configured, the following error would have occurred when the system was trying to do the automatic allocation. <br> <ul><li>The tax amount entered (&lt;value 1&gt;) different from the calculated amount (&lt;value 2&gt;). </li> </ul> |53517|