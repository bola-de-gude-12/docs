---
title: Detailed Changelog for Continia Expense Management 2024 R2
date: 18-09-2025
description:  
id: EM-260
lang: en
---
# Detailed Changelog for Continia Expense Management 2024 R2
This article lists all new features and bug fixes for each version of Continia Expense Management 2024 R2.

> [!TIP]
> As a Continia partner, you can be notified of new Expense Management versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005316840-Receive-a-notification-upon-new-Expense-Management-releases) in the Continia PartnerZone (only available to partners).

> [!IMPORTANT]
> Currently, Expense Management supports BC v14 and the three latest versions of Business Central. This will change with the release of Expense Management 2025 R1 (26.00) in April 2025. **Expense Management 2025 R1 (26.00) and all future versions from then on will only support the three latest versions of Business Central**.
> 
> **This version of Expense Management – Expense Management 2024 R2 (25.00) – will be the last version with support for Business Central April 2019 (BC v14)**.

## Expense Management 2024 R2, Service Pack 4

*Release date, online: June 27, 2025*  
*Release date, on-premises: June 27, 2025*  
*App version: 25.4.*  
*Fob version: 25.04*  

### New or changed functionality

| Functional Area | Description | ID |
| --- | --- | --- |
| General | When posting an expense report, the general ledger entries of documents will retain the original **Document Date**, but the balancing entries (like vendor or employee ledger entries) will use the expense report **Posting Date**. Previously all document dates were falling back to the **Posting Date** of the expense report.<br/>The following field is posted as the **Document Date** for each document type:<ul><li>Expense: **Document Date**</li><li>Mileage: **Registration Date**</li><li>Per Diem: **Return Date**</li></ul> | 65614 |
| Expenses | To enhance the integration between Expense Management and Document Capture, the system now automatically sends expenses for approval when the user selects <b>Process with Document Capture</b>. Additionally, expenses that have been sent to Document Capture will be automatically be posted as soon as they are approved. | 63252 |
| General Application | Procedure SetGlobalVars in report <b>CEM Status Report</b> is now available for external access. | 64982 |

### Bug fixes

| Functional Area | Description | ID |
| --- | --- | --- |
| Credit Card Transactions | Previously, when importing a bank transaction where the string value of the <b>Business Country/Region</b> field exceeded 10 characters, the system would bypass the <b>Bank/Region mapping</b> functionality and present the following error in the <b>Bank Transaction Inbox</b>: <ul><li><em>The length of the string is <length>, but it must be less than or equal to 10 characters. Value: <Business Country/Region>.</em></li></ul> | 65419 |
| Document Approval | Previously, some users encountered the following error when attempting to open the cross-company dashboard in the Continia Web Approval Portal: <ul><li><em>The Expense Management Setup does not exist. Identification fields and values: Primary Key='.'</em></li></ul> | 63853 |
| Document Approval | Previously, rejecting an approval entry in Expense Management could cause the following error to occur: <ul><li><em>Sorry, the current permissions prevented the action. (TableData 454 Approval Entry Modify: Continia Expense Management).</em></li></ul> | 64691 |
| Document Approval | The following error no longer appears when attempting to access the Continia Web Approval Portal: <ul><li><em>The length of the string is <Length>, but it must be less than or equal to 20 characters. Value: <Continia User ID><br>Page Approval Entries By Company (WS) has to close.</em></li></ul> | 64882 |
| Expenses | Expense allocations now self-correct decimal rounding differences, preventing the following error, at posting time: <ul><li><em>The transaction cannot be completed because will cause inconsistencies in the G/L Entry table. Check where and how the CONSISTENT function is used in the transaction to find the reason for the error. Contact your system administrator. Tables can be marked as inconsistent during comprehensive tasks, such as posting. This prevents data from being updated incorrectly.</em></li></ul> | 52524 |
| Expenses | Automatic allocations with <b>Distribution Codes</b> no longer add values in the <b>VAT Amount</b> field, preventing incorrect VAT calculations. This resolves the appearance of one of the following errors when trying to post an expense that had no VAT Amount specified: <ul><li><em>Allow VAT Difference must be equal to 'Yes' in Gen. Journal Batch: Journal Template Name=<TEMPLATE_NAME>, Name=EXPENSE. Current value is 'No'.</em></li><li><em>VAT % must have a value in Gen. Journal Line: <TEMPLATE_NAME>, Journal Batch Name=EXPENSE, Line No.=0. It cannot be zero or empty.</em></li></ul> | 64443 |
| Expenses | When attempting to run Expense Management Online Synchronization in Business Central, the following error would appear if a user entered a <b>Vendor Invoice No.</b> on an expense document that exceeded the 30-character limit: <ul><li><em>The length of the string is <Vendor Invoice No. Length>, but it must be less than or equal to 30 characters. Value: <Vendor Invoice No.></em></li></ul> | 64865 |
| Expenses | The <b>Expense Payment Type</b> lookup page in Business Central now correctly displays all <b>Payment Types</b> assigned to the user’s <b>Expense Group</b>. | 66136 |
| General Application | Several issues in the attachment viewer have been resolved to improve usability and accuracy when working with document attachments: <ul><li>The navigation arrows now cycle correctly through all attachments, even when reaching the last item in the sequence.</li><li>The attachment number counter now accurately reflects the current position in the list of attachments.</li><li>In expense reports, attachments from previously viewed records no longer persist when creating a new entry.</li><li>Newly added attachments are now immediately shown in the viewer without requiring a refresh or additional action.</li></ul>These fixes ensure a more consistent and intuitive attachment viewing experience across document types, especially during expense report entry. | 64013 |
| General Application | In Business Central version 25.2.x, it was briefly possible to assign a blocked dimension value to the <b>Global Dimension 1 Code</b> and <b>Global Dimension 2 Code</b> fields across all Expense Management document types. This could result in the following posting error: <ul><li><em>The field <Dimension Code> of table Gen. Journal Line contains a value (<Dimension Value>) that cannot be found in the related table (Dimension Value).</em></li></ul> | 64203 |
| General Application | The attachment viewer in expense and mileage entries now correctly displays the attachment counter when navigating between multiple documents. | 64745 |
| General Application | When attempting to post an expense with long values in the fields <b>Invoice No.</b> or <b>Vendor Invoice No.</b>, the following error would appear: <ul><li><em>The length of the string is 28, but it must be less than or equal to 20 characters. Value: <External Doc. No.></em></li></ul> | 64867 |
| General Application | One of the following errors could occur when attempting to directly or indirectly modify Expense Management documents that had never been synchronized with <b>Continia Online</b>, in a company where Expense Management was not activated: <ul><li><em>Excessive recursion has been detected in event subscriber function RunModify...</em></li><li><em>There is insufficient memory to execute this function. This can be caused by recursive function calls.</em></li></ul> | 66286 |
| Mileages | The configurable comment <em>The applied rate is more than a year old.</em> in mileage entries has been updated: <ul><li>The <b>Comment Type</b> has been changed from <em>Information</em> to <em>Warning</em> to draw greater attention to outdated mileage rates.</li></ul>The comment now also triggers when a mileage entry is dated exactly one year after the <b>Start Date</b> of the last configured <b>Mileage Rate</b>. | 65527 |
| Per Diem | The Per Diem taxable amount was not calculated correctly when a fixed amount was assigned to meals. | 64432 |



