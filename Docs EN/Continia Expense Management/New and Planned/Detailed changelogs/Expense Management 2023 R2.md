---
title: Detailed Changelog for Continia Expense Management 2023 R2
date: 18-09-2025
description:  
id: EM-181
lang: en
---
# Detailed changelog for Continia Expense Management 2023 R2
This article lists all new features and bug fixes for each version of Continia Expense Management 2023 R2.

> [!TIP]
> As a Continia partner, you can be notified of new Expense Management versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005316840-Receive-a-notification-upon-new-Expense-Management-releases) in the Continia PartnerZone (only available to partners).

## Expense Management 2024 R1 Service Pack 4

*Release date: January 31, 2025*  
*App version: 12.4.0*  
*Fob version: 12.04*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | Id |
| --- | --- |  --- |
| General Application|<span>The following events were updated on Page 6086402 &quot;CEM Client Addin - Settlement&quot;:</span><ul><li><span><span>Added Event Publisher&nbsp;</span><span><span>OnHandleXmlCommandOnActiveRecordChanged</span>.</span></span> </li><li><span><span>Added Event Publisher&nbsp;<span>OnLoadImageFromRecIDOnAfterSetRecRef.</span></span></span> </li><li><span><span>Added Event Publisher&nbsp;<span>OnLoadImageFromRecIDOnAfterFilterAttachment.</span></span></span> </li> </ul> |58788|
| Mileages|<span>(For Danish localization) When the 60-day rule is enabled, an error comment now generates if both the </span><b>From Home</b><span>&nbsp;and </span><b>To Home</b><span>&nbsp;fields are selected simultaneously. This ensures that only valid mileage data is processed and helps maintain accurate records.</span>  |61287|
| Mileages|(For Danish localization) To bring more clarity to calculating the 60-day rule, the <b>60-Day Rule Day Count</b> and <b>60-Day Rule Destination</b> fields have been added to the mileage list.<br> <ul><li>The <b>60-Day Rule Day Count</b> field provides a technical counter of how many days, in the past year, the employee has traveled to the same destination. </li><li>The <b>60-Day Rule Destination</b> field displays the address text of the first found destination. This value can be used for address lookups or filtering on similar destinations. For example, if the destination is a construction site spanning across two streets, it would be challenging for a bookkeeper to see the correlation between the addresses. With the newly added <b>60-Day Rule Destination</b> field, it is easy to filter on that address and see all related mileage entries.* </li> </ul> |61550|
| Mileages|<span>(For Danish localization) When the 60-day rule is enabled, you can now see a warning comment if neither the </span><strong>From Home</strong><span> nor </span><strong>To Home</strong><span> checkboxes are ticked but there is a clear correlation to a previously used home address within the default range of 300 meters.</span> |62432|
| Mileages|(For Danish localization) When the 60-day rule is enabled, you can now see a warning comment when GPS coordinates are missing on a mileage. <br>GPS coordinates are used to calculate the proximity to a destination address and perform checks around the home address. Lacking GPS coordinates affects the calculation of the 60-day rule, causing the calculation to fall back on identifying similar destination addresses based solely on the address text. |62433|
| Mileages|<span>(For Danish localization) When the 60-day rule is enabled, you can now see a warning comment if a mileage has either&nbsp;<strong>From Home</strong>&nbsp;or&nbsp;<strong>To Home</strong>&nbsp;specified but the home address is outside the 300 meter range when comparing it with the previously used address.</span> |62467|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | Id |
| --- | --- |  --- |
| Document Approval|Users with a CEM-APPROVE permission set assigned to them no longer receive the following error when trying to add an attachment to an Expense Document in the Continia Web Approval Portal: <ul><li><em>You do not have the following permissions on TableData CEM Attachment: Modify.</em></li></ul> |62512|
| Expenses|Allocations containing personal items will now be included when creating an invoice for a business vendor. Previously, personal items were excluded from business invoices. However, they are now classified as company expenses and will be reflected in the purchase document. |52886|
| General Application|The reimbursement dialog displayed an incorrect user count under certain conditions. This has been resolved. |55288|
| General Application|When using the <b>CEM Tax Report</b>, the <b>Settlement No.</b> filter on the request page was not respected. |58767|
| General Application|When an expense report was reimbursed, it triggered a notification in the Expense App for each sub-document. This has now been resolved so there is only one notification sent for the whole document. |59145|
| General Application|When upgrading a company where a <b>Digital Sign Attachments</b> is enabled, without having a <b>Company Code</b> specified in the <b>Continia Company Setup</b>, the following error would show: <ul><li><span>&quot;The remote party closed the WebSocket connection without completing the close handshake.&quot;</span> </li></ul>This has now been resolved.  |62215|

