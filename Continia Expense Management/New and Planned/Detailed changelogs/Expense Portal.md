---
title: Detailed Changelog for the Continia Expense Portal
date: 09-07-2025
description: Learn about new features and bug fixes for Continia Expense Portal version
lang: en
---

# Detailed changelog for the Continia Expense Portal
This article lists all of the new features and bug fixes for each version of the Continia Expense Portal.

## Expense Portal 26.2.0.6
*Released: July 04, 2025*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix |


## Expense Portal 26.2.0.5
*Released: July 01, 2025*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix - Sending an expense via email works again as it should. |


## Expense Portal 26.2.0.4
*Released: June 27, 2025*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 26.2.0.3
*Released: June 27, 2025*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 26.2.0.2
*Released: June 25, 2025*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 26.2.0.1
*Released: June 25, 2025*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 26.2.0.0
*Released: June 27, 2025*

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| Expense Reports | You can no longer submit expense reports that have departure dates < 01-01-2000. Such dates will instead be changed to today's date to avoid breaking the synchronization process in Business Central. |
| General | When a search returns exactly 1 value, non-editable fields are not auto-filled. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix - Better support for field dependency relations with multiple Field Types for the same Reference Field Type. |


## Expense Portal 26.0.0.5
*Released: June 11, 2025*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix - Documents were sometimes displaying textboxes with a height of 0. This made it appear as a flat line and meant it was impossible to enter text into. |


## Expense Portal 26.0.0.4
*Released: May 26, 2025*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfix - If a numeric field is mandatory, based on a field dependency and the document is added to settlement, the mandatory status is now tested. This means that when an expense type is "Electricity", the field "Electricity kwh" becomes mandatory. This works on a standalone expense, but not when the document is added to an expense report. |


## Expense Portal 26.0.0.3
*Released: May 21, 2025*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfix - The Milage OCR code following an attachment adding caused the description to be overwritten. The OCR did not perform. However, the OCR code was executed, which overwrote the description. |
| General | Minor bugfix - You can find the description on an expense report in `Description` > `Merchant` >  `TransactionDescription` (the same as it is in the expense overview). |


## Expense Portal 26.0.0.2
*Released: May 15, 2025*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfix - Add Merchant to the expense overview if the Description is empty. Next add a Transaction description to the expense overview if the Merchant field is empty, and then move the Merchant field to immediately after the Description field when an expense is being edited. |


## Expense Portal 26.0.0.1
*Released: May 7, 2025*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix - When a user logged in using Microsoft Office365 in the portal, delegation was not cleaned up. However, it worked for both login types in the app and for the username and password in the portal. |


## Expense Portal 26.0.0.0
*Released: April 1, 2025*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes and improvements to provide support for Boolean Fields in Field Dependency. (Expense Management 2025 R1 required). |


## Expense Portal 25.0.1.3
*Released: March 3, 2025*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 25.0.1.2
*Released: February 24, 2025*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix and improvements. |


## Expense Portal 25.0.1.1
*Released: January 9, 2025*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix to provide support for Polish characters. |


## Expense Portal 25.0.1.0
*Released: January 21, 2025*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 25.0.0.91
*Released: January 21, 2025*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 25.0.0.9
*Released: January 9, 2025*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 25.0.0.8
*Released: December 9, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Fixed an issue where expense document dates prior to January 1, 1900, in the Expense App and the Expense Portal resulted in problems when synchronized with Business Central. Such dates are now set to today's date to ensure seamless synchronization. |


## Expense Portal 25.0.0.7
*Released: December 3, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Improved PDF support. |
| General | Improved accessibility support: When the upload file box for receipts has focus, you can now open the upload file dialog by selecting the Spacebar or the Enter key. |


## Expense Portal 25.0.0.6

This version was only released internally.


## Expense Portal 25.0.0.5

*Released: November 11, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | In the Expense Portal, you can no longer select both **From home** and **To home** at the same time for a mileage. |