## Expense Management 2024 R2, Service Pack 3, Hotfix 1

*Release date, online: May 22, 2025*  
*App version: 25.3.1*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions| The following error would previously occur when the <b>Business Name</b> field on a bank transaction exceeded 100 characters: <ul><li><em>The length of string is &lt;Bank Transaction Business Name field string length&gt;, but it must be less than or equal to 100. Value: &lt;Bank Transaction Business Name field string value&gt;</em> </li> </ul> |66319|
| Credit Card Transactions|Duplicate transactions are now properly detected, even when currency mapping is applied. |66338|
| Expenses|An expense that was automatically allocated due to company policies, and later modified manually by the expense user, would previously generate the following error message in the <b>Expense Inbox</b> when attempting to synchronize the updates: <ul><li><em>Expense &lt;Entry No.&gt; cannot be updated as there are one or more unprocessed lines in the Expense Inbox. Please process the related lines in the Expense Inbox before making changes to this Expense.</em> </li> </ul> |66481|
| Mileages|A mileage subject to company policies that refund up to a limit would previously result in the following error when posting:   <ul><li><em>Mileage Taxable Account must have a value in Mileage: &lt;Entry No.&gt;. It cannot be zero or empty.</em> </li> </ul> |66333|



## Expense Management 2024 R2, Service Pack 3

*Release date, online: May 14, 2025*  
*Release date, on-premises: May 14, 2025*  
*App version: 25.3.0*  
*FOB version: 25.3.0*  

Only released in Business Central online.

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|This version includes no deliveries and is a technical release only. |66453|



## Expense Management 2024 R2, Service Pack 2, Hotfix 3

*Release date, online: March 31, 2025*  
*App version: 25.2.3*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|When attempting to post an expense with long values in the fields <b>Invoice No.</b> or <strong>Vendor Invoice No.</strong>, the following error would appear: <ul><li><em>The length of the string is 28, but it must be less than or equal to 20 characters. Value: &lt;External Doc. No.&gt; </em></li> </ul> |64867|



## Expense Management 2024 R2, Service Pack 2, Hotfix 2

*Release date, online: March 27, 2025*  
*App version: 25.2.2*  

Only released in Business Central online.
### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|Procedure SetGlobalVars in report <b>CEM Status Report </b>has been made available for external access. |64982|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Document Approval|Rejecting an Expense Management approval entry would previously cause the following error to occur: <ul><li><em>Sorry, the current permissions prevented the action. (TableData 454 Approval Entry Modify: Continia Expense Management).</em></li></ul> |64691|
| Expenses|When attempting to run Expense Management Online Synchronization in Business Central, the following error would appear if a user entered a <strong>Vendor Invoice No.</strong> on an expense document that exceeded the 30-character limit: <ul><li><em>The length of the string is &lt;Vendor Invoice No. Length&gt;, but it must be less than or equal to 30 characters. Value: &lt;Vendor Invoice No.&gt; </em></li> </ul> |64865|



## Expense Management 2024 R1, Service Pack 2, Hotfix 1

