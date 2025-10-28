---
title: Detailed changelog for Continia Expense Management 2021 R2
date: 18-09-2025
description: List of features and bug fixes for each version of Expense Management 2021 R2
id: EM-362
lang: en
---
# Detailed changelog for Continia Expense Management 2021 R2
This article lists all new features and bug fixes for each version of Continia Expense Management 2021 R2.

> [!IMPORTANT]
> This version of Expense Management is no longer supported. As a consequence of this, Continia will no longer correct any errors appearing in this version, and no further service packs relating to the version will be released. For supported versions of Expense Management, see [Software Lifecycle Policy and Continia Expense Management On-Premises](@EM-104).

> [!TIP]
> As a Continia partner, you can be notified of new Expense Management versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005316840-Receive-a-notification-upon-new-Expense-Management-releases) in the Continia PartnerZone (only available to partners).

## Expense Management 2021 R2 Service Pack 6

*Released: June 19, 2023*  
*App version: 8.6.0.0*   
*FOB version: 8.06.00*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Credit Card Transactions                                  | We have addressed an issue where parallel processes downloading transactions could potentially result in duplicated entries in the bank transaction inbox. | 47472 |
| Expenses                                                  | In Canadian localization, when a user created expense allocations marked as non-taxable, the system incorrectly allocated them as taxable amounts for sales tax purposes. | 43601 |
| Expenses                                                  | On the expense card, the Amount without VAT field now displays the total amount when the VAT calculation type is Reverse VAT. | 46594 |
| Expenses                                                  | We have resolved a problem where the default dimensions on Employee were not checked on the expense allocations, leading to occasional errors in specific situations. | 46639 |
| General Application                                       | The UNABLE-DEPR error displayed for a completed document that was later attached to a settlement. | 43696 |
| General Application                                       | After attempting to update a posted document from the inbox, all subsequent inbox entries are marked as Accepted. | 44410 |
| General Application                                       | To avoid errors, in the Spanish localization we no longer set the Document Type (Invoice) when posting a settlement. | 45115 |
| General Application                                       | To address the issue of posting documents related to a settlement being added to Job Queues, we have implemented a prevention measure to disable the posting functionality for such documents. | 45593 |
| General Application                                       | When deleting a Settlement inbox entry, the status is now checked. | 46484 |
| General Application                                       | When processing notification outbox entries, multiple updates of the same documents in Continia Online were sent. | 46514 |
| General Application                                       | The reminder e-mail sent to approvers presented the wrong currency on the settlements when the amounts were in local currency. | 46690 |
| General Application                                       | In Microsoft Dynamics NAV 2016; an error occurred when attempting to preview posting a settlement, causing inconsistencies in the G/L Entry table. | 46950 |
| General Application                                       | Previously, when transitioning from File Storage or Azure to Database, encountering an error during the deletion of old files would result in a complete rollback of the process, leading to the loss of already deleted files. We have now implemented a change to handle each document individually, allowing for the possibility of repeating the process in case of errors and enabling recovery of the deleted files. | 47561 |
| Per Diem                                                  | When utilizing per diem sub-rates, a specific issue occurred where a per diem starting precisely at midnight (00:00) would mistakenly include an additional full day allowance in the calculation. | 44537 |
| Per Diem                                                  | When clicking on the "0" value in the Allowance Rates on a Per Diem group, a dialog prompts the user to create a rate automatically. In specific localizations, the new rate has a wrong date format resulting in an error. | 46678 |

## Expense Management 2021 R2 Service Pack 5

*Released: January 19, 2023*  
*App version: 8.5.0.0*   
*FOB version: 8.05.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|We have added the following Event Publishers:<br> Codeunit 6086308 CEM Expense Inbox-Transfer<br> <ul><li>OnAfterExpenseInboxTransfer </li> </ul> |41366|
| Per Diem|Per Diem calculations are now done on a day-to-day basis in the German, Austrian and Swiss localizations, as opposed to the past when the sub-rates were applied only to the last day. |43238|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|When pressing &quot;Show not matched&quot; on the Reconciliation page, filters were applied only on the left side sub-page, but not on the right-side sub-page.&nbsp; |41368|
| Expenses|When pressing &quot;Show not matched&quot; on the Reconciliation page, filters were applied only on the left side sub-page, but not on the right-side sub-page. |41369|
| Expenses|When importing transactions and processing them, the status was not updated so multiple transactions and expenses could have been created based on the same transaction inbox. The issue was introduced in versions 7.05 and 8.04. |41841|
| Expenses|When downloading an expense from Continia Online (Synchronize) that is matched to a bank transaction, it would have failed in the Expense Inbox with the following error:<ul><li><span><em>Matched to Bank Transaction must be equal to 'No' &nbsp;in Expense: Entry No.=&lt;ExpenseNo&gt;. Current value is 'Yes'.</em></span> </li></ul> |42071|
| Expenses|When trying to &quot;Get Expenses&quot; from an Expense Report, when the expense would have been matched, the following error was shown:  <ul><li><em>Matched to Bank Transaction must be equal to 'No' in Expense: Entry No.=&lt;EntryNo.&gt;. Current value is 'Yes'.</em></li></ul>  |42497|
| Expenses|When posting allocations on an expense with the external reimbursement method set up, an error would not allow the expense to be posted. <ul><li><em><span>Allocation with Entry No. &lt;No.&gt;: Expense Account is missing. Posting Setup for Expense Type 'FOOD' is most likely not configured correctly.</span></em> </li> </ul>  |43536|
| General Application|We are now validating the input on&nbsp;<span>&quot;Expense Reminder Code&quot; and &quot;Expense User Group&quot; on the &quot;Continia User Setup&quot;.</span> |29465|
| General Application|<span>We have identified an issue that could lead to a duplicated ledger entry for an expense in the case where 2 users would both post said expense at the same time. The posting routine was able to prevent concurrent sessions, but not from the moment the button was pressed up to the moment the posting would start.</span><br> We have now made an extra check to ensure this cannot happen. |41300|
| General Application|When downloading a document which was ready to be automatically sent for approval but the user didn't have an approver, the synchronization process would have failed with the following error. <ul><li><em>The changes to the Expense Inbox record cannot be saved because some information on the page is not up-to-date. Close the page, reopen it, and try again.</em></li></ul> |41481|
| General Application|When posting an expense report with a very long posting description, you could get the following error message: <ul><li><em>The length of the string is &lt;length of posting description&gt;, but it must be less than or equal to 50 characters. Value: &lt;posting description&gt;</em> </li></ul> |41776|
| General Application|We have fixed a bug in the &quot;Upload Company Logo&quot; action on the Expense Management Setup page which prevented the logo from being sent to Continia Online, and consequently shown to app users. |42717|
| Mileages|When setting up Expense Management Setup to show extra fields on the &quot;Posted Mileage&quot; and &quot;Posted Mileage Card&quot;, the system would have been presenting extra fields for expenses instead. |41345|
| Mileages|Wrong comments were shown on the posted Mileage card (belonging to expenses rather than mileage). |43230|
| Mileages|The event OnBeforeCheckMileage was never used in Codeunit 6086344 CEM Mileage - Check. Instead, OnAfterCheckMileage was wrongly called from two locations. |43978|
| Per Diem|When only one Per Diem Group would exist, the filed &quot;Per Diem Group Code&quot; was not visible on the Per Diem Card. |40886|
| Per Diem|The amount shown on a Per Diem was wrong in the Expense App and Expense Portal when a per diem had multiple currencies. We are now showing the total amounts in the local currency. |42537|

