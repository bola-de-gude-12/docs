---
title: Frequently Asked Questions About the Continia Expense App
date: 18-06-2025
description: Frequently asked questions about the Continia Expense App
id: EM-245
lang: en
---

# Continia Expense App FAQs
Find answers to some of the most frequently asked questions about the Continia Expense App.

## Can I get a notification email when an expense document is approved or rejected?
No, email notifications for approved or rejected documents is currently not available in Expense Management. However, you can view the status of documents using the [Continia Expense Mobile App push notifications](@EM-46) or in the Expense Web Portal, under **Expense** > **History** (and rejected documents under **Report** > **Open**), or by viewing your [Expense Management job queues](@EM-278).
## Why is the **Attendees** field not working properly in the Continia Expense App/Expense Portal?

If you're required to fill in **Attendees** on an expense type, but it doesn't work as expected in the Expense Mobile App or the Expense Portal, then you may have overlooked one of the steps in the process.

Check that you've completed the following steps:

1. In Business Central, go to **Expense Types**.
2. In **Attendees Required**, select the checkboxes for the expense types for which attendees should be required.
3. Go to **Field Type Dependencies**.
4. Select **Process** > **Update System Dependencies**. Lines will now appear on the page, which will make the feature work properly.
6. Select **Continia Online** > **Force Synchronize** to push the changes to the users' devices.

The **Attendees** field is normally hidden until the specific expense type is selected in the Expense Portal or the Expense Mobile App.