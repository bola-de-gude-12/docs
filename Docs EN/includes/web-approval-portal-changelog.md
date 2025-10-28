This article lists all new features and bug fixes for each version of the Continia Web Approval Portal.

## Web Approval Portal 27.0.0
*Released: September 29, 2025*  

### New or changed functionality
| Description | ID |
| --- | --- |
| If you use Business Central cloud, environment names are now shown in the company selector. | 64762 |
| Destinations are now displayed for per diems, provided that you're using Expense Management 2025 R2 (v27). | 68319 |

## Web Approval Portal 25.2.6
*Released: September 8, 2025*  

### Bug fixes
| Description | ID |
| --- | --- |
| In on-premises setups, the cross-company overview failed to load in certain cases. | 69193 |

## Web Approval Portal 25.2.5
*Released: August 29, 2025*  

### Bug fixes
| Description | ID |
| --- | --- |
| Prior to this, forward slashes (/) in invoice numbers could return an error in ZUGFeRD documents. | 67907 |

## Web Approval Portal 25.2.4
*Released: August 26, 2025*  

### Bug fixes
| Description | ID |
| --- | --- |
| Added specific telemetry for the cross-company dashboard, with extra custom dimensions. | 68631 |
| Added default permissions in the scenario where a purchase document isn't found. The update of lines has been disabled, as they're no longer found. | - |

## Web Approval Portal 25.2.3
*Released: July 7, 2025*  

### Bug fixes
| Description | ID |
| --- | --- |
| Fixed an issue that affected documents found via web menus. | 64078 |

## Web Approval Portal 25.2.2
*Released: June 12, 2025*  

### New or changed functionality
| Description | ID |
| --- | --- |
| Users of Expense Management version 25 and later can now edit all allocations. | 66145 |

## Web Approval Portal 25.2.1
*Released: May 20, 2025*  

### Bug fixes
| Description | ID |
| --- | --- |
| If a user was soft-signed out of their Microsoft 365 account or if their session timed out, they would be required to re-enter their full credentials – including multi-factor authentication. | 66474 |
| Updated the German translations of four captions.            | 66475 |
| If the index exceeds the length of translated options, a default document type is now set. | - |

## Web Approval Portal 25.2.0
*Released: April 24, 2025*  

### New or changed functionality
| Description | ID |
| --- | --- |
| Added a GUID to the HTTP 401 unauthorized client error in the logs. | 64445 |
| {WapUrl}/account/companies now accepts a company code as a parameter (e.g.: cronus.com/account/companies?companyCode=1234ab56-a123), making it easier to cross-check companies from the Document Capture web service with the companies in the Auth database (ProductUserCompanySetups).<br><br>Additionally, you can now create or delete a tracing cookie directly from the **Settings** page – which can be useful when requesting support. | 64572 |

### Bug fixes

| Description | ID |
| --- | --- |
| Implemented a better calculation of the height of the HTML preview iframe. | 64244 |
| Previously, the following message could have been shown when selecting G/L accounts in purchase lines.<ul><li><em>More than 0 records found.</em></li><ul> | 56782 |
| Corrected a couple of small typos in the user interface. | 56794, 56795 |
| Previously, attempting to create a purchase before the first line was successfully created resulted in the following error:<ul><li><em>The Standard Text does not exist. Identification fields and values: Code='\<code value\>'.</em></li></ul> | 57829, 57942 |
| It's now possible to upload documents when the related company name contains a pipe ( \| ). | 65500 |
| Prior to this, the cross-company dashboard crashed if the document type was not in translations. | 65775 |

## Web Approval Portal 25.1.1
*Released: March 17, 2025*  

### Bug fixes
| Description | ID |
| --- | --- |
| Prior to this fix, attempting to show attachments in full screen returned an error. The related bug was introduced in version 25.1.0. | 64623 |
| Prior to this fix, attempting to download attachments returned an error. The related bug was introduced in version 25.1.0. | 64624 |

