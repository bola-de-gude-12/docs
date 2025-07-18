---
title: Detailed Changelog for the Expense Mobile App
date: 30-06-2025
lang: en
---

# Detailed Changelog for the Continia Expense App

This article lists all new features and bug fixes for each version of the Continia Expense Mobile App.

## Expense App 26.02

_Released: June 27, 2025_

### Bug fixes

| Functional area | Description                                                                                                                           |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------- |
| General         | On some Android devices it is not possible to search for an address when using the map functionality, as it returns an error.         |
| General         | Minor bug fix - Better support for field dependency relations with multiple Field Types for the same Reference Field Type on Mileage. |

## Expense App 26.01, hotfix 1

_Released: May 16, 2025_

### Bug fixes

| Functional area | Description                                                                                                |
| --------------- | ---------------------------------------------------------------------------------------------------------- |
| General         | In the list of documents, the **Merchant** field must be shown in case the **Description** field is empty. |
| General         | OCR data will not overwrite the **Merchant** field on Expenses, which is matched to a Bank Transaction.    |

## Expense App 26.01

_Released: May 01, 2025_

### Bug fixes

| Functional area | Description                                                                                                                                                                                                         |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | 60-Day Rule error message for missing GPS locations - The app now only displays an error message for missing GPS locations _if_ the 60-day Rule is enabled _and_ the Expense Management version is 12.04 or higher. |

### New or changed functionality

| Functional area | Description                                                                                                                   |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------- |
| General         | Ability to edit receipt details - Users can now edit saved receipt details that have been captured by the AI Receipt Scanner. |

## Expense App 26.00

_Released: March 10, 2025_

### Bug fixes

| Functional area | Description                                                                                                                                                                                                                                               |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | Support for Boolean Fields in Field Dependency - We now support Boolean fields in Field Dependency. This enhancement allows users to create more dynamic and flexible field dependencies including Boolean fields, (Expense Management 2025 R1 required). |

## Expense App 25.08

_Released: March 5 2025_

### Bug fixes

| Functional area | Description                                                                                                                                                                                                                                                                                                                              |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | Enhanced Lookup Description Field - The lookup description field has been improved to better handle text up to 100 characters. This enhancement ensures more accurate and comprehensive descriptions within the lookup field.                                                                                                            |
| General         | Ability to Open Attendee List for Historical Expenses - Users can now open the list of attendees for expenses that are in the history list. This enhancement allows for better review and verification of past expense records.                                                                                                          |
| General         | Duplicate Mileage Submission Confirmation - When submitting a mileage entry with details similar to a submitted document in the history document list, a confirmation message displays. This message asks the user to confirm if they are sure about submitting a mileage entry that appears to be a duplicate of one already submitted. |

## Expense App 25.07

_Released: February 11, 2025_

### Bug fixes

| Functional area | Description                                                                                                                                                                                                                                                |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | Address Validation: When the 60 Days Rule is enabled, a confirmation message now appears if the selected address differs from the home address but is within 500 meters. This ensures users are informed of minor address discrepancies before proceeding. |
| General         | Field captions now reflect the selected language on iOS devices accurately.                                                                                                                                                                                |
| General         | JPEG files can now be shared from storage to the Expense App on Android, restoring previous functionality.                                                                                                                                                 |

## Expense App 25.06

_Released: January 9, 2025_

### Bug fixes

| Functional area | Description    |
| --------------- | -------------- |
| General         | Minor bug fix. |

## Expense App 25.05

_Released: December 12, 2025_

### Bug fixes

| Functional area | Description    |
| --------------- | -------------- |
| General         | Minor bug fix. |

## Expense App 25.04

_Released: November 20, 2024_

### New or changed functionality

