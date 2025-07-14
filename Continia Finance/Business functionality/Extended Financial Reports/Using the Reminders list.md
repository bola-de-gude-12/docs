---
title: Using the Reminders list in Continia Finance
date: 08-10-2024
description: An overview of the additional functionality within the Reminders feature.
id: CF-121
lang: en
---

# Using the Reminders List

This article describes the Continia Finance functionality which enhances the standard **Reminders** feature in Microsoft Dynamics 365 Business Central.

>[!NOTE]
>Before you can create reminders, you need to configure reminder terms for the customer you want to remind. For more information, see [Set up reminder terms and levels](https://learn.microsoft.com/en-us/dynamics365/business-central/finance-setup-reminders) (Microsoft article).

## Additional functionality

To access the functionality described below, open the **Reminders** list:

* Choose the {{search}} icon, enter **Reminders**, and then choose the related link.

### Ext. Test Report and Reminder Proposal List

There's an additional action group in the **Reminders** list: **Continia Finance**. Select it and two actions appear:

* Ext. Test Report - preview the reminder text before issuing the reminder to the related customer.
* Reminder Proposal List - print a list of all reminders in the current proposal. If the **Include Entries** field is selected, the reminder entries are printed below each reminder header.

Select **+New** in the action bar to create a reminder. Here you can see two additional fields:

* No. - specifies the number of the involved entry or record, according to the specified number series.
* Salesperson Code - the code of the salesperson in charge of the related customer.

Select **Suggest Reminder Lines** in the action bar to create reminder lines in existing reminders for any overdue payments, based on the information in the **Reminder** window. There are three additional settings:

* Incl. Association - if enabled, all customers of the association are combined under one reminder header – provided that the customer is assigned to an association.
* Incl. Linked Vendors - if enabled, the vendor ledger entries of the linked vendors are considered for customer reminders.
* Include Credit-side Customers - if enabled, reminders are created even when the customer has a credit total sum.

### Issued Reminders

Once you issue a reminder to a customer, this reminder is shown in the **Issued Reminders** list. To access this list:

1. Choose the {{search}} icon, enter **Issued Reminders**, and then choose the related link.
2. In the action bar, select **Continia Finance** > **Ext. Reminder** to configure and generate a report based on the data in the **Issued Reminders** list.

## See also
[Adding Extended Reminders](@CF-109)