## Web Approval Portal 25.1.0
*Released: March 10, 2025*  

### Bug fixes
| Description | ID |
| --- | --- |
| Updated references to external resources to eliminate vulnerabilities. | - |
| Dimensions are now displayed on purchase orders. | 63282 |
| After forwarding an approval, users are now redirected to the next approval. | 62499 |
| When logging out from the WAP, Microsoft 365 accounts no longer log out out from other web apps. | 63905 |
| The Swedish localization of the mobile version of the cross-company dashboard crashed due to a translation issue. | 64232 |
| An invalid URL related to the **Document No.** caused a 404 error in the mobile version of the Archive. | 64248 |
| Multiple bugfixes in the mobile view, where **Document No.** wasn't URL-safe. | 62331 |

## Web Approval Portal 25.0.7
*Released: January 30, 2025*  

### Bug fixes

| Description | ID |
| --- | --- |
| A sign-in flow with Microsoft 365 resulted in a redirect loop, losing the original error message. | 62993 |
| Trying to sort on a stored index that exceeded the number of columns on the cross-company dashboard caused an error when the page was loaded. | 63025 |
| When using "trace=true" on premises to troubleshoot an on-premises portal, an error was shown. | 63233 |

## Web Approval Portal 25.0.6
*Released: December 18, 2024*  

### New or changed functionality

| Description | ID |
| --- | --- |
| Updated the SortOrder value from Int32 to Int64 to avoid overflows and ensuring the correct sorting order. | 62189, 62210 |
| Added a log reference ID when login fails, which can be searched by the Support team if needed. | 62062 |

### Bug fixes

| Description | ID |
| --- | --- |
| The cross-company dashboard failed in the Dutch and French localizations. | 62276 |

## Web Approval Portal 25.0.5

*Released: December 4, 2024*  

### Bug fixes

| Description | ID |
| --- | --- |
| Fetching the list of databases failed. | 61974 |
| Requesting passwords failed, if no email was provided. | 61975 |
| Viewing attachments failed. | 61976 |
| The mobile view of the cross-company dashboard wasn't working. | 61985 |

## Web Approval Portal 25.0.4
*Released: December 4, 2024*  

### Bug fixes

| Description | ID |
| --- | --- |
| Resetting password on premise failed to find the user. | 61716 |
| Refreshing tokens failed for Microsoft 365 authorized users (since version 25.0.3). | 61546 |
| Tracking the user's screen resolution in Application Insights is now possible. | 61775 |

## Web Approval Portal 25.0.3
*Released: November 18, 2024*  

### New or changed functionality

| Description | ID |
| --- | --- |
| Cross-company dashboard: navigation after approval/reject is now possible across companies when editing pages. | 60480 |
| Removed dependency to Auth. | 59767 |
| On-premise usernames are no longer case sensitive. | 59767 |
| Translated hardcoded texts. | 60167 |
| Expense Management hides private cachecard from version 9.00. | 61408 |
| Updated WebserviceRequestTrace to be able to write metric dimensions to Application Insights. | 60460 |

## Web Approval Portal 25.0.2
*Released: November 7, 2024*  

### New or changed functionality 

| Description | ID |
| --- | --- |
| Reading NAV-Error if web service returns a 500 error. | 60878 |

## Web Approval Portal 25.0.1
*Released: October 1, 2024*  

### New or changed functionality 

| Description | ID |
| --- | --- |
| Added missing translations. | 53842 |

## Web Approval Portal 25.0.0
*Released: October 1, 2024*  

### New or changed functionality 

| Description | ID |
| --- | --- |
| Removed Application Insights reference codes. |  |
| In advanced approval workflows, purchase lines requiring approval from the current approver are now highlighted in bold. This helps approvers easily identify the lines requiring their approval. | 57568 |
| The approval of purchase contracts is now supported. The following actions are available: **Approve**, **Reject**, and **Forward**. | 58404 |
| A new cross-company dashboard is now available. Approvers can choose between the classic dashboard and the new cross-company dashboard views in the web approval settings, offering more flexibility when managing approvals across multiple companies. | 58404 |
| Multi-factor authentication (MFA) device recovery process now allows you to receive the recovery link directly in your own trusted email (verifier email). Previously, a separate email address was required – often burdening admins. This update simplifies recovery and reduces admin involvement. | 59400 |
| When deleting an attachment with the original document present, the original document wasn't shown afterward – requiring a refresh of the page. | 56605 |