| Functional area | Description                                                                                                                                                                                                                                                                                         |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | <p>A new <strong>Merchant</strong> field has been added to the <strong>Expenses</strong> page. If data is available from a Business Central transaction or detected by the AI Receipt Scanner, the merchant will be displayed.<br></p><p>Note</p><p>Expense Management 2024 R2 SP1 is required.</p> |
| General         | <p>With the introduction of the <strong>Merchant</strong> field, the AI Receipt Scanner will no longer update the <strong>Description</strong> field if it is set as mandatory on the <strong>Configured Field</strong> page.<br></p><p>Note</p><p>Expense Management 2024 R2 SP1 is required.</p>  |
| General         | Support for VoiceOver (iOS) and TalkBack (Android) has been improved to increase accessibility for people who are blind or have low vision.                                                                                                                                                         |

## Expense App 25.03

_Released: October 31, 2024_

### Bug fixes

| Functional area | Description                                                                               |
| --------------- | ----------------------------------------------------------------------------------------- |
| General         | It was not possible to select a lookup value if there were more than two field relations. |
| General         | The time format always used the AM/PM system (12-hour clock).                             |

## Expense App 25.02

_Released: October 22, 2024_

### Bug fixes

| Functional area | Description                                                                                                     |
| --------------- | --------------------------------------------------------------------------------------------------------------- |
| General         | The **Select** action on the **Receipt** page was not visible when **Expense Report** was set to **Mandatory**. |

## Expense App 25.01

_Released: October 3, 2024_

### Bug fixes

| Functional area | Description                                                                |
| --------------- | -------------------------------------------------------------------------- |
| General         | Not always showing the right Description Value for lookup value selection. |

## Expense App 25.00

_Released: September 25, 2024_

### Bug fixes

| Functional area | Description                                                       |
| --------------- | ----------------------------------------------------------------- |
| General         | Limited Access to Camera Roll on iOS was not working as expected. |

## Expense App 24.00

_Released: September 16, 2024_

### Bug fixes

| Functional area | Description                                                                                           |
| --------------- | ----------------------------------------------------------------------------------------------------- |
| General         | App crash when applying the selection of Per Diem Detail default values.                              |
| General         | On Android, when Document Date is mandatory and selecting a new date, it starts on January 1rst 1900. |

## Expense App 3.68, hotfix 2

_Released: July 3, 2024_

### Bug fixes

| Functional area | Description                                                                                           |
| --------------- | ----------------------------------------------------------------------------------------------------- |
| General         | Creating new Expense from Expense Report, App do not check open documents for a matching transaction. |

## Expense App 3.68, hotfix 1

This version was only released internally.

## Expense App 3.68

_Released: April 5, 2024_

### Bug fixes

| Functional area | Description                                                                                   |
| --------------- | --------------------------------------------------------------------------------------------- |
| General         | Code fields were not inherited when using Drag & Drop to add a document to an expense report. |
| General         | Swiss numbers were not displayed correctly.                                                   |

## Expense App 3.67

_Released: January 16, 2024_

### Bug fixes

| Functional area | Description                                                                           |
| --------------- | ------------------------------------------------------------------------------------- |
| General         | Adding the decimal delimiter on some Android phones could result in application stop. |

## Expense App 3.66

_Released: January 9, 2024_

### New or changed functionality

| Functional area | Description                                                                                                  |
| --------------- | ------------------------------------------------------------------------------------------------------------ |
| General         | The receipt action is promoted on open expense or mileage page even if no saved receipts exist for the user. |

### Bug fixes

| Functional area | Description                                                                                                 |
| --------------- | ----------------------------------------------------------------------------------------------------------- |
| General         | Static map of mileage route got deleted when creating return mileage or creating mileage based on template. |
| General         | The app was crashing if Mileage was cancelled when the Expense Report was set to mandatory.                 |

## Expense App 3.65

_Released: December 15, 2023_

### Bug fixes

| Functional area | Description                                                                                                                          |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| General         | When an error message occurs at startup saying that the last used company does not exist, the user could not continue using the app. |

## Expense App 3.64

_Released: December 4, 2023_

### Bug fixes

| Functional area | Description                                                                                                 |
| --------------- | ----------------------------------------------------------------------------------------------------------- |
| General         | Static map of mileage route got deleted when creating return mileage or creating mileage based on template. |

## Expense App 3.63

_Released: November 20, 2023_

### New or changed functionality

