---
title: Detailed Changelog for Continia Expense Management 2025 R1
date: 11-07-2025
description: See the latest hotfixes and new and changed functionality for EM 2025 R1
id: EM-302
lang: en
---
# Detailed Changelog for Continia Expense Management 2025 R1
This article lists all of the new features, changes, and bug fixes for each version of Continia Expense Management 2025 R1.

> [!TIP]
> As a Continia partner, you can be notified of new Expense Management versions and service packs whenever they're released. To sign up for this service, go to [Receive a notification](https://continia.zendesk.com/hc/en-us/articles/360005316840-Receive-a-notification-upon-new-Expense-Management-releases) in the Continia PartnerZone (only available to partners).

> [!IMPORTANT]
> Expense Management supports the three latest versions of Business Central.



## Expense Management 2025 R1, Service Pack 2, Hotfix 1

*Release date online: July 10, 2025*  
*App version: 26.2.1*  

Only released in Business Central Cloud.

### New or changed functionality

| Functional area | Description | ID |
| --- | --- | --- |
| Expenses | The following event publisher has been added to Codeunit 6086338 "CEM Settlement-Post". It provides an opportunity to adjust the VAT Amount as necessary when posting Expenses:<br>- OnPostExpenseOnBeforeValidateVATAmount | 67569 |

### Bug fixes

| Functional area | Description | ID |
| --- | --- | --- |
| Expenses | When using the Process with Document Capture functionality, processed expenses were automatically posted when the status was set to Released. However, an issue introduced in version 26.2 caused all expenses to be posted—even those that were not processed with Document Capture, such as non-invoice documents. This has now been addressed to ensure that only relevant documents are posted as intended.<br>Additionally, expenses that have created a Document Capture document and were subsequently rejected will not be posted. | 67466 |
| General Application | The order of configured fields will now only reset to default values for system fields when using the **Reset to Default Setup** action on the **Configured Fields** page.<br>Previously, the field order would reset entirely each time the page was closed. | 67043 |

## Expense Management 2025 R1, Service Pack 2, Hotfix 0

