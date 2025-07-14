---
title: Detailed Changelog for Continia Expense Management 2022 R1
date: 24-04-2024
description:  
id: 
lang: en
---
# Detailed Changelog for Continia Expense Management 2022 R1

This article lists all new features and bug fixes for each version of Continia Expense Management 2022 R1.

> [!IMPORTANT]
> This version of Expense Management is no longer supported. As a consequence of this, Continia will no longer correct any errors appearing in this version, and no further service packs relating to the version will be released. For supported versions of Expense Management, see [Software Lifecycle Policy and Continia Document Capture On-Premises](@EM-104).

> [!TIP]
> As a Continia partner, you can be notified of new Expense Management versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005316840-Receive-a-notification-upon-new-Expense-Management-releases) in the Continia PartnerZone (only available to partners).

## Expense Management 2022 R1 Service Pack 7

*Released: April 24, 2024*  
*App version: 9.7.0.0*  
*FOB version: 9.07.00*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | Id |
| --- | --- |  --- |
| General Application|On a&nbsp;<span><b>Payment Type&nbsp;</b>&nbsp;when&nbsp;<span><b>Matched to Expense </b>was set to&nbsp;<span><b>Never Required, </b>the fields related to the matching (variance, etc.) were not cleared of their values, this resulted in an error later in the process.</span></span></span> |50326|
| General Application|We have added <b>CEM Pre-Cloud Migration Wizard </b>in the departments, so it is searchable.&nbsp; |54838|
| Mileages|When synchronizing with Continia Online, a mileage recalculation is automatically triggered in all the companies for all the mileage rates available in the company and for all the mileages with status not posted. Because of the calculation on each mileage rate, the same mileage was recalculated multiple times, and this was causing performance issues. |41445|
| Mileages|<span>The system went into a stage of a never-ending loop, if the date on&nbsp;<b>Starting Distance,&nbsp;</b>to calculate a </span>lower rate than the main rate, was different from the date on the main rate.&nbsp; |51566|

## Expense Management 2022 R1 Service Pack 6

*Released: November 6, 2023*  
*App version: 9.6.0.0*  
*FOB version: 9.06.00*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|We have addressed an issue where parallel processes downloading transactions could potentially result in duplicated entries in the bank transaction inbox. |47472|
| Expenses|In Canadian localization, when a user created expense allocations marked as non-taxable, the system incorrectly allocated them as taxable amounts for sales tax purposes. |43601|
| General Application| Previously, when transitioning from File Storage or Azure to Database, encountering an error during the deletion of old files would result in a complete rollback of the process, leading to the loss of already deleted files. We have now implemented a change to handle each document individually, allowing for the possibility of repeating the process in case of errors and enabling recovery of the deleted files. <br> |47561|
| General Application|Resolved the issue that was using the&nbsp;<span>default email scenario instead of the actual scenario that was set-up.&nbsp;</span> |47699|
| General Application|<span></span>The codeunit 6086569 &quot;CEM Update Field Dependencies&quot; in the Job Queue now correctly calculates the lookup values.<span></span> |47730|
| General Application|Configured fields settings like <b>Hide Visibility, Editable </b>and<b> Mandatory </b>were overwritten when clicking <b>Reset to Default Setup </b>in Configured Fields. This was also happening automatically if settings were changed in the Expense Management Setup page. |47940|
| General Application|When posting Per Diem in foreign currencies, the exchange rate was calculated based on the current travel day and not based on the posting date. |48113|

## Expense Management 2022 R1 Service Pack 5

*Released: May 24, 2023*  
*App version: 9.5.0.0*  
*FOB version: 9.05.00*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| Expenses                                                  | The total amount displayed on the expense card without VAT is incorrect when Reverse VAT is applied. | 46594 |
| Expenses                                                  | Default dimensions on Employee are not checked on expense allocations. | 46639 |
| General Application                                       | UNABLE-DEPR error displayed for a completed document that was later attached to an expense report. | 43696 |
| General Application                                       | After attempting to update a posted document from the inbox, all subsequent inbox entries are marked as Accepted. | 44410 |
| General Application                                       | The Taxable Meal Allowance field is shown on the Per Diem Rate Details even when taxable Per Diem rates are disabled. | 45143 |
| General Application                                       | Posting documents belonging to an Expense Report when the posting reports were added to the Job Queues. | 45593 |
| General Application                                       | Possibility to delete an Expense Report Inbox independently of the Status. | 46484 |
| General Application                                       | When processing notification outbox entries, it was possible that multiple processes would run in parallel, sending multiple updates of the same documents in Continia Online.&nbsp; | 46514 |
| General Application                                       | Reminder emails to approvers display the wrong currency for expense reports. | 46690 |
| Mileages                                                  | When using Taxable rates on Mileage and Per Diem, the amount posted adds the taxable amount twice. | 44396 |
| Per Diem                                                  | Whenever using per diem sub-rates, a per diem starting precisely at midnight (00:00) adds an extra full day allowance to the calculation. | 44537 |
| Per Diem                                                  | The configured field "Billable" on a Mileage or Per Diem is overwritten to True when downloaded in Business Central. | 46079 |
| Per Diem                                                  | When clicking on the "0" value in the Allowance Rates on a Per Diem group, a dialog prompts the user to create a rate automatically. In certain localizations, the new rate has a wrong date format resulting in an error. | 46678 |



## Expense Management 2022 R1 Service Pack 4

*Released: January 27, 2023*  
*App version: 9.4.0.0*  
*FOB version: 9.04.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|We are now adding default dimensions on the expense allocations, similar to expenses.&nbsp; |44141|
| Per Diem|Per Diem calculations are now done on a day-to-day basis in the German, Austrian and Switzerland localizations, as opposed to the past when the sub-rates were applied only to the last day. |43238|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|We have added an error message on the expense, if the <span>chosen<span>&nbsp;</span></span>payment type is missing a Bal. Account No. and Refund User is false. |42275|
| Expenses|When trying to &quot;Get Expenses&quot; from an Expense Report, when the expense would have been matched, the following error was shown: <br> <ul><li><em>Matched to Bank Transaction must be equal to 'No' in Expense: Entry No.=&lt;EntryNo.&gt;. Current value is 'Yes'. </li></em> </ul>  |42497|
| Expenses|When posting allocations on an expense with the external reimbursement method set up, an error would not allow the expense to be posted. <br> <em><ul><li><span>Allocation with Entry No. &lt;No.&gt;: Expense Account is missing. Posting Setup for Expense Type 'FOOD' is most likely not configured correctly.</span></em> </li> </ul>  |43536|
| Expenses|We have fixed an issue when detaching an allocated expense from an Expense Report that was causing the following error:<br><ul><li><em><span>This expense has been allocated and therefore you cannot change Amount.</span><br></em> </li> </ul> |44036|
| General Application|We have fixed a bug in the document add-ins, where clicking on the add-in on a document with no attachment, would result in a download of a random attachment. |42313|
| General Application|We have fixed a bug in the &quot;Upload Company Logo&quot; action on the Expense Management Setup page which prevented the logo from being sent to Continia Online, and consequently shown to app users. |42717|
| Mileages|Wrong comments were shown on the posted Mileage card (belonging to expenses rather than mileage). |43230|
| Mileages|<span>The event&nbsp;</span><span>OnBeforeCheckMileage was never used in&nbsp;</span><span>Codeunit 6086344 CEM Mileage - Check. Instead,&nbsp;</span><span>OnAfterCheckMileage was wrongly called from two locations.</span><br> |43978|
| Per Diem|The amount shown on a Per Diem was wrong in the Expense App and Expense Portal when a per diem had multiple currencies. We are now showing the total amounts in the local currency. |42537|
| Per Diem|<span>When multiple accommodation types were enabled on a Per Diem, the Accommodation Type field was not visible in the Per Diem Details Inbox page.&nbsp;</span><br> |43276|