## Expense Management 2023 R2 Service Pack 3
*Release date: July 1, 2024*  
*App version: 12.3.0*  
*FOB version: 12.03.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|When the <b>Card No.</b><span><span>&nbsp;</span>is blank on transactions imported as .csv file through <b>Transaction template tool,</b> users will get an error when trying to&nbsp;</span><b>Approve and Transfer.&nbsp;</b> |54141|
| Document Approval|A new event was added in Codeunit CEM Approvals Mgt.: <ul><li><span>OnAfterInitializeApprovalEntry.</span><br> </li></ul>The event publisher will provide opportunity to modify Approval Entry and the ApprovalAmounts, which are used for limit checks. <font color="#2f3941" face="system-ui, -apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Oxygen-Sans, Ubuntu, Cantarell, Helvetica Neue, Arial, sans-serif">This will be added in version 12.03, 24.01 and onwards.&nbsp;</font>  |54466|
| Expenses|The field&nbsp;<b>Matched to Bank Transaction</b>&nbsp;has been added&nbsp;<span>on Posted Expense List and Card pages.</span> |53354|
| General Application|Event Publisher has been added to Codeunit&nbsp;CEM Mileage Inbox-Transfer:<br> <ul><li>OnAfterMileageInboxTransfer </li> </ul> Event Publisher has been added to Codeunit&nbsp;CEM Settlement Inbox-Transfer:<br> <ul><li>OnAfterExpHeaderInboxTransfer </li> </ul> Event Publisher has been added to Codeunit&nbsp;CEM Per Diem Inb.-Transfer:<br> <ul><li>OnAfterPerDiemInboxTransfer </li> </ul>|55180|
| General Application|A new Event Publisher has been introduced in Codeunit&nbsp;6086373&nbsp;&quot;CEM Proxy Response Handling&quot; that allows setting show/hide parameter for the confirmation dialog when deleting Continia User Setup record: <ul><li>OnBeforeConfirmOnDeleteUserSetup. </li> </ul> |55619|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Document Approval|Approvers are now able to modify Expense Allocations when Expense is part of an Expense Report in Pending Approval Status. |54255|
| Expenses|When updating the foreign currency on an allocated expense, the <b>Amount (LCY)</b> would have not been recalculated. |55645|
| General Application|The RTC Client would have crashed if the first attachment file was not available. The issue was introduced in the version 12.01. |52792|
| General Application|The&nbsp;<b>Expense Management</b>&nbsp;<b>Status Report </b> kept failing when the <b>Corporate Language</b>&nbsp;was&nbsp;<b>ESP</b>. |54225|
| General Application|When having multiple attachments, only the first attachment was presented in the Roletailored Client. |54392|
| General Application|When posting expenses in foreign currencies where the <b>Amount Rounding Precision</b> allows more decimals than the local currency and&nbsp;<b>Post in Expense Currency</b><span><span>&nbsp;</span>was enabled. T</span>he following error message was stopping the process.&nbsp; <ul><li><span><em>Amount (LCY) &lt;Amount&gt; needs to be rounded in Gen. Journal Line Journal Template Name='',Journal Batch Name='',Line No.='0'.</em></span> </li></ul> |54691|
| General Application|When adding filters on a <b>Field Type</b>, in the <b>No. Of Source Table Filters</b>, the calculated <b>No. of Lookup Values</b> was not updated. The issue was only visually not updated. |55300|
| General Application|When automatically sending for approval expense reports, the process would only have been tried once after which it was abandoned, leaving extra work for the system administrators. The functionality now retries sending for approval every synchronization. |55597|
| Mileages|When calculating mileage over a certain <b>Starting Distance</b>, the lower rate was not applied. Instead the next year rate was picked up, if this was specified. |55306|

## Expense Management 2023 R2 Service Pack 2, Hotfix 1
*Release date: April 9, 2024*  
*App version: 12.2.1*  
*FOB version: 12.02.01*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Mileages|In the Spanish localization, when posting a mileage, the <b>Bill-to/Pay-to No.</b> was not respected resulting in a posting error. |54427|

