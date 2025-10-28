---
title: Email setup for external or guest users in Microsoft Entra
date: 27-05-2025
description: Learn how to set up email for external and guest users in Entra
id: EM-317
lang: en
---

# Email setup for external or guest users in Microsoft Entra

An External or Guest user in Microsoft Entra have either an #EXT# in their email address, or a name (for example, External Technician). Whereas a standard user name is usually given in the following format:

User_xxxxyyyyyzzzzzzz

When you create a Continia user account for a guest or external Business Central user, the email exported to Continia Online will show in the information on the **User Card**. You can find it under **Microsoft 365**, in the **Authentication Email** field. The information is usually the word Technician, or an email with EXT in it. This causes the Expense Mobile Portal and Web Portal logins to fail.

To successfully set up email for external or guest users:

1. Search for {{search}} for **Continia Users**.
1. In the top right corner, select **Settings** > **Personalize**.
1. On the **Personalizing** action bar, select **+Field** to add a column.
1. Drag the column heading from the **Add Field to Page** list into the table where you want it located.
1. Click the text of the field and name it: Office 365 Authentication Email.
1. Click **Done**.
1. Add the correct email address to the new column (so it is the same as the one that's listed in the **Email** column).
1. On the action bar, click **Export Users** > **OK**.

## Related information

[How to retain expense history when changing user emails](@EM-325) 