## Web Approval Portal 24.0.3
*Released: June 20, 2024*  

### New or changed functionality 

| Description | ID |
| --- | --- |
| Used GST for en-US language - changed to Tax. | 56819 |
| Culture names are no longer case-sensitive. | 56817 |
| Upgrading GdPicture to latest version (14.2.73). | 56694 |

### Bug fixes

| Description | ID |
| --- | --- |
| Changed async web service calls to use the "real" async methods. | 54406 |
| Fixed a bug which caused the overview to crash in case both versions were not updated from BC/NAV. | 56186 |

## Web Approval Portal 24.0.2
*Released: May 27, 2024*  

### Bug fixes

| Description |
| --- |
| Fixed an issue where the button “Put on hold and Approve” was not hidden while performing approval actions. |
| Fixed an issue where Expense Type were missing in overviews for Expense Management 12  SP 1 and above. |
| Fixed an issue for opening the Settings menu. |
| Fixed an issue where time zones incorrectly was taken into consideration. This caused some date fields to be displayed incorrectly. |
| Fixed an issue logging in with Microsoft 365 for on-premise installations. |
| Fixed an issue opening Purchase Contracts on mobile. |
| Fixed an issue changing VATProdPostingGroups on mobile. |

## Web Approval Portal 24.0.1
*Released: April 16, 2024*  

### Bug fixes

| Description |
| --- |
| Fixed an issue when calling the StdAmountDistributionCodes webservice. The error <em>“An asynchronous module or handler completed while an asynchronous operation was still pending”</em> occurred. Other webservices are still causing issues. These will be fixed in 24.0.3. |

## Web Approval Portal 24.0.0
*Released: April 16, 2024*  

### New or changed functionality 

| Description |
| --- |
| Added the number of approvals for the purchase, expense, mileage, per diem and expense report menu. Requires Document Capture 12 Service Pack 3. |
| Enhanced security around the use of password reset links. |

### Bug fixes

| Description |
| --- |
| Fixed an issue that occurred using the company selector in the mobile layout. |
| Fixed an issue where the columns got shifted when using the VendorRef column. |
| Fixed an issue accessing documents for customers running Expense Management 12 Service Pack 2. |

## Web Approval Portal 1.30.0
*Released: March 26, 2024*  

### New or changed functionality 

| Description |
| --- |
| A new column, **Vendor Invoice No**, has been added to the purchase approval documents. |
| Added columns for purchase contracts has been added for purchase invoices and credit memos. |
| Added the number and type of documents for approval in the company selector. |

## Web Approval Portal 1.29.2
*Released: February 16, 2024*  

### New or changed functionality 

| Description |
| --- |
| Change caching to being memory based instead of file based. |

### Bug fixes

| Description |
| --- |
| Fixed a bug where users got an error when creating a comment. |

## Web Approval Portal 1.29.1
*Released: January 9, 2024*  

### Bug fixes

| Description |
| --- |
| Dimension headers are now translated. |
| 2-decimal negative numbers are now formatted properly. |
| Fixed an issue with the PostedPurchaseInvoice webservice for Document Capture 12 Service Pack 2. |
| Fixed an issue with the DelegateMultiple functionality. |
| Fixed an issue when logging in with Office 365. |

## Web Approval Portal 1.29.0
*Released: December 4, 2023*  

### New or changed functionality 

| Description |
| --- |
| A new column, **Number**, has been added to all pages for Expense Management. |
| A new column, **Submitted by Delegated User**, has been added to all pages for Expense Management 2023 R2 Service Pack 1 and later. |
| A new column, **Matched to Transaction**, has been added to all pages for Expense Management 2023 R2 Service Pack 1 and later. |