*Release date, online: March 21, 2025*  
*App version: 25.2.1*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Document Approval|The following error no longer appears when attempting to access the <strong>Continia Web Approval Portal</strong>: <ul><li><em>The length of the string is &lt;Length&gt;, but it must be less than or equal to 20 characters. Value: &lt;Continia User ID&gt;<br>Page Approval Entries By Company (WS) has to close.</em> </li></ul> |64882|
| Expenses| Automatic allocations with<span>&nbsp;</span><b>Distribution Codes</b><span>&nbsp;</span>no longer add values in the<span>&nbsp;</span><b>VAT Amount</b><span>&nbsp;</span>field, preventing incorrect VAT calculations. This resolves the appearance of one of the following errors when trying to post an expense that had no VAT Amount specified:<ul><li><em>Allow VAT Difference must be equal to 'Yes' &nbsp;in Gen. Journal Batch: Journal Template Name=&lt;TEMPLATE_NAME&gt;, Name=EXPENSE. Current value is 'No'.&quot;</em></li><li><em>VAT% must have a value in Gen. Journal Line:<span>&nbsp;</span><span>&lt;TEMPLATE_NAME&gt;,</span><span>&nbsp;</span>Journal Batch Name=EXPENSE, Line No.=0. It cannot be zero or empty.</em></li></ul> |64443|



## Expense Management 2024 R2 Service Pack 2