## Expense Management 2022 R1 Service Pack 3

*Released: October 31, 2022*  
*App version: 9.3.0.0*  
*FOB version: 9.03.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|For Sales Tax allocation, the sales tax amount will be distributed into multiple lines in the event that an expense has already been allocated.  |38588|
| Expenses|Expense Allocation action is added to the Posted Expense Card. |39149|
| Expenses|<span>It is now allowed to delete a Payment Type, <span>as long as there are no un-posted documents.&nbsp;</span></span>  |40335|
| Expenses|<span>The field Job Line Type has been made editable on the following pages:&nbsp;</span><br> <span><ul><li><span>Expense Card and&nbsp;</span>Expenses </li><li>Mileage Card and Mileage </li><li>Per Diem Card and Per Diem </li><li>and the respective subpages on the Expense Report. </li> </ul></span>   |40916|
| Expenses|<span>We have added the following Event Publishers<br></span><br> Codeunit 6086308 CEM Expense Inbox-Transfer<br> <ul><li>OnAfterExpenseInboxTransfer </li> </ul> |41366|
| Expenses|<span>The expense and mileage system fields &quot;Gen. Bus. Posting Group&quot; and &quot;VAT Bus. Posting Group&quot; were not available in field types and could not be configured.</span>   |41950|
| General Application|<span>The fields&nbsp;&quot;Gen. Bus. Posting Group&quot; and &quot;VAT Bus. Posting Group&quot; have been added to the expense and mileage tabs on the Expense Report Card page.</span> |41056|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|Allocations did not inherit standard dimensions from the employee.&nbsp; |35143|
| Expenses|On the Payment Types page, the caption &quot;Default Payment Type&quot; has been changed to &quot;Apply to all Expense Users&quot; |38899|
| Expenses|An issue has been fixed that was causing decimal differences in the sales taxes appended to the Purchase Invoice when the user would not have changed the sales taxes allocated amount.  |39083|
| Expenses|An issue in the sales tax was causing the following error to be shown, even though the sales tax differences were within the setup ranges. This has been fixed. <ul><li><em>Government Sales Tax Expense Type 10 must not exceed General Ledger Setup Max. Tax Difference Allowed 5.</em> </li> </ul> |39337|
| Expenses|<span>Digital signing of expense attachments is now enabled in&nbsp;</span><span>demo environments.</span> |39582|
| Expenses|The&nbsp;<span>Expense Report (Settlement) posting date is used to post all the sub-documents on the same date. However, on an expense, the exchange rates were not calculated in regard to that date, but based on the &quot;Document Date&quot;.</span>  |41026|
| Expenses|When validating the expense “Document Date”, a recalculation of exchange rates will happen. |41027|
| Expenses|The expense report posting date is used for recalculating the currency exchange rates for expenses. Now amounts are recalculated to reflect currency exchange rates on expenses in an Expense Report (Settlement). Until now, these were only updated at posting time. |41029|
| Expenses|<span>An issue has been fixed, resulting in an error where an allocated expense would have an allocation without a Job Task specified when the original expense had a Job specified. The error can be bypassed if the main expense Job is removed.</span><span><em><ul><li><span>Job Task No. must have a value in Expense Allocation: Entry No.=53. It cannot be zero or empty.</span> </li> </ul></em></span>  <ul> </ul> |41145|
| Expenses|When pressing &quot;Show not matched&quot; on the Reconciliation page, filters were applied only on the left side sub-page, but not on the right-side sub-page.&nbsp; |41368|
| Expenses|<span>When posting a matched expense in&nbsp;</span><span>a system where posting transactions at import was disabled, when the expense currency matches the Bank Account currency, the posting amount was the result of an Amount LCY converted to the Bank Account currency. This was not necessary since the Bank Account currency matches the Expense Currency.</span> |41807|
| General Application|When changing the &quot;Expense Reminder Code&quot; or &quot;Expense User Group&quot; on the &quot;Continia User Setup&quot;, it was possible to add non-existing values and the system would have accepted it. |29465|
| General Application|The field Approver Name was editable in View mode on the Continia User Setup Card page. |34815|
| General Application|<span><span><span></span></span></span> If the field DESCRIPTION is not configured on Expense Reports, the user will get the following error message, even if the use of Expense Report is disabled in Expense Management Setup.<br> <ul><li><em>DESCRIPTION is a required Expense Report system field. Please configure it before synchronizing.</em> </li> </ul> The workaround is to run the Reset to Default Setup action on the Configured Fields page. The check will now only include required fields for enabled functionality. |38875|
| General Application|From the Expense Setup page, when choosing Manual Setup, the page will only show the entries for Expense Management. Filters for Continia Core setup have been added as well. <em><br></em> <span>When choosing Open Manual Setup on Continia Users Default Setup the Expense User Delegation opened. This has been fixed.</span>    |39092|
| General Application|The issue where it was possible to export O365 users to Continia Online with a blank email address has been fixed. |39274|
| General Application|An issue when batch-posting documents, that resulted in the following error, has been fixed. <br> <ul><li><em>Status must be Open or Pending Expense User in Expense 1.</em> </li> </ul> |39452|
| General Application|When an Expense Report would change status in the Expense Report Card (for example, when being approved), and then when closing this page and coming back to the Expense Report list,&nbsp;<span>wrong values would have been shown in the Comments, Details and &quot;Amount LCY&quot; areas. This issue was found in the Web Client.&nbsp;</span> |39454|
| General Application|When having an expense with a negative amount, in the Expense Report the Paid Out Amount was not visible.&nbsp; |40759|
| General Application|A permission issue that could result in the following message has been fixed:&nbsp; <ul><li><em>You do not have the following permissions to TableData Employee Ledger Entry: Read </em> </li> </ul> |40808|
| General Application|When downloading a document which was ready to be automatically sent for approval but the user didn't have an approver, the synchronization process would have failed with the following error. <ul><li><p><span><em>The changes to the Expense Inbox record cannot be saved because some information on the page is not up-to-date. Close the page, reopen it, and try again.</em></span> </p> </li> </ul> |41481|
| General Application|When adding an email address written in capital letters (ex: <span>USER@</span>DOMAIN.COM)&nbsp;in the field &quot;<span>O365 Authentication Email</span>&quot; in Continia User Setup, the following Expense Inbox error would have occurred, after a syncronization. <ul><li>The field Continia User ID of table Expense contains a value &lt;<span>USER@</span>DOMAIN.COM&gt; that cannot be found... </li> </ul> |41690|
| General Application|When posting an expense report with a very long posting description, you would get the following error message: <ul><li><em>The length of the string is &lt;length of posting description&gt;, but it must be less than or equal to 50 characters. Value: &lt;posting description&gt;</em> </li> </ul> |41776|
| General Application|When creating Lookup Value Access setup on a child field (for example TASK, related to JOB) the rule was never exported to Continia Online, therefore all the values were still available for selection in the Expense App and in the Expense Portal. |41955|
| Mileages|When attempting to modify a mileage rate that is already used for posting mileage entries, you would get the following error message.&nbsp; <ul><li><em>One or more mileage have been posted after &lt;fieldValue1&gt; and &lt;field2&gt; can therefore not be changed.</em> </li> </ul>The&nbsp;<em>&lt;fieldValue1&gt; </em><span>was intended to be the start date of the mileage rate but was showing random values from the mileage rate, making the error message unclear.&nbsp;</span>  |38492|
| Mileages|<span></span> An issue in the Company Policies that was resulting in the following error, has been fixed. The issue was occurring when opening Company Policies from the drill down, on the field. <ul><li><em>The field Document Account No. of table Company Policy contains value (PRIVATE CAR) that cannot be found in the related table (Expense Type)</em> </li> </ul> <ul> </ul> <span></span> |40815|
| Mileages|A user who has the permission set CEM-NAVUSER, would get the following error when creating a mileage. <ul><li><em>You do not have the following permissions on the TableData CEM Mileage Detail: Modify.</em> </li> </ul> |40953|
| Mileages|An issue in the mileage calculation, where in a very specific situation, the low mileage rate was wrongly assigned instead of the high rate have been fixed. This happened when a mileage existed in 2 periods and when the sum of the total distance driven by a user was exceeding the low rate. |41111|
| Mileages|When setting up Expense Management Setup to show extra fields on the &quot;Posted Mileage&quot; and &quot;Posted Mileage Card&quot;, the system would have been presenting extra fields for expenses instead. |41345|
| Mileages|<span>When exporting configurations through the Expense Management Assisted Setup Guide, decimal values were converted to integers (e.g., 1.23 was converted to 123). This impacted mileage rates.</span> |42127|
| Per Diem|In Per Diem Rate, when choosing the Calculation Method &quot;Sub rates&quot; under First and Last Day Setup and e<span>ntering a number of hours greater than 24 in the Minimum Stay (hours) field, the following error message would occur:&nbsp;</span> <ul><li><em>The length of the string is 13, but it must be less than or equal to 10 characters. Value: ACCOMMODATION</em> </li> </ul>The message has been changed to&nbsp; <ul><li><em>Minimum Stay (hours) cannot be more than 24. Per Diem Rate - Tax-Free Meal Allowance will be used for periods longer than a day.</em> </li> </ul>  |38529|
| Per Diem|When setting the First and Last Day Setup, Calculation Method to Sub rates immediately after creating the Per Diem Rate, you would get the following error message: <ul><li><em>The Per Diem Rate does not exist. </em> </li> </ul>  |38538|
| Per Diem|When posting a Per Diem with reimbursement method = both, you would get the following error. This has been fixed. <ul><li><em>Document No. must not be blank in ...</em> </li> </ul> <ul> </ul> |38762|
| Per Diem|When only one Per Diem Group would exist, the filed &quot;Per Diem Group Code&quot; was not visible on the Per Diem Card. |40886|
| Platform and Technology|<span>A bug have been fixed in the approval portal, where an approver could experience the following error message when opening an expense allocation:&nbsp;</span> <span><br></span> <ul><li><span><em>You do not have the following permissions on TableData Job: Read.</em></span> </li> </ul> |40489|

