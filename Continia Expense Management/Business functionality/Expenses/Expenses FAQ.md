---
title: Frequently asked questions about expenses
date: 23-06-2025
description: Frequently asked questions about expenses
id: EM-244
lang: en
---

# Expenses FAQs
In this section, you can find answers to some of the most frequently asked questions about the processing of expenses in Expense Management. The answers provide information on subjects such as notification, setting a default currency, and restricting selectable field values.

## Can I get a notification email when an expense document is approved or rejected?
No, such functionality is currently not available in Expense Management. However, you can view the status of documents using the [Continia Expense Mobile App push notifications](@EM-46) or in the the Expense Web Portal, under **Expense** > **History** (view rejected documents under **Report** > **Open**), or by viewing your [Expense Management job queues](@EM-278).

## Can I set a default currency for an expense user?

This action is currently not supported – unless the currency is locked (and can't be changed by the expense user).

However, the Continia Expense App uses location data to show the currency for the country in which the expense user is. If the expense user chooses another currency, the Continia Expense App remembers it for the next expense and retains that value. If the Continia Expense App is closed, it reverts to using the currency derived from location data. To assign a specific currency via lookup value access use the following workaround. This will mean the selected expense user or group (or both) can only access a specific currency, which will also be selected by default when they create a new expense.

To assign a specific currency to an expense user or group:

1. Select the ![Search](https://docs.continia.com/images/search_small.png) icon, enter **Configured Fields**, then select the related link.
1. In the table, under **Field Code**, select **Currency**.
1. On the **Fields on Header** action bar, select **Field Type**.
1. On the **Field Type Card** action bar, select **Field Type** > **Lookup Value Access**.
1. In the **Value Code** column of the table, select a currency. **Value Description** is automatically filled in with the currency that you selected.
1. Optional: In **Type**, select a type. The default is *User*.
1. In **Code**, select a specific user or a group.
1. To update these changes you must force a synchronization with Continia Online. On the **Field Type Card** action bar, select **Continia Online** > **Force Synchronize with Continia Online**.

## Can I limit what field values expense users can select in the Expense App?

Yes, you can. The way to specify what field values are available to expense users in Business Central is to *allow* access to certain field values, thereby limiting expense user access to only the field values specified.

For more information, see [Setting up Restrictions on Field Value Access](@EM-296).