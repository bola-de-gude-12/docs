---
title: Why Is the Resend Button Grayed Out?
date: 01-02-2024
description: Learn what may be the cause for the resend button to be grayed out, 
id: DO-157
lang: en
---

# Why Is the Resend Button Grayed Out?

## Question

Why Is the **Resend** button grayed out? 


## Answer

This issue may occur in production environments, for instance in BC v22.5, and also sandboxes based on BC v23.1. When it happens, the **Resend** button is grayed out on Document Output Email, and it can affect all users, including users with the SUPER permission set.

Here's how to fix it:

Open the email, and then click on the message part.
Now the resending the email will be possible.

Explanation: From a code perspective, the email editor must have been initialized as it contains the email, and modifications to the html (with reply/resend information in the top) are shown in it. You can minimize/close it again after it has been initialized, as we still have access to it afterwards.