## Expense Management 2022 R1 Service Pack 2, hotfix 4

*Released: July 11, 2022*  
*App version: 9.2.0.4*  

### Bug fixes

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | We have fixed the following error in the Status Report related to the Per Diem calculations over the number of hours.<br /><ul><li><span><em>Overflow under conversion of Microsoft.Dynamics.Nav.Runtime.Decimal18 value 16,5 to System.Int32</em></span><br/> </li> </ul> | 39458 |



## Expense Management 2022 R1 Service Pack 2, hotfix 3

*Released: July 06, 2022*  
*App version: 9.2.0.3*   

### Bug fixes

| Functional area          | Description                                                  | ID    |
| ------------------------ | ------------------------------------------------------------ | ----- |
| Credit Card Transactions | We've added a filter on the payment type lookup when assigning a payment type to a credit card from the bank transaction inbox. We've also added additional fields to the lookup, allowing the user to get a better idea of which payment type to select. | 39363 |
| Credit Card Transactions | We have fixed a bug that made it difficult to change the credit card user mapping from the bank transaction inbox. | 39339 |



## Expense Management 2022 R1 Service Pack 2, hotfix 2

*Released: June 23, 2022*  
*App version: 9.2.0.2*   

### Bug fixes

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | We have fixed an issue that was causing the synchronization to stop with the error below when documents were pending to be deleted. The issue has only been seen in the Business Central cloud client.<br /><ul><li><span><em>The following AL methods are limited during write transactions because one or more tables will be locked...</em></span></li> </ul> | 38907 |



## Expense Management 2022 R1 Service Pack 2, hotfix 1

*Released: June 22, 2022*  
*App version: 9.2.0.1*   

### Bug fixes

| Functional area     | Description                                                  | ID    |
| ------------------- | ------------------------------------------------------------ | ----- |
| General Application | We have fixed an issue that was causing the synchronization to stop with the error below when documents were pending to be deleted. The issue has only been seen in the Business Central cloud client.<br /><ul><li><span><em>The following AL methods are limited during write transactions because one or more tables will be locked...</em></span></li> </ul> | 38859 |



## Expense Management 2022 R1 Service Pack 2