## Expense Management 2023 R2 Service Pack 2
*Release date: March 7, 2024*  
*App version: 12.2.0*  
*FOB version: 12.02.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|With the introduction of Enforced Digital Vouchers in BC23.2, attaching documentation as incoming documents, prior to posting purchase document and journals, will in certain localizations become mandatory.<br>When using Expense Management in an environment where Enforced Digital Vouchers is configured to check for attached files prior to posting, Expense Management will transfer the underlying digital vouchers to the posted documents.<br> <span>When posting an <b>Expense</b>, the digital voucher will be enforced and the expense cannot be posted without providing an attachment which becomes the digital voucher.</span> <span>When posting </span><b>Mileage</b><span> and </span><b>Per Diem</b><span>,</span><b>&nbsp;</b><span>a tax report extract will be generated. This serves as a digital voucher for these documents.</span><br>How to enable the feature:<br> <span><p><span lang=EN-GB></span> </p><ul><li><span lang=EN-GB>All versions prior to BC23.2: The feature can be enabled in Expense Management Setup.</span> </li><li><span>BC23.2 and newer: The feature will be automatically enabled if “Digital Voucher Setup” and “Digital Voucher Entry Setup” is configured to check for attachments prior to posting.</span> </li><li>Specifically for Denmark: When using BC23.2 or newer, and the environment is a production environment in Cloud, the Digital Voucher functionality is forcedly enabled from July 1<sup>st</sup><span><span>&nbsp;</span>2024. Consequentially Expense Management will automatically create Digital Vouchers from that date and onwards.</span> </li> </ul></span> |50995|
| General Application|<b>Posting Date</b> has been added to expenses and mileages.  |50039|
| General Application|In the Web Approval Portal, when&nbsp;<span>when attempting to modify fields<span>&nbsp;</span></span><b>Job No.</b><span><span>&nbsp;</span>or<span>&nbsp;</span></span><b>Job Task No.</b> on then Expense Allocation line, the following error would have stopped the user <ul><li><em>&quot;Field JobTaskNoDesc is readonly!&quot;/&quot;Field JobNoDesc is readonly!&quot;</em> </li></ul> |52552|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|<span>When importing transactions with the </span><b>Transaction Template </b> it will no longer be possible to transfer data to the <b>Transaction Import Journal </b><span>unless a </span><b>Bank Code</b><span> is specified. The Bank Code is anyway necessary and will be reinforced later in the process, anyway.</span> |51874|
| Credit Card Transactions|When importing transactions via the Transaction Import Journal, and a field value was longer than 250 characters, it would fail with the error below. <ul><li><span><em>The length of string is X, but it must be less or equal to 250 characters. Value: ...</em></span> </li> </ul>  |52139|
| Expenses|When documents were approved due to <b>Company Policy</b> or <b>Purchase Contracts</b>, the Secure Archive log for approval was not created. |50434|
| Expenses|To prevent mismatches between the currency of expenses and their associated allocations, changing the Currency Code on an expense is no longer possible once allocations exist. This update ensures financial accuracy by maintaining consistent currency across expense entries and their allocations. |51136|
| Expenses|There is a new enhancement with the Enable Amount Distribution&nbsp;feature set and the Distribute by tax amount&nbsp;property enabled in the Distribution Code of the Expense Type<span>. The <b>Amount Including Tax</b>&nbsp;field on the expense and its allocations now automatically updates, calculating and reflecting the corresponding tax values.&nbsp;</span>  |51932|
| Expenses|<span>When a <b>Distribution Code</b> is applied to an Expense Type, and subsequently</span><span>, the </span><b>Expense Type</b> is cleared from the expense, a new dialogue feature has been implemented. This dialog will prompt users to confirm whether they want to remove the automatically allocated lines that were added based on the <b>Distribution Code</b><span>. This ensures greater control and accuracy in expense allocation processes.</span> |52037|
| Expenses|A negative expense would be created as a Purchase Invoice instead of a Credit Memo when a Preferable Purchase Invoice was set up. |52434|
| Expenses|Users with <b>Can Edit Approved Documents</b> enabled can now change the <b>VAT Amount</b> value on the Expense Card page when Expense has the status&nbsp;<b>Pending Approval</b>&nbsp;or <b>Released</b>. |52514|
| Expenses|The following Expense Comment&nbsp;now references the correct duplicate Expense Entry No.: <ul><li><em>A similar expense was found with the same date and amount. Please double check the expense entry number [Entry No.].</em> </li> </ul> |52582|
| Expenses|Posting a Purchase Credit Memo for the business Vendor number (Vendor No. on the expense) would not trigger the automatic payment that had to be applied to that document. |52803|
| Expenses|<span>When using the<span>&nbsp;</span></span><b>Vendor No.<span>&nbsp;</span></b><span>(business vendor)</span><b>&nbsp;</b><span>field on expenses, while having a<span>&nbsp;</span><b>Payment Type</b><span>&nbsp;</span>with a<span>&nbsp;</span><b>Vendor</b>&nbsp;(bank account), the following error would have been raised, if the <b>Continia User</b>&nbsp;did not have a <b>Vendor No.&nbsp;</b>specified<b>. </b>The error has been replaced by a more meaningful one.</span><br> We have fixed the following error when posting a Bank Purchase Invoice (a payment type posting on a Vendor).&nbsp; <ul><li><span><em>Document No. must have a value in Purchase Line: Document Type=Quote, Document No.=, Line No.=&lt;LineNo&gt;. It cannot be zero or empty.</em></span> </li> </ul> |52821|
| Expenses|<span>When an expense was marked as non-refundable (personal) and it involved the </span><b>Vendor No</b><span>. (business vendor) field, along with a </span><b>Payment Type</b><span> linked to a </span><b>Vendor</b> (bank account), a credit memo was issued to the business vendor. It was not correct to decide the document type based on the <b>No Refund </b>field on the expense, the document type should have always been <b>Invoice </b>for a positive expense and <b>Cr. Memo</b> for negative expenses. <span>Furthermore, the&nbsp;</span><span>creation of a business vendor document is skipped if the expense is non-refundable and the <b>Payment Type</b> posting Method is <b>Post on the Expense User Account.</b></span> |52859|
| Expenses|When navigating to <b>Find Entries</b> from a <b>Purch. Cr. Memo</b> generated by Expense Management, the expense was not shown in the <b>Related Entries</b>. |52878|
| Expenses|When a negative allocated Expense with <b>Vendor Invoice No.&nbsp;</b>was posted, multiple Purchase Credit Memos were created for each of the allocation lines instead of adding multiple allocation lines to the existing Purchase Credit Memo. |52887|
| Expenses|The field <b>Payment Type</b> is now visible on the Posted Expense Card page. |52921|
| Expenses|When downloading expense allocations with <b>Billable </b>set to <b>True, </b>the <b>Job Line Type </b>was not marked as <b>Billable.&nbsp;</b> |52938|
| General Application|On a <b>Payment Type</b>&nbsp;when <b>Matched to Expense</b> was set to <b>Never Required, </b>the fields related to the matching (variance, etc.) were not cleared of their values, this resulted in an error later in the process. |50326|
| General Application| On matched expenses, when the bank account currency code would have been different from the local currency (and the exchange rate was not available from the bank), currency differences would accumulate in the <b>Intermediate Account</b> because the posting date on the transaction would be different than the one on the expense. <b>Posting Date</b> was added on the expense. The posting date will be inherited from the bank transaction but available for editing for a user with the setting <b>Can edit approved documents.</b> |51752|
| General Application|When paying a cash expense the expense user was not receiving a push notification on his mobile app about the status change.  |51823|
| General Application|When running the Tax Report the user name was incorrectly shown. |51871|
| General Application|Since version 12.1 it was not possible to export users having the same email address in the <b>E-mail</b> and <b>O365 Authentication Email</b> field. The functionality has now been reverted so that the email address can be overwritten both for authentication and email communication.|52159|
| General Application|When running the <b>Tax Report</b>, the date filters were not respected. |52234|
| General Application|We have added the missing Lessor Integration objects (.fob) for Business Central April 2019 (BCv14) on the release package.  |52298|
| General Application|When changing the Document Date on a cash expense, the following error message was showing. <ul><li><em>Status must be Open or Pending Expense User in...</em> </li> </ul> |52328|
| General Application|The value of Attendees Inbox table field Name is now being trimmed to 50 characters during Continia Online Synchronization to prevent the error: <ul><li><em>The length of string is [length], but it must be less than or equal to 50 characters. Value: [Value].</em> </li> </ul> |52593|
| General Application|<span>When using the </span><b>Vendor No. </b><span>(business vendor)</span><b>&nbsp;</b><span>field on expenses, while having a <b>Payment Type</b> with a <b>Vendor</b> (bank account), an automatic payment was intended to happen when the invoice was posted. Instead, the error below would occur, while the invoice would have succeeded to post. <span><ul><li><em>There is no Vendor Ledger Entry within the filter.&nbsp;<span>Filters: Vendor No.: &lt;VendorNo&gt;, Document Type: ' ', Document No.: &lt;DocumentNo&gt;, Open: Yes</span></em> </li> </ul> </span> |52835|
| Mileages|When enabling <b>60-day-Rule, </b>addresses without geo-coordinates (but with the same address text) would have not been taken into the consideration. |53195|
| Per Diem|When using the <b>3-months-rule</b> and <b>Multiple Destination</b>&nbsp;was enabled on <b>Per Diem, </b>the system would prevent posting if the Address Code was not consistently specified.&nbsp; |51933|

