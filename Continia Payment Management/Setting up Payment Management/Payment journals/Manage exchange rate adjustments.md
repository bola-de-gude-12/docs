---
title: Manage Exchange Rate Adjustments
description: Information on how to manage currency exchange rate adjustments in the payment journal.
date: 17-11-2021
id: PM-68
lang: en
---

# Managing Exchange Rate Adjustments

When paying vendors in a foreign currency, the currency exchange rate in the file sent from Business Central to the bank may not always be the same as the currency exchange rate used by the bank when processing the payments. If you're using direct bank communication, some banks support returning a status file to Business Central with information about the actual currency exchange rate used for the foreign payments (non-LCY). If such a status file is supported by your bank, you can enable, for Payment Management to automatically update the currency exchange rate on the unposted payment lines in the payment journal.

## To enable exchange rate adjustments

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Management Setup**, then select the related link. 
1. On the **Payment Management Setup** page, on the **Purchase and Payments** FastTab, enable the **Use Exchange Rate Adjustment** feature. 

Exchange rates in the payment journal will now automatically be updated by Payment Management if this is supported in the status file received from your bank.

