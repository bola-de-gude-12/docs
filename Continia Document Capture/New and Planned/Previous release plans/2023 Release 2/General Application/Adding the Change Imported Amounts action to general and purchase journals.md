---
title: Adding the Change Imported Amounts Action to General and Purchase Journals
date: 26-11-2024
description:
id: DC-254
lang: en
---

# Adding the Change Imported Amounts Action to General and Purchase Journals

| Feature | Public preview | General availability online | 
| --- | :-: | :-: |
| Adding the **Change Imported Amounts** action to general and purchase journals | - | {{checkmark}} Oct 2023 |

## Business value

With the addition of the **Change Imported Amounts** action to general journals and purchase journals, users in your organization will now be able to change the imported amount of any purchase document that has been registered as one or more lines in a journal. This will help reduce errors and improve the accuracy of your accounting and financial reports.

## Feature details

The Continia Document Capture feature **Change Imported Amounts** will be added to the following two pages in Microsoft Dynamics 365 Business Central:

* **General Journals**
* **Purchase Journals**

The feature already exists for purchase documents but will now be expanded to include the above pages as well. In all other respects, the functionality is exactly the same though.

When a vendor sends you a purchase document such as an invoice, Document Capture automatically registers the total amount of this invoice and copies it to the corresponding purchase invoice that's created in Business Central. The original invoice total – known as the imported amount – is used to verify that the sum of all lines matches the amount of the imported document, but this amount can be changed by certain users if necessary. This functionality will now work for general journals and purchase journals as well, meaning that users will be able to change the imported amounts of [purchase documents that have been registered as journal lines](@DC-67#registering-documents-as-general-journal-lines) once the lines have been created in a journal upon document registration.

For more information, see [Customization of imported amounts](@DC-139#customization-of-imported-amounts).

> [!NOTE]
> The feature will be available for Business Central 2022 release wave 2 (BC v21) or later.