*Released: June 17, 2022*  
*App version: 9.2.0.0*   
*FOB version: 9.02.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Document Approval|We have added the possibility to add &quot;Out of office&quot; settings from the&nbsp;<span>Approval Entries page.</span> |28378|
| Expenses|We have implemented functionality to avoid and enforce the usage of Jobs/Tasks on sales tax allocation lines. Sales Tax allocation will no longer post Job ledger entries.&nbsp;<span>This is especially relevant for the Canada Sales Tax.</span> |31943|
| General Application|We are now marking &quot;User Delegation&quot; entries as Disabled. A delegation&nbsp;<span>could have become invalid because they were wrongly setup or because it became invalid over time.</span> <span><span>&nbsp;</span>The administrator can now easily identify disabled delegations and either fix them or remove them in the Expense User Delegation page.</span> |27907|
| General Application|<span>We have changed the behavior when rejecting a document. In the past if &quot;Auto submit for approval&quot; was set, the rejected document was sent to the user (status = Pending Expense User), otherwise, it would have been kept in Status = Open. Since this was inconsistent with the behavior when approving a document, we have changed so that all the rejected documents are sent to the Expense User, independently of setup.</span> <br> |28189|
| General Application|We are now processing the release notifications from the&nbsp;<span>Notification Outbox as part of the normal synchronization with Continia Online.</span> |28682|
| General Application|We are no longer marking the Ledger Entries as&nbsp;<span>&quot;System-Created Entry&quot;. This will allow reverting ledger entries posted by Expense Management.&nbsp;</span> <span><span>It also fixes an issue in the Australian localization, where the sales taxes were not posted in the &quot;GST Purchase Entry&quot; and tables alike.</span></span> |32161|
| General Application|We have made it possible to un-assign&nbsp;<span>payment types from users. The corresponding payment type is automatically un-asigned when a credit card is deleted.</span> |32275|
| General Application|We have made it possible to configure a mandatory field that is &quot;Hidden by Default&quot;. The field becomes mandatory only when visible to the user.&nbsp;<span>Therefore we have made ATTENDEES mandatory by default when you reset your configuration to the default setup, in the Configured Fields page.</span> |32434|
| General Application|We have reintroduced the&nbsp;<span>Field Type EMPLOYEE NO. so that it can be used in posting descriptions in the Expense Management Setup. It is an internal system field and it cannot be configured. The&nbsp;<span>EMPLOYEE NO. will show the User ID from the posted document, but without an eventual domain name.</span></span> |34700|
| General Application|We have added the possibility to show the Base Amount, VAT Amount and Percentage on the expenses lines on a settlement. Similar to what is already on the expense card page. |34790|
| General Application|We have created a tool meant to be use before upgrading from on premise to cloud, to help with the transition of attachments. The tool will move the document storage to Database and convert PDF files into PNG (necessary in later versions for preview). The process is described in the following article: <a href="https://continia.zendesk.com/hc/en-us/articles/360014053519">https://continia.zendesk.com/hc/en-us/articles/360014053519</a><br> |34921|
| General Application|<p><span>In Business Central 2021 release wave 1 (BC18),&nbsp;<span>email scenarios are now supported for the following processes:</span><br></span> </p><ul><li><span>Expense Management Approval Status Email - Used when sending the approval status email.</span> </li><li><span>Continia Welcome Email - Used when sending the welcome emails to Continia users.</span> </li><span>Expense Management Status Email&nbsp;</span><span>- Used when sending status emails to the expense users.</span><li><span><span>Expense Management Reminder Email</span> - Used when sending status emails to expense users that have pending documents.</span> </li> </ul><br> |38400|
| General Application|<span>When using Business Central online, the&nbsp;</span><span>Document Capture Activities part is only visible if Document Capture is activated.</span><br> |38656|
| General Application|We have added the following Event Publishers<br>  <br>  Table 6086309 CEM Posting Setup <ul><li>OnBeforeModifyExistingExpense </li> </ul> <ul><li>OnBeforeModifyExistingMileage </li> </ul>  <br>   Table 6086320 CEM Expense<br>  <span><ul><li><span>OnExpenseTypeValidateBeforeExpValidation</span> </li> </ul></span>  <span><ul><li><span>OnAfterNewCalculatedAccount</span> </li> </ul></span>  <br>  Table 6086330 CEM Bank Transaction <ul><li>OnBeforeInsertExpense </li> </ul>  <br> <span><span>Codeunit&nbsp;6086338 &quot;CEM Settlement-Post&quot;<br><ul><li><span>OnBeforeCreateGenJnlBalanceEntrySet</span> </li> </ul></span></span><font color="#171717"><span>Codeunit&nbsp;<span>6086319 &quot;</span><span>CEM NAV-version Mgt.</span><span>&quot;</span></span></font> <ul><li><span>OnBeforeBalancePostGenJnlLine</span> </li> </ul> <br>|38675|
| Platform and Technology|You can now change the size of the document view in the BC Web Client. This applies to the preview of the attachments on expenses, approvals, mileage and in the expense report. <br> Article:&nbsp;<a href="https://continia.zendesk.com/hc/da/articles/4404757400722-How-to-change-the-size-of-the-document-view-in-BC-Web-Client?source=search&amp;auth_token=eyJhbGciOiJIUzI1NiJ9.eyJhY2NvdW50X2lkIjoyOTY5MDQsInVzZXJfaWQiOjE0MDA3NDIxOTI1LCJ0aWNrZXRfaWQiOjczMDUyLCJjaGFubmVsX2lkIjo2MywidHlwZSI6IlNFQVJDSCIsImV4cCI6MTYzNTkzNTczMn0.ymcHK8rdkQ1DnHWAQiA064YNAhQgV1coQH6X89YBiK0">https://continia.zendesk.com/hc/da/articles/4404757400722-How-to-change-the-size-of-the-document-view-in-BC-Web-Client</a> |28928|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Credit Card Transactions|We have fixed an issue that was causing the upgrade to EM 9.00 and 9.01 to fail with the error below when the Bank Account number would have been a string longer than 10 characters. <ul><li><em>The length of the string is 12, but it must be less than or equal to 10 characters. Value: LONGER_THAN_10_VALUE</em> </li> </ul> |34393|
| Credit Card Transactions|We have fixed an issue, where rejecting a bank activation request, could result in the following error message during synchronization.<br> <br><em>&quot;Bank Code missing. Continia Online has provided an agreement activation but the bank doesn't exist.&quot;</em> |38522|
| Expenses|We have fixed an error, when attempting to merge two expenses that are not both cash/private card. Error Message: <ul><li><span><em>Merge not allowed</em></span><br> </li> </ul> |32723|
| Expenses|In earlier versions it was possible to use a system field from one table, as an extra field in another. We have prevented that, but if such fields still exist in your configuration you would get this error. Example from the Expense Report Inbox. <ul><li>&quot;<em>The Field Name COUNTRY/REGION is a system field and cannot be imported as an extra field.</em>&quot; </li> </ul>In order to fix the configuration issue, please&nbsp;<span>run the function Reset to Default Setup.</span> <span>In order to fix the expense report inbox entries in error, please find the <span>COUNTRY/REGION<span>&nbsp;</span></span>Extra Field&nbsp;<span>and delete the entry. Then, you can add the value of the <span>COUNTRY/REGION on the Expense Report Inbox entry, instead.</span></span></span>  |32732|
| Expenses|We have fixed an issue when submitting unmatched expenses with a payment type, for which matching is not required. The expense would not be send automatically for approval, as it should. <br> The user would get a comment saying:&nbsp; <ul><li><em>User has corporate credit card in Continia User Credit Card List. Verify this expense is not waiting for transaction to be matched.</em><br> </li> </ul> |32755|
| Expenses|We have fixed a bug that wasn't allowing the payment type to be edited when a user had no payment types assigned. |34518|
| Expenses|We have fixed a bug when creating a new expense in NAV/BC, would result in an error, if the Expense User had only one payment type assigned. |34816|
| Expenses|We have found an issue that could create duplicated bank transactions out of one single bank transaction inbox. That would occur if multiple users processed the transaction inbox in the exact split of a second. The bookkeeper would have been informed if an expense existed twice, though. |35047|
| General Application|We have fixed an issue that was suggesting translation &quot;Code&quot; for the dimensions when creating a Field Type.&nbsp; |19608|
| General Application|We have fixed a caption issue on the &quot;Field Type Dependencies&quot; page. |26878|
| General Application|We have disabled the drilldown functionality on the &quot;Continia User Name&quot; on all the pages since it was revealing a different result than the lookup on the Continia User ID. This was not only bringing confusion but sometimes it would lead to other issues, as well. |28322|
| General Application|Functions or actions modifying Approval Entries could in some cases experience a performance issue. This has been fixed.&nbsp; |28367|
| General Application|We have done some performance improvements based on feedback from the Application Insight logs. |28370|
| General Application|We have fixed a number of issues related to Continia Users with Limited Document Visibility. Some are related to approvers others are general.&nbsp; <span><br></span> <span>1) A Continia User&nbsp;</span><span>with limited document visibility can only view his or hers own documents.&nbsp;</span><span>The restriction also applied to approvers with limited document visibility.&nbsp;</span><span>Now we allow the next approver of the document to view the document, even if otherwise limited to only view own documents.&nbsp;</span><span>The approver would get the following error message:</span> <span><br></span> <span><ul><li><span>&quot;<em>Document X for User Y cannot be displayed because you only have access to your own documents.</em>&quot;</span> </li> </ul></span> <br> <span>If the approver is also an expense user with delegations the message would be:&nbsp;</span> <span><br></span> <span><ul><li><span>&quot;<em>Document X for User Y cannot be displayed because you are only allowed to handle documents for the following users: Z.</em>&quot;</span> </li> </ul></span> <span><br></span> <span>Where &quot;</span><em>Document</em><span>&quot; would be either Expense, Mileage, Per Diem or Expense Report/Settlement.</span><br> <span><br></span> <span>2) In older versions of Expense Management the message was wrong and looked like this:&nbsp;</span> <span><br></span> <ul><li>&quot;<em>Expense Expense for X cannot be displayed because you only have access to your own documents.</em>&quot; </li> </ul> <br> 3) We also found that in special cases, some users with limited document visibility would have had access to posted per diems where they shouldn't have had access.&nbsp;<span>This has been fixed.</span>  <span><span><br></span></span> <span><span>4) When opening an expense document by choosing View from the reimbursement matrix and release notification entries, it was in some cases possible to view the document in the wrong page and to navigate to other documents. This has been fixed.</span></span> <span><span><br></span></span> <br>  <span><span>5) The view document action button in the reimbursement details, approval entries and release notifications had three different icons. They now all have the View icon.&nbsp;</span></span> <span><span><br></span></span> <span><span><br></span></span> 6) In the Approval Entries (Forms only), the press the Show button and then choose the View option. It would not display per diems. This has been fixed.&nbsp; <br> <br> 7) Posted Expenses, Mileage, and Expense Report would not give an error message when a user with limited document visibility opened the Posted Document Card page. The Posted Per Diem card did give a message. This has been changed to that the logic on the Posted Card is the same as on the normal Card.&nbsp; <br> <br> 8) We were missing the Check Data Version on several document card pages.  |30712|
| General Application|We have fixed an issue that was causing the error below. It would occur when posting a Per Diem, for a user that was part of a group and there was posting setup only for the group. <br> <ul><li>&quot;<em>There is no Posting Setup within the filter. Filters: Type: Per Diem,Type Code: ACCOMMODATION.</em>&quot; </li> </ul> |31553|
| General Application|In version 9.00 we prevented creating a custom Field Type with the same code as a Global Dimension and this is an issue we have corrected. Global dimension codes are no longer reserved Field Type codes.&nbsp; |32249|
| General Application|When exporting the Expense Management configuration&nbsp; with the Expense Management Assisted Setup, the Vehicle table would always be exported. Now it is only exported if the user has selected to export Mileage Rate IDs. |32335|
| General Application|We did not increase the object Version number when we changed the captions &quot;Settlement&quot; to &quot;Expense Report&quot; in the following objects.&nbsp; <br> <span></span> Table 6086327 CEM Expense Management Cue<br>  Table 6086340 CEM Settlement Overview Line&nbsp;<br> Table 6086354 CEM Continia User Statistics<br> Table 6086361 CEM Comment<br> Table 6086364 CEM Reminder<br> Table 6086371 CEM Comment Line<br> Table 6086401 CEM Attachment Pages<br> Table 6086402 CEM Attachment Pages Inbox<br> Report 6086315 CEM Batch Post Per Diems<br> Codeunit 6086323 CEM Comment Mgt.<br> Codeunit 6086326 CEM Navigate Settlement - Find<br> Codeunit 6086339 CEM Settlement-Post (Yes/No)<br> Codeunit 6086359 CEM Move to Company<br> Codeunit 6086370 CEM Workflow Event Handling<br> Codeunit 6086371 CEM Workflow Response Handling<br> Codeunit 6086381 CEM Settlement - Validate<br> Codeunit 6086382 CEM Settlement - Send to User<br> Page 6086305 CEM Reminders<br> Page 6086308 CEM Limited Role Center<br> Page 6086409 CEM Expense Settlements<br> Page 6086431 CEM Continia User Factbox  |32340|
| General Application|<span>We have fixed an issue in the Assisted Setup that was leading to the errors below.<br><br></span> <em><span>&quot;Sorry, we just updated this page. Reopen it, and try again.&quot;&nbsp;<br></span><br> </em> <span><span><em>&quot;PD-BREAKFAST is a required Per Diem Detail system field. Please configure it before synchronizing.&quot;</em></span></span> |32349|
| General Application|We have fixed a bug in the approval portal, where an approver could experience the following error message:<br><br> &quot;<span><em>You do not have the following permissions on TableData Job: Read.&quot;</em></span> |32358|
| General Application|We corrected a spelling mistake on the approval page. |32373|
| General Application|We have fixed a silent error that could be found in a Business Central client, when looking for the &quot;Last Known Error&quot;. This was happening after a synchronization occurred, in a system where the Default Payment Type was, in the same time, assigned to a user. The error would come from the database, when trying to insert a duplicate entry. <br> &quot; <span><em>Error code: 85132273<br></em></span><em>DB:RecordExists<br></em> <em>&quot;CEM Online Synch. Mgt.&quot;(CodeUnit 6086305).UpdateLookupValueAcces line 46 - Continia Expense Management by Continia Software<br></em> <em>&quot;CEM Online Synch. Mgt.&quot;(CodeUnit 6086305).SetupValueAccess line 8 - Continia Expense Management by Continia Software<br></em> <em>&quot;CEM Online Synch. Mgt.&quot;(CodeUnit 6086305).SetupContiniaOnline line 6 - Continia Expense Management by Continia Software<br></em> <em>&quot;CEM Online Synch. Mgt.&quot;(CodeUnit 6086305).Code line 44 - Continia Expense Management by Continia Software<br></em> <em>&quot;CEM Online Synch. Mgt.&quot;(CodeUnit 6086305).OnRun(Trigger) line 2 - Continia Expense Management by Continia Software<br></em> <em>&quot;CEM Configured Field Types&quot;(Page 6086446).&quot;ForceSynchronize - OnAction&quot;(Trigger) line 5 - Continia Expense Management by Continia Software</em> <em><span></span></em>&quot; |32566|
| General Application|We have fixed an error in the upload company logo functionality, which would fail silently, and roll back the changes to the company logo. |32567|
| General Application|We have marked the table <span>6086373 Vehicle User&nbsp;</span>and the page&nbsp;6086403 CEM Vehicle User List as <span>deprecated.</span> |32730|
| General Application|We have corrected some spelling errors. |32753|
| General Application|If you had DEPARTMENT and PROJECT as global dimensions 1 and 2, we would add them as system field types when choosing the action Reset to Default Setup on the Configured Fields page. That was a mistake. Field types pointing to global dimensions are not considered system fields. If you have this issue, simply run the Reset to Default Setup action again.&nbsp; |32815|
| General Application|In an earlier version we renamed Settlement to Expense Report, but when creating demo data with the Expense Management Wizard (Assisted Setup), we continued to create a Source Code called SETTLEMENT. We have now changed it to REPORT. |32818|
| General Application|We have added a new Codeunit to automatically update Field Dependencies, intended to be used in the Job Queues.&nbsp;<span>Codeunit 6086569 CEM Update Field Dependencies&nbsp;will update lookup values and update system field type dependencies. If any field type dependency has been disabled due to conflicts, the Codeunit will stop with the first error found.&nbsp;</span> |32881|
| General Application|We have fixed an upgrade issue that would have been logged with the error below:&nbsp; <ul><li><em><span>CEM Upgrade Functions&quot;(CodeUnit 6086107).EM800UpgradePerDiemTables line 41</span></em> </li> </ul> |34438|
| General Application|<span><span>We have fixed an upgrade issue that would have been logged with the error below:&nbsp;</span></span><br> <ul><li><span><span><span><em>CEM Upgrade Functions&quot;(CodeUnit 6086107).MoveMandatoryEditableValues line 7</em></span></span></span> </li> </ul> |34439|
| General Application|<span><span>We have fixed an upgrade issue that would have been logged with the error below:&nbsp;</span></span><br> <ul><li><span><span><em>CEM Upgrade Functions&quot;(CodeUnit 6086107).CreatePaymentTypes line 75</em></span></span> </li> </ul> |34440|
| General Application|<span>We have corrected an issue that was naming all the Expense Management permission sets wrongly. The permission sets were prefixed with &quot;CCEM&quot; instead of &quot;CEM&quot; and this was leading to issues after the upgrade.</span> |34471|
| General Application|<span>The field type dependency can be disabled with the following message:&nbsp;</span><br> <ul><li><em>The following users don't have access to value X in the field Y</em> </li><li><em><em>The following user groups don't have access to value X in the field Y</em><br></em> </li> </ul>We have improved the consistency check to not disable field type dependencies in the case where user also had a restricted lookup value access on the specific value in the condition for the field dependency.  |34547|
| General Application|An expense document could be stuck in the inbox with this error text.&nbsp; <ul><li><em>The Field Name &nbsp;was not found in the Field Type table. </em> </li> </ul>This has been fixed.  |34581|
| General Application|We have fixed an issue where the inbox entries would have failed with the error below. This was happening only when using the &quot;O365 Authentification Email&quot; on the Continia User. <ul><li><span><span>&nbsp;</span>&quot;User with user ID &lt;email&gt; does not exist in the Continia User table.&quot;</span> </li> </ul> |34643|
| General Application|We have identified an isuse that could lead to a duplicated ledger entry for an expense in the case where, in the same split of a second, 2 users would have posted it. The posting routine was able to prevent concurrent sessions, but not from the moment the button was pressed up to the moment the posting would start.&nbsp; We have now making an extra check to ensure this cannot happen. |35019|
| General Application|We have fixed a bug, where a blank drop down list was presented, when trying to look up a vendor account on the payment type card. |38354|
| General Application|<span>We have extended the &quot;Reset to Default Setup&quot; function on Configured Fields, to automatically add the default dimensions, if not already there. The default setup file is therefore no longer containing dimension fields. This solves an issue where default dimensions were added by the setup file, but the dimension codes wouldn't actually match the dimensions in the system. For example, field type PROJECT must have been linked to dimension PROJEKT in a Danish localization.&nbsp;</span> |38367|
| General Application|We have fixed an issue that was returning the following error in the Web Approval Portal, when custom fields would have been created with value longer than 50 characters. The issue was present on Mileage, Per Diem and Expense Report. <ul><li><em>The length of the string is 51, but it must be less than or equal to 50 characters. Value: A very long description, longer than 50 characters.</em><br> </li> </ul> |38431|
| General Application|We have identified an issue that was not updating documents in the Expense App when they were paid, due to the fact that the payment was not made with a Document Type = Payment.&nbsp;<span>We are now not checking anymore the Document Type, we only make sure the payment applies to the initial entry.</span> |38505|
| Mileage |We have fixed an issue that was crashing the client while trying to calculate mileage amounts in an endless loop. This was happening when mileage rates would exist for 2 years in advance. The error received is the one below: <ul><li><span><em>There is insufficient memory to execute this function. This can be caused by recursive function calls. Contact your system administrator.</em></span> </li> </ul> |38457|
| Mileage |The information on the &quot;To Distance&quot;, in the mileage details was always 0. There is no expected impact on the calculation of the mileage rates, the issue is just a visibility one. This behavior was introduced in version 9.0. |38468|
| Per Diems |If was possible to set the arrival time of the first destination to earlier than the departure time of the Per Diem and i<span>t was possible to set the arrival time of the last </span><span>destination&nbsp;to later than the arrival time of the Per Diem. We are now preventing this.</span> |27121|
| Per Diems |On the Per Diem rates, we have removed the fields&nbsp;<span>&quot;Half Day Starting Time&quot; and&nbsp;</span><span>&quot;Half Day Latest Time&quot; because they were not used anymore.</span> |32391|
| Per Diems |<span>We have identified and fixed a wrong calculation on the Per Diem, when using hourly rates, on the last day of the trip.</span> |34367|
| Per Diems |We have fixed an issue on the Per Diem calculation in the case there where &quot;First/Last Day Calculation Method&quot; would have been &quot;First/Last Day fixed rate&quot;. If the number of hours in the current day would have been precisely the same as &quot;First/Last Day Minimum Stay&quot;, the rate was not applied but it should have been. |34501|
| Per Diems |<span>We have fixed an issue on the per diem calculation where the meal value deducted a wrong amount for rates where &quot;Meal Value Method&quot; was an Amount instead of Percentage</span><br> |34502|
| Per Diems |When configuring the &quot;Description 2&quot; field on a per diem the per diem would be stuck in the Inbox with the following error text: <ul><li><em>The Field Name P-DESCRIPTION 2 is a system field and cannot be imported as an extra field.</em> </li> </ul> |34618|
| Per Diems |We have fixed an issue where a Per Diem would show the following error if the &quot;Daily Meal Allowance&quot; was not set. <ul><li><span><em>Attempted to divide by zero.</em></span> </li> </ul> |34625|
| Per Diems |We have fixed an issue in the Per Diem calculation that was, in certain conditions, skipping one day rate when using sub-rates. |38607|