*Release date online: June 24, 2025*  
*Release date on-premises: June, 24, 2025*  
*App version: 26.2.0*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General | Expenses now include an **External Document No.** field that will be used when posting. This enhancement gives users more flexibility to choose between values provided by **OCR**, the **Applied Document No.**, or the default posting value (such as *EXPENSE 123*), depending on their preferred setup and processing flow. | 65844 |
| General | When posting an expense report, the general ledger entries of documents will retain the original **Document Date**, but the balancing entries (like vendor or employee ledger entries) will use the expense report **Posting Date**. Previously all document dates were falling back to the **Posting Date** of the expense report.<br/>The following field is posted as the **Document Date** for each document type:<ul><li>Expense: **Document Date**</li><li>Mileage: **Registration Date**</li><li>Per Diem: **Return Date**</li></ul> | 65614 |
| Per Diems | In the context of the <b>3-month rule</b> in the German localization, <b>Addresses</b> are now searchable outside of the <b>Per Diem</b> context. | 64704 |
| Document Approval|Custom filters applied on the <b>Approval Entries – Expense Management</b> page now remain active as users work with approval records. This enhancement improves usability by preserving filter context. In addition, the following procedures have been made available for external access for better extensibility and integration: <ul><li>PutOnHold, RemoveOnHold in codeunit <b>CEM Approval Management</b>.</li><li>Forward in codeunit <b>CEM Approvals Bridge</b></li></ul> |66088|
| Expenses| To enhance the integration between Expense Management and Document Capture, the system now automatically sends expenses for approval when the user selects <b>Process with Document Capture</b>. Additionally, expenses that have been sent to Document Capture will automatically be posted when they're approved. |63252|
| Expenses|When using <b>Expense Management</b> with <b>Continia Sustainability</b>, it is now mandatory to specify an <b>Emission Unit Code</b> on an expense if an <b>Emission Quantity</b> is provided. |65797|
| General Application|Procedure SetGlobalVars in&nbsp;report&nbsp;<b>CEM Status Report </b>is now available for external access. |64982|
| Per Diem|On the <b>Per Diem Rate</b> page, meal values for <b>breakfast</b>, <b>lunch</b>, and <b>dinner</b> now display dynamically based on your configuration: <ul><li>As <b>clean percentages</b>, when defined as percentages of the total allowance</li><li>In <b>local currency with decimals</b>, when using LCY values</li><li>In <b>foreign currency</b>, when applicable</li> </ul>  |65790|
| Platform and Technology|The custom FactBox pane resizing implementation has been disabled when running on <b>Business Central 26.0</b> and above, in favor of Microsoft's new native resizing feature. <br>The native implementation limits the FactBox pane width to a maximum of 50% of the screen, whereas the previous custom implementation allowed for wider expansion.|65063|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|It is now easier to process bank transactions that were initially marked as excluded from posting. When you uncheck the <b>Exclude Entry</b> field on a bank transaction, the transaction is automatically posted, ensuring that the correct G/L accounts are updated if the transaction is later matched to an expense. When the <b>Exclude Entry</b> field is unchecked manually, a confirmation dialog appears with the following message: <ul><li><em>This transaction was previously marked as excluded from posting. If you include it now, the transaction will be posted immediately. Do you want to continue?</em></li> </ul>In addition, the <b>Exclude Entry</b> field is automatically unchecked if a previously excluded transaction is manually matched from an expense. This streamlines the reconciliation process for transactions that require inclusion after initial exclusion. |62739|
| Credit Card Transactions| Previously, when importing a bank transaction where the string value of the <b>Business Country/Region</b> field exceeded 10 characters, the system would bypass the <b>Bank/Region mapping</b> functionality and present the following error in the <b>Bank Transaction Inbox</b>:<ul><li><em>The length of the string is &lt;length&gt;, but it must be less than or equal to 10 characters. Value: &lt;Business Country/Region&gt;.</em></li></ul> |65419|
| Credit Card Transactions| The following error previously occurred when the <b>Business Name</b> field on a bank transaction exceeded 100 characters: <ul><li><em>The length of string is &lt;Bank Transaction Business Name field string length&gt;, but it must be less than or equal to 100. Value: &lt;Bank Transaction Business Name field string value&gt;</em></li></ul> |66319|
| Credit Card Transactions|Duplicate transactions are now properly detected, even when currency mapping is applied. |66338|
| Document Approval|Previously, some users encountered the following error when attempting to open the cross-company dashboard in the Continia Web Approval Portal: <ul><li><em>The Expense Management Setup does not exist. Identification fields and values: Primary Key=''.</em></li> </ul> |63853|
| Document Approval|Previously, rejecting an approval entry in Expense Management could cause the following error to occur: <ul><li><em>Sorry, the current permissions prevented the action. (TableData 454 Approval Entry Modify: Continia Expense Management).</em></li> </ul> |64691|
| Document Approval|Users assigned the <b>CEM-APPROVE</b> permission set would previously encounter the following error in the <b>Web Approval Portal</b> or <b>Business Central client</b> when attempting to approve an expense matched to a bank transaction: <ul><li><em>Sorry, the current permissions prevented the action. (TableData 6086330 CEM Bank Transaction Bank Transaction Read: Continia Expense Management)</em></li></ul> |66207|
| Document Approval|Continia approver users with<b> Limit Document Visibility</b> enabled would previously encounter the following error when trying to open a document card using the <b>View</b>&nbsp;action on the&nbsp;<b>Approval Entries - Expense Management</b> page: <ul><li><em>&lt;Document Type&gt; &lt;Entry No.&gt; for &lt;User ID&gt; cannot be displayed because you only have access to your own documents.</em></li></ul> |66358|
| Document Approval|Expense Management approver users were previously unable to open the <b>Approval Entries - Expense Management</b> page due to the following permission error, which occurred when one of the documents was a matched expense created in a version prior to <b>Expense Management </b>26.0: <ul><li><em>Sorry, the current permissions prevented the action. (TableData 6086330 CEM Bank Transaction Bank Transaction Modify: Continia Expense Management)</em></li></ul> |66523|
| Document Approval|Cancelling an Expense Report approval request using the&nbsp;<b>Cancel Approval Request</b>&nbsp;action on the Expense Report card page now works as expected and changes the status of all of it's subdocuments to <b>Open</b>. |66664|
| Document Approval|Continia approver users with <b>Limit Document Visibility</b> enabled previously encountered the following error when trying to open an <b>Expense Report </b>sub-document card using the <b>View</b>&nbsp;action on <b>Expense Report</b> subpages: <ul><li><em>&lt;Document Type&gt; &lt;Entry No.&gt; for &lt;User ID&gt; cannot be displayed because you only have access to your own documents.</em></li></ul> |66965|
| Expenses|It is now mandatory to specify a <b>Payment Type</b> on an expense in order to create expense allocations using the <b>Expense Amount Distribution</b> functionality. This change ensures that allocations are created with the correct financial context and helps prevent incomplete or invalid distribution entries. |64392|
| Expenses|When using a <b>Distribution Code</b> to automatically allocate expenses, configurations with an odd number of distribution lines could result in incorrect rounding. This caused an inconsistency error when posting the expense. |64797|
| Expenses|When attempting to run Expense Management Online Synchronization in Business Central, the following error appeared if a user entered a <b>Vendor Invoice No.</b> on an expense document that exceeded the 30-character limit: <ul><li><em>The length of the string is &lt;Vendor Invoice No. Length&gt;, but it must be less than or equal to 30 characters. Value: &lt;Vendor Invoice No.&gt; </em></li></ul> |64865|
| Expenses|The default setup for the integration with Continia Sustainability has been improved for the <b>HOTEL</b>&nbsp;expense type in the Danish (DK) and United States (US) localizations. |65125|
| Expenses|It is no longer possible to configure a <b>Payment Type</b> to both:<ul><li>Submit amounts only in <b>LCY</b> (Local Currency), and</li><li>Require <b>matching</b></li></ul>These two settings are now validated as mutually exclusive, as they are incompatible by design. |65436|
| Expenses|When using a <b>Distribution Code</b> to automatically allocate expenses, the user-entered expense<b> Tax Amount</b> was previously ignored. Instead, standard tax values were calculated for the allocated lines, which could result in un-expected tax amounts being posted. |65498|
| Expenses| To ensure consistency with the <b>Expense </b>card page, the following VAT-related fields have been added to the <strong>Expenses</strong> page: <ul><li>Amount without VAT </li><li>VAT Amount (Calculated) </li><li>VAT % (hidden by default) </li> </ul> |65716|
| Expenses|The <b>Expense Payment Type</b> lookup page in Business Central now correctly displays all <b>Payment Types</b> assigned to the user’s <b>Expense Group</b>. |66136|
| Expenses|The Expense <b>Description</b> field is now automatically filled with the <b>Merchant</b> value when the <b>E-DESCRIPTION</b> configured field is not mandatory. If E-DESCRIPTION is mandatory, the <b>Description</b> field will remain empty to enforce user input.<br>The <b>Merchant</b> value is automatically inherited from the AI Receipt Scanner for cash expenses or from the transaction <b>Business Description</b> when the expense is matched. Additionally, the <b>Merchant</b> field has been added to the <b>Posted Expense Card</b> and the <b>Expense Report</b> subpage corresponding to expenses.  |66401|
| Expenses|An expense that was automatically allocated due to company policies, and later modified manually by the expense user, would previously generate the following error message in the <b>Expense Inbox</b> when attempting to synchronize the updates: <ul><li><em>Expense &lt;Entry No.&gt; cannot be updated as there are one or more unprocessed lines in the Expense Inbox. Please process the related lines in the Expense Inbox before making changes to this Expense.</em></li> </ul> |66481|
| Expenses|For expenses processed with Document Capture - when a Document Capture template was configured to&nbsp;<b>match & update order</b>, the expenses did not not link the generated purchase order document to the expense, resulting in the following:<ul><li>Expenses were automatically reopened/unposted with the comment:&nbsp;&nbsp;<em>&quot;This was reopened because the applied Document Capture Document &lt;No.&gt; was deleted&quot;</em></li><li>The following comment was added to expenses<em>:<em>&quot;The applied Document Capture Document &lt;No.&gt; was deleted&quot;</em></li></ul>|66692|
| Expenses|When <b>Expense Posting</b> is set to <b>Preferable Purchase Invoice</b>, posting an Expense now correctly creates a purchase invoice for the vendor specified on the <b>Payment Type</b>. |66933|
| General Application|Several issues in the attachment viewer have been resolved to improve usability and accuracy when working with document attachments: <ul><li>The navigation arrows now cycle correctly through all attachments, even when reaching the last item in the sequence. </li><li>The attachment number counter now accurately reflects the current position in the list of attachments. </li><li>>In expense reports, attachments from previously viewed records no longer persist when creating a new entry.</li><li>Newly added attachments are now immediately shown in the viewer without requiring a refresh or additional action.</li></ul>These fixes ensure a more consistent and intuitive attachment viewing experience across document types, especially during expense report entry.  |64013|
| General Application|In Business Central version 25.2.x, it was briefly possible to assign a blocked dimension value to the <b>Global Dimension 1 Code</b> and <b>Global Dimension 2 Code</b> fields across all Expense Management document types. This could result in the following posting error: <ul><li><em>The field &lt;Dimension Code&gt; of table Gen. Journal Line contains a value (&lt;Dimension Value&gt;) that cannot be found in the related table (Dimension Value).</em></li></ul>  |64203|
| General Application|The attachment viewer in expense and mileage entries now correctly displays the attachment counter when navigating between multiple documents.  |64745|
| General Application|When creating mileage entries, using the <b>Mileage </b>card page opened directly from an expense report, the attachment add-in would display an incorrect attachment. |64781|
| General Application|In a localized version of Business Central, the following error would have prevented users from posting expense documents where sustainability accounts were specified:<ul><li><em>The &lt;Environmental Account No.&gt; must be of type Posting.</em></li></ul> |64846|
| General Application|When attempting to post an expense with long values in the fields <b>Invoice No.</b> or <b>Vendor Invoice No.</b>, the following error would appear: <ul><li><em>The length of the string is 28, but it must be less than or equal to 20 characters. Value: &lt;External Doc. No.> </em></li></ul> |64867|
| General Application|When clearing the last expense from the <b>Expense List</b>, the viewer previously continued to display the last associated attachment, even though no expenses remained. |65543|
| General Application|Previously, when attempting to post a <b>Mileage</b> or <b>Per Diem</b> entry in a Business Central client localized for Belgium (BE), the following error occurred: <ul><li><em>Journal Template Name must have a value in Gen. Journal Line: Journal Template Name=, Journal Batch Name=, Line No.=0. It cannot be zero or empty.</em></li></ul> |65634|
| General Application|The access check for configured field dependency lookup values now correctly evaluates both the user's individual access and their group access permissions. Previously, lookup values might have been incorrectly hidden if the user lacked direct access, even when group-level access was granted. |65706|
| General Application|When attempting to upgrade to Business Central version 26, the following error would occur if the company was not activated but Expense Management documents, that have never been synchronized with Continia Online, existed. <ul><li><em>Excessive recursion has been detected in event subscriber function RunModify...</em></li></ul> |65995|
| General Application|One of the following errors could occur when attempting to directly or indirectly modify Expense Management<strong> </strong>documents that had never been synchronized with <b>Continia Online</b>, in a company where Expense Management was not activated:<ul><li><em>Excessive recursion has been detected in event subscriber function RunModify...</em></li><li><em>There is insufficient memory to execute this function. This can be caused by recursive function calls.</em> </li></ul> |66286|
| General Application|When using the <b>Find Entries</b> action on the <b>Posted Expense Reports</b> page, project ledger entries are now shown to users even when the documents have only created project ledger entries without general ledger entries (for example, when <b>Project No.</b> is specified but the <b>Reimbursement Method</b> is set to <b>External</b>). |66788|
| Mileages|The configurable comment: <em>The applied rate is more than a year old.</em> in mileage entries has been updated: <ul><li>The <b>Comment Type</b> has been changed from <em>Information</em> to <em>Warning</em> to draw greater attention to outdated mileage rates. </li><li>The comment now also triggers when a mileage entry is dated exactly one year after the <b>Start Date</b> of the last configured <b>Mileage Rate</b>.</li></ul>|65527|
| Mileages|A mileage subject to company policies that refund up to a limit would previously result in the following error when posting: <ul><li><em>Mileage Taxable Account must have a value in Mileage: &lt;Entry No.&gt;. It cannot be zero or empty.</em></li></ul> |66333|
| Per Diem|When <b>Per Diem</b> reimbursement method is set to <b>Both</b>, the system now correctly posts the per diem to general journal. |66572|
| Per Diem|Previously, when <b>Multi Destinations</b> was disabled in the <b>Expense Management Setup</b>, the <b>Per Diem Details</b> subpage was not displayed on posted <b>Per Diem</b> cards, even though relevant data existed.  |67000|
| Per Diem|Previously, when posting <b>Per Diems</b> that included more than one <b>Allowance Type</b> and using Dataloen's external payroll integration, only one allowance entry was automatically transferred. The remaining entries were left in the <b>External Interface Queue</b> with the status <em>On Hold</em>, requiring manual processing.&nbsp; All allowance entries included in a Per Diem are now correctly sent to Dataloen in a single automated process. |67069|