## Expense Portal 25.0.0.4
*Released: November 4, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Accessibility support has been added. This means that people who are blind or have low vision can add attachments using key combinations instead of having to use a mouse. |


## Expense Portal 25.0.0.3
*Released: October 29, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 25.0.0.2
*Released: October 23, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Improved push notifications for Android. |
| General | Minor improvements and bug fixes. |


## Expense Portal 25.0.0.1
*Released: October 2, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements and bug fixes. |


## Expense Portal 25.0.0.0
*Released: October 1, 2024*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Add existing documents to an expense report. |
| Mileage | Enhanced Attachment Control on Mileage Expenses (Expense Management 2024 R2 required.). |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements and bug fixes. |


## Expense Portal 24.0.0.5

*Released: August 5, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements and hot fixes. |


## Expense Portal 24.0.0.4

*Released: July 1, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Status Spinner was running for very long time. |
| General | Order of Configured Fields was not respected. |
| General | Improved general performance. |


## Expense Portal 24.0.0.3

*Released: June 27, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | If you in the Expense App or the Expense Portal deleted a document on an expense report, submitted the expense report, then regretted and reopened it before Business Central had completed synchronization, the deleted documents would be reopened as well. |
| General | New delegations were not exported after update 24.0.0.2. |

## Expense Portal 24.0.0.2

*Released: June 21, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor update. |


## Expense Portal 24.0.0.1

*Released: June 19, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Bug fixes and minor improvements. |


## Expense Portal 24.0.0.0

*Released: June 13, 2024*  

The versioning of the Expense Portal has changed to be in line with the rest of Continia's product portfolio, mening that there never was or will be any versions from and including 4.0.1.9 to and including 23.x.x.x.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Users are no longer signed out without being warned first. |


## Expense Portal 4.0.1.8

*Released: June 10, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements. |


## Expense Portal 4.0.1.7

*Released: May 30, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvement. |


## Expense Portal 4.0.1.6

*Released: May 29, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements and updates. |


## Expense Portal 4.0.1.5

This version was only released internally.


## Expense Portal 4.0.1.4

*Released: May 21, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 4.0.1.3

*Released: May 16, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvement. |


## Expense Portal 4.0.1.2

*Released: May 6, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 4.0.1.1

*Released: May 3, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements and bug fixes. |


## Expense Portal 4.0.1.0

*Released: April 30, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes and improvements. |


## Expense Portal 4.0.0.9

*Released: April 24, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 4.0.0.8

*Released: April 23, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes and improvements. |


## Expense Portal 4.0.0.7

*Released: April 22, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor updates and bug fixes. |


## Expense Portal 4.0.0.6

This version was only released internally.


## Expense Portal 4.0.0.5

*Released: April 15, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 4.0.0.4

*Released: April 11, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements. |


## Expense Portal 4.0.0.3

*Released: April 10, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | If you opened a settlements document and from the document used the browser backspace button to return to the settlement, the settlement threw an error if you saved it. |
| General | Mandatory fields are not shown based on field dependencies set on Payment Type if the payment type is filled in and set from bank transaction. Also works for currency if that is set by a bank transaction and has dependant fields. |
| General | Minor improvements and bug fixes. |


## Expense Portal 3.8.6.9-4.0.0.2

These versions were only released internally.


## Expense Portal 3.8.6.8

*Released: January 18, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvement. |


## Expense Portal 3.8.6.7

*Released: January 15, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvement. |


## Expense Portal 3.8.6.6

*Released: January 9, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements. |


## Expense Portal 3.8.6.5

*Released: January 9, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | When you send in an expense via email and you have multiple companies and the expense is added to a company that requires signed pdfs, signed pdfs will now be created. |
| General | Minor improvements. |


## Expense Portal 3.8.6.4

*Released: January 9, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor updates and improvements. |


## Expense Portal 3.8.6.3

*Released: December 15, 2023*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | If a selection in a parent field results in a search for a child field and the search only returns a single value, it is autoselected in the child. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | You can click backspace in the browser on preapproval of a settlement, and when you open the new settlement you can still add a preapproval amount. |


