---
title: Setting up Azure Blob Storage for Continia Banking
description: How to set up Azure Blob Storage for Continia Banking.
date: 01-10-2024
id: CB-74
lang: en
---

# Setting up Azure Blob Storage for Continia Banking

For banks using systems outside of Business Central, Continia Banking’s integration with Azure Blob Storage provides a convenient intermediary platform for managing and accessing files across multiple applications. To get started with Azure Blob Storage in Continia Banking, follow these two steps in the specified order.

1. In the [Microsoft Azure portal](https://portal.azure.com/), set up a storage account and container for Banking.
2. In Microsoft Dynamics 365 Business Central, set up Banking for Azure Blob Storage.

Both of these processes are described below.

## To set up a storage account and container

{{include "setting-up-azure-blob-storage" "Continia Banking"}}

## To set up the connection in Continia Banking

To set up the connection to Azure Blob Storage in Continia Banking:

1. Select the ![Search](https://docs.continia.com/images/search_small.png) icon, search for Bank Account Setup, and then select the related link.
2. The wizard now takes you through the steps to set up the connection. On the **Bank Accounts** page, go to the bank for which you want to set up a connection with Azure Blob Storage, and in the **Communication Type** column, select **Storage Account** and then select **Next**. 
3. On the **Choose Storage Account Type** page, select the Storage Account Type. 

   > [!TIP]
   >
   > Currently, Azure Blob Storage is the only available option. However, we are working on adding support for additional providers, such as SharePoint and OneDrive. 
4. If you set up a connection to Azure Blob storage for the first time, you will be prompted to enter your credentials to authenticate with your Azure Blob Storage account. Enter information for the following fields and select **Next**:

   * **Storage Account Name** - enter or copy and paste the Display Name of the Storage Account.
   * **Storage Account Key** - enter the Primary Key.
6. Choose **Select Container** to find the container by using the lookup functionality. 
7. On the **ABS Container List** page, select the container and select **OK**.
8. On the page that displays now, you will see a list of the bank's supported files. You can now specify the paths for the files to set up the connection:
   * **Outgoing files** - for outgoing files such as the payment files that you send to the bank, specify the path in the file path column. For example, Outgoing. 
   * **Incoming files** - for incoming files such as the bank statement files that you receive from the bank, you must specify the path and file type search pattern. The search pattern must contain at least one asterisk (\*). For example, /incoming/\*camt053.xml. However, if you have specified a different folder for each file type, you don't need to add a search pattern.
