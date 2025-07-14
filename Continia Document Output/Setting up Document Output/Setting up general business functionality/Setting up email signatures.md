---
title: Setting Up Email Signatures
date: 08-04-2024
description:
id: DO-71
lang: en
---

# Setting Up Email Signatures

Using an email signature ensures that you sign off on job emails in a professional way and that business information such as contact details is never omitted.

You can create as many email signature variants as you like in Document Output, but each one will have to be individually added to the email lines of an email template before it's used. A large variety of merge fields from Business Central can be used in email signatures. This lets you add personal or company details to the signature.

When you've installed Document Output, you can find two pre-made email signatures in the **Email Signatures** page: **SIG-ADVERTISE** and **SIG-DEFAULT**. Using these as examples, you can see how to add a simple picture to an email and how to put together a signature using merge fields.

## To create new email signatures

When you create—or edit—an email signature, you have a number of customization options, such as which fonts to use, setting a date from which the signature will be active, etc.

To create a new email signature, follow these steps:

1. Choose the {{search}} icon, enter **Email signatures**, and then choose the related link.
1. In the action bar, select **New**.
1. In the **General** FastTab, enter a unique code in **Code**. The code must start with **SIG-**.
1. Optional: In the **General** FastTab, enter a start date from which the signature will be active in **Start Date**.
1. Optional: In the **General** FastTab, enter a short description of the signature in **Description**.
1. In the **HTML Signature** FastTab, enter a signature. You can use text or merge fields (overview in the box in the upper-right corner) or a mix of both.
1. Select **Save Signature** in the action bar when you're done.

## To edit email signatures

To edit an email signature, follow these steps:

1. Choose the {{search}} icon, enter **Email signatures**, and then choose the related link.
1. in the table, select the signature you want to edit.
1. In the action bar, select **Edit**.
1. Make your changes, and select **Save Signature** in the action bar when you're done.

## Adding a signature to an email template

To add an email signature to an email template, follow these steps:

1. Choose the {{search}} icon, enter **Email Templates**, and then choose the related link.
2. Select the email template to which you want to add a signature.
3. In the action bar in the **Email Template Lines** FastTab, select **Email Template** > **Edit HTML Template**.
4. Apply a signature to the template by writing a **%** followed by the signature code, e.g. **%SIG-DEFAULT**, where you want the signature to be displayed.

In the **Signature** menu on the bottom right of the **Email Templates** page, you'll find the signature options that are available to choose from.

To the right in the **Signatures** menu, there's a number that indicates if more variants of a signature have been created. When you select a number, a list of available signatures will be displayed. Using this list, you can specify a signature that will be used going forward as well as define start dates for signature variants. Document Output will automatically change the signature in all affected email templates on the specified date.
<br>
<br>
<iframe src="https://player.vimeo.com/video/880833091?h=903d58abee&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="DO Learn_1b Email message contents"></iframe>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.