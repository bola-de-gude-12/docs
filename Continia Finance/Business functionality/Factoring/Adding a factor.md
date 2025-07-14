---
title: Setting up a Factor
date: 08-02-2024
description: Learn how to set up a factor and set data exchange definitions. 
id: CF-214
lang: en
---

# Setting up a Factor

To be able to send factoring proposals to a factor, you must first set up the factor in Business Central. Since the factor acts as a vendor from the company's perspective, factors can be directly linked to a vendor.

## To set up a factor

To set up a factor:

1. Use the {{search}} icon, enter **Factor**, and select the related link.

2. On the **Factor** card, on the action bar, select **New**.

3. Go to the **General** FastTab to enter general information about the factor, such as Vendor No., Name, Address, and so on.

4. Other optional fields on the **General** FastTab are:
   * Due Date Tolerance
   * Limit (LCY) - specify the amount the factor will accept for factoring.
   * Blocked

5. On the **Export** FastTab, you can find settings for exporting files containing the receivables:
   * **Data Exch. Def. Export Proposal Lines** - here you select the Data Exchange Definition used for exporting proposed receivables.

   * **Data Exch. Def. Exported Applied Lines** - here you select the Data Exchange Definition that allows you to export the receivables that have already been balanced up to any given cutoff date.

   * **Data Exch. Def. Export Customer Data** - indicates the Data Exchange Definition that is used to export customer data.

     > [!NOTE]
     >
     > Data exchange definition templates covering the key information from the factoring proposals are provided automatically during the setup. To learn more about data exchange definitions, refer to [Microsoft Learn.](https://learn.microsoft.com/en-us/dynamics365/business-central/across-how-to-set-up-data-exchange-definitions)

6. On the **Import** FastTab, you can define, which data exchange definition will be used to re-import data related to the exported proposals into the system.

## To assign a customer to a factor

After setting up the factor, you can proceed to assign customers whose receivables the factor can contractually acquire from the company. You can assign individual customers or use batch processing by using the available filtering options (no., customer posting group, currency code, etc.).

To assign a customer to a factor:

1. On the **Factor** card, on the action bar, select **Customers**.

2. On the **Factoring Customers** page, select **Add Customers** and use the filters to find the customers whose receivables will be assigned to the factor. 

   Now, you can create and export [factoring proposals](@CF-215). 
