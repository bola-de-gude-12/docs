---
title: Tracking emissions in Document Capture
date: 28-03-2025
description: How to track GHG emissions in Document Capture.
id: DC-232
lang: en
---

# Tracking emissions in Document Capture with Continia Sustainability
This article describes the integration between Continia Document Capture and Continia Sustainability, which allows you to track your company's greenhouse gas (GHG) emissions within Microsoft Dynamics 365 Business Central.

Emission-related data captured in Document Capture can be imported into your environmental journals in Continia Sustainability, where you can also verify the source document of a specific data point. For more information on environmental journals, see [Working with environmental journals](@CS-34).

## Continia Sustainability template fields
When Continia Sustainability is activated in an environment where Document Capture is already active (or vice versa), the following header and line fields are made available across all master templates in the purchase category:

* **Environmental Account Type** - key business areas and associated activities. For example, Facility.

   >[!NOTE]
   >If the **Environmental Account Type** field in a G/L account or item has a value other than blank, the following fields are validated. If a value in any of those fields needs attention, a configurable comment is displayed under the **Comments** section in the document journal and on the document card.

* **Environmental Account No.** - the number of the environmental account related to the type of emission activity. For example, 10110 (Electricity).
* **Emission Type** - common sources of emissions related to a company’s activities. For example, Electricity or Fuels.
* **Emission Code** - the code assigned to the related type of emission. For example, EL-UK for Electricity type.
* **Emission Unit Type** - the measurement unit associated with the type of emission. For example, Energy or Distance.
* **Emission Unit Code** - the code assigned to the measurement unit associated with the type of emission. For example, KWH (kilowatt-hour) or KCAL (kilocalorie).
* **Emission Quantity** - the actual quantity related to the emission. For example, 100 (miles, or MI), 25 (kilowatt-hour, or KWH), etc.
* **Total Emission Quantity** - the result of the value in the **Emission Quantity** field(s) multiplied by the quantity of the related item. For example, if you purchased 20 copy paper packs, the total emission quantity is 20 multiplied by the emission quantity assigned to the item, such as its weight.
  
   >[!NOTE]
   >If you've already added environmental data to an item, including a weight or other metric, make sure to leave the **Total Emission Quantity** field empty when populating the Continia Sustainability fields on the line level.

You can configure these fields in a G/L account, on an item card, or directly in a template. All three methods are covered in this article.

>[!NOTE]
>No matter which approach you choose to configure the Continia Sustainability fields, make sure to either enter or capture a value for the **Emission Quantity** field. Only then can the emission be calculated with the corresponding [emission factor](@CS-22).

### To configure Continia Sustainability fields in a template

Before you can configure Continia Sustainability fields in a template, you need to add these fields to a template:

1. Search ({{search}}) for and select **Document Categories**.
2. Select the **PURCHASE** code to open the document journal.
3. In the document list, select the document whose template you want to add the Continia Sustainability fields to.
4. On the action bar, click **Template** > **Add Template Fields**.
5. Select the field(s) you want to add to the template, then select **OK**.

You can then either manually populate these fields with the corresponding values, or capture the required information from the document itself.

### To configure Continia Sustainability fields in a G/L account

To configure Continia Sustainability fields in a G/L account:

1. Choose the {{search}} icon, enter **Chart of Accounts**, and then choose the related link.
2. Select the account you want to configure.
3. On the **Environmental Accounting** FastTab, assign values to the **Environmental Account Type** and **Environmental Account No.** fields. For example, Facility and 10110.
4. The **Emission Type**, **Emission Code**, **Emission Unit Type**, and **Emission Unit Code** fields are populated automatically.

[Once the Continia Sustainability fields are added to a template](#to-configure-continia-sustainability-fields-in-a-template), their values are automatically populated based on the preconfigured G/L account when you select the **Type** and **No.** in the document header. The same can be accomplished by entering a G/L account in **Accounts for Amounts**, though currently this approach requires that you select **Home** > **Recognize Fields** after entering the values.

When using line recognition, configure **Translation to Type** and **Translation to No.** to apply the default values from G/L accounts or items to the related template line fields. Alternatively, enter the required values directly in the template line fields.

### To configure Continia Sustainability fields on an item card
To configure Continia Sustainability fields on an item card:

1. Choose the {{search}} icon, enter **Items**, and then choose the related link.
2. Select the number of the item you want to configure. For example, 1920-S.
3. On the **Environmental Accounting** FastTab, assign values to the **Environmental Account Type** and **Environmental Account No.** fields. For example, Goods and Services and 10003.
4. In this case, only the **Emission Unit Type** and **Emission Unit Code** fields are populated automatically. You can then enter a value for the **Emission Quantity**, if it's always the same. Otherwise, add the corresponding values to each document.

[Once the Continia Sustainability fields are added to a template](#to-configure-continia-sustainability-fields-in-a-template), their values are automatically populated based on the preconfigured item card when you select the **Type** and **No.** in the document header. The same can be accomplished by entering an item in **Accounts for Amounts**, though currently this approach requires that you select **Home** > **Recognize Fields** after entering the values.

>[!NOTE]
>At present, Continia Sustainability fields are in some cases not automatically populated on the line level due to a bug. Therefore, you need to re-enter the value under **No.** or **Translate to No.** in the document journal or on the document card before the Continia Sustainability fields are populated.

When using line recognition, configure **Translation to Type** and **Translation to No.** to apply the default values from G/L accounts or items to the related template line fields. Alternatively, enter the required values directly in the template line fields.

## To import emission-related data into Continia Sustainability
When you post documents with data related to emissions, this data becomes available to Continia Sustainability. For more information, see [Importing emission-related lines from document lines](@CS-53).

## Related information
[Creating an emission factor set](@CS-74)  
[The basic concepts in Continia Sustainability](@CS-58)  
[Continia Sustainability and Document Capture](@CS-78)  
[The Assisted Setup Guide for Continia Sustainability](@CS-80)  
[Adding a predefined emission factor set managed by Continia](@CS-94)