## Expense Portal 3.8.6.2

*Released: December 14, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvement. |


## Expense Portal 3.8.6.1

*Released: December 13, 2023*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Added amount including tax field to backend and UI. |
| General | Added system-created allocation field to backend. |
| General | Made VAT amount and other decimals editable in an allocation if the the field setup says editable. |
| General | An empty file was saved as company logo because of a missing size check. |


## Expense Portal 3.8.6.0

*Released: November 21, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes and improvements. |


## Expense Portal 3.8.5.7

*Released: November 9, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.8.5.6

*Released: November 7, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.8.5.5

*Released: November 1, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.8.5.4

*Released: November 1, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.8.5.3

*Released: October 25, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.8.5.2

*Released: October 17, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.8.5.1

*Released: October 16, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.8.5.0

*Released: October 16, 2023*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Support for Autofill (requires Expense Management 2023 R2). |
| General | Support for ESG Expense Types (requires Expense Management 2023 R2). |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes and improvements. |


## Expense Portal 3.8.4.3

*Released: October 4, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 3.8.4.2

*Released: October 3, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements and bug fixes. |


## Expense Portal 3.8.4.1

*Released: October 3, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements and bug fixes. |


## Expense Portal 3.8.4.0

*Released: October 2, 2023*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Capabilities for autofill on field types is added. Field values can be suggested in the Expense Portal and Expense Mobile App based on previously used values. |
| General | Expense users can edit VAT Amounts, but only if the "VAT amount" field has been configured. |


## Expense Portal 3.8.1.3

*Released: May 15, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements and bug fixes. |


## Expense Portal 3.8.1.2

This version was not released to production.


## Expense Portal 3.8.1.1

*Released: May 2, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements and bug fixes. |


## Expense Portal 3.8.1.0

This version was not released to production.


## Expense Portal 3.8.0.0

*Released: April 25, 2023*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Preparing for future Expense App 3.58 release, allowing new document types for receipts for the app: "doc", "docx", "xls", "xlsx", "ppt", "pptx". |


## Expense Portal 3.7.9.2

*Released: March 30, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvement. |


## Expense Portal 3.7.9.1

*Released: March 29, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvement. |


## Expense Portal 3.7.9.0

*Released: March 28, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvement. |


## Expense Portal 3.7.8.0

*Released: March 27, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements. |


## Expense Portal 3.7.7.7

*Released: March 14, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 3.7.7.6

*Released: March 10, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.7.5

*Released: March 6, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.7.4

*Released: February 27, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.7.3

*Released: February 13, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.7.2

*Released: February 8, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 3.7.7.1

*Released: February 8, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 3.7.7.0

*Released: February 7, 2023*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | When .heic images are uploaded, they will be converted to .jpg. |
| General | Company Display Names will be displayed in the same way in the Expense Portal as in the Expense App. |
| General | Support for amounts in LCY on per diem days added. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes and updates. |


## Expense Portal 3.7.6.4

*Released: January 25, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.6.3

*Released: December 15, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes and improvements. |


## Expense Portal 3.7.6.2

*Released: December 7, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.6.1

*Released: December 2, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.6.0

*Released: November 30, 2022*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Added support for AI Receipt Scanner in the Expense Management Portal. |
| General | Continia rebranding: New logo, new colors, etc. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes and improvements. |


## Expense Portal 3.7.5.0

*Released: November 4, 2022*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Added support for AI Receipt Scanner in the Expense App. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes and improvements. |


## Expense Portal 3.7.4.3

*Released: October 25, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.4.2

*Released: October 11, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.4.1

*Released: October 11, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes and improvements. |


## Expense Portal 3.7.4.0

*Released: September 28, 2022*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Images saved to Saved Images are now synchronized automatically between the Expense App and the Expense Portal. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes and improvements. |


## Expense Portal 3.7.3.1

*Released: August 17, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.3.0

*Released: August 15, 2022*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Users now have the option to define the regional settings Language and Numbers and Units, which makes it possible to use one UI language but use the rules for the numbers format in accordance with another language.  |


