---
title: Using dimensions in fixed assets in Continia Finance
description: Learn how to use dimensions for tracking fixed assets. 
date: 07-10-2024
id: CF-125
lang: en
---

# Using Dimensions in Fixed Assets

Fixed asset templates make it easier to add assets to Microsoft Dynamics 365 Business Central by providing predefined templates. This allows you to efficiently register fixed assets such as office furniture, vehicles, and machinery. By using these templates, you can standardize the registration process and ensure that assets are categorized and posted correctly. For more information, see [Using Fixed Asset Templates](@CF-86).

Fixed asset templates also support the use of dimensions, which provide further categorization and tracking of assets. In Business Central, dimensions enable detailed analysis by allowing you to track transactions (like sales orders) and categories (like department or location). For more information, see [Work with dimensions](https://learn.microsoft.com/en-us/dynamics365/business-central/finance-dimensions) (Microsoft article).

With Continia Finance, setting dimensions on fixed asset templates helps you categorize the acquisition and deprecation of assets for reporting and analysis. For example, to ensure that all purchased chairs are attributed to the Marketing department, you can assign the appropriate dimension to the fixed asset template. 

Additionally, if you use Continia Finance in association with Continia Document Capture, the system supports dimension-based document approval – where documents can be routed for approval based on dimension codes. This ensures that fixed assets are accurately tracked within the correct context, such as department or project budgets.

To configure dimensions on a fixed asset template:

1. Choose the {{search}} icon, enter **Fixed Asset Templates** and select the related link.

2. Select the desired fixed asset template. For example, FURNITURE.

3. In the action bar, select **Dimensions**.

4. On the **Dimensions** page, configure the following fields:

   - **Dimension Code** - specifies the default dimension for the asset, such as **Department**. To associate your purchased chairs with a specific department, for example, select **Department** as the dimension code.
     
   - **Dimension Value Code** - specifies the value of the selected dimension. This is useful if you frequently assign assets to specific entities. For example, if Marketing is the most common department receiving chairs, set **MKT** as the dimension value code.
     
   - **Dimension Value Name** - the name associated with the dimension value code. For example, the value code **MKT** might have the name **Marketing**, helping users identify which department it refers to.
   - **Value Posting** - specifies how the default dimensions and their values must be applied during system postings. You can set rules to enforce how the dimensions should be used.  The options are: 
      * **Code Mandatory** - requires a dimension for the account, but allows any dimension value code.
      * **No Code** - prevents the use of a particular dimension with the account.
      * **Same Code** - restricts the account to a single dimension value code. If the correct code isn't selected when posting, an error occurs.
   - **Allowed Values** - defines the permissible dimension values for the selected account. You can set up rules to control which dimension values can be used, and specify posting requirements through the **Dimension Value Posting** field. Click the three dots to change the settings. On the **Allowed Dimension Values** page, you can now specify whether dimension values can be used for an account by selecting **Set Allowed** or **Set Disallowed**. For example, if only the Marketing and Sales departments are allowed to use certain office assets, you can restrict postings to only these departments by setting their dimension values.

