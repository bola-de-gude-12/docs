---
title: Can I set a default currency for an expense user?
date: 18-10-2023
description: Export and import of customer data 
id: EM-192
lang: en
---

# Can I Set a Default Currency for an Expense User?

## Question

Is it possible to set a default currency for an expense user? It should be available in the Mobile Expense App and the Expense Portal. Maybe even pre-selected?

## Answer

No, setting a default currency code for an expense user is currently not supported – not unless the currency is locked and consequently can't be changed by the expense user.

It's worth noting that the Expense Mobile App will use location data to show the currency for the country in which the expense user is. If the expense user chooses another currency, the Expense Mobile App will remember it for the next expense and keep that value. If the Expense Mobile App is closed, it reverts to using the currency derived from location data.

A workaround is to assign a specific currency to an expense user or group via lookup value access. Here's how you do it:

1. Go to **Configured Fields**.
1. Under **Field Code**, select **Currency**.
1. In the action bar, select **Manage** > **Field Type**.
1. In the action bar, select **Field Type** > **Lookup Value Access**.
1. In **Value Code**, select a currency. **Description** is automatically filled in with the currency you selected.
1. Optional: In **Type**, select a type. Default is *user*.
1. In **Code**, select a user or a group.

Now all that remains is to force a synchronization with Continia Online, and you're done. In essence, this change means that the selected expense user or group (or both) only has access to this one currency, which will also be selected by default when they create a new expense. 