## Expense Management 2021 R2 Service Pack 4, Hotfix 2

*Released: October 20, 2022*  
*App version: 8.4.0.2*   
*FOB version: 8.04.02*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses | When downloading an expense from Continia Online (Synchronize) that is matched to a bank transaction, it would have failed in the Expense Inbox with the following error:<ul><li><em>Matched to Bank Transaction must be equal to 'No'  in Expense: Entry No.=<ExpenseNo>. Current value is 'Yes'.</em></ul></li> | 42071 |

## Expense Management 2021 R2 Service Pack 4, Hotfix 1

*Released: October 11, 2022*  
*App version: 8.4.0.1*   
*FOB version: 8.04.01*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses | When importing transactions and processing them, the status was not updated so multiple transactions and expenses could have been created based on the same transaction inbox. The issue was introduced in version 8.04. | 41841 |

## Expense Management 2021 R2 Service Pack 4

*Released: September 26, 2022*  
*App version: 8.4.0.0*   
*FOB version: 8.04.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|For Sales Tax allocation, the sales tax amount will be distributed into multiple lines in the event that an expense has already been allocated.  |38588|
| Expenses|The field Job Line Type has been made editable on the following pages: <ul><li><span>Expense Card and&nbsp;</span>Expenses </li><li>Mileage Card and Mileage </li><li>Per Diem Card and Per Diem </li><li>and the respective subpages on the Expense Report. </li></ul>   |40916|
| General Application|We are now processing the release notifications from the&nbsp;<span>Notification Outbox as part of the normal synchronization with Continia Online.</span> |28682|
| General Application|The fields&nbsp;&quot;Gen. Bus. Posting Group&quot; and &quot;VAT Bus. Posting Group&quot; have been added to the expense and mileage tabs on the Expense Report Card page. |41056|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | Id |
| --- | --- |  --- |
| Credit Card Transactions|We have fixed an issue, where rejecting a bank activation request, could result in the following error message during synchronization. <ul><li><em>&quot;Bank Code missing. Continia Online has provided an agreement activation but the bank doesn't exist.&quot;</em> </li></ul> |38522|
| Expenses|We have found an issue that could create duplicated bank transactions out of one single bank transaction inbox. That would occur if multiple users processed the transaction inbox in the exact split of a second. The bookkeeper would have been informed if an expense existed twice, though. |35047|
| Expenses|Allocations did not inherit standard dimensions from the employee.&nbsp; |35143|
| Expenses|An issue has been fixed that was causing decimal differences in the sales taxes appended to the Purchase Invoice when the user would not have changed the sales taxes allocated amount.  |39083|
| Expenses|An issue in the sales tax was causing the following error to be shown, even though the sales tax differences were within the setup ranges. This has been fixed. <ul><li><em>Government Sales Tax Expense Type 10 must not exceed General Ledger Setup Max. Tax Difference Allowed 5.</em> </li> </ul> |39337|
| Expenses|The&nbsp;<span>Expense Report (Settlement) posting date is used to post all the sub-documents on the same date. However, on an expense, the exchange rates were not calculated in regard to that date, but based on the &quot;Document Date&quot;.</span>  |41026|
| Expenses|When validating the expense “Document Date”, a recalculation of exchange rates will happen. |41027|
| Expenses|The expense report posting date is used for recalculating the currency exchange rates for expenses. Now amounts are recalculated to reflect currency exchange rates on expenses in an Expense Report (Settlement). Until now, these were only updated at posting time. |41029|
| Expenses|<span>An issue has been fixed, resulting in an error where an allocated expense would have an allocation without a Job Task specified when the original expense had a Job specified. The error can be bypassed if the main expense Job is removed.<ul><li><em>Job Task No. must have a value in Expense Allocation: Entry No.=53. It cannot be zero or empty.</em> </li> </ul> |41145|
| General Application|When exporting the Expense Management configuration&nbsp; with the Expense Management Assisted Setup, the Vehicle table would always be exported. Now it is only exported if the user has selected to export Mileage Rate IDs. |32335|
| General Application|The field type dependency can be disabled with the following message: <ul><li><em>The following users don't have access to value X in the field Y</em> </li><li><em>The following user groups don't have access to value X in the field Y</em></li> </ul>We have improved the consistency check to not disable field type dependencies in the case where user also had a restricted lookup value access on the specific value in the condition for the field dependency.  |34547|
| General Application|We have fixed an issue where the inbox entries would have failed with the error below. This was happening only when using the &quot;O365 Authentification Email&quot; on the Continia User. <ul><li><span><span>&nbsp;</span>&quot;User with user ID &lt;email&gt; does not exist in the Continia User table.&quot;</span> </li> </ul> |34643|
| General Application|The field Approver Name was editable in View mode on the Continia User Setup Card page. |34815|
| General Application|We have fixed an issue that was returning the following error in the Web Approval Portal, when custom fields would have been created with value longer than 50 characters. The issue was present on Mileage, Per Diem and Expense Report. <ul><li><em>The length of the string is 51, but it must be less than or equal to 50 characters. Value: A very long description, longer than 50 characters.</em></li></ul> |38431|
| General Application|We have identified an issue that was not updating documents in the Expense App when they were paid, due to the fact that the payment was not made with a Document Type = Payment.&nbsp;<span>We are now not checking anymore the Document Type, we only make sure the payment applies to the initial entry.</span> |38505|
| General Application|We have fixed an issue that caused the error below when synchronizing. The issue has been introduced in version 9.2 <ul><li><em><span><em>The following AL methods are limited during write transactions because one or more tables will be locked...</em></span></em> </li> </ul> |38859|
| General Application|We have fixed an issue that was causing the synchronization to stop with the error below when documents were pending to be deleted. The issue has only been seen in the Business Central cloud client. <ul><li><span><em>The following AL methods are limited during write transactions because one or more tables will be locked...</em></span> </li> </ul> |38907|
| General Application|From the Expense Setup page, when choosing Manual Setup, the page will only show the entries for Expense Management. Filters for Continia Core setup have been added as well. <br>When choosing Open Manual Setup on Continia Users Default Setup the Expense User Delegation opened. This has been fixed.    |39092|
| General Application|An issue when batch-posting documents, that resulted in the following error, has been fixed.  <ul><li><em>Status must be Open or Pending Expense User in Expense 1.</em> </li> </ul> |39452|
| General Application|A permission issue that could result in the following message has been fixed:&nbsp; <ul><li><em>You do not have the following permissions to TableData Employee Ledger Entry: Read </em> </li> </ul> |40808|
| Mileages|We have fixed an issue that was crashing the client while trying to calculate mileage amounts in an endless loop. This was happening when mileage rates would exist for 2 years in advance. The error received is the one below: <ul><li><span><em>There is insufficient memory to execute this function. This can be caused by recursive function calls. Contact your system administrator.</em></span> </li> </ul> |38457|
| Mileages|When attempting to modify a mileage rate that is already used for posting mileage entries, you would get the following error message.&nbsp; <ul><li><em>One or more mileage have been posted after &lt;fieldValue1&gt; and &lt;field2&gt; can therefore not be changed.</em> </li> </ul>The&nbsp;<em>&lt;fieldValue1&gt; </em><span>was intended to be the start date of the mileage rate but was showing random values from the mileage rate, making the error message unclear.&nbsp;</span>  |38492|
| Mileages|An issue in the Company Policies that was resulting in the following error, has been fixed. The issue was occurring when opening Company Policies from the drill down, on the field. <ul><li><em>The field Document Account No. of table Company Policy contains value (PRIVATE CAR) that cannot be found in the related table (Expense Type)</em> </li> </ul> |40815|
| Mileages|A user who has the permission set CEM-NAVUSER, would get the following error when creating a mileage. <ul><li><em>You do not have the following permissions on the TableData CEM Mileage Detail: Modify.</em> </li> </ul> |40953|
| Mileages|An issue in the mileage calculation, where in a very specific situation, the low mileage rate was wrongly assigned instead of the high rate have been fixed. This happened when a mileage existed in 2 periods and when the sum of the total distance driven by a user was exceeding the low rate. |41111|
| Mileages | When exporting configurations through the Expense Management Assisted Setup Guide, decimal values were converted to integers (e.g., 1.23 was converted to 123). This impacted mileage rates. | 42127 |
| Per Diem|If was possible to set the arrival time of the first destination to earlier than the departure time of the Per Diem and i<span>t was possible to set the arrival time of the last </span><span>destination&nbsp;to later than the arrival time of the Per Diem. We are now preventing this.</span> |27121|
| Per Diem|On the Per Diem rates, we have removed the fields&nbsp;<span>&quot;Half Day Starting Time&quot; and&nbsp;</span><span>&quot;Half Day Latest Time&quot; because they were not used anymore.</span> |32391|
| Per Diem|We have identified and fixed a wrong calculation on the Per Diem, when using hourly rates, on the last day of the trip. |34367|
| Per Diem|We have fixed an issue on the Per Diem calculation in the case there where &quot;First/Last Day Calculation Method&quot; would have been &quot;First/Last Day fixed rate&quot;. If the number of hours in the current day would have been precisely the same as &quot;First/Last Day Minimum Stay&quot;, the rate was not applied but it should have been. |34501|
| Per Diem|When setting the First and Last Day Setup, Calculation Method to Sub rates immediately after creating the Per Diem Rate, you would get the following error message: <ul><li><em>The Per Diem Rate does not exist. </em> </li> </ul>  |38538|
| Per Diem|When posting a Per Diem with reimbursement method = both, you would get the following error. This has been fixed. <ul><li><em>Document No. must not be blank in ...</em> </li> </ul> |38762|
| Per Diem|For Per Diem calculation, in certain conditions, if skipping one day rate when using sub-rates, an issue has been fixed.  |38931|
| Per Diem|A wrong calculation on the Per Diem, when using hourly rates, on the last day of the trip has been fixed.  |38932|
| Per Diem|We have fixed the following error in the Status Report, related to the Per Diem calculations over the number of hours:  <ul><li><em>Overflow under conversion of Microsoft.Dynamics.Nav.Runtime.Decimal18 value 16,5 to System.Int32</em> </li> </ul> |39458|

