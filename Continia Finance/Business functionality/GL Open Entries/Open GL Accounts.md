---
title: Open G/L accounts in Continia Finance
date: 13-03-2023
description: Learn how to open and apply open entries in the G/L Open Entries. module.
id: CF-83
lang: en
---

# Handling G/L Open Entries

The G/L Open Entries module helps you create and manage open entries for your G/L accounts. This is similar to how you handle such entries for your customers and vendors. This feature makes it easier to keep track of payments that are in progress, such as money transfers, transit entries, or social insurance.

## To handle G/L open entries

To handle G/L open entries:

1. On the Continia Finance menu, select **Open G/L Accounts**.

2. The page that now opens presents two distinct sections: the top lists accounts with the G/L Open Entries feature activated, while the lower section contains the corresponding G/L account entries.
   
   > [!TIP]
   >
   > To activate this feature, navigate to the Continia Finance menu and select **G/L Accounts**. Then, select an account to edit. Scroll down to the Continia Finance FastTab and toggle on the **Build Open Entries** option.
   
   On the action bar, select **Edit List**, to open the page in an editable mode. On this page, you can now directly set applications for individual entries. Select **Manage** > **Set Applies-to ID**. 
   
4. Select **Manage** > **Post Application**. Alternatively, select **Apply Partial Payment**. 
   
   You can enter the application balance into the **Amount to Apply** field of the current entry and post the application. If the current entry doesn’t have an Applies-to ID, it will be set automatically.

## To handle open G/L entries from interim postings

With Continia Finance you can also handle open G/L entries that result from interim postings. This feature allows you to determine whether value entries originating from receipt or shipment postings are recorded in the general ledger. Expected costs, such as estimates of purchased item costs recorded before receiving the invoice, are managed through this process.

To use this functionality, you must set up interim accounts in the general ledger for relevant posting groups. 

> [!NOTE]
>
> It's important to note that expected costs are only applicable to item transactions, not immaterial transaction types like capacity and item charges. 

To activate expected costs postings:

1. Use the {{search}} icon, enter **Inventory Setup**, and select the related link. 
2. Activate the **Expected Cost Posting to G/L** field to apply interim postings automatically to corresponding interim accounts employing G/L open entries. 
3. Access this functionality through the G/L Acc Application menu item. A request page enables you to filter and specify the posting date for automatic application, as well as select specific cases or customer fields for analysis.

## To print or export open G/L entries

For printing or exporting open G/L Entries:

1. Navigate to **G/L Open Entries** > **G/L Account** > **Open Entries** from the main menu.
2. Use the **Options** tab to export report contents to Excel and choose between Posting Date or Document Date display.
3. Specify G/L accounts and apply date filters under the G/L Account tab. The report reflects entries due as of the specified date. Optionally, select G/L entries to include, preview the report, and export it as needed.