## Expense Management 2025 R1, Service Pack 1, Hotfix 2

*Release date online: June 4, 2025*  
*App version: 26.1.2*  

Only released in Business Central Cloud.
### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Per Diems | When the Per Diem reimbursement method is set to <b>Both</b>, the system now correctly posts the Per Diem to the general journal. | 66572 |
| Expense Reports | Cancelling an Expense Report approval request using <b>Cancel Approval Request</b> on the <strong>Expense Report card</strong>, changes the status of all of its subdocuments to <strong>Open</strong>. | 66664 |
| Expenses | For expenses processed with Document Capture, when the Document Capture template had been configured to match and update the order, the expenses would not link the generated purchase order document to the expense. This resulted in the following: <ul><li>Expenses were automatically reopened/unposted with a comment: <em>"This was reopened because the applied Document Capture Document &lt;No.&gt; was deleted"</em></li><li>The following comment was added to expenses: <em>"The applied Document Capture Document &lt;No.&gt; was deleted"</em>.</li></ul> | 66692 |
| Expense Reports | When using <b>Find Entries</b> on the <b>Posted Expense Reports</b> page, project ledger entries are now shown to users even when the documents have only created project ledger entries without general ledger entries (for example, when <b>Project No.</b> is specified but the <b>Reimbursement Method</b> is set to <b>External</b>). | 66788 |
| Expenses | When <b>Expense Posting</b> is set to <b>Preferable Purchase Invoice</b>, posting an Expense now correctly creates a purchase invoice for the vendor specified on the <b>Payment Type</b>. | 66933 |
| Document Approval | Continia approver users with <b>Limit Document Visibility</b> enabled would previously encounter the following error when trying to open an <b>Expense Report</b> sub-document card using <b>View</b> on Expense Report subpages: <ul><li><em>&lt;Document Type&gt; &lt;Entry No.&gt; for &lt;User ID&gt; cannot be displayed because you only have access to your own documents.</em></li></ul> | 66965 |