*Release date, online: March 12, 2025*  
*Release date, on-premises: March 12, 2025*  
*App version: 25.2.0*  
*FOB version: 25.02*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Document Approval|Users can now click the <b>Approval By</b> field in <b>Expense Report </b> card and list pages to open the approval entries page for the document, similar to other Expense Management document types. |46382|
| Expenses|The <b>Invoice No.</b><span> is transferred to the </span><b>External Document No.</b><span> when posting, together with information about the expense document number. The </span><b>Invoice No.</b> is captured by the AI Receipt Scanner. In the Spanish localization, the field <b>Vendor Invoice No.</b> can be configured for expense user input, for similar purposes. In this case, the <b>Vendor Invoice No.</b> value will be transferred to the <b>External Document No.</b> |59773|
| Expenses|The following event has been added to R<span>eport</span><span>&nbsp;</span><span>CEM Export Attachments:</span> <ul><li><em>OnExportAttachmentsOnCreateFileName</em></li></ul> |61796|
| Expenses|The <b>Post in Expense Currency</b> feature now ensures that expenses for users associated with an <b>Employee</b>, where the <b>Currency Code</b> is specified, are posted in their respective currencies—consistent with the behavior for users associated with a vendor. |62142|
| General Application|Users can now select which documents to post using the <b>Post Batch</b> functionality on Expense Management document list pages. This applies to all Expense Management document types. |45456|
| General Application|When running <b>Run GDPR Maintenance</b> in <b>Expense Management Setup</b> to delete old documents, the associated <b>Document Log</b> entries are now also removed.  |60996|
| General Application|<span>The values in the </span><b>Request Page</b> fields for batch posting reports are now retained for future use.|61937|
| General Application|The caption for the configured field &lt;DOCUMENT DATE&gt; has been changed from &quot;Registration Date&quot; to &quot;Document Date&quot;. |62651|
| General Application|<span>The following</span><span>&nbsp;</span><span>event publisher</span><span>&nbsp;</span><span>has been added to</span><span>&nbsp;</span><span>table 6086333</span><strong> </strong>CEM Exp. Posting Desc. Field<span>&nbsp;</span><span>to enable customization of the</span><span>&nbsp;</span><b>Posting Description</b><span>&nbsp;</span><span>field when posting Expense Management documents:</span> <ul><li><em>OnBeforeReplacePlaceholdersWithValues</em></li></ul> |63479|
| General Application|Missing translations have now been added.|63902|
| Mileages|In the Danish localization, when the 60-day rule is enabled, an error comment is now displayed if both the <b>From Home</b> and <b>To Home</b> fields are selected simultaneously. This ensures that only valid mileage data is processed and helps maintain accurate records.  |61287|
| Mileages|To improve clarity in the calculation of the 60-day rule in the Danish localization, the <b>60-Day Rule Day Count</b> and <b>60-Day Rule Destination</b> fields have been added to the mileage list.<br> <ul><li><b>60-Day Rule Day Count</b> provides a count of how many days, within the past year, the employee has traveled to the same destination</li><li><b>60-Day Rule Destination</b> displays the address text of the first recorded destination, which can be used for address lookups and filtering similar destinations. For example, if a construction site spans multiple streets, bookkeepers can use this field to easily filter and identify related mileage entries.</li></ul> |61550|
| Mileages|<span>The following event has been added to<span>&nbsp;</span></span><span>Table</span><span>&nbsp;</span><span>CEM Mileage Rate:</span> <ul><li>OnBeforeRecalcMilAcrossComp </li></ul>The event enables filtering of companies for which mileages will be recalculated. |61621|
| Mileages|In the Danish localization, when the 60-day rule is enabled, a warning comment now appears if neither the <b>From Home</b> nor the <b>To Home</b> checkboxes are selected, but there is a clear correlation to a previously used home address within the default range of 300 meters. |62432|
| Mileages|In the Danish localization, when the 60-day rule is enabled, a warning comment now appears if GPS coordinates are missing on a mileage. GPS coordinates are used to determine proximity to a destination address and validate home address checks. If GPS coordinates are missing, the system defaults to identifying similar destination addresses based solely on the address text, which may affect the accuracy of the 60-day rule calculation. |62433|
| Mileages|In the Danish localization, when the 60-day rule is enabled, you can now see a warning comment if a mileage has either<b>From Home</b> or <b>To Home</b> specified but the home address is outside the 300 meter range when comparing with the previously used address. |62467|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|For Sales Tax handling, a new error message has been introduced to prevent posting when sales tax amounts are specified on an expense, but the <b>G/L Account</b> does not have tax posting setup configured. |63921|
| Credit Card Transactions|When a credit card is assigned to multiple users, it's possible to manually assign the relevant Continia User by changing the value in the <b>Continia User ID</b> field in the <b>Bank Transaction Inbox</b>, then using the <b>Reprocess</b> action. This functionality was previously unintentionally removed resulting in the following error:<ul><li><em>'Card No. &lt;Card No.&gt; is used for more than one user. You must therefore manually select Continia User ID.'</em> </li> </ul> |62212|
| Document Approval|When attempting to take actions such as Approve or Reject on documents in the <b>Web Approval Portal</b>, users occasionally encountered the following error: <ul><li><em>Sorry, the current permissions prevented the action. (TableData 6086300 CEM Expense Management Setup Expense Management Setup Read: Continia Expense Management).</em></li></ul> |62456|
| Document Approval|Users with the CEM-APPROVE permission set can now attach files to an Expense Document in the Continia Web Approval Portal without receiving the following error:<ul><li><em>You do not have the following permissions on TableData CEM Attachment: Modify.</em></li></ul> |62512|
| Document Approval|Documents can no longer be sent for approval if the entire approver chain is not fully defined. Previously, this allowed users to approve their own entries when they lacked an <b>Approver ID</b><span> in </span><b>Continia User Setup</b><span> and had an </span><b>Approval Limit</b><span> higher than the document amount.</span> |63106|
| Document Approval|<b>Expense Management</b> Approval Entries for multi-level approvers now update correctly when the first approver rejects the request. Instead of remaining in <b>Created</b> status, all related Approval Entries for the document will now be set to <b>Rejected</b>.|63846|
| Expenses|Personal item allocations are now included when creating an invoice for a business vendor. Previously, personal items were excluded from business invoices, but they are now classified as company expenses and will be reflected in the purchase document. |52886|
| Expenses|Expenses can now be posted without errors when the <b>Reimbursement Method</b> is set to <b>External Payroll System</b> and the <b>Continia User</b> does not have an <b>Employee</b> or <b>Vendor No.</b> specified. Previously, the following error occurred:<ul><li><em>Vendor No. or Employee No. must be specified on the user &lt;Continia User ID&gt; before posting a document.</em></li></ul> |62744|
| Expenses|The <b>Expense Amount Distribution</b> feature now correctly assigns <b>Dimensions</b> to automatically created <b>Expense Allocation lines</b>. |63544|
| General Application|The following configurable message was added to the <b>Configurable Messages</b> list, making it possible for users to set the <b>User Defined Comment Type</b> before the it's first occurrence. <ul><li>&quot;If you want to link your purchase invoice to an existing invoice, use the %1 field.&quot; </li></ul> |49154|
| General Application|Creating a new <b>Expense Posting Setup</b> record for an <b>Expense Type</b> no longer results in the following error: <ul><li><em>The Expense Type does not exist. Identification fields and values: Code=''.</em></li></ul> |61620|
| General Application|<span><span><span>Delegated administrator</span></span></span><span> users can now run <b>CEM Online Synchronization</b> without encountering the following error:<ul><li><em>You are not authorized to create or execute scheduled tasks.</em></li></ul> |61632|
| General Application|Importing the <b>Expense Management</b> configuration file now works as expected. Previously, the process was blocked by the following error:<ul><li><em>The Field Type &lt;Field Code&gt; is expected to have lookup values. Please check the configuration of the field.</em></li> </ul>|62056|
| General Application|The <b>Mileage Details</b> page in the <b>Mileage Reimbursement</b> process now correctly displays the field captions for <b>Global Dimension 1 Code</b> and <b>Global Dimension 2 Code</b>. |62071|
| General Application|Upgrading a company where <b>Digital Sign Attachments</b> is enabled now requires a <b>Company Code</b> in <b>Continia Company Setup</b> to prevent the following error:<ul><li><em>&quot;The remote party closed the WebSocket connection without completing the close handshake.&quot;</em></li></ul>  |62215|
| General Application|Expenses with an invoice attachment no longer remain stuck in the <b>Expense Inbox</b> when using <b>Document Capture</b> and <b>Expense Management</b>. Previously, the following error occurred: <ul><li><em>The length of the string is 253, but it must be less than or equal to 250 characters. Value: This is a purchase document. You can apply an already existing document in Applied Purchase Document Number. You can also create a Document Capture document using Process With Document Capture. But yo...</em></li></ul> |62402|
| Mileages|The <b>Expense App</b> now sends push notifications when <b>Mileages</b>, <b>Per Diems</b>, and <b>Expense Reports</b> are approved. |62401|
| Mileages|<span>Disabling the </span><b>Mileage Attachment</b> toggle in <b>Expense Management Setup</b> will remove the attachment requirement in the <b>Expense Portal</b> and <b>Expense App</b>. Previously, <b>Mileage Attachments</b> remained mandatory despite being disabled in the setup. |62438|