## Expense Management 2023 R2 Service Pack 1, Hotfix 3
*Release date: February 7, 2024*  
*App version: 12.1.3*  
*FOB version: 12.01.03*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|Configuring an approval sharing record to send the approval status email to &quot;Both Approvers&quot; would in certain situations add the wrong recipient as CC to the email. The functionality has been disabled in this version of Expense Management. <span><br></span> <span>Existing approval sharing setup records configured to send the email to&nbsp;<span>&quot;Both Approvers&quot; will be treated the same way as records configured to send to &quot;Only Shared To User&quot;. The system will display an error message if the user attempts to configure an a<span>pproval sharing setup record to&nbsp;<span>send the approval status email to &quot;Both Approvers&quot;.</span></span></span></span> |53175|

## Expense Management 2023 R2 Service Pack 1, Hotfix 2
*Release date: January 24, 2024*  
*App version: 12.1.2*  
*FOB version: 12.01.02*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|The field <b>Tax Liable </b>has been added to&nbsp;expenses to control Canada's tax calculations. Tax Liable is set by default when both <b>Tax Group Code</b> and <b>Tax Area</b> are specified. |52421|
| Expenses|On an allocated expense, when the <b>Amount LCY </b>decimal places were to be rounded because the total wouldn't fit 100%, in special conditions, this expense could not be posted because of CONSISTENT error: <ul><li><em><span>The transaction cannot be completed because it will cause&nbsp;</span><span>inconsistencies in the G/L Entry table. Check where and how the&nbsp;</span><span><font><span>CONSISTENT function used in the </span></font></span><span>transaction</span><span><font><span>&nbsp;to find the&nbsp;</span></font></span><span>reason for the error.</span></em> </li> </ul> |52588|
| General Application|When enabling the digital signing of documents, the functionality was too restrictive with attachment types that could not be signed anyway. For example, .eml attachments would have prevented the posting of that expense. The functionality is changed for checks only on relevant document types. (.png, .jpg, .pdf). |52304|


## Expense Management 2023 R2 Service Pack 1, Hotfix 1
*Release date: December 21, 2023*  
*App version: 12.1.1*  
*FOB version: 12.01.01*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Document Approval|When a user accesses the Continia Web Approval Portal without using Document Capture, they encounter the following error:<br> <ul><li><em>This function requires the following module to be activated: Continia Document Capture, Document Approval.</em> </li> </ul> |52074|
| General Application|When using the VAT/Tax amount fields, <b>Expense Template Name </b>and&nbsp;<b>Expense Batch Name </b>becomes mandatory for posting, but the fields were not visible. The following error would have occurred at posting time. <br> <blockquote><span>&quot;The Gen. Journal Batch does not exist. Identification fields and values: Journal Template Name='',Name=''&quot;.</span> </blockquote>|51878|
| General Application|When using <b>Post on multiple document numbers, </b> in certain conditions the documents were grouped under the same document number, which was not the intention of the functionality. |51994|
| General Application|The 'Export Users' action on the Continia User Setup list was not visible if both Document Capture and Expense Management were installed, and no Web Portal had been configured. |52077|
| Per Diem|Fixed an issue with the per diem amount when the calculation became taxable because of the german&nbsp;<span>3-month-rule</span>. |52011|