| Functional area | Description                                                                                                                                    |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | Added the ability to filter by documents with a checkmark in History.                                                                          |
| General         | Added the ability to filter by the status **Submitted by** in History.                                                                         |
| General         | Attendees are visible in the Template view.                                                                                                    |
| General         | OCR details detected by the AI Receipt Scanner are now visible in Details in Saved Receipts.                                                   |
| General         | Added the ability to add one self as an attendee on the Attendees page.                                                                        |
| General         | The expense user's name is now displayed below the company name on the start page. The email address can still be viewed on the Settings page. |

### Bug fixes

| Functional area | Description                                                                    |
| --------------- | ------------------------------------------------------------------------------ |
| General         | It was possible to add documents to expense reports with the status Submitted. |

## Expense App 3.62

_Released: October 10, 2023_

### New or changed functionality

| Functional area | Description                                                                           |
| --------------- | ------------------------------------------------------------------------------------- |
| General         | If Arrival and Departure is detected on Hotel invoice, we calculate "Number of days". |

## Expense Mobile App 3.61, hotfix 1

_Released: October 4, 2023_

### Bug fixes

| Functional area | Description                                                                   |
| --------------- | ----------------------------------------------------------------------------- |
| General         | Android only: Fixed bug where camera was not working on some Samsung devices. |

## Expense App 3.61

_Released: September 23, 2023_

### Bug fixes

| Functional area | Description                                                                                                            |
| --------------- | ---------------------------------------------------------------------------------------------------------------------- |
| General         | Fixed bug where the Cash/Private Card boolean always was sent with value FALSE in case user don't have a company card. |

## Expense App 3.60

_Released: September 18, 2023_

### New or changed functionality

| Functional area | Description                                                                                                                                                                   |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | Introduced the Auto-Fill feature.                                                                                                                                             |
| General         | When adding a new receipt that does not match an existing expense, the user will get a message and be guided to the Receipt List.                                             |
| General         | Expense App will allocate VAT Items lines (Expense Management 2023 R2 required.).                                                                                             |
| General         | A new warning if the user tries to create an expense from a receipt and an equal expense with same date and amount has already been submitted.                                |
| General         | Currency Code, ISO code and AI Receipts scanner values are now mapped (Expense Management 2023 R1, Service Pack 2 required).                                                  |
| General         | Matching Tolerance from Payment Type is now respected in Expense App. Hardcoded to 4 days, before if before Expense Management 2023 R2 (Expense Management 2023 R2 required). |
| General         | If errors on any Allocation lines when submitting, the user will be guided to the lines.                                                                                      |
| General         | If errors are found on one or more documents on an Expense Report when submitting, the user is now guided to the error.                                                       |

## Expense App 3.58

_Released: June 7, 2023_

### New or changed functionality

| Functional area | Description                                                                                                    |
| --------------- | -------------------------------------------------------------------------------------------------------------- |
| General         | Enhanced sharing capabilities.                                                                                 |
| General         | Introducing Receipt List: an advanced replacement for the Saved Image List, supporting various document types. |
| General         | Enhanced matching capabilities for receipts and expenses, improving accuracy and efficiency.                   |
| General         | Assisting user not to create duplicate expense.                                                                |

## Expense App 3.57

_Released: March 20, 2023_

### New or changed functionality

| Functional area | Description                                                                                                          |
| --------------- | -------------------------------------------------------------------------------------------------------------------- |
| General         | Added the possibility to assign expenses to a company when having multiple companies.                                |
| General         | The user will be asked if they want to merge two expenses if these expenses have the same amount, currency and date. |

## Expense App 3.56

_Released: February 10, 2023_

### New or changed functionality

| Functional area | Description                                               |
| --------------- | --------------------------------------------------------- |
| General         | Improved allocation functionality.                        |
| General         | Expense type icons are now displayed in allocation lines. |

### Bug fixes

| Functional area | Description                                                                    |
| --------------- | ------------------------------------------------------------------------------ |
| General         | FROM and TO fields get added to dimension values in some situations now fixed. |
| General         | Bug fixes and improvements.                                                    |

