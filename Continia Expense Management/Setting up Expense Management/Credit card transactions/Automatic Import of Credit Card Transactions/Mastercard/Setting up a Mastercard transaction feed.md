---
title: Setting up a Mastercard Transaction Feed
date: 22-10-2024
description: Details on how to set up a Mastercard transaction feed to Continia Expense Management
id: EM-280
lang: en
---

# Setting up a Mastercard Transaction Feed 

This article describes how to set up a transaction feed to Continia Expense Management, so that your Mastercard transactions can be imported directly into Expense Management.

> [!NOTE]
> The transaction feed must be set up by your bank using the below guide, which describes a process that's external to Continia. The guide may therefore not be entirely up to date at all times, although Continia generally strives to make sure that it is.

## To set up a transaction feed to Expense Management

As a user of Expense Management, you must reach out to your banking relationship manager and request that your CDF feed be sent directly to Continia Software in the Mastercard SmartData Portal. Refer the banking relationship manager to this guide.

As a banking relationship manager, to set up a Mastercard transaction feed to Expense Management on behalf of the user's organization, follow these steps:

1. Open the Mastercard SmartData Portal.
1. On the **Format** page, make the following selections:
   * Under **Vendor Name**, select **Continia Software**.
   * Under **Application Name**, select **Continia Expense Management**.

      ![Mastercard SmartData Portal interface](/images/EM/mastercard-smartdata-portal-interface.png)
1. On the **Frequency** page, make the following selections:
   
   ![Frequency](/images/EM/frequency.png)
1. On the **Record Selection** page, make the following selections:
   
   ![Record Selection](/images/EM/record-selection.png)
1. On the **Filtering** page, select **No**.
1. On the **Masking** page, select whether or not data like credit card IDs should be masked.
   > [!NOTE]
   > If the user's organization chooses to mask credit card IDs, make sure that all credit card IDs used in the organization are unique when masked. 
1. On the **Notifications** page, select **No**.
1. On the **Data Initialization** page, do one of the following:
   * If historical data should *not* be included, make the following selections:
      
      ![Data Initialization, no historical data](/images/EM/data-initialization-no-historical-data.png)
   * If historical data *should* be included, make the following selections, and specify the date of the earliest transactions you'd like to include:
      
      ![Data Initialization, historical data](/images/EM/data-initialization-historical-data.png)

Your bank will initiate delivery of the feed by finding Continia Software in Mastercard's Smart Data Portal. Once this is done, the bank will send you an email containing the file delivery ID, for example G0123456. This is your confirmation that the setup has been completed.

You're now ready to set up a bank agreement in Expense Management to receive Mastercard transactions automatically. For information on how to do this, see [Activating Credit Card Agreements](@EM-32).

## See also

[Importing Mastercard Transactions](@EM-279)  