## Expense Portal 3.7.2.46

*Released: May 10, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.2.45

*Released: April 06, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.2.44

*Released: April 06, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 3.7.2.43

*Released: April 05, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 3.7.2.43

*Released: April 05, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 3.7.2.42

*Released: April 04, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 3.7.2.41

*Released: April 01, 2022*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Lookup values for payment types can limit to default currency in currency lookup. |
| General | If a user has not gotten payment types assigned, the lookup values list in CO will show no values (for other fields it will be all values). |


## Expense Portal 3.7.2.4

*Released: March 22, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 3.7.2.3

*Released: March 21, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.2.2

*Released: March 21, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 3.7.2.1

*Released: March 16, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Improvements and bug fixes. |


## Expense Portal 3.7.2.0

*Released: February 21, 2022*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Added the payment type feature, which expands payment options (Expense Management 2022 R1 required). |
| General | Added Selectable possibility for payment type to backend between nav and app (Expense Management 2022 R1 required). |
| General | Added Description2 field for mileages and per diems. |
| General | The term ”Settlement” has been changed to “Report”. This only applies to the English localization of the website. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Improved exception handling. |
| General | Much faster fetch of long lists of lookup values in the app. |


## Expense Portal 3.7.1.41

*Released: January 11, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements and updates. |


## Expense Portal 3.7.1.4

*Released: December 20, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements. |


## Expense Portal 3.7.1.3

*Released: December 16, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements. |


## Expense Portal 3.7.1.2

*Released: December 16, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor improvements. |


## Expense Portal 3.7.1.1

*Released: December 15, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Improvements and minor bug fixes. |


## Expense Portal 3.7.1.0

*Released: December 7, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 3.7.0.14

*Released: December 2, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Bug fixes. |


## Expense Portal 3.7.0.13

*Released: November 30, 2021*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Added a manual bank, Belfius. |


## Expense Portal 3.7.0.12

*Released: November 16, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fixes. |


## Expense Portal 3.7.0.11

*Released: November 10, 2021*  


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bug fix. |


## Expense Portal 3.7.0.10

*Released: November 8, 2021*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Support for extra date fields added. |
| General | The document menu items Expense, Mileage, Per Diem, and Settlement are now displayed if certain conditions are met.<br>The specific conditions are as follows: 1) OnlyUseSettlement is true but the user has open documents of that type (expense, mileage or per diem), 2) OnlyUseSettlement is false and either 2.a) the document type is enabled in expense setup for any of the user’s companies, or 2.b) the document type is disabled in expense setup for all the user’s companies, but the user has (old) documents of that type in any user company. |
| General | Translating history status to UI language. |
| General | When you transfer a document to a settlement in the app, the settlement dimensions are transferred to the documents on the settlement if valid. Requires Expense App 3.15 (soon to be released) or newer. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Optimizations in the portal. |


## Expense Portal 3.7.0.9

*Released: November 2, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Portal optimizations. |


## Expense Portal 3.7.0.8

*Released: November 2, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfixes. |


## Expense Portal 3.7.0.7

*Released: November 1, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfixes and optimizations. |


## Expense Portal 3.7.0.4-3.7.0.6

These hotfixes were never released to production.


## Expense Portal 3.7.0.3

*Released: September 30, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfixes and optimizations. |


## Expense Portal 3.7.0.2

*Released: September 30, 2021*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Updating style.css so the active page (Expense, mileage per diem etc) is marked as active with another color. |


## Expense Portal 3.7.0.1

*Released: September 22, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfixes and improvements. |


## Expense Portal 3.7.0.0

*Released: September 21, 2021*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | New UI for OnlyUseSettlement. |
| General | Show warning if user tries to submit a per diem without days. |
| General | New Per Diem days can now have all selections true or false based on a company setting. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | If you have more than 100 items in a list the “More results in database” will again be the last item on the list. |
| General | Minor bugfixes and improvements. |


## Expense Portal 3.6.1.1

