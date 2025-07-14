---
title: Can I Restrict Which Field Values Expense Users can Select in the Continia Expense App?
date: 15-11-2023
description: Export and import of customer data 
id: EM-196
lang: en
---

# Can I Restrict Which Field Values Expense Users can Select in the Continia Expense App?

## Question

Can I restrict which field values expense users can select in the Continia Expense App?

## Answer

Yes, you can!

You can easily restrict field values that are available to expense users. The way to do that in Business Central is to *allow* access to certain field values rather than restricting access to particular field values.

Let's go through an example where a company wants to restrict which expense types that are available to the expense users:

1. Go to **Configured Fields**.
1. Under **Field Code**, select **Expense Type**.
1. In the action bar, select **Field Type**.
1. In the action bar, select **Field Type** > **Lookup Value Access**.
1. In **Value Code**, select the expense type you want to allow access to. **Description** is automatically filled in with the currency you selected.<br><br>Note that you need to create an entry for each expense type you want to allow access to. If you only make one line, the user/user group you define in **Type** will only have access to this one expense type.<br><br>
1. In **Type**, select a user type. You can select either *user* or *user group*. Here, it makes a lot of sense to select **User Group** so you don't have to apply the settings to each individual expense user.
1. In **Code**, select a particular user or a user group.

This method can be used for many other fields than expense types, for example job, departments, etc.

## See also
[Expense User Group Setup for Expense Management](@EM-35)