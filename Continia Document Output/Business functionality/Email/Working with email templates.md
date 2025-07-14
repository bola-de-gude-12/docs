---
title: Working with email templates
date: 11-07-2025
description:  
id: DO-52
lang: en
---

# Working with Email Templates

For a variety of reasons, such as name changes or organizational changes, you'll be editing your email templates from time to time. In this article, you'll be introduced to how to do that.
<br>
<br>
<iframe src="https://player.vimeo.com/video/880833091?h=903d58abee&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="DO Learn_1b Email message contents"></iframe>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

## To edit email templates

On the **E-mail template card** page, the **General** FastTab contains the information you'll see in the header of your email, such as **From Email** and **Email Recipient**, as well as data used in Business Central, such as **Code**, **Report-ID** and **Dimension Code**.

To edit an email template:

1. Select the {{search}} icon, enter **Email Templates**, and then select the related link.
1. From the list, select a template to edit, and on the action bar, select **Edit**.
1. In the **General** FastTab, you can edit the following fields:
   * **Report-ID** – specifies the report number for this template. The report is used to create the PDF that's attached to the email.
   * **Template Variant Field No.** – specifies the field number that's used for different template variants. You can't use both this field and **Dimension Code** at the same time.
   * **Dimension Code** – specifies the dimension code you can use as a variant on the template line. An email template can be set for each dimension. You can't use both this field and  **Template Variant Field No.** at the same time.
   * **Merge Fields** – specifies the number of merge fields available for use.
   * **Recipients Setup Lines** – specifies the number of fields where Document Output looks for email recipients.
   * **From Email** – specifies how to find the from (sender) email address. Choose between the four options in the drop-down menu.

## Email template FactBoxes

All email templates have three FactBoxes attached to them. They provide an easy overview of certain important information regarding recipients and the selected email template line.  You find the FactBoxes in the right side of the screen when you open an email template. The FactBoxes are:

**Recipients Setup** – This FactBox displays the prioritized list of where the recipient email address is retrieved. You can use the dropdown menu to enter the **Template Recipient Setup** and change the list, including prioritization.

**Template Line Attachment** – This FactBox displays all attachments for the selected template line.

**Document Output Log** –  This FactBox displays the log entries where the selected template line has been applied.

>  [!TIP]
>  If the FactBoxes are not displayed when you open an email template, select the **Expand the FactBox Pane** icon (a lowercase "i" in a circle) in the top right corner. 


## To configure email recipients

To make sure that every email has at least one recipient, the system currently uses the recipient email address from the customer card if no specific recipient is specified. However, the email templates provide various options to customize the email recipient setup based on document group, template type, or a fixed email address, offering a flexible approach to defining recipients for different scenarios.

To edit the recipient setup:

1. Select the {{search}} icon, enter **Email Templates**, and then select the related link.

1. From the list, select a template to edit, and on the action bar, select **Edit**.

1. In the **Recipient** FastTab, you can edit the following fields:

   * **Document group** – email templates can be attached to a document group. This allows you to assign different email addresses for specific purposes, such as directing accounting-related emails to the finance department, sending contract-related emails to a particular contact, or sharing shipment details with a designated recipient within a different document group. Once a document group is defined on an email template, it will be used if it's defined in the customer email recipients in the customer FactBox.

   * **Recipients Setup Lines** – shows the number of configured recipient lines. These lines are used when you want to define from where the recipient email address for the specific email template type is retrieved. This means that you can establish a list of places from where the recipient email address is retrieved and set the priority for each according to your needs.

   * **Email is mandatory** – when enabled, checks if everything is ok for a configured email before a draft email is opened. When a draft email is opened, it will count as a sent document, regardless of whether it's been sent to the email server or not.

   * **Fixed Cc Recipient(s)** and **Fixed Bcc Recipient(s)** – used to send a copy of all emails of a specific document type to a sales representative or similar internal employee in your company when emails are sent out.

   * **Test Recipient** – overrides all configured email recipients configured in an email template.
<br>
<br>
<iframe src=https://player.vimeo.com/video/1046810200?h=7a5cf0a368&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479 width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media; web-share" title="Configure Document Output email template recipients"></iframe>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

## To edit email template lines

The **Email Template Lines** FastTab allows you to edit the information in the email itself, such as the email text, the signature, and the subject field.

To edit an email template lines:

1. Choose the {{search}} icon, enter **Email Templates**, and then choose the related link.
1. Select a template from the list to edit, then select **Edit** on the action bar.
1. To edit the email text, select **Email Template** > **Edit HTML Template**. Some of the options are:
   * **Language Code** - specifies a localized template version for the selected language code.
     Explanatory notes on selected actions:
   * **Background PDF** > **Set Background PDF** - lets you pick a PDF that will be used as background for your template. Important: **Engine** must be set to NAV-PDF on either the template or the Document Output Setup page. You can read more about this in the article [Setting a Background PDF](@DO-45).
   * **Merge PDF** > **Set Merge PDF File** - adds pages from a PDF to the resulting PDF report.