*Released: September 07, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfixes and improvements. |


## Expense Portal 3.6.1.0

*Released: September 05, 2021*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Simpler UI for OnlyUseSettlement. |
| General | Showing which settlement a document belongs to, when it belongs to a settlement. |
| General | When you save a document belonging to a settlement, you return to the settlement, not to the document overview. |
| General | Warning showing if a user tries to submit a per diem without days. Preventing submit. |
| General | Warning showing if a user tries to submit a per diem where nothing has been selected for any days. Yes/No choice since this is valid. |


## Expense Portal 3.6.0.2

*Released: September 01, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfixes. |


## Expense Portal 3.6.0.1

*Released: September 01, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfixes. |


## Expense Portal 3.6.0.0

*Released: August 30, 2021*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Easy and simple login with Microsoft 365. |
| General | Support for per multiple diem destinations (Expense Management 2021 R2 required). |
| General | Support for settlement pre-approval (Expense Management 2021 R2 required). |
| General | New quick and efficient activation flow for credit card agreements in both new and old versions of Microsoft Business Central. |
| General | Minor bugfixes and improvements. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfixes and improvements. |


## Expense Portal 3.5.0.2

*Released: June 04, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfixes. |


## Expense Portal 3.5.0.1

*Released: June 04, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description |
| --- | --- |
| General | Minor bugfixes and improvements. |


## Expense Portal 3.5.0.0

*Released: May 25, 2021*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  |
| --------------------------------------------------------- | ------------------------------------------------------------ |
| General                                                   | Notifications are now sent to the user’s phone when there are changes, relevant for the user, in Microsoft Business Central. |
| General                                                   | Currency field default to Amount LCY sent from BC. Requires Expense Management 6.50 or later. |
| General                                                   | Adding support for Diners Club International. Automatic credit card transactions import. |

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  |
| --------------------------------------------------------- | ------------------------------------------------------------ |
| General                                                   | A field dependency is require to have the Attachment option to work correctly. |
| General                                                   | Relationship to Delegated user is not removed when company is completely deleted. |


## Expense Portal 3.4.0.5

*Released: April, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                             |
| --------------------------------------------------------- | --------------------------------------- |
| General                                                   | Minor Microsoft 365 login optimization. |


## Expense Portal 3.4.0.4

*Released: April, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  |
| --------------------------------------------------------- | ------------------------------------------------------------ |
| General                                                   | When you have a field dependency relation between ie Department and JobNo but only Department exist on ie a mileage, you would get a null exception. |


## Expense Portal 3.4.0.3

*Released: April, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                  |
| --------------------------------------------------------- | -------------------------------------------- |
| General                                                   | Updated component for digital signing PDF’s. |


## Expense Portal 3.4.0.2

*Released: March 1, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  |
| --- | --- |
| General | Small fix to support some app functionality. |


## Expense Portal 3.4.0.1

*Released: March 1, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  |
| --- | --- |
| General | Small fix for Field Dependencies, this could fail in some cases not showing all values the user had access too. |


## Expense Portal 3.4.0.0

*Released: February 18, 2021*  

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  |
| --- | --- |
| General | Delegations - Feature support for Expense Management 7.00 with the secretary function, allowing one user to have responsibility for another users expenses, mileage etc |
| General | Field Dependencies - Feature support for Expense Management 7.00 where we introduced Field dependencies. meaning we allow fields to change behavior based on value choosen in another field |
| General | Attachment expectations - Feature support for Expense Management 7.00 where you can choose when an attachment is required |
| General | Disable possibility to create new document types (Expense, mileage Settlement or per-diem) but allow edit of existing documents of the type, if the document type is disabled in Expense Management Setup in BC/NAV |
| General | Settlements Required - Feature support for Expense Management 7.00 where you can make settlements mandatory, meaning the user can only press send on settlements, not other document types. |



<style>
  .content table tr td:nth-child(1) {
    width: 40px;
  }
  .content table tr td:nth-child(2) {
    width: 690px;
  }  
</style>