## Expense Management 2022 R1, hotfix 2

*Released: May 3, 2022*  
*App version: 9.1.0.2*   
*FOB version: 9.01.02*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Expenses|We have fixed a bug that wasn't allowing the payment type to be edited when a user had no payment types assigned. |34518|

## Expense Management 2022 R1, hotfix 1

*Released: May 2, 2022*  
*App version: 9.1.0.1*   
*FOB version: 9.01.01*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|We have fixed an issue that was causing the upgrade to EM 9.00 and 9.01 to fail with the error below when the Bank Account number would have been a string longer than 10 characters. <ul><li><em>The length of the string is 12, but it must be less than or equal to 10 characters. Value: LONGER_THAN_10_VALUE</em> </li> </ul> |34393|
| General Application|We have fixed an upgrade issue that would have been logged with the error below:&nbsp; <ul><li><em><span>CEM Upgrade Functions&quot;(CodeUnit 6086107).EM800UpgradePerDiemTables line 41</span></em> </li> </ul> |34438|
| General Application|<span><span>We have fixed an upgrade issue that would have been logged with the error below:&nbsp;</span></span><br> <ul><li><span><span><span><em>CEM Upgrade Functions&quot;(CodeUnit 6086107).MoveMandatoryEditableValues line 7</em></span></span></span> </li> </ul> |34439|
| General Application|<span><span>We have fixed an upgrade issue that would have been logged with the error below:&nbsp;</span></span><br> <ul><li><span><span><em>CEM Upgrade Functions&quot;(CodeUnit 6086107).CreatePaymentTypes line 75</em></span></span> </li> </ul> |34440|
| General Application|<span>We have corrected an issue that was naming all the Expense Management permission sets wrongly. The permission sets were prefixed with &quot;CCEM&quot; instead of &quot;CEM&quot; and this was leading to issues after the upgrade.</span> |34471|