## Expense Management 2024 R2 Service Pack 1, Hotfix 4

*Release date, online: January 9, 2025*  
*App version: 25.1.4*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| General Application                                       | When using Document Capture and Expense Management, expenses with an invoice attachment would have occasionally remained in the Expense Inbox with the following error: <ul><li>The length of the string is 253, but it must be less than or equal to 250 characters. Value: This is a purchase document. You can apply an already existing document in Applied Purchase Document Number. You can also create a Document Capture document using Process With Document Capture.</li></ul> | 62402 |



## Expense Management 2024 R2 Service Pack 1, Hotfix 3

*Release date, online: December 20, 2024*  
*App version: 25.1.3*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Document Approval                                         | The following error will no longer appear when trying to access the Continia Web Approval Portal: <ul><li>The length of the string is &lt;Length&gt;, but it must be less than or equal to 20 characters. Value: &lt;Continia User ID&gt;<br>Page Approval Entries By Company (WS) has to close.</li></ul> | 61730 |



## Expense Management 2024 R2 Service Pack 1, Hotfix 2

*Release date, online: December 19, 2024*  
*App version: 25.1.2*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Credit Card Transactions                                  | When a credit card is assigned to multiple users, it&nbsp;<span>is possible to manually assign the relevant Continia User by changing the value in&nbsp; the&nbsp;<b>Continia User ID&nbsp;</b>field in&nbsp;<b>Bank Transaction Inbox </b>and&nbsp;<span>then using the <b>Reprocess</b> action.&nbsp;</span></span><span>This functionality was unintentionally removed resulting in the following error:</span> <ul><li>'Card No. &lt;Card No.&gt; is used for more than one user. You must therefore manually select Continia User ID.'</li></ul> | 62212 |
| General Application                                       | When upgrading a company where <b>Digital Sign Attachments</b> is enabled, but without having a <b>Company Code</b> specified in the <b>Continia Company Setup</b>, the following error would have been shown: <ul><li>"The remote party closed the WebSocket connection without completing the close handshake."</li></ul> | 62215 |



## Expense Management 2024 R2 Service Pack 1, Hotfix 1

*Release date, online: December 11, 2024*  
*App version: 25.1.1*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| General Application                                       | When importing the Expense Management configuration file, the following error would have been preventing the user to succeed:<ul><li><em>The Field Type \<Field Code\> is expected to have lookup values. Please check the configuration of the field.</em></li></ul> | 62056 |
| General Application                                       | The Mileage Details page in the Mileage Reimbursement process now displays accurate field captions for &quot;Global Dimension 1 Code&quot; and &quot;Global Dimension 2 Code.&quot; | 62071 |



## Expense Management 2024 R2 Service Pack 1