## Expense Management 2025 R1, Service Pack 1, Hotfix 1

*Release date online: May 21, 2025*  
*Release date on-premises: May 21, 2025*  
*App version: 26.1.1*  

Only released in Business Central Cloud.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions| The following error would previously occur when the <strong>Business Name</strong> field on a bank transaction exceeded 100 characters: <ul><li><em>The length of string is &lt;Bank Transaction Business Name field string length&gt;, but it must be less than or equal to 100. Value: &lt;Bank Transaction Business Name field string value&gt;</em><br> </li> </ul> |66319|
| Credit Card Transactions|Duplicate transactions are now properly detected, even when currency mapping is applied. |66338|
| Document Approval|Continia approver users with<b> Limit Document Visibility</b> enabled would previously encounter the following error when trying to open a document card using the <b>View</b>&nbsp;action on the&nbsp;<b>Approval Entries - Expense Management</b> page: <ul><li><span><em>&lt;Document Type&gt; &lt;Entry No.&gt; for &lt;User ID&gt; cannot be displayed because you only have access to your own documents.</em></span><br> </li> </ul> |66358|
| Document Approval|Expense Management approver users were previously unable to open the <strong>Approval Entries - Expense Management</strong> page due to the following permission error, which occurred when one of the documents was a matched expense created in a version prior to <strong>Expense Management </strong>26.0: <ul><li><em>Sorry, the current permissions prevented the action. (TableData 6086330 CEM Bank Transaction Bank Transaction Modify: Continia Expense Management)</em> </li> </ul> |66523|
| Expenses|The Expense <b>Description</b> field is now automatically filled with the <b>Merchant</b> value when the <b>E-DESCRIPTION</b> configured field is not mandatory. If E-DESCRIPTION is mandatory, the <b>Description</b> field will remain empty to enforce user input.<br>The <b>Merchant</b> value is automatically inherited from the AI Receipt Scanner for cash expenses or from the transaction <b>Business Description</b> when the expense is matched. Additionally, the <b>Merchant</b> field has been added to the <b>Posted Expense Card</b> and the <b>Expense Report</b> subpage corresponding to expenses.  |66401|
| Expenses|An expense that was automatically allocated due to company policies, and later modified manually by the expense user, would previously generate the following error message in the <strong>Expense Inbox</strong> when attempting to synchronize the updates: <ul><li><em>Expense &lt;Entry No.&gt; cannot be updated as there are one or more unprocessed lines in the Expense Inbox. Please process the related lines in the Expense Inbox before making changes to this Expense.</em> </li> </ul> |66481|
| Mileages|A mileage subject to company policies that refund up to a limit would previously result in the following error when posting:   <ul><li><em>Mileage Taxable Account must have a value in Mileage: &lt;Entry No.&gt;. It cannot be zero or empty.</em> </li> </ul> |66333|