## Expense Management 2021 R2 Service Pack 3

*Released: April 27, 2022*  
*App version: 8.3.0.0*   
*FOB version: 8.03.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Document Approval                                         | <span>We have added the following Event Publishers</span><br>  <span>Codeunit 6086312&nbsp;CEM Approval Management</span> <ul><li><span>OnBeforeApprovalMgtCode</span> </li> </ul> | 31358 |
| General Application                                       | We have improved the usability when creating a new Field Type. Simply give the field a description in the corporate language and the first translation is automatically added. Then click the No. of translations to add more.&nbsp;<span>The Corporate Language is defined in the Expense Management Setup.&nbsp;</span> | 19608 |
| General Application                                       | It is possible that some User Delegations are invalid. Either because they were wrongly setup or because they became invalid over time. For example if a delegation owner or delegated user is no longer an Expense Management user. These user delegations are now marked as Disabled and will not be exported to Continia Online. The administrator can now easily identify disabled delegations and either fix them or remove them in the Expense User Delegation page. | 27907 |
| General Application                                       | We are no longer saving the default dimensions calculated at posting time, back to the original expense document. This has been causing issues in the past and it can lead to errors when posting a document in multiple transactions.&nbsp; | 30811 |
| General Application                                       | We have enabled the feature of signing expense attachments digitally in the French and Belgium localizations. | 31662 |
| General Application                                       | We are no longer marking the Ledger Entries as&nbsp;<span>&quot;System-Created Entry&quot;. This will allow reverting ledger entries posted by Expense Management.&nbsp;</span> <span><span>It also fixes an issue in the Australian localization, where the sales taxes were not posted in the &quot;GST Purchase Entry&quot; and tables alike.</span></span> | 32161 |
| General Application                                       | We have added the following Event Publishers<br>  <br>  Table 6086309 CEM Posting Setup <ul><li>OnBeforeModifyExistingExpense </li> </ul> <ul><li>OnBeforeModifyExistingMileage </li> </ul>  <br>   Table 6086320 CEM Expense<br>  <span><ul><li><span>OnExpenseTypeValidateBeforeExpValidation</span> </li> </ul></span>  <span><ul><li><span>OnAfterNewCalculatedAccount</span> </li> </ul></span>  <ul> </ul> <span></span> | 32188 |
| Mileage                                                   | We've amended the sixty day check with a crude text string comparison on the addresses in cases where geographic coordinates are not available (e.g. legacy data from prior to introduction of the feature). | 31850 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Credit Card Transactions                                  | We've increased the length limit of the Transaction ID to 150 characters. | 13728 |
| Credit Card Transactions                                  | We have fixed the following error when synchronizing the activation of a bank agreement:&nbsp; <ul><li>&quot;<em>The bank does not exist. Identification fields and value Code='',Country/Region Code='' &quot;</em>&quot; </li> </ul> | 31742 |
| Document Approval                                         | We have added a link to setup out of office approval sharing to the Approval Entries page in NAV/BC. | 28378 |
| Expenses                                                  | <span>We have fixed an issue that was causing the &quot;External Document No.&quot; to be empty after posting matched expenses.&nbsp;</span> | 31102 |
| Expenses                                                  | We have fixed a bug on the expense card, where for cases of reverse charge VAT, the VAT and Base Amount was displayed wrongly. | 31410 |
| Expenses                                                  | We have implemented functionality to avoid and enforce the usage of Jobs/Tasks on sales tax allocation lines. Sales Tax allocation will no longer post Job ledger entries.&nbsp;<span>This is especially relevant for the Canada Sales Tax.</span> | 31943 |
| Expenses                                                  | <span>We have fixed an issue in MS Dynamics NAV 2009 R2, when an expense with Jobs was posted. There would have been an error like the one below.&nbsp;</span> <span>This issue doesn't affect other versions.&nbsp;</span> <ul><li><em>&quot;Bal. Account Type must be G/L Account in Gen. Journal Line Journal Template Name='GENERAL',Journal Batch Name='EXPENSE',Line No.='0'.&quot;</em> </li> </ul> | 32562 |
| General Application                                       | We have fixed a caption issue on the &quot;Field Type Dependencies&quot; page. | 26878 |
| General Application                                       | We have fixed a bug where it was possible to reopen/recreate a document from NAV/BC when that document had been deleted by the user in the app/portal. | 27291 |
| General Application                                       | We have fixed an issue that was showing an error if the same filters were applied on similar fields. For example, PD-DESTINATION and P-DESTINATION. | 27407 |
| General Application                                       | We have disabled the drilldown functionality on the &quot;Continia User Name&quot; on all the pages since it was revealing a different result than the lookup on the Continia User ID. This was not only bringing confusion but sometimes it would reveal other issues. | 28322 |
| General Application                                       | Functions or actions modifying Approval Entries could in some cases experience a performance issue. This has been fixed.&nbsp; | 28367 |
| General Application                                       | We have fixed an issue in the add in that was setting a default zoom of 1% on the attachments.&nbsp; | 28658 |
| General Application                                       | We have changed the caption on an action on the bank agreement page from &quot;Request Agreement&quot; to &quot;Request New Agreement&quot;. | 30229 |
| General Application                                       | We have fixed a number of issues related to Continia Users with Limited Document Visibility. Some are related to approvers others are general.&nbsp; <span><br></span> <span>1) A Continia User&nbsp;</span><span>with limited document visibility can only view his or hers own documents.&nbsp;</span><span>The restriction also applied to approvers with limited document visibility.&nbsp;</span><span>Now we allow the next approver of the document to view the document, even if otherwise limited to only view own documents.&nbsp;</span><span>The approver would get the following error message:</span> <span><br></span> <span><ul><li><span>&quot;<em>Document X for User Y cannot be displayed because you only have access to your own documents.</em>&quot;</span> </li> </ul></span> <br> <span>If the approver is also an expense user with delegations the message would be:&nbsp;</span> <span><br></span> <span><ul><li><span>&quot;<em>Document X for User Y cannot be displayed because you are only allowed to handle documents for the following users: Z.</em>&quot;</span> </li> </ul></span> <span><br></span> <span>Where &quot;</span><em>Document</em><span>&quot; would be either Expense, Mileage, Per Diem or Expense Report/Settlement.</span><br> <span><br></span> <span>2) In older versions of Expense Management the message was wrong and looked like this:&nbsp;</span> <span><br></span> <ul><li>&quot;<em>Expense Expense for X cannot be displayed because you only have access to your own documents.</em>&quot; </li> </ul> <br> 3) We also found that in special cases, some users with limited document visibility would have had access to posted per diems where they shouldn't have had access.&nbsp;<span>This has been fixed.</span>  <span><span><br></span></span> <span><span>4) Opening an expense document by choosing View from the reimbursement matrix and release notification entries it was in some cases possible to view the document in the wrong page and to navigate to other documents. This has been fixed.</span></span> <span><span><br></span></span> <br>  <span><span>5) The view document action button in the reimbursement details, approval entries and release notifications had three different icons. They now all have the View icon.&nbsp;</span></span> <span><span><br></span></span> <span><span><br></span></span> 6) In the Approval Entries (Forms only), the press the Show button and then choose the View option. It would not display per diems. This has been fixed.&nbsp; <br> 7) Posted Expenses, Mileage, and Expense Report would not give an error message when a user with limited document visibility opened the Posted Document Card page. The Posted Per Diem card did give a message. This has been changed to that the logic on the Posted Card is the same as on the normal Card.&nbsp; <br> <br> 8) We were missing the Check Data Version on several document card pages. | 30712 |
| General Application                                       | We have fixed an issue where the number of documents was not correct in the Approval Portal.&nbsp; | 30722 |
| General Application                                       | <span>In the EM versions </span><span>8.01 and 4.00.06&nbsp;</span><span>we have corrected an issue where default dimensions were not created at posting time.&nbsp;</span><span>Unfortunately, the change further revealed another issue:&nbsp;</span><span>the default dimension was then used for posting and re-added on the document, instead of the dimension added by the user.</span> | 30737 |
| General Application                                       | We have fixed an issue that was calculating wrong total amounts on the Per Diems, in the Status Report. | 30927 |
| General Application                                       | We have fixed a bug in NAV/BC where the first subdocument line on a Settlement (Expense Report) would not inherit the global dimensions from the main document. | 31238 |
| General Application                                       | A filter on a Field Type of data type &quot;Code&quot; would have not worked unless the value was spelled with capital letters.&nbsp; <span>This has been fixed by uppercasing the filter value.</span> | 31255 |
| General Application                                       | We have fixed a bug where an empty agreement was created, when an activation request was rejected. | 31300 |
| General Application                                       | We have fixed an issue that was causing the error below. It would occur when posting a Per Diem, for a user that was part of a group and there was posting setup only for the group.  <ul><li>&quot;<em>There is no Posting Setup within the filter. Filters: Type: Per Diem,Type Code: ACCOMMODATION.</em>&quot; </li> </ul> | 31553 |
| General Application                                       | We have fixed a bug where it was possible to send a welcome mail to an Expense Management user with an &quot;empty&quot; link to the Expense Portal. | 31566 |
| General Application                                       | We have fixed an issue when the same number series was used for both posted and un-posted settlements. In this case, the posted document would have still increased the number series number when it was not expected to do so. | 31575 |
| General Application                                       | We have improved the caption on the request page of the batch posting of expenses, mileages and expense reports. | 31650 |
| General Application                                       | We have fixed an error in the upload company logo functionality, which would fail silently, and roll back the changes to the company logo. | 32567 |
| Mileage                                                   | On the Approval Entries page, on a mileage, when choosing the action Details.&nbsp;You would get the error message&nbsp;  <ul><li>&quot;<em>Allocations are not supported on mileage</em>&quot;.&nbsp; </li> </ul> Now it will open the page Mileage Details. | 28305 |
| Mileage                                                   | <span>We have fixed an inconsistent&nbsp;error which was present when posting a mileage where the default dimensions were changed during posting. <br></span>The error would come up with messages similar to the ones below.  <ul><li>&quot;<em>The changes to the Mileage record cannot be saved because some information on the page is not up-to-date</em>&quot; </li> </ul> | 30470 |
| Per Diem                                                  | We have fixed an inconsistency error which was present when posting a per diem where the default dimensions were changed during the posting. The error would come up with messages similar to the ones below. <br> &quot;The changes to the Per Diem record cannot be saved because some information on the page is not up-to-date. Close the page, reopen it, and try again.&quot; <br> &quot;Inconsistent read of field(s): 'Global Dimension 2 Code', on table 'Per Diem', identification values: 'Entry No.='xxxx''&quot; | 30813 |
| Platform and Technology                                   | In rare cases wrong Lookup Values Access setup could cause the synchronization with Continia Online to fail. This has been prevented. | 32687 |

