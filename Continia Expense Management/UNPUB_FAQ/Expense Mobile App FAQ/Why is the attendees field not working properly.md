---
title: Why Is the Attendees Field not Working Properly?
date: 30-11-2023
description: 
id: EM-200
lang: en
---

# Why Is the Attendees Field not Working Properly?

## Question

Why is the **Attendees** field not working properly in the Expense Mobile App/Expense Portal?

## Answer

If it's a requirement to fill in **Attendees** on an expense type, but it doesn't work as expected for you in the Expense Mobile App or the Expense Portal, some steps are probably missing in the setup process.

In Business Central, check the following:

1. Go to **Expense Types**.
2. In the **Attendees Required**, select the checkboxes for the expense types for which attendeees should be required.
3. Go to **Field Type Dependencies**.
4. Select **Process** > **Update System Dependencies**.
5. Lines will now appear on the page, which will make the feature work properly.
6. Select **Continia Online** > **Force Synchronize** to push the changes to the users' devices.

The **Attendees** field is normally hidden until the specific expense type is selected in the Expense Portal or the Expense Mobile App.