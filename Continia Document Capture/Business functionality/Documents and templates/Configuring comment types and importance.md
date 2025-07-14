---
title: Configuring Comment Types and Importance
date: 07-10-2022
description:  
id: DC-72
lang: en
---

# Configuring Comment Types and Importance

The Continia Document Capture document journal features a comments section, which displays various comments relating to the document you've selected. There are three different comment types:

<br>

| Comment&nbsp;type | Description |
| --- | --- |
| **Information** | Typically used to inform you that a certain process has been completed without your involvement. Examples: <ul><li>“Due date has been calculated based on document date”</li><li>“Automatically Matched”</li></ul> |
| **Warning** | Informs you that something in the document may require manual handling or adjustment. Documents with comments of this type will be excluded from the batch registration process. Examples: <ul><li>“WARNING: Payment Terms (CM) not correct.”</li><li>"Order No. = '[order number]' exists but with a different currency."</li></ul> |
| **Error** | Indicates that something is preventing the system from registering the document. Errors are displayed in bold red in the comments section. Examples: <ul><li>"Amounts do not match."</li><li>"Vendor Invoice No. [invoice number] already exists (on Vendor Ledger Entry, Entry No. = [entry number])."</li></ul> |

## Configurable comments

Many of the comments displayed in the document journal are configurable, meaning that they can be edited in the following two ways:

* You can change the comment type.
* For error comments, you can specify if documents with this error should be automatically assigned to a user that can resolve the underlying issue.

If a comment is configurable, the word **Yes** will be displayed in the **Configurable** column for that comment – if not, **No** is displayed instead.

Comment configuration changes can be applied to: 
1. A specific vendor template. You do this from the **Document Category** card (or directly from the document journal) by following the [guide below](#to-configure-comments-for-specific-templates).
1. All templates in the current company. You do this in the **Message Center Setup** by following [this guide](#to-configure-comments-for-all-templates-in-a-company).

> [!NOTE]
> If you make changes to specific individual templates using option 1, these changes will overwrite any comment changes that you may have applied to all company templates using option 2.

## To configure comments for specific templates

To configure comments for a specific vendor template, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the relevant document category – for example, **PURCHASE** – and then select **Edit** on the action bar to open the **Document Category** card.
1. On the **Templates** FastTab, in the list of templates, select the relevant template, and then select **Manage** > **Edit** to open the template card.
1. On the action bar, click **Related** > **Template** > **Message Center Setup** to open the **Edit - Message Center Setup** page for the selected template.
1. Configure the comments as needed by editing one or more of the following fields for each relevant comment:

   <br>

   | Field | Description |
   | --- | --- |
   | **User Defined comment type** | Enables you to change the comment type. It's generally possible to escalate the severity of a comment – for example, to change from **Warning** to **Error** – whereas de-escalating from **Error** to **Warning** typically isn't an option. |
   | **Assign on Error** | Indicates that whenever the currently selected comment appears in a document, the document is automatically assigned to a specified user for further action in order to resolve the issue. The field is only selectable for **Error** comments. |
   | **Assign to User ID** | Enables you to specify the ID of the user to whom you want documents with the selected comment to be assigned. The field is only editable if **Assign On Error** has been selected. |

   > [!NOTE]
   > Whenever you configure a comment, the text of the entire comment line in the setup is made bold to highlight the change, and the **Template No.** column displays the number of the template that's affected by the change. Note that the **Template No.** field itself isn't editable – it's merely for display purposes.

1. Select **Close** when you're done.

## To configure comments for all templates in a company

To configure comments for all templates in the current company, follow these steps:

1. Choose the {{search}} icon, enter **Message Center Setup**, and then choose the related link.
1. On the action bar, click **Edit List**.
1. In the list of comments, locate or select the comment that you want to configure, and then configure it as needed by editing one of the following fields:

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