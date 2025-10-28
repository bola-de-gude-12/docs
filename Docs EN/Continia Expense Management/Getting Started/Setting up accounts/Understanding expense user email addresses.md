---
title: Understanding Expense user email addresses
date: 27-05-2025
description: Learn about the different email address fields and what they mean
id: EM-322
lang: en
---

# Understanding Expense user email addresses
An Expense user is usually identified by their email address specified in the Continia User Setup in Microsoft NAV/Business Central. However, other email fields are sometimes exported into Continia instead, these include the email address specified in the following fields: Authentication Email (in Users) or Office 365 Authentication Email (on the Continia Users list). Learn more about each field in the following sections.

## The Continia User Setup field explained

This field is normally for the email address of the username/login for the Expense user.

It is the address that will receive the Expense Management welcome email, and will be the same address to sign in to the Expense Mobile App or the Expense Web Portal. The only exception to this is if they're using Office365 to sign in. For more information, see [Office 365 on the Expense Web Portal and Expense Mobile App](https://continia.zendesk.com/hc/da/articles/360019865699).

## The Users Authentication Email explained

When a Continia user is also a Microsoft NAV/Business Central user, you'll find the Authentication Email listed on the Users list. This is the email address that will be exported in to Continia as the user's Expense user email address (regardless of what is stated on the Continia User Setup.

## The Continia Users list Office 365 Authentication email explained

The third email field relevant for Expense Management is the Office365 Authentication Email field. You can see this on the Continia Users List if you have already manually added this column.

This email address overrules the Users Authentication Email address. It's useful for external users, alias users (i.e. Partner Technician), or to avoid using the long onmicrosoft-email address. 

If an Office365 Authentication Email is used, make sure the Continia User Setup email address, and the email address in this field, are the same. Otherwise the system may not find the right user ID when sending reminders and updates.


## Related information

[How to retain expense history when changing user emails](@EM-325)  
[Email setup for external or guest users in Microsoft Entra](@EM-317)  