## Expense App 3.55

_Released: January 18, 2023_

### New or changed functionality

| Functional area | Description                                                               |
| --------------- | ------------------------------------------------------------------------- |
| General         | The Polish and Portuguese languages are now available in the Expense App. |

### Bug fixes

| Functional area | Description                                                                                                                                                           |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | If start and end date are used on Expense Reports, expense users will now get a warning if they try to add documents outside of the defined start and end date range. |
| General         | Mileage distance on Expense Reports now match the distance unit that's specified on the Expense Management Setup page.                                                |
| General         | If the amount has been added already, and AI Receipt Scanner finds the same amount, allocations will not be cleared.                                                  |

## Expense App 3.54

_Released: December 15, 2022_

### New or changed functionality

| Functional area | Description                                                           |
| --------------- | --------------------------------------------------------------------- |
| General         | It's now possible to save attachment images from submitted documents. |

### Bug fixes

| Functional area | Description                       |
| --------------- | --------------------------------- |
| General         | Minor bug fixes and improvements. |

## Expense App 3.53

_Released: December 3, 2022_

### Bug fixes

| Functional area | Description                       |
| --------------- | --------------------------------- |
| General         | Minor bug fixes and improvements. |

## Expense App 3.52

_Released: November 28, 2022_

### New or changed functionality

| Functional area | Description                                          |
| --------------- | ---------------------------------------------------- |
| General         | It's now possible to enter negative expense amounts. |

### Bug fixes

| Functional area | Description                                                                                              |
| --------------- | -------------------------------------------------------------------------------------------------------- |
| General         | If no amount is detected, AI Receipt Scanner will not insert a currency, even if a currency is detected. |

## Expense App 3.51

_Released: November 17, 2022_

### New or changed functionality

| Functional area | Description                                        |
| --------------- | -------------------------------------------------- |
| General         | Continia rebranding: New app icons and new colors. |

## Expense App 3.50

_Released: November 8, 2022_

### New or changed functionality

| Functional area | Description                                              |
| --------------- | -------------------------------------------------------- |
| General         | Added support for AI Receipt Scanner in the Expense App. |

## Expense App 3.20

_Released: September 28, 2022_

### New or changed functionality

| Functional area | Description                                                                                                     |
| --------------- | --------------------------------------------------------------------------------------------------------------- |
| General         | Images saved to Saved Images are now synchronized automatically between the Expense App and the Expense Portal. |

### Bug fixes

| Functional area | Description                       |
| --------------- | --------------------------------- |
| General         | Minor bug fixes and improvements. |

## Expense App 3.19, hotfix 3

_Released: September 1, 2022_

### Bug fixes

| Functional area | Description                                                                                                             |
| --------------- | ----------------------------------------------------------------------------------------------------------------------- |
| General         | Fixed a bug where it was not possible to add an image from Saved Images to an expense when expense report is mandatory. |

## Expense App 3.19, hotfix 2

_Released: August 23, 2022_

### Bug fixes

| Functional area | Description                                                                              |
| --------------- | ---------------------------------------------------------------------------------------- |
| General         | Fixed an issue that caused the app to crash in certain scenarios when saving an expense. |

## Expense App 3.19, hotfix 1

_Released: August 18, 2022_

### Bug fixes

| Functional area | Description                                     |
| --------------- | ----------------------------------------------- |
| General         | Fixed Cash/Private action for earlier versions. |

## Expense App 3.19

_Released: August 15, 2022_

### New or changed functionality

| Functional area | Description                                                                                                             |
| --------------- | ----------------------------------------------------------------------------------------------------------------------- |
| General         | We have improved access to Saved Images, now through the Open page.                                                     |
| General         | We have improved access to the camera action on the front page.                                                         |
| General         | It is now also possible to save multiple vehicle registration numbers, and there is an option to set a default vehicle. |

### Bug fixes

| Functional area | Description                                                                               |
| --------------- | ----------------------------------------------------------------------------------------- |
| General         | Changing departure or arrival time no longer clears all detail changes for existing days. |

