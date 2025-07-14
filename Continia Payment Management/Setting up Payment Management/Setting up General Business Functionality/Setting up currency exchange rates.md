---
title: Setting up Currency Exchange Rates
description: How to set up currency exchange rates
date: 01-10-2021
id: PM-41
lang: en
---

# Setting up Currency Exchange Rates

Payment Management supports the import of exchange rates from a predefined selection of exchange rate providers. Payment Management does only support the currency exchange rate import from the currency exchange rate providers which come with the Payment Management installation. After having selected a currency exchange rate provider you can manually import exchange rates or you can define settings for an automatic and periodic import.

## To choose currency exchange rate provider

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Currency Exchange Rate Setup**, then select the related link.
1. On the **Currency Exchange Rate Setup** page,on the **General** FastTab, in the **Currency Exchange Rate Provider** field, choose the exchange rate provider you want to use when importing currency exchange rates.
> [!TIP]
>
> In case Payment Management has updated the selection of currency exchange rate providers, you can update the list by selecting **Currency Exchange Rate Providers** in the action bar, and select **Import Currency Exchange Rate Providers**. Please note, that Payment Management does not support manually added exchange rate providers.

## To set up automatic currency exchange rate import

To import currency exchange rates automatically:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Currency Exchange Rate Setup**, then select the related link.
1. On the **Currency Exchange Rate Setup** page, on the **General** FastTab, enable the **Automatic Import** feature, if you want the currency exchange rates to be imported automatically by Payment Management.
1. On the **Recurrence of Import** FastTab, set the **Status** field to **On Hold** to edit the import settings. You can switch the status using the action **Ready/On Hold**.
1. Activate the days you want the automatic service for currency import to run.
1. After completing the setup, set the status to **Ready** to activate the setup.



## To manually import currency exchange rates

To import currency exchange rates manually:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Currency Exchange Rate Setup**, then select the related link.
1. On the currency exchange rate setup page, on the action bar, choose the **Import Currency Exchange Rates** action.

Or

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Currencies**, then select the related link. This will open that page **Currencies**.

   > [!NOTE]
   >
   > Please be aware that the page **Currencies** contains default Business Central actions for updating and handling currency exchange rates which are very similar to the Payment Management-supported actions. 
1. To access the Payment Management currency exchange rate actions, in the action bar, select **More Options** > **Actions** > **Payment Management**, from where you can load exchange rates and access the exchange rate setup.
1. Select **Import Currency Exchange Rates**.
   > [!NOTE]
   >
   > Manual import of currency exchange rate providers, supported by Payment Management, requires you to choose a payment management-supported currency exchange rate provider. For more information, see [To choose currency exchange rate provider](#to-choose-currency-exchange-rate-provider).