## Expense Management 2025 R1, Service Pack 1, Hotfix 0

*Release date online: May 14, 2025*  
*Release date on-premises: May 14, 2025*  
*App version: 26.1.0*  

Only released in Business Central Cloud.

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|This version includes no deliveries and is a technical release only. |66453|


## Expense Management 2025 R1, Hotfix 4

*Release date: May 7, 2025*  
*App version: 26.0.4*  

Only released in Business Central Cloud.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Document Approval|Users assigned the <b>CEM-APPROVE</b> permission set would previously encounter the following error in the <b>Web Approval Portal</b> or <b>Business Central client</b> when attempting to approve an expense matched to a bank transaction: <br><ul><li><em>Sorry, the current permissions prevented the action. (TableData 6086330 CEM Bank Transaction Bank Transaction Read: Continia Expense Management)</em> </li></ul> |66207|
| Expenses|When using a <b>Distribution Code</b> to automatically allocate expenses, configurations with an odd number of distribution lines could result in incorrect rounding. This caused an inconsistency error when posting the expense. |64797|
| Expenses|When using a <b>Distribution Code</b> to automatically allocate expenses, the user-entered expense<b> Tax Amount</b> was previously ignored. Instead, standard tax values were calculated for the allocated lines, which could result in un-expected tax amounts being posted. |65498|
| General Application|When attempting to upgrade to Business Central version 26, the following error would occur if the company was not activated but Expense Management documents<b>, </b>that have never been synchronized with Continia Online<b>,</b>&nbsp;existed. <ul><li><em>&nbsp;Excessive recursion has been detected in event subscriber function RunModify...</em></li></ul> |65995|

## Expense Management 2025 R1, Hotfix 3

*Release date: April 10, 2025*  
*App version: 26.0.3  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|When attempting to post a Mileage or a Per Diem in a Belgium (BE) localized Business Central client the following error would previously occur: <ul><li><em>Journal Template Name must have a value in Gen. Journal Line: Journal Template Name=, Journal Batch Name=, Line No.=0. It cannot be zero or empty.</em> </li> </ul> |65634|

## Expense Management 2025 R1, Hotfix 2
*Release date: April 1, 2025*  
*Release date on-premises: April 10, 2025*  
*App version: 26.0.2*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|This version <b>26.0.2</b> marks the official release of <b>Expense Management 2025 R1</b>. The preview version was released as <b>26.0.0</b>, with minor updates included in version <b>26.0.1</b>.&nbsp; This current version includes no deliveries and is a technical release only. |65650|

## Expense Management 2025 R1, Hotfix 1
*Release date: April 1. 2025*  
*Release date online: April 9, 2025*  
*App version: 26.0.1*  

Only released in Business Central online.

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|Procedure SetGlobalVars in report <b>CEM Status Report </b>has been made available for external access. |64982|
| Platform and Technology|The custom FactBox pane resizing implementation has been disabled when running on <b>Business Central 26.0</b> and above, in favor of Microsoft's new native resizing feature. Note that the native implementation limits the FactBox pane width to a maximum of 50% of the screen, whereas the previous custom implementation allowed for wider expansion.|65063|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Document Approval|Rejecting an Expense Management approval entry would previously cause the following error to occur: <ul><li><em>Sorry, the current permissions prevented the action. (TableData 454 Approval Entry Modify: Continia Expense Management).</em> </li> </ul> |64691|
| Expenses|When attempting to run Expense Management Online Synchronization in Business Central, the following error would appear if a user entered a <b>Vendor Invoice No.</b> on an expense document that exceeded the 30-character limit: <ul><li><em>The length of the string is &lt;Vendor Invoice No. Length&gt;, but it must be less than or equal to 30 characters. Value: &lt;Vendor Invoice No. ></em></li> </ul> |64865|
| General Application|When creating mileage entries using the <b>Mileage</b> card<strong>&nbsp;</strong>page, opened directly from an expense report, the attachment add-in would display an incorrect attachment. |64781|
| General Application|In a localized version of Business Central, the following error would have prevented users from posting expense documents where sustainability accounts were specified: <ul><li><em>The &lt;Environmental Account No.&gt; must be of type Posting.</em> </li> </ul> |64846|
| General Application|When attempting to post an expense with long values in the fields <b>Invoice No.</b> or <b>Vendor Invoice No.</b>, the following error would appear: <ul><li><em>The length of the string is 28, but it must be less than or equal to 20 characters. Value: &lt;External Doc. No.&gt; </em></li></ul> |64867|