*Release date, online: December 6, 2024*  
*Release date, on-premises: December 6, 2024*  
*App version: 25.1.0*  
*FOB version: 25.01*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|<span>In the Canadian localization, functionality has been enhanced to support multiple tax jurisdictions of the same type (e.g., PST1 and PST2). The Tax Amount is now distributed proportionally based on the respective tax percentages for each tax entry. Previously, this setup would have resulted in an error. This improvement is particularly useful for expenses that are capitalized.</span> |60308|
| Document Approval| <span>In the Business Central client, when a document is rejected and sent back to the previous approver, the system will prompt the user to provide a comment.</span> |60596|
| Document Approval|<span>Event Publisher has been added to Codeunit&nbsp;CEM Approval Management:</span><ul><li><em>OnBeforeGetNextApprover</em> </li></ul> |61006|
| Expenses|Deleting a document from the <b>Documents for Import</b> queue in Document Capture will clear the <b>Applied Document No.</b> field on the linked expense. If the expense has already been posted, the expense will be reopened as well. |59523|
| Expenses|Expenses can now be sent to Document Capture, even if the attachment is not a PDF file. |59779|
| Expenses|It is now possible to specify the Volume Unit on the Expense Management Setup page. The Volume Unit, along with the Distance Unit, will be used in various areas. |60178|
| Expenses|When <b>Applied Purch. Doc No.</b> is manually updated, <b>Process with Document Capture </b>will not longer send the document for OCR processing because a document is already applied. |60651|
| Expenses|Invoice documents associated with an expense report cannot be processed with Document Capture. The document must be detached first. |61240|
| General Application|When running the data maintenance job, users will now see an overview of the data scheduled for deletion. Additionally, the date intervals have been aligned with those in Document Capture. |54571|
| General Application|A new field <b>Posted Document No.</b> has been added to the <b>Posted Expense Report </b>card, and list pages. It shows the <b>Document No.</b> of the ledger entries created during Expense Report posting. The field is visible when <b>Post on multiple document numbers</b> is disabled on <b>Expense Management Setup</b> page. |59765|
| General Application|Global dimension fields have been added to the following pages:&nbsp;<span><b>CEM Per Diem Reimbursement Details,&nbsp;</b></span><span><b>CEM Expense Details</b>,&nbsp;</span><span><b>CEM Mileage Details</b></span> |59766|
| General Application|<span>Rejecting a document in Document Capture will clear the <b>Applied Document No.</b> on a linked expense. If the expense has already been posted, it will also be reopened.</span> |59914|
| General Application|The <b>Transaction Description</b> field for expenses, which previously displayed the merchant's name only when an expense was created from a bank transaction, has been updated. Merchant names will also be captured via OCR from the expense portal or app. To enhance clarity, the <b>Transaction Description</b> field has been replaced with a new <b>Merchant</b> field, which is automatically populated by OCR and bank transactions. |60637|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Document Approval|The hyperlink in the Expense Management Approval Status email now leads the user to settlements approval view on the Web Approval Portal page if <b>Expense Report</b>&nbsp;is set to <b>Mandatory</b> in Expense<span>&nbsp;Management Setup.</span> |61197|
| Expenses|In the Expense Management Role Center, individual document cues (expense, mileage, per diem) are displayed as long as there is an open document, even when the Expense Report is set as mandatory.  |61243|
| Expenses|<span>It is no longer allowed to change </span><b>Applied Purchase Document Type</b><span> and </span><b>Applied Purchase Document No</b><span>. when the document has already been sent to&nbsp;</span><span>Document Capture</span><span>.</span> |61333|
| General Application|When posting expenses, mileage or per diems as separate documents, ledger entries will retain the original <b>Document Date</b>. Previously this date was falling back to the <b>Posting Date</b>. |58912|
| General Application|When downloading an update to an existing Per Diem or Expense, the Posting Date was previously reset, overwriting the original value. |60597|
| General Application|Applying a <b>Fixed Filter</b> on the <b>Field Type Source Table</b> with a length exceeding 100 characters would previously result in the following error: <ul><li><em>The length of the string is &lt;filter length&gt;, but it must be less than or equal to 100 characters. Value: &lt;filter value></em></li></ul> |61230|
| General Application|The fields <span><b>Description</b> and <b>Autofill</b>&nbsp;on field types are no longer reset to default during the daily synchronizations.</span> |61359|
| Per Diem|Users can now deactivate the <b>3-Month Rule</b> when using the German language by selecting the blank option in the Expense Management Setup. |57621|
| Per Diem|On the <b>Expense Management Status Report</b>, the grand total amount was incorrectly calculated. |60203|



## Expense Management 2024 R2, Hotfix 3

*Release date: November 27, 2024*  
*App version: 25.0.3*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Document Approval                                         | The following error will no longer appear when trying to access the Continia Web Approval Portal: <ul><li>The length of the string is &lt;Length&gt;, but it must be less than or equal to 20 characters. Value: &lt;Continia User ID&gt;<br/>Page Approval Entries By Company (WS) has to close.</li></ul> | 61730 |



## Expense Management 2024 R2, Hotfix 2

*Release date: November 12, 2024*  
*App version: 25.0.2*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application |In earlier versions of Business Central, upgrading from on-premises to cloud could unintentionally run the upgrade process more than once, leading to data inconsistencies. The current solution now includes a check on the Expense Management Data Version during upgrades which ensures the system only runs the necessary upgrade steps once. |61089|



## Expense Management 2024 R2, Hotfix 1

*Release date: October 28, 2024*  
*App version: 25.0.1*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|In the Canadian localization, when generating purchase invoices for allocated expenses, the line amount was incorrectly set to the total amount instead of the allocated amount. |60280|
| Country and Regional|General i<span>mprovements and issue resolutions for handling Canadian Sales Tax.</span> |60321|



## Expense Management 2024 R2