## Expense Management 2023 R2 Service Pack 1
*Release date: December 15, 2023*  
*App version: 12.1.0*  
*FOB version: 12.01.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|In the Belgian localization, an option to post an expense report by using multiple document numbers has been introduced. This is to ease the payment processing and is especially helpful for the EB Payment Journal. The functionality can be enabled in Expense Management Setup on the Expense Report tab: Post on multiple document numbers. |46157|
| Expenses|Expense Management now supports distribution codes, giving the possibility to automatically allocate expenses based on predefined rules on the expense types. The distribution codes can be added on the expense types and automatic allocations will be triggered when the document is sent for approval.&nbsp; In the Australian localization, the distribution codes can also allocate based on the GST percentage, once the AMOUNT INCLIDING TAX field is used. The allocation will also happen if the user changes expense types on the documents. |50042|
| Expenses|An EventPublisher &quot;OnBeforeValidateAttachments&quot; has been added in Codeunit 6086321"CEM Expense-Validate&quot; to allow bypassing our standard Expense Attachments validation. |51117|
| General Application|The following events were updated in Codeunit&nbsp;6086338&nbsp;&quot;CEM Settlement-Post&quot;: <ul><li><span>Added Event Publisher </span><span>OnAfterExpensePostGenJnlLine2.</span> </li><li><span>Obsoleted&nbsp;</span><span>Event Publisher</span><span>&nbsp;<span>OnAfterExpensePostGenJnlLine (redundant).</span></span> </li><li><span>Obsoleted&nbsp;</span><span>Event Publisher</span><span>&nbsp;<span>OnBeforeExpensePostGenJnlLine</span><span><span><span>&nbsp;</span>(redundant).</span></span></span> </li> </ul>  |49134|
| General Application|&quot;Updated By Delegation User&quot; was changed to &quot;Submitted By Delegated User&quot;. |50295|
| General Application|"Submitted By Delegated User&quot; is added to Expense Report. |50297|
| General Application|The following procedures on&nbsp;<span>Page 6086402 "CEM Client Addin - Settlement" are now available for external access: <ul><li>ClearImage </li><li>LoadImageFromRecID </li> </ul> |50553|
| Per Diem|When users travel to the same destination for more than 3 months, the rate will be set to taxable in Per Diem. This is known as the &quot;3 months&quot; in Germany, and it's only available in this localization. The setting can be enabled from the Expense Management setup page under the Per Diem tab. This functionality relies on the <b>Address Code</b>&nbsp;to do the calculations. |46291|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|When <b>Payment Type</b><span><span>&nbsp;</span>was set to Selectable = No, </span>the action <b>Match or Create Expenses&nbsp;</b>on&nbsp;<b>Bank Transactions,&nbsp;</b>was not visible.&nbsp; |46193|
| Credit Card Transactions|In rare circumstances, as when multiple synchronizations were running at the same time from different sessions, it would create two similar Bank Transaction entries with the same Transaction ID. |50244|
| Credit Card Transactions|When importing transactions via the Transaction Import Journal, the Currency Code on the Bank Transaction will be set to empty if it matches the local currency of the company.   |50454|
| Credit Card Transactions|Importing Bank Transactions via Transaction Import Journal now correctly imports numerical (e.g. 840) Currency Code column value. |51550|
| Document Approval|When sending the approval mail for the sharing users, the mail was only sent to the first user. |47819|
| Expenses|When splitting an expense into multiple, the attachment file hash check would have failed even though the original file was not altered. |49995|
| Expenses|Secure Archive did not log when documents were automatically approved based on limits set with Company policies or purchase contracts set to auto approval. |50434|
| General Application|Bank Transactions were not able to be matched with Expenses in the status &quot;Pending Approval&quot; as it was causing an error for Users without &quot;Can edit approved documents&quot; enabled. |27365|
| General Application|On Expense Reports the attachment add-in was not showing properly when selecting a per diem. |49988|
| General Application|Expense Management (CA) is enabled to work in OnPrem installation. |49994|
| General Application|Fixed a bug where Outbox Notification entries are stuck in the Inbox in an error state but without an Error Text. |50030|
| General Application|An issue causing an error when running&nbsp;<span>Report&nbsp;6086314&nbsp;&quot;CEM Batch Post Settlements&quot; via Job Queue has been fixed.&nbsp;</span> |50488|
| General Application|Editing is re-enabled for the field &quot;Status&quot; of the following records (if other conditions are met).&nbsp; These were made non-editable unintentionally in version 12.0.0 <ul><li>&quot;CEM Expense Inbox&quot; </li><li>&quot;CEM Settlement Inbox&quot; </li><li>&quot;CEM Mileage Inbox&quot; </li><li>&quot;CEM Per Diem Inbox&quot; </li> </ul>  |50636|
| General Application|<span>When VAT is specified on the </span><b>Payment Type</b> balancing account, the error below will prevent posting the matched expense, when it should have prevented posting the bank transaction. The check is moved to the bank transaction posting checks. <ol><li><span><em>VAT % must be 0 on Bal. Account No. should only be checked for Expenses w/o Bank Trans.</em></span> </li> </ol> |50807|
| General Application|&quot;Configurable&quot; field is available in the Comments page when it is opened from Settlement subdocuments (via Line -&gt; Comments). |50845|
| General Application|Fixed an issue with the CEM-ALL permission set related to the secure archive feature. |51208|
| General Application|When integrating with Payment Management via the Continia Connectivity App, grouping payment suggestions would result in duplicated document entry numbers. |51386|
| General Application|Attempting to rotate a .jpeg file attachment no longer results in an error. |51409|
| Mileages|When synchronizing with Continia Online, a mileage recalculation is automatically triggered in all the companies for all the mileage rates available in the company and for all the mileages with status not posted. Because of the calculation on each mileage rate, the same mileage was recalculated multiple times, and this was causing performance issues. |41445|
| Mileages|The Mileage fields &quot;From Home&quot; and &quot;To Home&quot; can now be added to the Mileage subpage on Expense Report Card via page personalization. |50489|
| Mileages|When posting a mileage on a purchase invoice, the posting would fail if the "Mileage Tax&quot; or &quot;Mileage Fuel&quot; account code was longer than 10 symbols. |50641|
| Mileages|The system went into a stage of a never-ending loop, if the date on&nbsp;<b>Starting Distance,&nbsp;</b>to calculate a lower rate than the main rate, was different from the date on the main rate.&nbsp; |51566|
| Per Diem|After modifying a Per Diem that had the status &quot;Pending Expense User&quot;, attempting to modify Per Diem Details would cause multiple errors. |31295|
| Per Diem|When using Taxable Per Diem rates the calculations was not calculated correctly.&nbsp; |51399|
| Purchase Contracts|The relation was not removed when clearing the <b>Purchase Contract Line No. </b>value on the expense. |47828|
| Purchase Contracts|Previously, when submitting an expense with the purchase contract, which matches all the conditions for auto-approval, the expense was not released. Now, the expense is successfully released based on the purchase contract. |50436|
| Purchase Contracts|Previously, the 'Purchase Contract Missing' comment was not added for the expense with allocations, when one of the allocations has the Expense Type with the Purchase Contract set as Mandatory. |51464|