## Expense App 3.18

_Released: May 10, 2022_

### Bug fixes

| Functional area | Description                                                                                                                                                       |
| --------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | Dialog for transactions when Expense Reports = Mandatory, moved to Saved action, so Expense user is not disturbed with this message every time expense is opened. |

## Expense App 3.17, hotfix 1

_Released: April 26, 2022_

### Bug fixes

| Functional area | Description                                                                                                        |
| --------------- | ------------------------------------------------------------------------------------------------------------------ |
| General         | Fixed a problem where it was not possible to submit a Per Diem when the Per Diem Details destination was assigned. |

## Expense App 3.17

_Released: April 1, 2022_

### Bug fixes

| Functional area | Description                                                                 |
| --------------- | --------------------------------------------------------------------------- |
| General         | Fixed an issue where the Expense attachment image sometimes got very fuzzy. |

## Expense App 3.16.1

_Released: February 24, 2022_

### Bug fixes

| Functional area | Description                                                                                                             |
| --------------- | ----------------------------------------------------------------------------------------------------------------------- |
| General         | Fixed an issue where the app sometimes crashed when a field lookup page with more than 20,000 lookup values was opened. |

## Expense App 3.16

_Released: February 5, 2022_

### New or changed functionality

| Functional area | Description                                                                                                   |
| --------------- | ------------------------------------------------------------------------------------------------------------- |
| General         | Payment type, which expands payment options. (Expense Management 2022 R1 required.)                           |
| General         | The term ”Settlement” has been changed to “Report”. This only applies to the English localization of the app. |
| General         | New icons throughout the Expense App.                                                                         |
| General         | Support for custom icons for Expense Type and Payment Type (Expense Management 2022 R1 required).             |

### Bug fixes

| Functional area | Description                                                                |
| --------------- | -------------------------------------------------------------------------- |
| General         | Block expense user from submitting mileage with ZERO distance.             |
| General         | Status is now shown with corresponding color in open documents in History. |

## Expense App 3.15

_Released: November 25, 2021_

### New or changed functionality

| Functional area | Description                                                                                                                                                           |
| --------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | Template improvements - It's now possible to create new templates from a blank document.                                                                              |
| General         | If a Mileage description exists, this is now shown for each Mileage in list view instead of To address. If description does not exist, the To address is still shown. |
| General         | Added description to 3D touch Image action for supported phones with haptic and 3D touch.                                                                             |
| General         | If list view is empty, the user is now guided with text.                                                                                                              |
| General         | If user is removed from Company, or Company is deleted, user will get the option to choose another Company if any is available.                                       |

### Bug fixes

| Functional area | Description                                                                                                                                                                              |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | Mileage decimal separator was wrong if user for example had language= Danish and Region=Mauritius on their iPhone.                                                                       |
| General         | Documents in a Settlement with Completed status cannot be opened.                                                                                                                        |
| General         | In rare cases the user was logged out of the Expense App.                                                                                                                                |
| General         | Field Values selected on a settlement are now added to documents when documents are added to a settlement and has the same fields on both the settlement and the document, i.e. Expense. |
| General         | Company dropdown action now only shown if user is active in more than 1 company.                                                                                                         |

## Expense App 3.14

_Released: October 1, 2021_

### New or changed functionality

| Functional area | Description                                                                                                        |
| --------------- | ------------------------------------------------------------------------------------------------------------------ |
| General         | Respect new company setting for default values for Per Diem Details.                                               |
| General         | Simplify UI when only 1 action on start page. This is for customers only using Expenses or only using Settlements. |

### Bug fixes

| Functional area | Description                                                                                      |
| --------------- | ------------------------------------------------------------------------------------------------ |
| General         | Show error when creating Per diem destination outside of Per Diem Departure and Return datetime. |

## Expense App 3.13

_Released: September 7, 2021_

### Bug fixes

| Functional area | Description                                                                                                                                                                                                                                                                                                                                                   |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | <p>If Expenses have been created as reminders from BC, show the Expenses in Open, which have not been attached to a Settlement.<br>Attaching PDF or other files with Sharing on the Mobile device, will also be a way the user can create Expenses, but apart from this it should not be possible for the Expense User to create out side the Settlement.</p> |

