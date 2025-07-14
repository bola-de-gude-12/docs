---
title: Extended total balance report in Continia Finance
date: 09-10-2024
description: An overview of the functionality within the Extended Total Balance reports.
id: CF-123
lang: en
---

# Extended Total Balance

This article describes the **Extended Total Balance** report in Continia Finance, which enhances the standard **Trial Balance** functionality in Microsoft Dynamics 365 Business Central.

You can access the **Extended Total Balance** report from a G/L account, a customer, or a vendor. To access this report from a G/L account, for example:

1. Choose the {{search}} icon, enter **Chart of Accounts**, and then choose the related link.
2. Select a G/L account in the list and then select **Continia Finance** > **Ext. G/L Total Balance**.

By default, extended total balance reports also include the starting balance of an account, customer, or vendor – as well as a comparison between the selected period and the year as a whole. Therefore, these reports combine the functionality of the **Trial Balance** and **Trial Balance by Period** reports.

## Additional functionality

### G/L accounts, customers, and vendors

The following functionality is available on the G/L account, customer, and vendor levels:

* Only Print Accounts With - Only accounts whose balance matches the selected criterion are printed. Although the same result can be achieved with a filter in the standard **Trial Balance** report, it's not as straightforward.
  
* Create Excel File - Specifies if the report's content should be transferred to Excel. The exported content is formatted correctly, therefore it's ready to be used.

### G/L accounts and customers

The following functionality is available on the G/L account and customer levels:

* Show Company - Specifies whether the name or the display name of the company should be used.

### Customers and vendors

The following functionality is only available on the customer and vendor levels:

* Adjust Exch. Rate Differences - Specifies whether exchange rate differences should be included in the report. If you select this checkbox, all debit and credit amounts are corrected by the realized profit and loss due to the exchange rate differences.
   >[!WARNING]
   >If you don't select this checkbox, none of the exchange rate differences of realized profit and loss are considered. This could lead to problems with reconciling with the corresponding receivables accounts.