## Expense Management 2022 R1 Service Pack 1

*Released: April 1, 2022*  
*App version: 9.1.0.0*   
*FOB version: 9.01.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Document Approval|We have added an event publisher to Codeunit 6086312: OnBeforeApprovalMgtCode() |31358|
| General Application|Configured Fields are dynamically added or removed based on when functionality is enabled or disabled in Expense Management Setup.&nbsp; <span>We have added an action to help the user access the Configured Fields page directly from the Expense Management Setup page.&nbsp;</span><br> |29018|
| General Application|We have removed the &quot;Error Email&quot; field from the Expense Management Setup, as this field had been made redundant by other improvements on the Continia User Setup.&nbsp; We have also removed the field &quot;<span>SMTP Require SSL/TLS</span>&quot; which becomes obsolete in the enhanced email context.&nbsp; |31577|
| General Application|We have enabled the feature of signing expense attachments digitally in the French and Belgium localizations. |31662|
| General Application|We have added the Job and Task description in the Approval Portal. |32035|
| Mileages|We've amended the sixty day check with a crude text string comparison on the addresses in cases where geo coordinates are not available (e.g. legacy data from prior to introduction of the feature). |31850|
| Per Diems |In the Norwegian localization, when calculating per diem allowances, we have changed the rounding precision to the nearest ones so that it complies with the legislation.&nbsp;<span>In the past it was based on the currency rounding precisions.&nbsp;</span> |31865|
| Per Diems |On per diems sub-rates, we have added the possibility to specify the minimum number of hours after which a full day allowance is refunded. |31866|
| Platform and Technology | With Expense Management 2022 R1 service pack 1 (9.01), we have released Expense Management for Microsoft Dynamics 365 Business Central 2022 release wave 1 (BC20). <br><br> Expense Management 2022 R1 service pack 1 (9.01) in Business Central online will not be available for Microsoft Dynamics 365 Business Central 2021 release wave 2 (BC19). You will only be able to use Expense Management 2022 R1 service pack 1 (9.01) in Business Central online when you have upgraded to Microsoft Dynamics 365 Business Central 2022 release wave 1 (BC20). | 32415 |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Credit Card Transactions|We've increased the length limit of the Transaction ID which the bank can send to 150 characters. |13728|
| Credit Card Transactions|We have fixed the following error when synchronizing the activation of a bank agreement:&nbsp; &quot; The bank does not exist. Identification fields and value Code='',Country/Region Code='' &quot; |31742|
| Expenses|When no Expense Type was specified on the expense we gave two error messages.&nbsp; This has been reduced to one: &quot;Expense Type must be specified.&quot; The second message &quot;You must specify Expense Account Type and Expense Account in Expense Posting Setup for expense type .&quot; only appears when the expense type is specified. |27782|
| Expenses|We have fixed a bug on the expense card, where for cases of reverse charge VAT, the VAT and Base Amount was displayed wrongly. |31410|
| Expenses|We have fixed a bug where the Payment Type field was uneditable on the Expense List Page. |31454|
| Expenses|When using the Vendor number (business vendor) on expenses, the payments on the Vendor were only applied in the Spanish localization. We are now applying the payments in all localizations. |31630|
| Expenses|The Reimbursement page was showing the error below if an expense didn't have a payment type.&nbsp; &quot;<span>Continia User Setup: The Payment Type does not exist. Identification fields and values: Code=''</span>&quot; |31641|
| Expenses|We have moved the &quot;Submit Cash Expenses in LCY&quot; from Expense Management Setup to Payment Type. |31948|
| General Application|We have fixed a bug where it was possible to reopen/recreate a document from NAV/BC when that document had been deleted by the user in the app/portal. |27291|
| General Application|Expense Management can store documents in three different locations: on the server hard disk (file system), the database, and in an azure blob storage. When running the Expense Management Setup Assisted Setup, the user could only choose File System and Database. We have added Azure Blob Storage to the Wizard.&nbsp; |28806|
| General Application|We have fixed a bug in NAV/BC where the first subdocument line on a Settlement (Expense Report) would not inherit the global dimensions from the main document. |31238|
| General Application|We have fixed a bug where it was possible to send a welcome mail to an Expense Management user with an &quot;empty&quot; link to the Expense Portal. |31566|
| General Application|We have fixed an issue when the same number series was used for both posted and un-posted settlements. In this case, the posted document would have still increased the number series number when it was not expected to do so. |31575|
| General Application|We have improved the caption on the request page of the batch posting of expenses, mileages and expense reports. |31650|
| General Application|<span>In 9.00 we </span><span>introduced a bug where Lookup Value Access&nbsp;</span><span>on User Groups did not get synchronized to Continia Online. Lookup Value Access restricts the values a user or a user group can see in the Expense App/Portal. The issue was that, for a group, we would have shown all the values, not only those specific to the group. We have now corrected the issue.</span>  |31805|
| General Application|We did not increase the object version number when we changed the captions &quot;Settlement&quot; to &quot;Status Report&quot; in the following objects. Therefore we have done it now. <br> <span>Page&nbsp;6086301 &quot;CEM Role Center&quot;&nbsp;</span><br> Page&nbsp;6086302 &quot;CEM Activities&quot; |31912|
| General Application|We added an image to the Tax Report action on the posted document lists. |32152|
| General Application|<span>We have fixed an issue in the Assisted Setup that was leading to the errors below.</span> <em><span>&quot;Sorry, we just updated this page. Reopen it, and try again.&quot;&nbsp;</span><br> </em> <span><span><em>&quot;PD-BREAKFAST is a required Per Diem Detail system field. Please configure it before synchronizing.&quot;</em></span><br></span> |32349|
| Mileages| <p><span lang=EN-US>On the Approval Entries page, on a mileage, when choosing the action Details.</span> </p><p><span lang=EN-US>You would get the error message </span><span lang=EN-US><em>Allocations are not supported on mileage.</em></span> </p><p><span>Now it will open the page Mileage Details.</span> </p> |28305|
| Mileages|Due to an issue in created demo data, the system could end up having two default vehicles. When trying to unselect one of them you would get an error message.&nbsp; <br> <em>There can only be one default Vehicle.</em> <br> This has been changed so that when the user sets default to Yes on a vehicle, then all others vehicles are automatically have default set to No. |31992|
| Per Diems |Per Diem taxable amounts were calculated wrongly for a Per Diem with Sub-Rates, when the trip was shorter than 24 hours. This functionality was introduced in EM 9.00. |31640|
| Per Diems |Meal taxable allocation values were wrongly calculated. This functionality was released in EM 9.00 |31867|
| Platform and Technology|We have added support for Automated Data Upgrade in&nbsp;Business Central Spring 2019 Release (BC14). |32280|

