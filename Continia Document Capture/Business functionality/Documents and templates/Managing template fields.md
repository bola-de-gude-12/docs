---
title: Managing template fields in Document Capture
date: 09-10-2025
description: How to add and remove template fields in Document Capture.
id: DC-241
lang: en
---

# Managing template fields

This article describes how to add and remove template fields, so you can capture respectively more or less information from your documents.

## To add template fields
You can easily capture more information than what’s captured by the default templates. To do so, either add one of the additional fields that are included in the standard configuration, or create your own custom field.

To add an additional field from the standard configuration, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.

2. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.

3. On the action bar, click **Template** > **Add Template Field** to open the **Template Field List**.

4. In the list, under **Field Name**, select the field you want to add to the template.

The **Template Field List** is closed, and the selected field is added to the list of template fields in the document fields section (under **Document Header**).

>[!NOTE]
>By following the instructions above, you’re only adding the selected field to the template that’s assigned to the current document. If there are fields that you would like to capture in all or most of your documents, add these fields to the master template. If you do this, newly created templates will automatically have these fields available. To learn more, see [Working with templates](@DC-18).

If you need other fields than the ones included in the standard configuration, you can create a custom field. To learn more, see [Setting up new template fields](@DC-19).

> [!TIP]
   > If the field you want to capture a value for isn't available in the **Document Header** or **Lines** sections, you can add it by selecting the desired value in the document viewer. 
   >
   > 1. Select a header or line field. Header fields can be selected from the document card or the document journal, while line fields can only be selected from the document card.
   > 2. Press <kbd>Ctrl</kbd> and select the desired value in the document viewer to open the **Assisted Template Field Setup Guide**. Note that values must be recognized with <kbd>Ctrl</kbd> and the left mouse button, and captions with <kbd>Ctrl</kbd> and the right mouse button.
   > 3. Click **Next** > **Template Field** to open the **Template Field List** and choose an existing field from the master template, or **Next** > **Create New** to create a custom field.
   > 4. When you're done, click **Finish** to return to the document card.

## To remove template fields
Just as you can add fields, you can also remove fields from a template. To remove a field from a template, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
2. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
3. On the action bar, click **Template** > **Remove Template Field** to open the **Template Field List**.
4. In the list, under **Field Name**, select the field that you want to remove from the template.
5. A dialog box appears, asking you if you want to remove the chosen field from the template. Click **Yes**.

The dialog box is closed, and the selected field is removed from the list of template fields in the document fields section (under **Document Header**).

## Related information

[Capturing header fields in a document](@DC-110)  
[Capturing line fields in a document (line recognition)](@DC-147)  
[Working with paper and PDF documents](@DC-71) 