## Expense Management 2021 R2 Service Pack 2, Hotfix 2

*Released: February 2, 2022*  
*App version: 8.2.0.2*   

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Platform and Technology | When updating to Business Central 19.3, the receipt or mileage image was no longer shown on any screens, including on the Expense page, the Mileage page, the Settlement page, and the Approval page. This meant it was not possible to see the receipt or mileage image in Business Central.  |

## Expense Management 2021 R2 Service Pack 2, Hotfix 1

*Released: January 19, 2022*  
*App version: 8.2.0.1*   
*FOB version: 8.02.01*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | In Expense Management version 8.1.0.1 we have corrected an issue where default dimensions were not created at the time of posting. Unfortunately, the change further revealed another issue: the default dimension was then used for posting and re-added on the document instead of the dimension added by the user. We have now corrected the issue.  |

## Expense Management 2021 R2 Service Pack 2

*Released: January 6, 2022*  
*App version: 8.2.0.0*   
*FOB version: 8.02.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | On the reimbursement pages it was not possible to reimburse all the users at the same time when the number for the user filter would exceed 1024 characters. When pressing the Reimburse action we now process all the users in the view. |
| General Application | We have changed the reimbursement pages so that they only show the users from the current company. In the past all the users from all the companies were shown on the pages. |
| General Application | We have added a new event:<br>Codeunit 6086312 CEM Approval Management<br><ul><li>OnAfterInitApproverID</li></ul>The event allows to initialize the approver. |
| General Application | We have introduced the possibility to use Tax Area and Tax Group Code on the Mileage and Per Diems. |
| General Application | We have added functionality to inherit Job Task default dimensions, on top of the existing default dimensions. The Job Task default dimensions have the highest priority. |
| General Application | We have added a new event<br>Codeunit 6086319 CEM NAV-version Mgt.<br><ul><li>OnAfterCreateJnlLineDefaultDim</li></ul>This allows dimensions to be changed before posting. This event should be especially useful for adding dimensions before posting transactions. |
| General Application | We are now creating Document Capture permission sets at the same time we are creating the Expense Management ones, in the on-premise versions. Some of these permissions sets are needed, in addition to the Expense Management ones. |
| General Application | When documents would have been registered in advance (for a date in the future) we would have shown an error to prevent document posting. Posting documents ahead is sometimes desired, therefore we changed the functionality to only show warnings instead. |
| Credit Card Transactions | We are now copying the Transaction Business Country/Region to the Expense that is matched to. |
| Credit Card Transactions | It is now possible to create statement transactions from the transaction import journal. |
| Credit Card Transactions | We have made visible the Reject Reason field on the "Agreement Activation Log" page so that it's more obvious when an agrement has been rejected. |
| Per Diem | The default per diem rates are now created without a specific country, to improve the user experience for users that don't actually use the destination country because it is always local. |
| Expenses | We have improved the posting description when posting a Settlement with expenses where the Business Vendor was specified. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | We have fixed an issue on the Posting Setup, when copying the Expense or Mileage Account to the actual document. If no account was found on that user, it would have taken a posting account from any other user. |
| General Application | We have fixed an issue that was leading to desynchronization issues on subdocuments belonging to a settlement. When documents were being downloaded in Business Central, if the user would have modified the documents in the exact same split of a second, the last change of the user would have never been downloaded inside Business Central. The sub-document would have failed in the Inbox with an error. |
| General Application | We are now preventing non-reimbursable expenses to be sent to the Lessor/Bluegarden payroll interfaces. |
| General Application | We have fixed an issue in the Lessor integration codeunits where the Expense Management description was always overwritten by the Pay Type description. |
| General Application | In previous versions we had blocked the possibility for specifying Field Dependencies where the TASK could expect a specific value. This check has been removed and we do now allow for this again. It is now up to the user to ensure that the selected Task Code exists in all Projects. If a required Task Code does not exist in the selected project, the dependency will simply be ignored. |
| General Application | When synchronizing, there was functionality to recalculate mileage across all companies. This code was triggering permission errors when the user that synchronizes would have not had permissions on all the companies. We have changed the functionality so that it skips the calculations when the user doesn't have enough permissions. We do not foresee a major downside in doing so, as this calculation was mostly for presentation purposes. A mileage will always be recalculated before posting. |
| General Application | We have fixed a translation issue that was causing confusion when sending welcome e-mails from the Continia User Setup list. The translations affected the Danish and German languages. |
| General Application | We have fixed the following error when loading a PDF file in the add-in. Please reinstall the add-in components.<br><em>"A generic error occurred in GDI+"</em>. |
| General Application | We have fixed an issue in the field dependencies area, where the error below would have prevented the calculations<br><br><em>The length of the string is 273, but it must be less than or equal to 250 characters. Value: The following users don't have access to value SALES in the field DEPARTMENT:[A very long list of users]</em>. |
| General Application | We have prevented the following error when synchronizing. If a user didn't have the CEM-SUPER permission set but had some basic Expense Management permissions, he would have gotten a similar error when he was trying to modify a Job or a Task, for example. The error would have occurred in areas of standard Business Central, but when using a field type was configured in Expense Management over that table (for example, Job/Task)<br><br><em>"You do not have the following permissions o TableData CEM Field Type: Modify"</em>. |
| Expenses | Attendees were not copied to the Sales Tax allocation lines in the Canadian localization, when synchronizing expenses from Continia Online. |
| Expenses | When posting a Settlement with expenses having a Business Vendor, in some cases the external document number was set from the next document. |
| Mileage | We have prevented creating a mileage rate without starting date. |
| Per Diem | On the Per Diem, the number of hours was rounded to the next full hour, resulting in calculation problems when sub-rates were used. |
| Per Diem | When generating demo data, the allowance codes were not set on the Per Diem Group. We have fixed the issue. |
| Credit Card Transactions | Some actions related to the transaction processing were not available on the Expense when there was no agreement activated. This proved to be too restrictive since transactions can be imported manually, without an agreement. We changed the functionality so that it shows Transactions related actions always when there are transactions in the inbox. |