## Expense Management 2025 R1
*Pre-release date: March 21, 2025*  
*Release date, online: April 1, 2025*  
*Release date, on-premises: April 1, 2025*  
*App version: 26.00*  

Released on-premise and in Business Central online.

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|<span>In the Canadian localization, functionality has been enhanced to support multiple tax jurisdictions of the same type (e.g., PST1 and PST2). The Tax Amount is now distributed proportionally based on the respective tax percentages for each tax entry. Previously, this setup would have resulted in an error. This improvement is particularly useful for expenses that are capitalized.</span> |60308|
| Credit Card Transactions|More flexibility has been introduced when changing <strong>Payment Type</strong> or creditcard settings. Users can now modify these details even when there are transactions and expenses that are not yet posted. Previously, these changes were restricted until the documents were posted. |60587|
| Credit Card Transactions|Upon opening, the <strong>CEM Banks</strong> page now automatically populates with supported banks, so you no longer have to manually select the <strong>Get Supported Banks</strong> action.&nbsp; |62654|
| Credit Card Transactions| You can now correct the<span>&nbsp;</span><b>Continia User Credit Card</b><span>&nbsp;</span>record if an incorrect<span>&nbsp;</span><b>User ID</b><span>&nbsp;</span>or<span>&nbsp;</span><b>Payment Type</b><span>&nbsp;</span>was assigned, even where <b>Bank Transactions</b><span>&nbsp;</span>are present. The system automatically updates the associated open<span>&nbsp;</span><b>Bank Transactions</b><span>&nbsp;</span>with the new values. However, posted and/or matched transactions will not be updated, they instead retain their original settings. Additionally, you can remove, delete, or update the associated credit cards from the payment type.<br>When the <b>Posting Method</b><span> or </span><b>Matching Method</b> is updated to an option that doesn't require associate cards, the user is asked if the associated cards should be removed. You cannot change the <b>Currency Code</b> of a <b>Bank Account</b> or a <b>Vendor</b> that is related to a <b>Payment Type</b> that has bank transactions. |62677|
| Document Approval|Users can now click the <strong>Approval By</strong> field in <strong>Expense Report</strong> card, and list pages, to open the approval entries page for the document, similar to other Expense Management document types. |46382|
| Document Approval| You can now handle document approval directly on <strong>Expense Management </strong>document cards, streamlining the approval process. Moreover, approval-related actions are now reorganized into groups, similar to those on purchase documents.<br> On document card pages, the following new action groups have been introduced:<ul><li><strong>Approve</strong>: Contains actions for <strong>Approve</strong>, <strong>Reject</strong>, <strong>Forward</strong>, and <strong>On Hold</strong>, as well as the existing <strong>Force Approval</strong> actions. </li><li><strong>Request Approval</strong>: Includes <strong>Send Approval Request</strong> and <strong>Cancel Approval Request</strong>, along with a link to the <strong>Approvals</strong> page. </li> </ul> |60573|
| Document Approval| In the Business Central client, when a document is rejected and sent back to the previous approver, the system now prompts the user to provide a comment. |60596|
| Document Approval|The following event has been added to Codeunit&nbsp;CEM Approval Management:<ul><li><span>OnBeforeGetNextApprover</span> </li> </ul> |61006|
| Expense Mobile App and Portal|When the <strong>60-Day Rule</strong> is enabled, a confirmation message now appears if the selected address differs from the home address, but is within 500 meters. This ensures users are informed of minor address discrepancies before proceeding. |62019|
| Expenses|You can now view an unlimited number of <strong>expense types</strong> on the <strong>Expense Reimbursement</strong> page by navigating using the <strong>Next/Previous</strong> actions. |44715|
| Expenses|Deleting a document from the <b>Documents for Import</b> queue in Document Capture now clears the <b>Applied Document No.</b> field on the linked expense. If the expense has already been posted, the expense will also reopen. |59523|
| Expenses| <span>The </span><b>Invoice No.</b><span> is transferred to the </span><b>External Document No.</b><span> when posting, together with information about the expense document number. The </span><b>Invoice No.</b> is captured by the AI Receipt Scanner. In the Spanish localization, you can configure the <b>Vendor Invoice No.</b> field for expense user input, for similar purposes. In this case, the <b>Vendor Invoice No.</b> value will transfer to the <b>External Document No.</b> | 9773  |
| Expenses|You can now send Expenses to Document Capture, even if the attachment is not a PDF. |59779|
| Expenses|You can now specify the Volume Unit on the Expense Management Setup page. The Volume Unit and the Distance Unit are used in various areas, including the sustainability fields that require this type of information. |60178|
| Expenses|When <b>Applied Purch. Doc No.</b> is manually updated, <b>Process with Document Capture </b>will no longer send the document for OCR processing, because a document is already applied. |60651|
| Expenses|The field <strong>Business Description</strong> has been renamed to <strong>Merchant</strong>. The values for this field are now inherited from the matching transactions or from the <strong>AI Receipt Scanner</strong> in the Expense Mobile App and Expense Portal. As a result, the <strong>Copy Description from Bank Transaction</strong> setting in Expense Management has been removed. |61237|
| Expenses|Invoice documents associated with an expense report cannot be processed using <strong>Document Capture</strong>. To process the document, you must first detach it from the expense report. This restriction ensures proper handling of invoice documents within the system. |61240|
| Expenses|<span>The following event has been added to</span><span>&nbsp;</span>R<span>eport</span><span>&nbsp;</span><span>CEM Export Attachments:</span> <ul><li><span>OnExportAttachmentsOnCreateFileName</span> </li> </ul> |61796|
| Expenses|The <strong>Post in Expense Currency</strong> feature now ensures that expenses for users associated with an <strong>Employee</strong>, where the <strong>Currency Code</strong> is specified, are posted in their respective currencies. This is consistent with the behavior for users associated with a <strong>Vendor</strong> and ensures consistency in currency handling across different user types. |62142|
| General Application|For <b>Expense Report</b>&nbsp;posting, the ledger entries corresponding to the expense user (<b>Employee/Vendor</b>) can now be grouped based on the document type (expense, mileage, per diem) or combined for the entire expense report. This enhancement provides greater flexibility in financial reporting and reconciliation. However, you cannot group ledger entries in the following cases: <ul><li>Different balancing accounts </li><li>Different currencies </li><li>Different dimension sets </li> </ul>Additionally, business vendor entries (where <b>Vendor No.</b> is specified on the expense) will not be grouped. |38895|
| General Application|Users can now select which documents to post using the <b>Post Batch</b> functionality on Expense Management document list pages. This applies to all Expense Management document types. |45456|
| General Application|You can now open card pages for <strong>expenses, mileages, and per diems</strong> directly from an expense report, allowing for easier access and review of individual entries. |45892|
| General Application|When running a data maintenance job, you can now see an overview of the data scheduled for deletion. Additionally, the date intervals have been aligned with those in Document Capture. |54571|
| General Application|The <strong>DESCRIPTION</strong> configured field, used for <strong>expenses</strong>, <strong>mileages</strong>, and <strong>expense reports</strong>, has been split into individual fields for each document type. This change allows for different descriptions on each document type, and provides for greater flexibility and customization. |55259|
| General Application|The field types <strong>JOBNO</strong> and <strong>TASK</strong> have been renamed to <strong>PROJECT NO.</strong> and <strong>PROJECT TASK NO.</strong>, respectively. This change improves consistency in terminology across the system. |56888|
| General Application| Improvements have been made to enhance the user experience when managing sustainability-related data. |59226|
| General Application|A new field <b>Posted Document No.</b> has been added to the <b>Posted Expense Report </b>card&nbsp;and list pages. It shows the <b>Document No.</b> of the ledger entries created during Expense Report posting. The field is visible when <b>Post on multiple document numbers</b> is disabled on <b>Expense Management Setup</b> page. |59765|
| General Application|Global Dimension fields have been added to the following pages: <b>CEM Per Diem Reimbursement Details</b>, <b>CEM Expense Reimbursement Details</b>, <b>CEM Mileage Reimbursement Details</b>. |59766|
| General Application|Posting is now restricted on blocked <strong>General Posting Groups</strong> and <strong>VAT Posting Groups</strong>, preventing transactions from being posted to blocked accounts. |59826|
| General Application|Rejecting a document in Document Capture  now clears the <b>Applied Document No.</b> on a linked expense. If the expense has already been posted, it will also reopen. |59914|
| General Application|Boolean (<strong>Yes/No</strong>) values are now supported in <b>field dependencies</b>, allowing for improved flexibility in conditional logic and data validation. |60327|
| General Application|In approval emails, the domain name is now removed from the user name<strong>.</strong> |60560|
| General Application|The <b>Transaction Description</b> field for expenses, which previously displayed the merchant's name only when an expense was created from a bank transaction, has been updated. Merchant names are now also captured via OCR from the Expense Portal or Expense Mobile App. To enhance clarity, the <b>Transaction Description</b> field has been replaced with a new <b>Merchant</b> field, which is automatically populated by OCR and bank transactions. |60637|
| General Application|During the upgrade from v24 to v25, the Sustainability fields and their values are converted. Previously, these values were not managed. |60663|
| General Application|When running <b>Run GDPR Maintenance</b> in <b>Expense Management Setup</b> to delete old documents, the associated <b>Document Log</b> entries are now also removed.  |60996|
| General Application|The sustainability fields are now editable on the <b>Posted Expense Card</b> page, enabling the completion of sustainability data after upgrading from earlier versions of Expense Management. |61612|
| General Application|The <b>EM Countries/Regions</b> page now automatically populates with standard <b>Country/Region</b> records upon opening. |61773|
| General Application|The values in the <b>Request Page</b> fields for batch posting reports are now retained for future use.|61937|
| General Application|The caption for the configured field &lt;DOCUMENT DATE&gt; has been changed from &quot;Registration Date&quot; to &quot;Document Date&quot;. |62651|
| General Application|Multiple controls, especially pages, have been renamed to include the <b>- Expense Management</b> suffix instead of abbreviations such as <b>EM</b>. This improves clarity and consistency across the system. |63290|
| General Application|The following event publisher has been added to Table 6086333 CEM Exp. Posting Desc. Field<span>&nbsp;</span><span>to enable customization of the</span><span>&nbsp;</span><b>Posting Description</b><span>&nbsp;</span><span>field when posting Expense Management documents:</span> <ul><li><span>OnBeforeReplacePlaceholdersWithValues</span> </li> </ul> |63479|
| General Application|The configured field <b>BILLABLE</b> has been renamed to <b>PROJECT BILLABLE</b>. |63673|
| General Application|You can now preview PDFs directly from the <b>attachment list</b> avoiding having to download them to do so. |64399|
| Mileages|Project ledger entries are now posted independently of the <b>reimbursement method</b>, allowing expenses to be posted to projects in Business Central while processing employee reimbursements externally. |42271|
| Mileages|In the Danish localization, when the 60-day rule is enabled, an error comment now displays if both the <b>From Home</b> and <b>To Home</b> fields are selected simultaneously. This ensures that only valid mileage data is processed and helps maintain accurate records.  |61287|
| Mileages|To improve clarity in calculating the 60-day rule in Danish localization, the <b>60-Day Rule Day Count</b> and <b>60-Day Rule Destination</b><span> fields have been added to the mileage list.</span><br><ul><li><b>60-Day Rule Day Count</b> provides a count of how many days, within the past year, the employee has traveled to the same destination </li><li><b>60-Day Rule Destination</b> displays the address text of the first recorded destination, which you can use for address lookups and filtering similar destinations. For example, if a construction site spans multiple streets, bookkeepers can use this field to easily filter and identify related mileage entries.</li> </ul> |61550|
| Mileages|The following event has been added to Table CEM Mileage Rate: <ul><li>OnBeforeRecalcMilAcrossComp </li> </ul>The event enables filtering of companies where mileages will be recalculated. |61621|
| Mileages|In the Danish localization, when the 60-day rule is enabled, a warning comment now appears if neither the <b>From Home</b> nor <b>To Home</b> checkboxes are selected, but there is a clear correlation to a previously used home address within the default range of 300 meters. |62432|
| Mileages|In the Danish localization, when the 60-day rule is enabled, a warning comment now appears if GPS coordinates are missing on a mileage. GPS coordinates are used to determine proximity to a destination address and validate home address checks. If GPS coordinates are missing, the system defaults to identifying similar destination addresses based solely on the address text, which may affect the accuracy of the 60-day rule calculation. |62433|
| Mileages|In the Danish localization, when the 60-day rule is enabled, you can now see a warning comment if a mileage has either <b>From Home</b> or <b>To Home</b> specified but the home address is outside the 300 meter range when comparing with the previously used address. |62467|
| Mileages|An event publisher has been added to Codeunit&nbsp;CEM Mileage-Reimburse: <ul><li>OnMileageReimburseOnAfterSetReimbursed </li> </ul> |64123|
| Per Diem|For improved transparency of calculations, a new <b>FactBox</b> has been added to <b>Per Diem</b>, displaying a summary of the calculations. Additionally, you can now access a detailed daily calculation breakdown by navigating on the amount. |62095|
| Per Diem|On the <b>Per Diem Rate </b>page,<strong>&nbsp;</strong>the captions for the fields <b>Breakfast</b>, <b>Lunch</b>, and <b>Dinner</b> are now dynamically updated based on the selected <b>Value Method</b>. If the value method is percentage-based, a percentage sign (%) is appended to the captions. If the value method is based on real amounts, the currency code is displayed instead. This improvement ensures the captions clearly reflect the context of the entered values.   |62106|
| Per Diem|You can now view per diem details directly on the <b>Per Diem Card</b> and the <b>posted Per Diem Card</b> without opening any extra pages. You can also view and modify allowances directly on the <b>Per Diem Card</b>, again, avoiding having to navigate to additional pages. This update streamlines workflows and improves efficiency for users managing per diem expenses.  |62794|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|On <b>Continia User Credit Cards</b>, a filter is applied so only matching credit cards are available for assignment. |61879|
| Expenses|The dynamically calculated <b>VAT Amount</b> field, in the <b>Amounts</b> group on the <b>Expense Card</b> page, has been renamed to <b>VAT Amount (Calculated)</b> to better indicate that the value of this field is calculated automatically. It also better distinguishes from the optional editable VAT Amount field that you can enable via Configurable Fields functionality. A similar change has also been made to the Expense Report's Expenses subpage. |52757|
| General Application|When creating demo data, the <b>GENERAL</b> journal template is now selected by default if it exists. |44365|
| General Application|Performance of the <b>Consistency Check</b> in field dependencies has been optimized to improve efficiency and reduce processing time. |56183|
| General Application|Business Central users now only see the <b>Continia Expense Management Activities</b> cue and tiles on their role centers if they have an appropriate permission set assigned to them (<b>CEM-SUPER</b>, <b>CEM-NAVUSER</b>, or <b>CEM-APPROVE</b>). This ensures the Continia Expense Management role center cue and tiles are hidden from users who are not intended to interact with Expense Management. |61960|
| General Application| The <b>Expense Management Online Synchronization</b> process has been improved to prevent documents from getting stuck in their inboxes with the following errors:<ul><li>Status must be Open or Pending Expense User in Expense Report &lt;Expense Report No.&gt;. </li><li>Status on Expense &lt;Entry No.&gt; is incorrect and therefore changes are not allowed. </li><li>The Mileage &lt;Entry No.&gt; has incorrect status. Updates are not allowed. </li><li>The Per Diem &lt;Entry No.&gt; has incorrect status. Updates are not allowed. </li> </ul><ul> </ul> |63245|
| General Application|Context-sensitive help page URLs have been fixed to ensure they direct users to the correct help pages. |64337|