### Bug fixes

| Description |
| --- |
| Fixed an issue that occured in the archive for Document Capture 2022 R2 Service Pack 2 when users selected the **Resource** type. |

## Web Approval Portal 1.28.2
*Released: October 2, 2023*  

### Bug fixes

| Description |
| --- |
| Fixed issue when using the Resource type for purchase lines. |

## Web Approval Portal 1.28.1
*Released: September 27, 2023*  

### Bug fixes

| Description |
| --- |
| Fixed issue with caching for Continia Online (cloud only). |

## Web Approval Portal 1.28.0
*Released: September 18, 2023*  

### New or changed functionality 

| Description |
| --- |
| Added header field Cash/Private Card to Expense |
| Added Description2 field to Expense |
| Added support for viewing attachment files with JPEG extension (Expense) |
| Removed the All and Comment link headers in the Per Diem view (Expense) |

### Bug fixes

| Description |
| --- |
| Fixed issue related to missing comments on Expenses. |
| Fixed issue with full-screen view of documents/attachments. |
| Fixed issue with Session Timeout warning overriding full-screen preview. |
| Fixed issue with Preview and Download links in the My Processed view. |
| Fixed issue with the amount being reset in the Amount Distribution view |
| Fixed issue with drag'n'drop files not showing in archive view. |

## Web Approval Portal 1.27.3
*Released: April 4, 2023*  

### Bug fixes

| Description |
| --- |
| Fixed issue with PDF reports for purchase orders |

## Web Approval Portal 1.27.2
*Released: March 28, 2023*  

### New or changed functionality 

| Description |
| --- |
| Added support for purchase orders and return orders (requires Document Capture 11 or later) |

### Bug fixes

| Description |
| --- |
| Limit of 200 companies in the Company selector has been removed |
| Fixed display issue for calculated distance for mileage |
| Display name is now correctly used for selected company |
| Added the option 'Beginning of Next Period' as a start date for deferral templates |
| Showing more fields for purchase contracts (requires Document Capture 11 or later) |
| Fixed issue with missing file extension resulting in an error |
| Fixed issue where special characters or keywords could result in an error |
| Updated branding images on the login page |

## Web Approval Portal 1.26.1
*Released: December 8, 2022*  

### Bug fixes

| Description |
| --- |
| Purchase Contracts removed from the Expense menu. |
| Fixed incorrect German text under the Purchase Contracts page. |

## Web Approval Portal 1.26.0
*Released: December 1, 2022*  

### New or changed functionality 

| Description |
| --- |
| Updated Continia branding |

### Bug fixes

| Description |
| --- |
| Suggested shared approver caused an error when saving settings. |
| Approve action in mobile view did not ask to keep on-hold status on a document. |
| Fixed issue with Deferral Templates web service. |
| Resetting the MFA code for the on-premises version failed. |
| Improved error messages. |

## Web Approval Portal 1.25.2
*Released: October 5, 2022*  

### Bug fixes

| Description |
| --- |
| Incorrect order of approvers shown on edit page. |

## Web Approval Portal 1.25.1
*Released: October 3, 2022*  

### Bug fixes

| Description |
| --- |
| Showing expense approvals resulted in an error message when using Expense Management version 3.0 or older. |

## Web Approval Portal 1.25.0
*Released: September 28, 2022*  

### New or changed functionality

| Description |
| --- |
| Added Finish language. |
| Added Portuguese language. |
| Added Billable field for Expense allocations. |
| Expense with attendees supports expense types other than "Food with guests". |
| Purchase Contract module updated for Document Capture version 9.03 and later. |
| User export data now includes company display name. |
| Outgoing e-mails for the on-premises version now support Modern Authentication (OAuth2). |

### Bug fixes

