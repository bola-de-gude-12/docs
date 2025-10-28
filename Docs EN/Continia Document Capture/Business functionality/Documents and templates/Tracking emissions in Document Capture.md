---
title: Tracking emissions in Document Capture
date: 31-08-2025
description: How to track GHG emissions in Document Capture.
id: DC-232
lang: en
---

# Tracking emissions in Document Capture with Business Central Sustainability
This article describes the integration between Continia Document Capture and Business Central Sustainability, which allows you to track your company's greenhouse gas (GHG) emissions within Microsoft Dynamics 365 Business Central.

Emission-related data captured in Document Capture can be transferred into purchase invoice lines when the document is registered, resulting in sustainability reports in Business Central Sustainability when posted.

>[!NOTE]
>The **Use Emissions in Purchase Invoices** setting must be enabled on the **Sustainability Setup** page for the system to transfer the **Sustainability Account No.**, **Emission CO2**, **Emission CH4**, and **Emissions N2O** data from the document journal to the purchase lines.

## Business Central Sustainability template fields
The following header and line fields are made available across all master templates in the purchase category in Document Capture:

* **Sustainability Account No.** - a unique identifier within the Chart of Sustainability Accounts (CoSA), used for tracking and categorizing emissions data and more. Each account is configured with an Account Category (which defines the calculation foundation) and an Account Subcategory (which defines the Emission Factor). For more information, see [Chart of sustainability accounts and ledger](https://learn.microsoft.com/en-us/dynamics365/business-central/finance-sustainability-accounts-ledger) (Microsoft article). 
* **Fuel/Electricity*** - the quantity of fuel or energy used (e.g.: liters of gasoline, kWh, etc.).
* **Distance*** - the distance traveled or shipped (e.g.: vehicle mileage, freight kilometers, etc.).
* **Custom Amount*** - a user-defined measure (e.g.: cost, tons of waste, hotel nights, etc.).
* **Installation Multiplier*** - a factor applied for fugitive emissions (e.g.: leaks, assembly losses, etc.).
* **Time Factor*** - a duration component (e.g.: hours, days, years, etc.), used with the **Installation Multiplier** and **Custom Amount**.
* **Emission CO2** - the amount of carbon dioxide emitted.
* **Emission CH4** - the amount of methane emitted.
* **Emission N2O** - the amount of nitrous oxide emitted.

>[!NOTE]
>Water-, Waste-, and Energy-related fields haven't been integrated into Document Capture yet.

The fields marked with an asterisk above are used for collecting the required activity data. When multiplied by the emission factor value, this activity data results in total emissions (i.e.: CO2, CH4, and N2O emissions). This activity data is only kept temporarily to calculate the total emissions to be transferred to the purchase invoice line and it's not stored in any entry.

If a document provides the total emissions, you can use this data to fill out the relevant emission fields instead.

The field to be filled out with activity data is determined by the information collected in the Sustainability Account Category. A message under the **Comments** section provides you with this information, without preventing the posting of the document if any information is missing.

>[!NOTE]
>It's your responsibility to ensure the activity data entered in the Business Central Sustainability fields matches the unit of measure required to perform the calculations with the emission factor, as specified in the related Sustainability Account Subcategory.

When you register the document, the fields **Sustainability Account No.**, **Emission CO2**, **Emission CH4**, and **Emission N2O** are transferred to the purchase invoice lines. Then, they follow the standard sustainability posting process – as established by Business Central Sustainability, such as the creation of sustainability ledger entries.

You can configure a default Sustainability Account No. in the related field of a G/L account card. This prior enabling the functionality in the Sustainability Setup page.

### To configure Business Central Sustainability fields in a template

Before you can configure Business Central Sustainability fields in a template, you need to add these fields to a template:

1. Search ({{search}}) for and select **Document Categories**.
2. Click the **PURCHASE** code to open the document journal.
3. In the document list, select the document whose template you want to add the Business Central Sustainability fields to.
4. On the action bar, click **Template** > **Add Template Fields**.
5. Select the field(s) you want to add to the template, then click **OK**.

You can then either manually populate these fields with the corresponding values or capture the required information from the document itself.

### To configure Business Central Sustainability fields in a G/L account

To configure Business Central Sustainability fields in a G/L account:

1. Search ({{search}}) for and select **Sustainability Setup**.
2. On the **Procurement** FastTab, enable the **G/L Account Emissions** setting.
3. Search ({{search}}) for and select **Chart of Accounts**.
4. Select the account you want to configure.
5. On the **Sustainability** FastTab, assign a value to the **Sustainability Account No.** fields. For example, 12110.
6. The **Emission Type**, **Emission Code**, **Emission Unit Type**, and **Emission Unit Code** fields are populated automatically.

[When the Business Central Sustainability fields are added to a template](#to-configure-Business-Central-sustainability-fields-in-a-template), the value of the **Sustainability Account No.** field is automatically populated – based on the preconfigured G/L account when you select the **Type** and **No.** in the document header. *The same can be accomplished by entering a G/L account in **Accounts for Amounts**, though currently this approach requires that you select **Home** > **Recognize Fields** after entering the values.*

*When using line recognition, configure **Translation to Type** and **Translation to No.** to apply the default values from G/L accounts or items to the related template line fields. Alternatively, enter the required values directly in the template line fields.*

### To configure Business Central Sustainability fields on an item card
To configure Business Central Sustainability fields on an item card:

1. Search ({{search}}) for and select **Sustainability Setup**.
2. On the **Procurement** FastTab, enable the **Item Emissions** setting.
3. Search ({{search}}) for and select **Items**.
4. Select the number of the item you want to configure. For example, 1920-S.
5. On the **Environmental Accounting** FastTab, assign values to the **Environmental Account Type** and **Environmental Account No.** fields. For example, Goods and Services and 10003.
6. In this case, only the **Emission Unit Type** and **Emission Unit Code** fields are populated automatically. You can then enter a value for the **Emission Quantity**, if it's always the same. Otherwise, add the corresponding values to each document.

[When the Business Central Sustainability fields are added to a template](#to-configure-Business-Central-sustainability-fields-in-a-template), the value of the **Sustainability Account No.** field is automatically populated – based on the preconfigured G/L account when you select the **Type** and **No.** in the document header. *The same can be accomplished by entering a G/L account in **Accounts for Amounts**, though currently this approach requires that you select **Home** > **Recognize Fields** after entering the values.*

*When using line recognition, configure **Translation to Type** and **Translation to No.** to apply the default values from G/L accounts or items to the related template line fields. Alternatively, enter the required values directly in the template line fields.*