## Expense Management 2023 R2, Hotfix 2
*Release date: November 17, 2023*  
*App version: 12.0.2*  
*FOB version: 12.00.02*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Mileages|When synchronizing with Continia Online, a mileage recalculation is automatically triggered in all the companies for all the mileage rates available in the company and for all the mileages with status not posted. Because of the calculation on each mileage rate, the same mileage was recalculated multiple times, and this was causing performance issues. |41445|

## Expense Management 2023 R2, Hotfix 1
*Release date: November 8, 2023*  
*App version: 12.0.1*  
*FOB version: 12.00.01*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|In rare circumstances, as when multiple synchronizations were running at the same time from different sessions, it would create two similar Bank Transaction entries with the same Transaction ID. |50244|
| General Application|Editing is re-enabled for the field &quot;Status&quot; of the following records (if other conditions are met).&nbsp; These were made non-editable unintentionally in version 12.0.0 <ul><li>&quot;CEM Expense Inbox&quot; </li><li>&quot;CEM Settlement Inbox&quot; </li><li>&quot;CEM Mileage Inbox&quot; </li><li>&quot;CEM Per Diem Inbox&quot; </li> </ul>  |50636|
| Mileages|When posting a mileage on a purchase invoice, the posting would fail if the &quot;Mileage Tax&quot; or &quot;Mileage Fuel&quot; account code was longer than 10 symbols. |50641|

