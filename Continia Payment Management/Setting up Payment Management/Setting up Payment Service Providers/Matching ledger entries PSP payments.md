---
title: Matching ledger entries with PSP payments
date: 23-05-2023
description: Describes how to match customer ledger entries with PSP imported payment lines.
id: PM-339
lang: en
---

# Matching ledger entries with PSP payments

> [!IMPORTANT]
>
> Available for version 6.2.0.0 or higher.

To enable the matching of ledger entries with payment lines imported from a PSP, it is essential to configure specific settings for the External Payment Reference field in the Payment Management setup. This field is included in sales documents and customer ledger entries, allowing it to be matched with the corresponding reference field specified in the imported file. Successful reconciliation takes place when these two fields have identical values. By accurately specifying the relevant fields or columns for each PSP, we ensure precise reconciliation based on the payment references provided within the file.

> [!IMPORTANT]
>
> Only users with the CPM365 ADMIN, SUPER, or CPM PSP IMPORT permission set can create PSP agreements and import PSP files.

To apply External Payment Reference field settings to prepare to add a PSP agreement:

1. Use the ![Search for a page or report](/images/search_small.png) icon, search for **Payment Management Setup** and select the related link.

2. Navigate to the FastTab **Payment Receipt Import**, and enter information for the following fields:

   * **Update External Payment Reference** - select the field to use on sales documents as the reference number. You can choose from the following options: **Using Custom Field**, **Using Your Reference**, **Using External Document No.** 
   * **Custom External Payment Reference Field Name** - Select the appropriate field from the Sales Header table if you selected Using Custom Field in the Update External Payment Reference field.

   Payment Management now prompts you to update External Payment Reference in not posted sales documents and open the customer ledger entries. 

If the standard payment reference field in the file is not suitable for reconciliation and a custom field is needed, you can refer to the PSP Reconciliation Setup for instructions on how to configure it. This setup enables you to customize the reconciliation process according to your needs.

1. Go to the PSP Agreement you want to set up the reconciliation for.

2. On the action menu, select **Related** > **PSP Reconciliation Setup**.

3. In the **PSP Reconciliation** window, you can now use the following settings:

   * **Extended Search** – enhances the search functionality by introducing additional criteria for matching ledger entries. Specifically, when enabled, the search will only come back with results if both the external payment reference and the posting date, along with the amount, are identical or fall within a predefined tolerance range.

   * **Posting Date Tolerance** – specify a tolerance for the number of days that posting days can deviate when using Extended Search.

   * **Payment Reference Position** – this setting determines which field is used as the payment reference value. The default values are pre-filled and explained for each PSP. However, you can choose a custom field position in the file if necessary. Please note that the field position is represented by an integer value starting from 0. For example, in Excel, column A would be 0, column B would be 1, and so on.

   * **Date Format** – this setting is utilized during file import to ensure the correct formatting of the posting date. While default values are provided, it is important to adjust the date settings to match the local or date settings of the downloaded file if they differ.  

     > [!NOTE]
     >
     > The date format is based on the [.NET DateTime format](https://learn.microsoft.com/en-us/dotnet/standard/base-types/custom-date-and-time-format-strings).

## Related information

[Importing PSP payments](@PM-299)

[Payment Service Providers](@PM-300)



