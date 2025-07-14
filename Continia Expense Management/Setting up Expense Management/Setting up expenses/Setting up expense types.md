---
title: Setting up Expense Types
date: 02-06-2025
description: Learn how to set up an expense type.
id: EM-41
lang: en
---
# Setting up expense types

Expense types are codes that allow expense users to categorize their expenses efficiently. For example, users can quickly identify Food, Parking, or Accommodation expenses.

With Expense Management in place, you can customize specific settings for each expense type. For example, specify whether a particular expense type requires an uploaded receipt for validation. Additionally, you can hide certain expense types from specific users, customizing the experience to accommodate individual requirements and personal preferences.

To set up an expense type:

1. Search for {{search}} **Expense Type**.
2. On the action bar, click **New**.
3. Fill in the following fields:
   - **Code** - enter the code associated with the expense type.
   - **Description** - provide a brief explanation of the purpose of the expense type.
   - **Search name** - specify the name to find the expense type easily.
   - **No Refund** - specifies whether the expense is eligible for company reimbursement. The employee will be responsible for charges incurred using the company credit card if not eligible. This setting is also used when the user withdraws cash from an ATM using the company credit card.
   - **Attachment required** - this setting allows you to specify whether uploading an attachment is required for a particular expense type. The options are:
     - _Recommended_ - Select this option to warn the user if they forget to attach a file. It doesn't block the user from sending an expense without an attachment but it does inform them about the missing attachment.
     - _Mandatory_ - Select this option if attaching a file is necessary for an expense. Then the user can't send an expense without providing an attachment, and the bookkeeper can't process such expenses.
     - _Optional_ - Use this option if attachments are not expected for a specific expense type. It's suitable for cases such as credit card fees where a receipt may not be available. The user won't receive any warnings or error messages. However, if they attach a receipt anyway, the system accepts it.
   - **Hide from Expense User** - If selected the expense type will no longer be visible within the Continia Expense Mobile App or the Expense Portal. This can be useful for fee-related expense types for example.
   - **Exclude Transaction** - Select if you want to exclude transactions from being posted immediately upon import. This exclusion uses matching rules, where a specific keyword within the transaction identifies the corresponding expense type. Consequently, Expense Management prevents these transactions from being posted. For more information, see [Handling fees](@EM-163).
   - **Attendees required** - In some companies, you can incur higher expenses when multiple users participate in the same event, provided that the names of the participants are specified. To enforce this requirement, you can configure an expense to include the mandatory field **Attendees Required**. For any changes to take effect, you must [update system dependencies](/continia-expense-management/setting-up-expense-management/setting-up-general-business-functionality/setting-up-field-dependencies#update-system-dependencies).
   - **Image** - Determines the image displayed in the Expense Mobile App and the Expense Portal for the expense type.
   - **No. of Company Policies** - Indicates the number of company policies applicable to this expense type. To learn more about configuring default dimensions and define specific [company policies for expense](@EM-39) and [company policies for mileage expenses.](@EM-40)
   - **Purchase Contract** - Specifies whether a purchase contract is required for the expense type.

## Add a posting setup

You also have to add a posting setup to your expense type.

1. Select an expense type, and then click **Setup** on the action bar.
1. Fill in the following fields:
   * **Employee No.** - This is the employee for which the posting account will be used. If this account is used for multiple employees, leave the value empty.
   * **Employee Group** - This is  the employee group for which the posting account will be used. If there's no requirement for specific groups, you can leave this value empty.
   * **Posting Account Type** - Enter the account type to use when posting. A G/L account is the common option.
   * **Posting Account No.** - Enter a G/L account number (or in rare cases, the Item number) for posting *internally*, not in a payroll system.
   * **Gen. Prod. Posting Group** - Here, you can add a general product posting group to use when posting. This will overwrite the default values from the posting account.
   * **Gen. Bus. Posting Group** - The general business posting group is the group used when posting. This will overwrite the default values from the posting account.
   * **VAT Prod. Posting Group**/**Tax Prod. Posting Group** - Specifies the VAT/tax product posting group to use when posting. This will overwrite the default values from the G/L account.
   * **VAT Bus. Posting Group**/**Tax Bus. Posting Group** - Specifies the VAT/tax business posting group to use when posting. This will overwrite the default values from the G/L account.
1. You can differentiate the posting of your expense type based on expense user, expense user group, or country (for example, if applying a different VAT or sales tax for specific countries). To do this,  [personalize the page](https://docs.microsoft.com/en-us/dynamics365/business-central/ui-personalization-user) by following these steps:
   1. Click **Settings** {{settings}} > **Personalize**.
   1. In the upper-left corner, click **+ Field** to open the **Add Field to Page** pane.
   1. Drag the relevant fields – in this case **Country/Region Code** and **Country/Region Type** – from the pane to the table header.
   1. Click **Done** to close the **Personalizing** banner.

1. The new columns are added to the table. If you want to specify a default VAT or sales tax for all countries, 

   1. Go to **Country/Region Type** for the first line in the table.
   1. Click **All Countries/Regions**. 
   1. Fill in the remaining fields as needed for this line.

1. To specify a VAT or sales tax for a specific country, 

   1. Go to **Country/Region Type** for the second line in the table.
   1. Click **Country**. 
   1. In the **Country/Region Code** column, click the code of the relevant country, then fill in the remaining fields as needed for this line.

   > [!TIP]
   > For example, for **VAT Prod. Posting Group**, select  **NO VAT** if the selected expense type is exempt from VAT for the selected country.
1. Search for {{search}} **Configured Fields**.
1. In the table, go to the **Field Code** column for an empty line, and click **COUNTRY/REGION** for that line.
1. On the action bar, click **Continia Online** > **Force Synchronize with Continia Online**.

In the Expense Mobile App and the Expense Portal, the **Country/Region Code** field will now be visible for expenses, meaning that you can see or specify the country where any given expense was incurred. So if you create an expense with a posting setup that's been customized for a specific country (as described in the guide above) and this country appears in the **Country/Region Code** field, the customized posting setup will automatically be applied, and the expense will be posted accordingly.

> [!IMPORTANT]
> If you customize a posting setup for a specific country, it's important that all other countries have a posting setup too. 

Here is an example of a posting setup:

1. Search for {{search}} **Expense Posting Setup**.
2. Go to **Country/Region Type** for the first line in the table.
3. Click **All Countries/Regions** to set up a default posting setup that applies to all countries. 
4. You can then specify custom posting setups for any countries that deviate from this default by adding additional table lines; Under **Country/Region Type**, click **Country**.
5. Add the relevant country code under **Country/Region Code**.

You can even gather multiple countries with the same posting setup into one group – for example, a group named "Countries abroad" – whose code you specify under **Country/Region Code**. This would save time in your workflow, as you only have to create one additional table line using this method, instead of creating one line per country.