## Expense App 3.12

_Released: August 30, 2021_

### New or changed functionality

| Functional area | Description                                                                                              |
| --------------- | -------------------------------------------------------------------------------------------------------- |
| General         | Support for settlement pre-approval (Expense Management 2021 R2 required).                               |
| General         | Support for per diem destinations (Expense Management 2021 R2 required).                                 |
| General         | Message is now shown to Expense user when submitting a per diem with no details.                         |
| General         | Message is now shown to Expense user if submitting a per diem identical to a per diem already submitted. |

### Bug fixes

| Functional area | Description                                                                                                                                 |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | New Zealand date format updated to DMY from MDY.                                                                                            |
| General         | Date format corrected for US English on Android devices.                                                                                    |
| General         | Default is now false for details in the Multiple Days action in Per Diem.                                                                   |
| General         | Actions did not work on Settlement page if Plus action was selected and Cancel selected right after, adding no documents to the settlement. |

## Expense App 3.11

_Released: May 20, 2021_

### New or changed functionality

| Functional area | Description                                                                                                                  |
| --------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| General         | On iPhone it is now possible to drag and drop a document to a settlement in the Open list view.                              |
| General         | Notifications are now sent to the user’s phone when there are changes, relevant for the user, in Microsoft Business Central. |

### Bug fixes

| Functional area | Description                                                                                                                                                                                      |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| General         | Having many documents in History list could resolve in Expense App crashing. We have introduced paging, so documents not visible to the user are not loaded until the user scroll down the list. |
| General         | Attachment of PDF files was broken in latest update on Android.                                                                                                                                  |
| General         | Manual contacts added by user was not removed when user had deleted these.                                                                                                                       |
| General         | Search box was misaligned in latest Expense App update.                                                                                                                                          |
| General         | Status color removed from documents in Settlement. Status colors are still shown for the Settlement.                                                                                             |

## Expense App 3.10

_Released: March 17, 2021_

### New or changed functionality

| Functional area | Description                                                                                                                          |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| General         | Message displayed to user if Expense is above amount allowed limit in Busines Central (Require Expense Management 7.0 or later)      |
| General         | Adding support for Recommend, Optional and Mandatory attachments (Require Expense Management 7.0 or later)                           |
| General         | Adding support for 60 days mileage rule used in Denmark (Require Expense Management 7.0 or later)                                    |
| General         | Adding support for deducting mileage distance from home to office i.e. used in New Zeeland (Require Expense Management 7.0 or later) |
| General         | Now possible to sign in with Microsoft 365                                                                                           |

### Bug fixes

| Functional area | Description                                                                                                                 |
| --------------- | --------------------------------------------------------------------------------------------------------------------------- |
| General         | Two synchronize status indicators are shown when user synchronize from settings page                                        |
| General         | Expense Amount is not always updated correctly in History view.                                                             |
| General         | Template action is read only in History documents, so not easy to create new template based on a completed expense document |
| General         | In Mileage the swipe action is stuck if user hits cancel                                                                    |

## Expense App 3.09

_Released: February 18, 2021_

\


| Functional area | Description                                                                                                                                                                                                         |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| General         | Delegations - Feature support for Expense Management 7.00 with the secretary function, allowing one user to have responsibility for another users expenses, mileage etc                                             |
| General         | Field Dependencies - Feature support for Expense Management 7.00 where we introduced Field dependencies. meaning we allow fields to change behavior based on value choosen in another field                         |
| General         | Attachment expectations - Feature support for Expense Management 7.00 where you can choose when an attachment is required                                                                                           |
| General         | Disable possibility to create new document types (Expense, mileage Settlement or per-diem) but allow edit of existing documents of the type, if the document type is disabled in Expense Management Setup in BC/NAV |
| General         | Settlements Required - Feature support for Expense Management 7.00 where you can make settlements mandatory, meaning the user can only press send on settlements, not other document types.                         |