## Expense Management 2022 R1

*Released: March 1, 2022*  
*App version: 9.0.0.0*   
*FOB version: 9.00.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Expenses | We have introduced the concept of Payment Types, which replaces the Cash/Private field and takes over functionality from Expense Management and Credit Card.<br>A payment type is an account that defines the behavior of an expense. On the Payment Type, you can specify the posting accounts, if matching is required or if the user has to be reimbursed.<br>As part of the upgrade, all the expenses will have a Payment Type added, if a decision can be taken and if the expense can be updated. |
| General Application | We have added more setup pages to the Business Setup (Manual Setup) list. |
| General Application | When choosing to add a Field Type to a configured Field, the user was presented with the complete list of Field Types. We have optimized this to only show the list of relevant fields. |
| General Application | We have improved the usability of Field Type and Configured Fields. From the Configured Fields, you can create field types and the card page will lead you through the possible settings. We have removed the Field Type list and we expect the Configured Fields page to be the entry point. |
| General Application | We have removed the field type "EMPLOYEE NO". |
| General Application | We are now showing the Filter column by default in the Table Filters of the Field Types. |
| General Application | When specifying the Source Table on the Field Type, the user can directly type the table caption or part of it. For example, "Currency", "currency", "curr", "4" (the table id) are all valid values.<br>Furthermore, the user can copy the Source Table information from the Help, About this page and paste it directly to the Source Table field. For example, "Currency (4)" will also work. |
| General Application | The setup file now activates history in the Cloud to 6 months by default. |
| General Application | We have renamed "Settlement" to "Expense Report". |
| General Application | Teaching Tips on Expense Page. |
| General Application | Teaching Tips on Mileage Page. |
| General Application | Teaching Tips on Per Diem Page. |
| General Application | Teaching Tips on Expense Report Page. |
| General Application | Teaching Tips on Bank Transactions Page. |
| General Application | We have renamed the "Navigate" action to "Find Entries", to be more consistent with the standard Business Central client. |
| General Application | We have added Description 2 on Mileage and Per Diem. |
| General Application | Digital signing is also available in France. |
| Expenses | We can now disable standard approval notifications. |
| Expenses | We have also added the External Document No. to the expenses that are matched. |
| Per Diem | We have introduced the possibility to disable the Accommodation or Meal allowances on the Per Diem. |
| Per Diem | On the Per Diem sub-rates, the percentage of meals is subtracted from the sub-rate value. In the past, a meal amount was calculated from a full day. This functionality comes to help the Austrian Per Diem rules. |
| Per Diem | We have added several features for Per Diems, in order to support requirements in the Norwegian market.<br>We have added the possibility to add taxable rates on top of the tax-free rates.<br>We have added the possibility to add an accommodation type like a hotel, guest house, etc.<br>We have added a tax report which can be handed to the tax authorities, which sums all the main details about a document so that the validity of the document can be assesed. |
| Platform and Technology | We have improved the Icon (Image) handling. An icon can be chosen from a predefined list of images and it's present on the main account types: Expense Types, Vehicles, Allowances, Payment Types. |
| Platform and Technology | <b>With the release of Expense Management 2022 R1 (9.00), we only support Business Central 2019 Spring (BC14) and newer versions.</b><br><br>Even though we don't support Business Central October 2018 (BC13) or older versions in Expense Management 2022 R1 (9.00), we will still support the old NAV/Business Central versions in future service packs released for Expense Management 2021 R2 (8.00). |


### Bug fixes

All relevant bugfixes released in service pack 1 to service pack 2, hotfix 3 for Expense Management 2021 R2 (8.00), service pack 1 to 3 for Expense Management 2021 R1 (7.00), and service pack 1 to 4 for Expense Management 2020 R2 (6.50) are also included in Expense Management 2022 R1 (9.00). The description of these bugfixes is not repeated on this page.

<br>

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General Application | We have fixed an issue that was calculating wrong total amounts on the Per Diems, in the Status Report. |
| General Application | We have fixed an issue that was showing an error if the same filters were applied on similar fields. For example, PD-DESTINATION and P-DESTINATION. |
| General Application | We have fixed an issue in the addin that was setting a default zoom of 1% on the attachments. |
| General Application | We have fixed an issue where the number of documents was not correct in the Approval Portal. |
| General Application | We have fixed a bug where an empty agreement was created when an activation request was rejected. |