| Description |
| --- |
| PDF preview failed if filename had capitalized file extension. |
| Attachments on Expense mileages could not show in "Expense Report". |
| Date on expense edit page did not adjust for timezone. |

## Web Approval Portal 1.24.1
*Released: April 7, 2022*  

### Bug fixes

| Description |
| --- |
| Fixed missing translations |
| Fixed issue opening expenses when using Expense Management version 9.1 |

## Web Approval Portal 1.24.0
*Released: April 4, 2022*  

### New or changed functionality

| Description |
| --- |
| Added support for DC module Purchase Contracts (requires DC 9.00 or later) |
| Added brute-force protection for NavUserPassword login types (Web service key users). |
| Added support for multi-factor authentication (MFA) to the on-premises Web Approval Portal. For more information, see [On-premises features](https://continia.zendesk.com/hc/en-us/articles/4405372443922-OnPremise-features). |

### Bug fixes

| Description |
| --- |
| Fixed issue with headers during navigation in mobile view. |
| Fixed issue with "back" navigation in mobile view. |
| Fixed issue with error messages not showing correctly. |
| Fixed security vulnerabilities. |
| Fixed issue with browser auto-complete in "Forward to user" dialog. |
| Fixed issue during login, that might occur if the preferred tenant is not available. |
| Fixed issue with empty Job No. and Job Task No. descriptions. |
| Fixed issues when updating or filtering purchase line values containing some special characters. |

## Web Approval Portal 1.23.0
*Released: March 10, 2022*  

### New or changed functionality

| Description |
| --- |
| Added field Payment Type to Expense Management approval page (requires Expense Management version 9.0 or later). |

### Bug fixes

| Description |
| --- |
| Fixed issue with missing timestamp on document approval history. |
| Renamed the term "Settlement" to "Expense report" to conform with the change in Expense Management 9.0. |

## Web Approval Portal 1.22.0
*Released: January 27, 2022*  

### New or changed functionality

| Description |
| --- |
| Added support for new Continia demo system (cloud only). |

### Bug fixes

| Description |
| --- |
| Fixed issue with incorrect decimal formatting in some languages (e.g. Switzerland). |
| Fixed issue with documents not showing up correctly if using a direct link to Continia Online (Cloud only). |
| Fixed issue with company name not showing correctly when exported (on-premises only). |

## Web Approval Portal 1.21.0
*Released: December 13, 2021*  

### Bug fixes

| Description |
| --- |
| Reduced Windows credential login attempts to one attempt per domain to avoid blocking user account in Active Directory earlier than defined by company policy. |
| Fixed issue with dimension values missing. |
| Improved error messages. |
| Text field dimensions on ileages, per diems and settlements are now shown correctly. |
| Fixed issue of not being able to change company name when exporting users (on-premises only) |
| Fixed issue with not being able to delete all users (on-premises only) |

## Web Approval Portal 1.20.0
*Released: October 1, 2021*  

### New or changed functionality

| Description |
| --- |
| Added support for pre-approvals of Settlements. (Require Expense Management 8.0 SP1 or later) |

### Bug fixes

| Description |
| --- |
| The company with the most approvals is now set as the active company at login. |
| If a Microsoft 365 user is using the login form by mistake, we will automatically redirect to Microsoft 365 login. |
| Changing a dimension for a purchase line now updates the total amounts. |
| Fixed issue with Next and Previous buttons in Expense, Mileage, Per Diem, and Settlements. |
| Fixed an error in regards to token expiration when using Microsoft 365 login. |
| Fixed various translations- and spelling mistakes. |

## Web Approval Portal 1.19.0
*Released: August 31, 2021*  

### New or changed functionality

| Description |
| --- |
| Added support for Resource type on purchase lines (requires Document Capture 7.00 service pack 3 or later) |
| Changing company will no longer default to the purchase menu, but remember which menu was last used (e.g. Expense, Mileage, Per Diem, etc.) |

### Bug fixes

| Description |
| --- |
| Number formatting on purchase lines failed in localizations using space as a delimiter (e.g. Norwegian). |
| Translation errors |
| Improved error messages |
| Improved traceability on user export scenarios (Cloud only) |

## Web Approval Portal 1.18.4
*Released: July 2, 2021*  

### Bug fixes

| Description |
| --- |
| Errors when calling a web service could lead to the web page becoming unresponding (no error was shown). |
| Performance has been improved when approving expenses with allocation lines disabled. |
| Performance has been improved on many pages, as an unneeded call to WebUserCompanies has been removed. |

## Web Approval Portal 1.18.3
*Released: June 16, 2021*  

### Bug fixes

| Description |
| --- |
| Extended per-user traceability on web service requests (troubleshooting only) |
| Extended functionality of diagnostics page to include actual company data |

## Web Approval Portal 1.18.2
*Released: June 2, 2021*  

### Bug fixes

| Description |
| --- |
| Using direct links from an e-mail for a user with access to multiple databases and Document Capture 4.00.03 (this version specifically) would cause an error. |

## Web Approval Portal 1.18.1
*Released: May 27, 2021*  

### Bug fixes

| Description |
| --- |
| Microsoft 365 users would get an "Access Token is missing" error upon login. |
| Selecting a type in a purchase line in mobile view would cause an error. |

## Web Approval Portal 1.18.0
*Released: May 17, 2021*  

### Bug fixes

| Description |
| --- |
| Direct links (from emails or browser-favorites) did not always select the correct database. |
| Fixed a translation in Mileage where it mentions expenses by mistake. |
| Fixed Polish translations for Inter-Company labels. |
| The "wait spinner" would not stop, when an attachment was dragged to a Purchase-, Expense-, Mileage- or Per Diem document. |
| Switching databases on mobile view would result in an error if using a Document Capture version older than 4.0.3 |
| Failed to send an e-mail when a user is requesting to reset password. |
| Cached user permissions are cleared when exporting users. |

## Web Approval Portal 1.17.2

### Bug fixes

| Description |
| --- |
| OnPremise version failed when exporting users from Document Capture, if the optional field FullName was not filled. |

## Web Approval Portal 1.17.1
*Released: March 10, 2021*  

### Bug fixes

| Description |
| --- |
| An error message related to the mapping of Inter-Company fields was shown on some Document Capture versions. |
| The progress icon shown during purchase line updates was displayed in multiple copies on the line updating. |
| A misleading error message was shown when a user, with access to multiple NAV/BC instances, did not have proper access to the instance the user was currently trying to connect to. |
| A Javascript error resulted in users not being able to update purchase lines when using Internet Explorer 11. (Please note that we do not actively support IE11 as described in our documentation) |
| An error message was shown if a new purchase line was created by clicking in a drop-down field on the empty line. |

## Web Approval Portal 1.17.0
*Released: February 25, 2021*  

### New or changed functionality

| Description |
| --- |
| Added support for Inter-Company fields on purchase lines. (Requires Document Capture 7.0 or later) |
| Copy Out-of-Office to all companies. (Requires Document Capture 7.0 or later) |
| Added a calculated column to show the difference between imported and assigned amounts. |

### Bug fixes

| Description |
| --- |
| Summed amounts on grouped approvals (approval sharing) showed incorrectly or not at all. |
| Error loading preview of PDF images sometimes blocked the entire approval page. |
| "More search results" were incorrectly showing when the MaxSearchResult property was set to 0 in the configuration file. (On-premises only) |
| View- and download buttons on the Archive search result were not working. |
| The "Back to search result" button in the Archive view did not return to the most recent search result in case more than one search was performed. |
| E-mails dragged from Outlook to the attachment list on a document were moved instead of copied. |
| The preview of multipage PDF files was not working on the approval overview list. |
| Expense, Mileage, and Per Diem menus were still shown when Settlements was configured to be mandatory. |

<style>
  .content table tr td:nth-child(1) {
    width: 690px;
  }
  .content table tr td:nth-child(2) {
    width: 40px;
  }  
</style>