## Expense Management 2023 R2
*Release date: October 2, 2023*  
*App version: 12.0.0*  
*FOB version: 12.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses| The expense user has the ability to edit the VAT Amount. This VAT Amount is utilized during the posting process and is incorporated into VAT differences when the General Ledger Setup includes this feature. <br> In the Expense Portal and Mobile App, this functionality is enhanced by the inclusion of Optical Character Recognition (OCR) technology for reading the VAT Amount. Additionally, whenever feasible, the Expense Portal and Mobile App functions automatically allocate expenses based on various VAT percentages. You must configure the &quot;VAT AMOUNT&quot; field to take advantage of this functionality.<br>Within the Expense Management CA app, similar functionality is available, replacing the automatic allocation of expenses based on Tax Areas. As sales tax amounts are now present, there is no longer a need for automatic expense allocation. This eliminates the requirement for specific expense types such as GST/HST and streamlines the process of posting to GL Accounts using General Journal posting. It also eliminates synchronization delays and resolves the limitation associated with &quot;Expense/Capitalize. |46817|
| Expenses|When using the configuration file, new Expense Types, special Field Types with lookup functionality for airports and harbors based on Google Maps, as well as functionality for recording data related to carbon footprint calculations, have been added. <br>When you set up Expense Management in a new system, the configuration package will include multiple Expense Types that can be used for recording carbon footprints. Additionally, Configured Fields and Field Dependencies have been adapted to make it easy to get started recording carbon footprint-related data. |48377|
| Expenses|Field dependencies are imported and exported with the assisted setup wizard. |49110|
| General Application|The field &quot;Submit Date/Time&quot; is added to all documents. The field is hidden by default and can be set to show by adding it through <b>Personalized</b>. |39602|
| General Application|Introducing the new CEM Image Quality (6086520) page, which offers users the ability to customize image size and quality settings. This feature provides the ability to override default values for Picture Size and Picture Quality, providing greater control. |45546|
| General Application|Fields &quot;Matching tolerance Amount (%)&quot; and &quot;Matching tolerance Date (Days)&quot; will be used in the future&nbsp;<span>in our Expense Management Mobile App,&nbsp;</span><span>when matching Expense with an existing receipt.</span> |45650|
| General Application|The attachment images are automatically zoomed in to the &quot;best-fit&quot; size for the admin to avoid spending time adjusting zoom for every attachment.&nbsp; |46689|
| General Application|Support for multiple levels of parent-child field relations, similar to Job and Tasks. |47388|
| General Application|The Configurable Messages module is added, which allows control over the validation comments. In this module comments can be configured to have the type Information, Warning or Error. |47591|
| General Application|The &quot;General Journals&quot; action is removed from the Expense Management Role Center, as legacy views will no longer be supported in Business Central. |48101|
| General Application|Capabilities for autofill on the field types is added. Field values can be suggested in the <b>Expense Portal</b> and <b>Expense Mobile App</b> based on the previously used values. The autofill functionality is controlled from the field types available only for Code and Option data types. The functionality is enabled by default but can be disabled for each individual <b>Field Type</b>. |48617|
| General Application|The Secure Archive in Expense Management preserves original digital documents for bookkeeping, safeguarding them from tampering or deletion. <br>These documents remain traceable within legally defined secure periods. The built-in log function tracks document processes from receipt to bookkeeping. To use the log function independently, you can enable it without Secure Archive's restrictions.|48680|
| General Application|The document logging functionality is included to enable in<span>&nbsp;</span><b>Expense Management Setup</b>. Enabling this feature will record the following changes:&nbsp; <ul><li><span>Receive: Logs the incoming documents (expenses, mileages, per diems, expense reports, creditcard transactions). The log entries are inserted as soon as records are downloaded from Continia Online or inserted.</span> </li><li>Adding/removing attachments: Logs when document attachments are added or removed on the expenses and mileage. </li><li>Discard duplicated transactions at import: Adds a log entry if a transaction is discarded due to having a duplicated ID. </li><li>Deleted: Adds a log entry when a document is deleted. </li><li>Split: Adds a log entry when an expense allocation is creating a new expense. </li><li>Merge: Adds a log entry when one or more expenses are merged into one. </li><li>Matched/Unmatched: Adds logs when expenses and transactions are matched and unmatched </li><li>Add/Remove to Expense Report: Adds logs when documents are added or removed to an Expense Report. </li><li>Approved: Adds a log entry when a document is approved. </li><li>Posted: Adds a log when documents are posted. Expense Management can post directly on a Ledger Entry, case in which the &quot;Document No.&quot; and the &quot;Ledger Entry No.&quot; is specified. In other situations, Expense Management can generate purchase invoices and credit memos based on setup. </li><li>Posted Invoice or Credit Memo updates: When Expense Management generates a purchase invoice or a credit memo, important changes on these documents are logged. </li> </ul> |49168|
| General Application|Files imported in Expense Management will get a Hash (SHA1). When Secure Archive is enabled the Hashing will help to determine if files related to a given historic posting are identical to the time of posting. <br> The Hash value is calculated when one of the following events occurs: <ul><li>Attachment download by synchronization with Continia Online </li><li>Attachment added manually in Business Central </li><li>Attachment modified using Split and Merge. </li> </ul>|49226|
| General Application|Files imported through Expense Management will be undergo conversion into a digitally signed PDF when Secure Archive is enabled. Additionally t<span>he original file will be retained.&nbsp;</span> <span><br></span> The file signature occur under the following circumstances:&nbsp; <ul><li>When the user uploads the file using the Expense Mobile App, provided that &quot;Enable Document Signing&quot; has been synchronized with Continia Online. </li><li><span>When the file is uploaded from within Business Central and &quot;Enable Document Signing&quot; is explicitly enabled.&nbsp;</span> </li> </ul> |49227|
| General Application|By enabling the Secure Archive functionality, you can establish a timeframe during which the posted purchase invoices and posted purchase credit memos are protected from deletion.    |49229|
| General Application|<span>An action to Continia Hub has been added to the home tab for the following pages:</span><br> <ul><li>Expense Management Setup </li><li>Continia User Setup </li><li>Continia User Setup Card </li><li>Default User Setup </li><li>Expense Types<br> </li><li>Company Policies<br> </li><li>Payment Type List<br> </li><li>Configured Field Types<br> </li><li>Mileage Rates<br> </li><li>Mileage Reimbursement<br> </li><li>Per Diem Rates<br> </li><li>Per Diem Reimbursement<br> </li><li>Bank Mapping Rules<br> </li> </ul>  <span>The following feature is only available in App based versions of Business Central.</span>|49491|
| Purchase Contracts|Purchase Contracts cues is added to the&nbsp;<b>Expense Management Rolecenter</b>. The cues will show when the Purchase Contract application area is enabled. This can be enabled in the Expense Management Setup. |44331|
| Purchase Contracts|When the user changes Continia User Id on an expense, which has a relation to a purchase contract, the following comment will be added for the expense: <ul><li><em><span>The p</span><span>urchase contract relation has been removed, as the new value in Continia User ID does not match with the Continia User ID on the purchase contract.</span></em> </li> </ul> |45018|
| Purchase Contracts| Actions to the Expenses and Posted Expenses pages is added: Open Purchase Contract and Create Purchase Contract. Additionally, introduced new fields to the Expenses and Posted Expenses pages: Purchase Contract, Purchase Contract No., Purchase Contract Line No., and Purchase Contract Line Amount. |46412|
| Purchase Contracts|A new field, Enable Purchase Contracts, has been added to the&nbsp;Expense Management Setup, and is used to disable or enable Purchase Contracts functionality. |47339|
| Purchase Contracts|When a new expense is linked to a purchase contract line that already has an association with a posted or open expense, a validation process is initiated to ensure that these expenses do not fall within the invoicing period specified by the related purchase contract.<br>The following comments are appended based on the circumstances:<br> If the purchase contract line is linked to an open expense within the current invoicing period of the purchase contract:<br> <ul><li><em>An open expense already exists within the current invoicing period of the purchase contract. (entry number &lt;Expense Entry Number&gt;)</em> </li> </ul> If the purchase contract line is linked to a posted expense within the current invoicing period of the purchase contract:<br> <ul><li><em>A posted expense already exists within the current invoicing period of the purchase contract. (entry number &lt;Expense Entry Number&gt;)</em> </li> </ul> If the purchase contract is associated with multiple such expenses within the current invoicing period:<br> <ul><li><span><em>Multiple expenses already exist within the current invoicing period of the purchase contract. (entry numbers: &lt;Expense Entry Numbers&gt;)</em></span> </li> </ul> <ul> </ul> <ul> </ul> <p> </p> <ul> </ul> |47347|
| Document Approval|A new option field,&nbsp;<b>Send Email To,&nbsp;</b>replacing the field<span>&nbsp;</span><b>Forward Emails,</b>&nbsp;has been implemented on the&nbsp;<b>Approval Sharing (EM)<span>&nbsp;</span></b>page<b>.&nbsp;</b><span>The following options are available:</span> <ul><li>Only Original Approver </li><li>Only Shared Approver </li><li>Both Approvers </li> </ul> <span>Selecting the<span>&nbsp;</span><b>Both Approvers</b>&nbsp;option, you ensure that&nbsp;<span>both the original approver and the substitute are notified w</span></span>hen activating the&nbsp;<b>Send Status email to Approvers<span>&nbsp;</span></b>function. |48773|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|<span>The &quot;Vendor No.&quot; on expenses is used to represent the business<span>&nbsp;</span></span><span>from<span>&nbsp;</span></span><span>where the purchase was made.&nbsp;</span>When a &quot;Vendor No.&quot; is added to an expense similar to the &quot;Vendor No.&quot; set on Continia User Setup, an error will be raised. |32586|
| Expenses|After a transaction is matched to an expense, which is completed by the expense user, the expense is sent back to the expense user unintentionally.&nbsp; |49381|
| Expenses|When downloading expenses with allocations from Continia Online, the &quot;TAX GROUP CODE&quot; value was removed when the field was not configured. |49546|
| General Application|<span>When posting an expense on an Employee, with posting groups specified, the following error would appear.</span><br> <em>Gen. Posting Type must be equal to ' ' in Gen. Journal Line: Journal Template Name=, Journal Batch Name=, Line No.=0. Current value is 'Purchase'.</em> |49922|
| Mileages|Posting negative mileage is supported when using Purchase Invoice.&nbsp;&nbsp; |49849|
| Purchase Contracts| <p><font face="Segoe UI, sans-serif"><p><span>In the past, when linking an expense to a purchase contract, no consideration was given to the Contract End Date and Start Date<b>.</b><span>&nbsp;</span>However, there have been updates:</span> </p><p><span>Now, if the Expense<span>&nbsp;</span></span><b>Document Date</b><span><span>&nbsp;</span>precedes the Purchase Contract's<span>&nbsp;</span></span><b>Start Date</b><span>, the system will generate the following error message:</span><br> </p><p><em><span>This expense is associated with a purchase contract, and therefore, the Document Date must occur after the purchase contract's start date.</span></em> </p><p><span>Conversely, if the Expense<span>&nbsp;</span></span><b>Document Date</b><span><span>&nbsp;</span>falls after the Purchase Contract's<span>&nbsp;</span></span><b>End Date</b><span>, the following error will be displayed:</span><br> </p><p><em><span>This expense is linked to a purchase contract, and as such, the Document Date must precede the purchase contract's end date.</span></em> </p><p><span>Moreover, if the Expense<span>&nbsp;</span></span><b>Document Date</b><span><span>&nbsp;</span>is earlier than the Purchase Contract Line's<span>&nbsp;</span></span><b>Start Date</b><span>, the system will provide the following error:</span><br> </p><p><em><span>This expense is associated with a purchase contract line, and consequently, the Document Date must precede the purchase contract line's start date.</span></em> </font>|47338|

