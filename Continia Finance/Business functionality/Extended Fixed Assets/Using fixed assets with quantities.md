---
title: Using fixed assets with quantities in Continia Finance
date: 08-10-2024
description: How to use fixed assets with quantities in Continia Finance.
id: CF-43
lang: en
---

# Using Fixed Assets with Quantities

This article describes the use of quantities in fixed assets (FAs), which simplifies the creation and management of multiple fixed assets of the same type.

## Creating a fixed asset with a quantity

### Creating a fixed asset with a quantity from scratch
To create a fixed asset with a quantity from scratch:

1. Choose the {{search}} icon, enter **Fixed Assets**, and then choose the related link.

2. On the **Fixed Assets** page, select **+ New**.

3. On the **Fixed Asset Card**, under the **General** FastTab, enter a **No.**, **Description**, and **FA Subclass Code**.

4. On the **Depreciation Book** FastTab, populate the **Depreciation Starting Date** and **No. of Depreciation Years** fields. Note that the value of the **Depreciation Ending Date** field is calculated automatically.

5. On the **Continia Finance** FastTab, enable the **Maintain quantity** setting.

Your fixed asset is now ready to be acquired.

### Creating a fixed asset with a quantity from a template
Before you can create a fixed asset with a quantity from a template, you need to [create a fixed asset template](@CF-86).

To create a fixed asset with a quantity from a template:

1. Choose the {{search}} icon, enter **Fixed Assets**, and then choose the related link.

2. Select **Continia Finance** > **Create FA from Template**.

3. On the **Create FA from Template** page, select a value for **Fixed Asset Template Code**.

   >[!NOTE]
   >This value must have a checkmark under the **Maintain quantity** column. Otherwise, you need to open the related fixed asset template and enable the **Maintain quantity** setting.

4. Populate the other fields according to your needs, such as **Serial No. / Dimensions**.

5. When you're done configuring, select **Create Fixed Asset**.

6. On the **Fixed Assets** page, select your new fixed asset.

7. Check the fields that contain values and, if needed, populate other necessary fields.

Your fixed asset is now ready to be acquired.

## Using a fixed asset with a quantity
You can use fixed assets with a quantity when creating purchase invoices or [partially disposing of assets](@CF-08), for example. This article covers the former.

### Using a fixed asset with a quantity in purchase invoices
To use a fixed asset with a quantity in a purchase invoice:

1. Choose the {{search}} icon, enter **Purchase Invoices**, and then choose the related link.
2. On the **Purchase Invoices** page, select **+ New**.
3. On the **Purchase Invoice** page, under the **General** FastTab, enter a **No.** or **Vendor Name**.
4. Under the **Lines** section, select **Fixed Asset** under **Type**.

   >[!TIP]
   >It's also possible to create a fixed asset from a template directly from a purchase invoice. After selecting **Fixed Asset** under **Type**, select **Fixed Assets** > **Create FA from Template** and follow the steps described in [Creating a fixed asset with a quantity from a template](#creating-a-fixed-asset-with-a-quantity-from-a-template).

5. Select a value under **No.**, and populate the **Quantity** and **Direct Unit Cost Excl. VAT** fields.

Your fixed asset is now ready to be posted.

## See also
[Using Fixed Assets Templates](@CF-86)  
[Applying Partial Disposal of Assets](@CF-08)