---
title: Expenses FAQs
date: 10-09-2025
description: Frequently asked questions about expenses and expense documents
id: EM-244
lang: en
---

# Expenses FAQs
In this section, you can find answers to some of the most frequently asked questions about the processing of expenses in Expense Management. The answers provide information on subjects such as notification, setting a default currency, and restricting selectable field values.

## Why can't I see expense documents in Business Central?

If you can't see any documents in lists such as Expenses, Mileages, or Reports, but your Partner can - or if you can only see your own profile on the Continia User's List or Continia Users Setup - you may need to check which version of Expense Management you are running. After Expense Management, version EM 8.00 (Expense 2021, R2), the Limit Document Visibility setting was added, so you will need to adjust this setting.

To set document visibility:

1. Search for ![Search](https://docs.continia.com/images/search_small.png) **Continia User Setup Card**.
1. Under **Expense Management**, toggle **Limit Document Visibility** to *Off*.

If **Limit Document Visibility** is toggled *On*, then you will only see your own documents.


> [!NOTE]
> In versions prior to EM 8.00 (Expense 2021, R2), the Permission Role Set CEM-NAVUSER limits an Expense user to see only their own expenses in Expense Management.

## Can I get a notification email when an expense document is approved or rejected?
No, such functionality is currently not available in Expense Management. However, you can view the status of documents using the [Continia Expense Mobile App push notifications](@EM-46) or in the the Expense Web Portal, under **Expense** > **History** (view rejected documents under **Report** > **Open**), or by viewing your [Expense Management job queues](@EM-278).

## Can I set a default currency for an expense user?

This action is currently not supported – unless the currency is locked (and can't be changed by the expense user).

However, the Continia Expense App uses location data to show the currency for the country in which the expense user is. If the expense user chooses another currency, the Continia Expense App remembers it for the next expense and retains that value. If the Continia Expense App is closed, it reverts to using the currency derived from location data. To assign a specific currency via lookup value access use the following workaround. This will mean the selected expense user or group (or both) can only access a specific currency, which will also be selected by default when they create a new expense.

To assign a specific currency to an expense user or group:

1. Search for ![Search](https://docs.continia.com/images/search_small.png) **Configured Fields**.
1. In the table, under **Field Code**, click **Currency**.
1. On the **Fields on Header** action bar, click **Field Type**.
1. On the **Field Type Card** action bar, click **Field Type** > **Lookup Value Access**.
1. In the **Value Code** column of the table, select a currency. **Value Description** is automatically filled in with the currency that you selected.
1. Optional: In **Type**, select a type. The default is *User*.
1. In **Code**, select a specific user or a group.
1. To update these changes you must force a synchronization with Continia Online. On the **Field Type Card** action bar, click **Continia Online** > **Force Synchronize with Continia Online**.

## Can I limit what field values expense users can select in the Expense App?

Yes, you can. The way to specify what field values are available to expense users in Business Central is to *allow* access to certain field values, thereby limiting expense user access to only the field values specified.

For more information, see [Setting up Restrictions on Field Value Access](@EM-296).