1. When you're done editing the HTML template, on the action bar, select **Save Email Template**.

> [!TIP] 
> If an invoice doesn't use the correct template, it's possible that you forgot to save the HTML template after having edited it. Unlike other options in Business Central, HTML templates are not saved automatically. To avoid this issue, ensure that you select **Save** when you've edited an HTML template.

> [!TIP]
> It's super easy to insert merge fields into your HTML template. Just enter a **%**, which will make a list of all available merge fields appear. Pick one and you're done!

> [!IMPORTANT]
> Always leave **Language Code** and **Template Variant Value Code** empty in the first line. This empty line will be the default template used if documents don't fall into any of the variants defined in **Language Code** or **Template Variant Value Code**.  

## To copy email template lines
It's easy to copy email template lines for language variants, etc. in Document Output. Go to any email template, and do the following:

1. In the **Email Template Lines** FastTab, select the email template line you want to copy.
1. In the action bar, select **Manage** > **Copy Line** > **Yes**.
1. Choose a language code or/and the variant you choose in either **Variant Field Name ** or **Dimension Code** under **Variants** in the **General** FastTab.
1. Enable the line by selecting the checkbox in the **Enabled** column.

<br>
<iframe src="https://player.vimeo.com/video/884852596?h=06ab05defe&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="DO Learn_1d Use variants of email templates"></iframe>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

## To create a new email template

Continia Document Output comes with several ready-to-use email templates so you can start sending documents immediately.

Naturally, you also have the option to create your email templates from scratch. However, it's *highly* recommended to always use one of the existing templates as a starting point and then carry out the necessary corrections. This is because, usually, a lot of the information in a template, such as merge fields, recipient(s), etc., can be reused.

To create a new email template:

1. Choose the {{search}} icon, enter **Email Templates**, and then choose the related link.
1. On the action bar, select **New**.
1. In the **General** FastTab, fill out the fields as necessary.
1. In the **Email Template Lines** FastTab, fill out the fields and use the actions as necessary.
1. On the General FastTab, the **Merge fields** field helps to insert dynamic customer-specific data, such as invoice numbers, customer names or addresses, or company logos, into email lines, signatures, or file names. When you use merge fields, you ensure that changes to your customer data are reflected in all relevant places as soon as modifications occur on customer cards.
1. On all email templates, you'll find an attached report selection that can be used for the general layout of the email content. From this report selection, the **First Table** field in **Report** will indicate where the available merge fields are fetched. You can view a list of available merge fields in the template you're modifying by selecting the number next to the merge field caption. This will open a list of the merge fields that are available for use.

## Support of email templates in multiple languages

Being able to send your documents in the specific languages of your customers can be a great way of distinguishing your company from competitors, and it may even be required by some of the customers. Overall, you have two options for creating multiple language versions of your documents:

* Letting Translate with Copilot translate the text of your existing email templates
* Importing predefined email templates in a specific language

**The Translate with Copilot action** lets you start with a copy of the text in your existing email HTML template. This is useful if you've already edited the default email template to suit your company.

To use the Translate with Copilot action, follow these steps: 

1. On the **Email template card**, in the **Email Template Lines** FastTab, select a line to copy in the table.
1. In the FastTab action bar, select **Manage** > **Copy Line**.
1. In the dialog that opens, select **Yes** to confirm that you want to copy the line.
1. In **Language Code**, specify the language code for the new email template line. Select **OK** to close the dialog and return to the email template card.
1. Select the new email template line.
1. In the FastTab action bar, select **Email Template** > **Edit HTML Template**.
1. Select **Translate with Copilot**, and then select the appropriate language.
1. Under **Subject**, manually translate the subject line, if necessary.
1. In the action bar, select **Save Email Template** when you're done. 

The translated email template is now saved and ready for use. 

**Alternatively, you can use the predefined language email templates** provided by Continia. When you run the assisted setup guide during the installation of Document Output, it will automatically import email templates that match the language of your Business Central database, but Document Output also includes functionality to import predefined language variants of these email templates.

To import predefined email templates in a specific language, follow these steps:

1. Select the {{search}} icon, enter **Email Templates**, and then select the related link.
1. On the action bar, select **Template** > **Download Template**.
1. In the list, select the language you want to import email templates for, and select **OK**.
1. In the **Action** column, you can choose between three actions for each template: **Create** to create the language variant template, **Replace** to create the language variant template and make it the default template, and **Skip** to skip the creation of this email template variant. As default, all email template language variants are marked as **Create**.
1. After you've made your selections, select **OK** to complete the import.

You find your email template language variants under each default email template as email template lines.
<br>
<br>
<iframe src="https://player.vimeo.com/video/1050743783?h=3b7c4a4b6e&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write; encrypted-media" title="Email Template Line Variants"></iframe>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.

## See also
[Merging PDF Files](@DO-53)  
[Signing PDF Files](@DO-47)  
[Password Protecting PDF Files](@DO-35)  