## Expense Management 2021 R2 Service Pack 1, Hotfix 3

*Released: December 17, 2021*  
*App version: 8.1.0.3*   
*FOB version: 8.01.03*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | In the Spanish localizations, the Employee number was not shown on the Continia User Setup pages because of a limitation of this type of posting. Some customers have started to use the system as such, so we have decided to keep the field even though in some situations this scenario will anyway be prevented by standard Business Central checks. |

## Expense Management 2021 R2 Service Pack 1, Hotfix 2

*Released: November 24, 2021*  
*App version: 8.1.0.2*   
*FOB version: 8.01.02*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | We have fixed an error when using the business vendor feature which was showing the following message.<ul><li><em>"Purchase Invoice EXPENSE 1 already exists for this vendor."</em></li></em> |
| Expenses | When posting a reconciliation journal, the following error would appear if the statement lines were manually inserted (without having an underlying statement transaction).<br><em>The Bank Transaction does not exists. Identification fields and value Entry No. = "0"</em> |
| Expenses | For the Spanish localization, the Document Type is only specified when documents are posted to the business Vendor. The Document Type is no longer specified for the employee vendor. |
| Expenses | We have fixed an inconsistency error which was present when posting an expense where the default dimensions were changed during the posting. The error would come up with messages similar to the ones below.<br><br><em>"The changes to the Expense record cannot be saved because some information on the page is not up-to-date. Close the page, reopen it, and try again."</em><br><br><em>"Inconsistent read of field(s): 'Global Dimension 2 Code', on table 'Expense', identification values: 'Entry No.='xxxx''"</em> |
| Per Diem | On the Per Diem validation we would sometimes show a wrong error message similar to the one below. This is due to a wrong calculation.<br><br><em>“There is no rate for the destination '' for the 08-06-21.”</em> |
| Per Diem | We have fixed the following error message on the Per Diem, so that it shows the correct date in the placeholder.<br><br><em>"There is no rate for the %2."</em> |


