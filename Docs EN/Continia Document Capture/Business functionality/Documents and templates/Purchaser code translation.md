---
title: Purchaser Code Translation
date: 28-02-2023
description:  
id: DC-128
lang: en
---

# Purchaser Code Translation

Purchaser codes serve a number of important purposes in Microsoft Dynamics 365 Business Central, such as initiating standard purchase approval and providing a basis for statistics. If any of these purposes are important to your organization, it's essential that all incoming documents are assigned the correct purchaser codes. Continia Document Capture can assist you in doing so, using the **Our Contact** field in the **Document Header** section of each incoming document. 

When Document Capture [recognizes the fields of an incoming document](@DC-110), it may capture a value for **Our Contact**, or you may add one manually yourself. Either way, unless the value that's present in this field is in fact the exact purchaser code of the correct purchaser (which is rarely the case), the value must be translated into the right purchaser code in order for you to be able to register the document correctly. This translation can be done in two ways:

* Document Capture can be set up to [automatically translate the captured value to a specific purchaser code](#automatic-translation) during document registration. 
* You can [manually select the relevant purchaser code](#manual-selection) every time you register a document.

Each of these methods is described in more detail in the sections below, along with a description of how to [edit, delete, or create multiple translations for one or more vendors](#to-edit-delete-or-create-multiple-translations-for-one-or-more-vendors).

## Automatic translation

To set up Document Capture so that it automatically translates a captured **Our Contact** value to a specific purchaser code, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** code to open the document journal.
1. In the list of documents, select the one whose **Our Contact** value you want to translate.
1. Make sure that document fields have been recognized. If not, select **Home** > **Recognize Fields**.
1. In the **Document Header** section, check that a value has been captured for **Our Contact**.
1. On the action bar, click **Home** > **Register**. This will open the **Purchaser Translation** page, provided that the **Our Contact** value in step 4 is not an existing purchaser code.
1. Under **Get purchaser from**, select one of the following, depending on your preference:
   * **Vendor**: Select this option if you want to translate the **Our Contact** value to the purchaser code that's been set up on the vendor card.
   * **Select purchaser from list**: Select this option to open the **Salespeople/Purchasers** page, where you can then select the purchaser code that you want to translate the **Our Contact** value to.
1. No matter which of the options you choose in step 7 above, the **Save your selection on the template** option under **Setup Translation** will be enabled automatically. To make the selected purchaser code the default translation for the assigned template, leave this option enabled, and then select **OK** to close the page and apply your settings.

Document Capture will now automatically translate any instances of the captured **Our Contact** value to the selected purchaser code whenever you register a document that has been assigned the template in question.

## Manual selection

To manually select the purchaser code that you want a captured **Our Contact** value translated to, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** code to open the document journal.
1. In the list of documents, select the one whose **Our Contact** value you want to translate.
1. Make sure that document fields have been recognized. If not, select **Home** > **Recognize Fields**.
1. In the **Document Header** section, check that a value has been captured for **Our Contact**.
1. On the action bar, click **Home** > **Register**. This will open the **Purchaser Translation** page, provided that the **Our Contact** value in step 4 is not an existing purchaser code.
1. Under **Get purchaser from**, select one of the following, depending on your preference:
   * **Vendor**: Select this option if you want to translate the **Our Contact** value to the purchaser code that's been set up on the vendor card.
   * **Select purchaser from list**: Select this option to open the **Salespeople/Purchasers** page, where you can then select the purchaser code that you want to translate the **Our Contact** value to.
1. No matter which of the options you choose in step 7 above, the **Save your selection on the template** option under **Setup Translation** will be enabled automatically. Disable this, and then select **OK** to close the page and apply your settings.

The captured **Our Contact** value will now be translated to the selected purchaser code for this particular document when you register the document.

## To edit, delete, or create multiple translations for one or more vendors

An alternative way to set up automatic translation is to use the **Our Contact to Salespeople/Purchasers** page. An added benefit of using this page is that it also enables you to edit or delete existing translations, to set up multiple translations in one go, and to apply your translation settings globally to all vendors.

To manage translations using this page, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Select the **PURCHASE** code to open the document journal.
1. Select one of the documents in the list.
1. Make sure that document fields have been recognized. If not, select **Home** > **Recognize Fields**.
1. On the action bar, click **Translations** > **Salespeople/Purchasers** to open the **Our Contact to Salespeople/Purchasers** page.
1. To add a new translation or edit an existing one, enter a value in the **Our Contact** column of the table.
1. In the **Salesperson/Purchaser Code** column, select the purchaser code that you want the entered **Our Contact** value translated to.
1. In the **Enabled for** column, specify if the translation should apply to all vendors or only to the one that's assigned to the document you selected in step 3 above.
   > [!NOTE]
   > If you select **This vendor only**, the **Vendor No.** and **Vendor Name** fields are automatically filled out. You can't edit these values.
1. Repeat steps 6-8 for any additional translations you want to set up or edit.
1. **Optional**: To delete a translation, select the relevant line in the table, and then select **Delete** on the action bar. In the dialog that opens, select **Yes** to confirm.
1. When you're done, close the **Our Contact to Salespeople/Purchasers** page to return to the document journal.

Your translation settings are now applied either to all vendors or to the current one (as specified by you in step 8 above), and any captured **Our Contact** values in documents sent by the selected vendor(s) will be automatically translated according to your setup.

## Related information

[Capturing Fields in a Document](@DC-110)  
[Registering Documents](@DC-67)  