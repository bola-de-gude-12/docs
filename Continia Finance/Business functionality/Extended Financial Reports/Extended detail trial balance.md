---
title: Extended detail trial balance report in Continia Finance
date: 09-10-2024
description: An overview of the functionality within the Extended Detail Trial Balance.
id: CF-122
lang: en
---

# Extended Detail Trial Balance

This article describes the **Extended Detail Trial Balance** report in Continia Finance, which enhances the standard **Detail Trial Balance** functionality in Microsoft Dynamics 365 Business Central.

You can access the **Extended Detail Trial Balance** report from a G/L account, a customer, or a vendor. To access this report from a G/L account, for example:

1. Choose the {{search}} icon, enter **Chart of Accounts**, and then choose the related link.
2. Select a G/L account in the list and then select **Continia Finance** > **Ext. Detail Trial Balance**.

## Additional functionality

### G/L accounts, customers, and vendors

The following functionality is available on the G/L account, customer, and vendor levels:

* Show Company - specifies if the name or the display name of the company should be used.
* Incl. Comments - specifies if any existing entry comments should be printed below the respective entry.
* Output in Excel - specifies if the report's content should be transferred to Excel. The exported content is formatted correctly, therefore it's ready to be used.
* Output in Excel with all Dimensions - specifies if all shortcut dimensions of the selected entries should be transferred to Excel. The exported content is formatted correctly, therefore it's ready to be used.

### Customers and vendors

The following functionality is only available on the customer and vendor levels:

* Column Description - specifies whether to print the posting description or balance account information in the **Description** column.
* Show Application - if enabled, the associated application appears in the report below the entry.
* Consider Date Filter in Application - if the **Show Application** setting is enabled, you can enable this setting to apply a date filter to the application entries.