## Expense Management 2021 R2 Service Pack 1, Hotfix 1

*Released: November 8, 2021*  
*App version: 8.1.0.1*   
*FOB version: 8.01.01*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Pre-approved settlements with amounts exceeding the pre-approved amount are now sent for approval rather than having status "Open". At the moment, this is not what happens in EM 8.01 Business Central 2019 Spring (BC14). |
| General Application | The automatic allocation did not work in Canada, in Business Central 2019 Spring (BC14) client due to a missing object. |
| General Application | Preview posting was sometimes failing with the error below when default dimensions were configured on accounts that were external to Expense Management (for example, a G/L Account). The functionality would have tried to copy those default dimensions back to the expense document. The functionality was failing to find the Expense Management document because, in preview mode, the relation between the expense document and the un-posted document '\*\*\*' doesn't exist.<br><br><em>The Expense Header does not exist. Identification fields and values: Document Type='Settlement',No.='\*\*\*'</em>. |
| General Application | "Tax Area Code" and "Tax Group Code" were missing on the Settlement expense subpage. |
| General Application | When sending a reminder email with two or more recipients, the following error would have occured:<br><br><em>“The email message has been deleted by another user.”</em> |
| Expenses | When specifying a business Vendor on the Expense, if the employee Vendor would have had a currency code, the expense could not be posted. We have, instead, created a balancing line on the same currency code. |
| Expenses | We have fixed an issue where the Tax Group Code was not copied from the Expense Type setup to the Expense. |
| Expenses | In a settlement where Cash and non-Cash expenses would have been found, out of which some had Jobs specified, the balancing account would have been calculated incorrectly and therefore the expense would be posted as if it was Cash when the expense was not marked as such. This is found in systems where "Matching Required" is Never. |
| Expenses | When selecting a Vendor on the expense, in some specific cases, the balancing amount was incorrectly calculated to 0. The expense could not have been posted, then. We have fixed the issue. |
| Expenses | On expense with "Vendor No." specified, in some specific cases, the following error would have occurred. That was because the posting currency was incorrectly calculated.<br><br><em>"Currency must be in Bank Account MASTERCARD".</em> |
| Expenses | We have fixed an issue that was leading with 0 amounts in the automatic allocation lines of the sales tax. This was happening only when the Expense was not yet inserted but the Tax Area and Tax Group would be specified. |
| Expenses | We have fixed an issue where automatic allocations (due to Sales Tax) would not inherit Extra Fields values from the main expense to the allocation lines. |
| Expenses | When automatically allocating due to sales taxes, the Tax Area Code was not copied to the tax lines. If "TAX AREA CODE" was a mandatory field, the expense would have encountered an error in the mobile app, preventing the sending. The user were supposed to manually type the "TAX AREA CODE" values on all the allocation lines. |

## Expense Management 2021 R2 Service Pack 1