*Release date, online: October 1, 2024*  
*Release date, on-premises: October 21, 2024*  
*App version: 25.0.0*  
*Fob version: 25.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|When the <b>Card No.</b><span><span>&nbsp;</span>is blank on transactions imported as .csv file through <b>Transaction template tool,</b> users will get an error when trying to&nbsp;</span><b>Approve and Transfer.&nbsp;</b> |54141|
| Document Approval|When using the standard page <b>Requests to Approve</b>, the Expense Management workflow was creating inconsistencies and differences compare to when the same actions were taken from the <b>Approval Entries (EM)</b> page. <span>Rejecting Expense Management documents from within the standard </span><b>Requests to Approve</b><span> page would have left the approval document in status </span><b>Pending Approval</b><span>, while the approval entry would have actually been rejected.&nbsp;</span> <span>Approving from the same page would have not sent a release notification to the expense user.</span> |21200|
| Document Approval|A new event was added in Codeunit CEM Approvals Mgt.: <ul><li><span>OnAfterInitializeApprovalEntry.</span><br> </li></ul>The event publisher will provide opportunity to modify Approval Entry and the Approval Amounts, which are used for limit checks. This will be added in version 12.03, 24.01 and onwards.  |54466|
| Document Approval|A new cross-company dashboard has been introduced in Continia Web Approval Portal.|58048|
| Expenses|The fields <b>Payment Type</b> and <b>Expense Type</b>&nbsp;are now enforced to have a value before allocating an expense. |52911|
| Expenses|A warning will be shown in case the manually entered VAT amount does not match the calculated VAT amount on an expense. The warning is created as a configurable comment.|54777|
| Expenses|When creating a Purchase Invoice/Purchase Credit Memo during Expense posting, an existing Purchase document will no longer be re-opened if it's status is &quot;Pending Approval&quot; or &quot;Released&quot;. The system will create a new Purchase document instead. |57971|
| General Application|Expenses documents can now be sent to Document Capture for processing. In this way, the bookkeeper takes full advantage of the purchase handling capabilities in Document Capture, while the refund will be handled in Expense Management. The expense will then be posted without generating the purchase side. As soon as the purchase document is posted, Expense Management will apply a payment to that document, refunding the&nbsp;employee. Furthermore, an expense can be linked to a Document Capture document or a purchase document (purchase invoice or credit memo) directly.&nbsp; The new fields&nbsp;<b>Applied Document Type</b> and <b><span>Applied Document&nbsp;</span>Number</b> have been introduced for this purpose. The functionality is only available when cloud OCR is enabled in Document Capture. |16409|
| General Application|<span>Job queues can now be set up with ease from withing the Expense Management setup page, simplifying the administrative processes for recurring jobs.</span> Moreover, when sending emails (approval, reminder or expense status report), the functionality makes sure that there has been a recent synchronization, avoiding sending outdated information.  |53988|
| General Application|Procedure LockToSpecificDocumentNo() has been made externally available on all the relevant card pages.  |54658|
| General Application|Users can now change <b>Document Storage Type</b> in Exp. Management Setup page without having to move existing files in the storage. |54715|
| General Application| In Canada, sales tax handling has been enhanced to ensure that the specified tax amount is now posted into the Tax Ledger Entries, even when using Expense Posting via the General Journal in Expense Management. In Microsoft Business Central™, the handling of tax differences produces varying outcomes depending on whether the differences are posted through a Purchase Invoice or the General Journal. Since Expense Management typically defaults to posting via the General Journal, this can further contribute to discrepancies. To address this issue, Expense Management has been refining its posting routines. It now posts directly into the sales tax accounts and strives to replicate, as closely as possible, the results of posting through a Purchase Invoice. |54850|
| General Application|Event Publisher has been added to Codeunit&nbsp;CEM Mileage Inbox-Transfer: <ul><li>OnAfterMileageInboxTransfer </li></ul> Event Publisher has been added to Codeunit&nbsp;CEM Settlement Inbox-Transfer: <ul><li>OnAfterExpHeaderInboxTransfer </li></ul> Event Publisher has been added to Codeunit&nbsp;CEM Per Diem Inb.-Transfer: <ul><li>OnAfterPerDiemInboxTransfer </li></ul> <span><em> </em></span>|55180|
| General Application| We have enhanced the way comments are displayed in Expense Reports. Previously, comments were marked by a flag on the line item, requiring users to navigate to the comments page through the actions menu. With the latest update, the expense report level now features a summarized comment line that indicates the total number of comments, while each individual line displays the most relevant comment directly on the line item. Users can still access the full comments page by clicking on any displayed comment within the report. These improvements aim to provide a clearer and more efficient way to manage and review comments. |55275|
| General Application|A new Event Publisher has been introduced in Codeunit&nbsp;6086373&nbsp;&quot;CEM Proxy Response Handling&quot; that allows setting show/hide parameter for the confirmation dialog when deleting Continia User Setup record: <ul><li><em>OnBeforeConfirmOnDeleteUserSetup.</em> </li> </ul> |55619|
| General Application|Enhancements in the demo machines, setup configuration files and demo data have been made. |55945|
| General Application|The Payroll Integration is enhanced to collect all the requests into the <b>External Interface Queue</b> view. This insures that requests to external payroll interfaces (for example, Dataloen), are only sent when all documents are posted. The functionality enhancement ensures no duplicated calls are made to the interfaces, creating better traceability of the process. |56349|
| General Application|The following events were updated in Codeunit&nbsp;6086319 "CEM NAV-version Mgt.": <span><ul><li><span>Added Event Publisher&nbsp;</span><span>OnAfterPostGenJnlLine.</span> </li> </ul></span>|57028|
| General Application|The following events have been added in the&nbsp;<span>codeunit CEM Settlement-Post, to facilitate integration with other payroll systems.</span>&nbsp; <ul><li><span>OnAfterTransferExpense</span> </li><li><span>OnAfterTransferMileage</span> </li><li><span>OnAfterTransferPerDiem</span> </li> </ul> |57039|
| General Application|The fields <b>Employee No.</b> and <b>Vendor No.</b>&nbsp;have been added to the following pages for easier sorting and filtering. The fields are hidden by default. <ul><li>6086315 &quot;CEM Expense Reimburse Matrix" </li><li>6086322 &quot;CEM Mileage Reimburse Matrix"</li><li>6086454 &quot;CEM Per Diem Reimburse Matrix&quot; </li> </ul> |57604|
| General Application|The following events were added in order to allow adding custom fields and functionality in the export to Excel functionality, on the reimbursement pages.<br>Codeunit <span>CEM Export Expense Reimb. (</span>6086565)<ul><li><span><span>OnAfterCreateRowWithColumnsCaptions</span></span> </li><li><span><span><span>OnAfterCreateDataSheetLine</span></span></span> </li> </ul> Codeunit CEM Export Mileage Reimb. (6086566)<ul><li><span><span>OnAfterCreateRowWithColumnsCaptions</span></span> </li><li><span><span><span>OnAfterCreateDataSheetLine</span></span></span> </li> </ul> Codeunit Export Per Diem Reimb. (6086567)<ul><li><span><span>OnAfterCreateRowWithColumnsCaptions</span></span> </li><li><span><span><span>OnAfterCreateDataSheetLine</span></span></span> </li></ul> |57813|
| General Application|The following event was added in order to allow additional posting before the preview stops the process and before the COMMIT.<br>Codeunit CEM Settlement-Post (6086338)<ul><li><span>OnAfterPostExpenseReportOnBeforeStopPreview</span><span>.</span> </li></ul> |57955|
| General Application|<span>Event Publisher has been added to Codeunit&nbsp;CEM Approval Functions (WS):</span><br><ul><li>OnBeforeForwardApprovalEntryWS </li></ul>  |58646|
| General Application|<span>The following events were updated on Page 6086402 &quot;CEM Client Addin - Settlement&quot;:</span><ul><li><span><span>Added Event Publisher&nbsp;</span><span><span>OnHandleXmlCommandOnActiveRecordChanged</span>.</span></span> </li><li><span><span>Added Event Publisher&nbsp;<span>OnLoadImageFromRecIDOnAfterSetRecRef.</span></span></span> </li><li><span><span>Added Event Publisher&nbsp;<span>OnLoadImageFromRecIDOnAfterFilterAttachment.</span></span></span> </li></ul> |58788|
| General Application |Administrators can now view detailed information about the types of  sign-in being used by users, including Microsoft 365 and other  authentication methods. They can upgrade the authentication method. As a result, the welcome mail is also tailored to the users'  authentication method. |27051|
| Mileages|Attachments requirements on mileage can now be setup, similar to the existing functionality for expenses. Furthermore, the settings will be reflected in the Expense App and Portal. Similar to expenses, the mileage attachments can be: Recommended, Mandatory and Optional. The attachment requirement can be setup on a company level, in Expense Management setup, when the Vehicle field is not configured. When the Vehicle field is configured, the attachment options can be set individually on each vehicle. The customers that currently use fuel rates, where attachments are currently enforced in Business Central will be upgraded to have attachment mandatory.|45583|
| Per Diem|Enhanced control over the defaulting of per diem allowances. It is now possible to specify on each allowance type whether is should be Disabled (no allowances by default) or Enabled (allowances by default). |55204|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|When setting&nbsp;<b>Enable</b>&nbsp;<b>Multiple Users per Card, </b>the <b>Bank Account No.</b> was not being set on the transactions, impacting the reconciliation. |54229|
| Document Approval| When forwarding approval entries, the system previously did not consider the approval limits of the approvers. This allowed approval entries to be sent to approvers with lower approval limits. The functionality has now been enhanced to ensure that a user with sufficient approval permissions is always included in the approver chain.<br>To support this improvement, workflow responses have been redesigned, and workflow template upgrades are required. If you are using extensions, the upgrade process will automatically disable the old workflows and recreate them based on the updated workflow templates. However, for FOB-based versions, this step must be completed manually as part of the upgrade process. Detailed instructions for this step can be found in the relevant upgrade articles, which you will need to follow anyway as part of the upgrade routines.<br>Note that after the upgrade, any existing documents in a Pending Approval status will continue to follow the previous workflow behavior. This is because such documents will remain tied to the old workflows until they are either fully approved or rejected. To transition these documents to the new workflows, simply reopen the document and resubmit it for approval. |13674|
| Expenses|When posting expenses with Expense Posting Preferable Purchase Invoice, in some situations the Unit Cost was calculated wrongly. |53212|
| Expenses|When using amount distribution codes on the expense types, in an North American localization, the allocation lines were not created.&nbsp; |57285|
| Expenses|When creating an expense allocation, the default dimensions were inserted on the first line. The functionality is not changes so that the dimensions are copied from the main expense. Default dimensions will be triggered when changing relevant values on the allocation. |58995|
| General Application|When calculating lookup values for field types during the synchronization, only the configured fields will be recalculated. That is to improve performance by not doing un-necessary calculations during the synchronization. |54837|
| General Application|When using the <b>CEM Tax Report</b>, the <b>Settlement No.</b> filter on the request page was not respected. |58767|
| Per Diem|In the Expense Management Setup, under the <b>Per Diem</b> fast tab, the allowance for accommodation can be activated or deactivated. When deactivated, all <b>Accommodation Allowance Codes</b>&nbsp;will be removed from the <b>Per Diem Posting Groups</b>. This will avoid the following error:<ul><li>Expense Management Setup does not allow Accommodation Allowance Code to be used on Per Diem Posting Group '&lt;PostingGroup&gt;' </li></ul> |55804|