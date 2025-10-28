---
title: Configuring comment types and importance in Document Capture
date: 30-09-2025
description: How to work with configurable comments in Document Capture.
id: DC-72
lang: en
---

# Configuring comment types and importance

The document journal in Continia Document Capture features a comments section, which displays various comments relating to the document you've selected. There are three types of comment:

<br>

| Comment&nbsp;type | Description |
| --- | --- |
| **Information** | A certain process has been completed without your involvement. Examples: <ul><li>“Due date has been calculated based on document date”</li><li>“Automatically Matched”</li></ul> |
| **Warning** | Something in the document may require manual handling or adjustment. Documents with comments of this type will be excluded from the batch registration process. Examples: <ul><li>“WARNING: Payment Terms (CM) not correct.”</li><li>"Order No. = '[order number]' exists but with a different currency."</li></ul> |
| **Error** | Something is preventing the system from registering the document. Errors are displayed in bold red in the comments section. Examples: <ul><li>"Amounts do not match."</li><li>"Vendor Invoice No. [invoice number] already exists (on Vendor Ledger Entry, Entry No. = [entry number])."</li></ul> |

## Configurable comments

Many of the comments displayed in the document journal are configurable, meaning that they can be edited in the following two ways:

* You can change the comment type.
* For error comments, you can specify if documents with this error should be automatically assigned to a user that can resolve the underlying issue.

If a comment is configurable, the word **Yes** is displayed in the **Configurable** column for that comment – if not, **No** is displayed instead.

Comment configuration changes can be applied to: 
1. A specific vendor template. You do this from the **Document Category** card (or directly from the document journal) by following the [guide below](#to-configure-comments-for-specific-templates).
1. All templates in the current company. You do this in the **Message Center Setup** by following [this guide](#to-configure-comments-for-all-templates-in-a-company).

> [!NOTE]
> If you make changes to specific individual templates using option 1, these changes will overwrite any comment changes that you may have applied to all company templates using option 2.

## To configure comments for specific templates

To configure comments for a specific vendor template:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the relevant document category – for example, **PURCHASE** – and then click **Edit** on the action bar to open the **Document Category** card.
1. On the **Templates** FastTab, in the list of templates, select the relevant template, and then click **Edit** to open the template card.
1. On the action bar, click **Related** > **Template** > **Message Center Setup** to open the **Edit - Message Center Setup** page for the selected template.
1. Configure the comments as needed by editing one or more of the following fields for each relevant comment:

   <br>

   | Field | Description |
   | --- | --- |
   | **User Defined comment type** | Enables you to change the comment type. It's generally possible to escalate the severity of a comment – for example, to change from **Warning** to **Error** – whereas de-escalating from **Error** to **Warning** typically isn't an option. |
   | **Assign on Error** | Indicates that whenever the currently selected comment appears in a document, the document is automatically assigned to a specified user for further action in order to resolve the issue. The field is only selectable for **Error** comments. |
   | **Assign to User ID** | Enables you to specify the ID of the user to whom you want documents with the selected comment to be assigned. The field is only editable if **Assign On Error** has been selected. |

   > [!NOTE]
   > When you configure a comment, the text of the entire comment line in the setup is made bold to highlight the change, and the **Template No.** column displays the number of the template that's affected by the change. Note that the **Template No.** field itself isn't editable – it's merely for display purposes.

1. Click **Close** when you're done.

   > [!TIP]
   > To reset a template-specific comment setting, either click **Related** > **Template** > **Message Center Setup** on the desired template card or click **Yes** under the **Configurable** column of a comment in a document. Then, select the same value under the **User Defined Comment Type** as the value shown under the **Company Comment Type** column.

## To configure comments for all templates in a company

To configure comments for all templates in the current company:

1. Search ({{search}}) for and select **Message Center Setup**.
1. On the action bar, click **Edit List**.
1. In the list of comments, locate or select the comment that you want to configure, and then configure it as needed by editing one of the following fields.

   <br>

   | Field | Description |
   | --- | --- |
   | **User Defined comment type** | Enables you to change the comment type. It's generally possible to escalate the severity of a comment – for example, to change from **Warning** to **Error** – whereas de-escalating from **Error** to **Warning** typically isn't an option. |
   | **Assign on Error** | Indicates that whenever the currently selected comment appears in a document, the document is automatically assigned to a specified user for further action in order to resolve the issue. The field is only selectable for **Error** comments. |
   | **Assign to User ID** | Enables you to specify the ID of the user to whom you want documents with the selected comment to be assigned. The field is only editable if **Assign On Error** has been selected. |

   <br>

1. Repeat step 3 for any additional comments you want to configure.

> [!TIP]
> You can also configure comments for all templates by accessing the general **Message Center Setup** from the template-specific one: In the comments section of the document journal, locate a configurable comment, select **Yes** to open the **Edit - Message Center Setup** page, and then select **Show Default Setup** on the action bar to open the general setup page. Any changes you make here will then be applied to all templates in the current company.