*Released: October 1, 2021*  
*App version: 8.1.0.0*   
*FOB version: 8.01.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Pre-approved settlements with amounts exceeding the pre-approved amount is now send for approval, rather than having status "open". See also the changelog for the [Web Approval Portal](Web Approval Portal.md). |
| General Application | We have added multiple new Event Publishers. The updated list can be found [here](https://continia.zendesk.com/hc/en-us/articles/360020969779-Expense-Management-Event-Publishers). |
| General Application | We now display validation comments on settlements. |
| Country and Regional | The Faroe Islands localization is now supported in Business Central online. |
| Country and Regional | The Greenland localization is now supported in Business Central online. |
| Credit Card Transactions | We have added support for TAB sepparated files in the Transaction Import. |
| Per Diem | In the Per Diem rates page we have added an action for opening the Per Diem Groups. |
| Per Diem | We have introduced the possibility to control the default selections on a Per Diem, based on setup. On the Expense Management Setup the field "User chooses deductions" will make all per diem details to be set when creating new documents. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | Improved captions on the Continia User list. |
| General Application | It was not possible to export expense attachments in the "old" web client on NAV installations. |
| General Application | We have fixed an issue where the payment of a document didn't change the state in the Expense App for a purchase invoice. |
| General Application | We have added the per diem destinations in the status report. |
| General Application | Improved captions in connection with Expense Approver ID. |
| General Application | We have added the pre-approval settlements in the status report. |
| General Application | Improved captions on the per diem detail page. |
| General Application | In the Configured Fields form in the classic client we displayed the following message in English: "Details are only displayed for Per Diem". Now the message is translated to the user's language. |
| General Application | Reopening a document was not possible if there were unproceessed inbox entries. We are now allowing reopening if the document is Pending Approval or Approved. |
| General Application | User Delegation was translated to User Responsibility in several languages. This was fixed in the Menu and in the User Delegation Page. |
| General Application | The Expense Management version was wrongly stated as "Expense Management 2021 R1" in the About Continia Expense Management page and in the Solution Management page. We have corrected to "Expense Management 2021 R2". |
| General Application | Approval notification was not sent in the Expense App for a document that was automatically sent for approval.<br><br>Approval notification was not sent in the Expense App for a document that was automatically approved due to company policies. |
| General Application | We have added the pre-approval amount and status to the settlement approval entries page in both NAV/BC and the Web Approval Portal. |
| General Application | On the Settlement Card in the Classic client (NAV 2009 R2), when displaying a Per Diem line on the Settlement, and choosing Card from the Line menu button, it would display a Mileage. |
| General Application | A settlement submitted for pre-approval was not send back to the user, when approved or rejected by his/her approver. |
| General Application | Improved captions in Dutch. |
| General Application | Improved translations on the Continia Setup User page. |
| General Application | Added pre-approval fields to the settlement list, when the feature is enabled from Expense Management Setup. |
| General Application | Force approval of pre-approval requests would not update the pre-approval status correctly, or send the settlement back to the expense user. |
| Expenses | It was not possible to add allocations to an Expense in the classic client. |
| Expenses | When expenses were allocated based on the sales tax the functionality was not calculating correctly the tax amount. |
| Expenses | We have added the missing "Vendor No." field on the expense-related forms. The field is necessary to enable post-to-business-vendor functionality. |
| Expenses | Mismatch in the decimal places on the allocations would have triggered the error below, when the expense was posted. This was due to the fact that the amounts on the allocations would not fit to the total amount, leaving some decimal differences. These errors will now be signaled in the comment section and user input will be neccessary. The error is more user friendly.<br><br><em>"The transaction cannot be completed because it will cause inconsistencies in the G/L Entry table. Check where and how the CONSISTENT function is used in the transaction to find the reason for the error.<br><br>Contact your system administrator."</em> |
| Expenses | When sending a reminder email to the expense users we would in some cases give a wrong message or no message to explain the choices.<br><br>Wrong message: "This expense contains values that have not been synchronized to Continia Online. This is required before this expense can be sent to the expense user. Would you like to synchronize values with Continia Online?"<br><br>The message should have said: "Do you want to send a status e-mail to all the users or only to the selected ones?" |
| Expenses | We have fixed an issue where a promoted action on the expense allocations page would have said Category 4 instead of the actual caption. |
| Expenses | We have fixed an issue that didn't allow the Approver to change allocation lines. |
| Expenses | We have fixed an issue where the Tax Group Code was not copied from the Expense Type setup to the Expense. |
| Expenses | In some cases it was possible to edit Dimensions on approved documents. We have changed this to follow the logic on the document. So if you can edit the document, then you can edit the dimensions. |
| Mileage | In Microsoft Dynamics NAV 2013 the menu suite was still showing the "Default Vehicle per User" page which has become obsolete once we introduced the "Default Continia User Setup" functionality. The corresponding table is deleted in the upgrade routines, so the following error was received when trying to open the page.<br><em>"Cannot build the page 6086403. The metadata object Page 6086403 was not found."</em> |
| Mileage | It was not possible for a user with permission to edit approved documents to edit a mileage on the card form. |
| Per Diem | On the Per Diem list and card we are controlling the visibility of the "Departure Country/Region" and "Destination Country/Region" based on the setup that enables multiple destinations. |
| Per Diem | Per Diem rates are re-calculated when changing destinations. |
| Per Diem | When posting a per diem with multiple destinations (which had different posting setup) the functionality would not take into consideration the different setup for each destination. |
| Per Diem | When using multiple destinations on a Per Diem there was a calculation error when the user would return in the home country, after he's been travelling abroad. The rate was calculated for the foregin country instead of the home country. |
| Per Diem | When enabling multiple destination on the Per Diem, the functionality was always requesting for a default Per Diem rate (countr code empty). We have avoided these error messages. |
| Platform and Technology | A user with a limited permission set including CEM-NAVUSER could not use the function Send to Expense User on the pages Expense Card or Expenses.<br><br>The user would get the following message: You do not have the following permissions on TableData CEM Synchronization Log: Read. |
| Platform and Technology | Many tooltips were missing in the main areas of Expense Management. We have corrected the issue. |
| Document Approval | The field Settlement Pre-approval in the Expense Management Setup page was not translated and was thus displayed in English in all local versions. |
| Credit Card Transactions | Attempting to send a request for activation of a bank agreement in Demo, now results in an error immediately after pressing the action. |
| Credit Card Transactions | Additional filter added when linking an activated bank agreement, to avoid conflicts in cases where different banks use the same agreement no. |
| Credit Card Transactions | We have disabled the "next" button in the Agreement Activation Wizard, when all required information has not been provided. |
| Credit Card Transactions | Added a missing duplicate on the bank transaction id, when importing transactions with the manual import tool. |
| Credit Card Transactions | In BC18 and onwards it was not possible to do field mapping. We have fixed this. |


## Expense Management 2021 R2

*Released: September 1, 2021*  
*App version: 8.0.0.0*   
*FOB version: 8.00.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  |
| --------------------------------------------------------- | ------------------------------------------------------------ |
| General Application                                       | It's now possible to allow selected users to edit approved documents in Expense Management. In the Continia User Setup, set the flag Can Edit Approved Documents. These users can now edit a selection of fields on documents with the status Pending Approval and Released. Fields that influence amounts on documents can't be modified unless a document is reopened and approved again. |
| General Application                                       | It's now possible to pre-approve settlements. The feature has to be enabled in the Expense Management Setup. |
| General Application                                       | It's now possible to post to a business vendor on an expense. This can be useful when the business vendor is known, and the transaction has to be visible in ledger entries. The functionality is activated by adding a "Vendor No." on an expense. |
| General Application                                       | The "send welcome email" feature has been expanded. Now, you can choose between sending/re-sending an email to a selection of users or just sending it to all the users who haven't received it yet. |
| General Application                                       | With the release of Expense Management 2021 R2 (8.00), we now support the modernized email communications in Dynamics 365 Business Central 2021 Wave 1 and newer. Expense Management uses the default profile when sending out emails. |
| General Application                                       | <b>With the release of Expense Management 2021 R2 (8.00), Dynamics NAV 2009 RTC (Role Tailored Client) is no longer supported. NAV 2009 Classic Client will still be supported, and RTC is also still supported for Dynamics NAV 2013 and newer versions.</b><br><br>Even though Dynamics NAV 2009 RTC in Expense Management 2021 R2 (8.00) is no longer supported, Dynamics NAV 2009 RTC will be supported in future service packs released for Expense Management 2021 R1 (7.00)<br><br><b>When Expense Management 2022 R1 (9.00) is released in April 2022, no objects for the obsolete Dynamics NAV and Business Central versions will be released. Expense Management 2022 R1 (9.00) will only be released for Business Central 14 and newer versions.</b> |
| General Application                                       | It's now possible to upgrade from older versions – as early as EM 2.60 – to EM 8.00 in one step. See the upgrade documentation for details. |
| General Application                                       | The name of the page Default Continia User Setup has been changed to Continia Users Default Setup. |
| General Application                                       | A cue displaying the number of approval entries awaiting action has been added. When you select this tile, the Approval Entries page opens. |
| General Application                                       | We have marked the method CalcLookupValForFieldAndParent as "external" in the table 6086345 "CEM Field Type". |
| General Application                                       | When generating demo data, an agreement with ID 11111111 was created. That no longer happens, as the new agreement activation doesn't expect an ID to be provided. |
| General Application                                       | The functionality that was dependent on permission set names has been improved, so that renaming permission sets will not affect behavior. In connection with this change, the functionality related to the CEM-NAVUSER permission set (limiting the documents that a user can view) was replaced by the "Limit Document Visibility" property in the Continia User Setup. The upgrade routine will update the new value. |
| Expenses                                                  | We have added the possibility to specify if an attachment is recommended, optional or mandatory on an expense type. The rule will then be respected in the Expense App and the Expense Portal. |
| Expenses                                                  | New fields containing the VAT amount and the amount without VAT have been added on the expense card and the expense split and allocate page. |
| Transactions                                              | The activation flow for the bank agreement has been changed. The user will be asked to provide transaction details, and if all conditions are met, Continia's support will activate the agreement. |
| Country and regional                                      | Support for per diem trips through different countries has been added. |
| Document approval                                         | Performance optimizations have been done in regard to approval flows. |


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | When trying to export the approval template or the reminder template from the Expense Management Setup page, no message was displayed if there was no template. This has been changed, so that if there's no template, the actions Export Template and Delete Template are hidden. |
| General Application | In Field Type Dependencies, the condition "Has a specific value" and the expectation "Must have a specific value" can only be used for field types that meet specific conditions. If used with other field types, the Field Type Dependencies page displays an error message explaining the reason why. Field types must be of the type Code, must have lookup values, and must not depend on a parent field type. |
| General Application | In extension-based versions of Business Central, the add-in on the settlement card wasn't refreshed when navigating to per diem lines, which it is now. |
| General Application | It was possible to post documents with a job but without a task. This was misleading, and an error message is now displayed when a task is expected. |
| General Application | The fields Employee Number and Employee Name have been removed from the Spanish version because employee posting would still require vendor information. |
| General Application | The Notification Outbox cue had a rather long Danish translation "Ubehandlede notifikationer". This has been changed to "Fejl". |
| General Application | The error SET-NOT-FOUND isn't displayed anymore when a settlement is reopened. |
| General Application | In MS Dynamics NAV 2009 RTC, the expense fact box was not displayed. This issue has been fixed. |
| General Application | A confirmation dialog that was displayed when web services were created in Expense Management has been removed. This was causing a problem when upgrading from EM 6.50 to 7.00.<br><br><em>"The function UpdatePerCompany in the company initialization codeunit 6086102 in company XXX. has failed due to the following error: 'Microsoft Dynamics NAV Server attempted to issue a client callback to show a confirmation dialog box: Do you want to update all web services for Continia Online? (CodeUnit 6086360 CEM Create Web Services). Client callbacks are not supported on Microsoft Dynamics NAV Server."</em> |
| General Application | An issue causing the error "You do no have the following permissions on CodeUnit CEM Business Setup Management Execute" when opening Business Setup was fixed. |
| General Application | A scenario where a document could be recreated by the expense user (in the Expense App or the Expense Portal) after the document was deleted from Business Central because updates were allowed has been blocked. |
| General Application                                       | Improvements to translation quality, especially the French translation. |
| Expenses | Bank transactions could be blocked in the Bank Transactions Inbox if the posting date was outside the allowed posting dates. For example, when the previous period had been closed, and the bank transactions arrived a few days later. It's now possible to change posting date, but only if the imported posting date is in a closed period. The error text on the Bank Transaction Inbox entry has been improved. |
| Expenses | When an expense was reopened and re-sent to the user, there would be a notification as if the document was new. The notification has been changed to reflect that it's an update. |
| Expenses | When trying to merge an allocated expense, you would get the error message "Expense %1 cannot be merged when it has been allocated to one or more lines". With this update, the parameter %1 will be updated with the expense entry number. |
| Mileage | It was possible to change dimensions on a posted mileage. With this release, that's no longer possible. |
| Mileage | An issue that was causing job ledger entries to be posted twice on a mileage has been fixed. The issue was introduced in EM 7.00. |
| Per Diem | When a per diem with the status Pending Expense User was changed, an update was not sent to Continia Online. This issue has been fixed. |