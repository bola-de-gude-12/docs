---
title: The G/L Documents category in Document Capture
date: 27-08-2025
description: How to OCR-process and attach searchable documents to G/L entries in Document Capture.
id: DC-352
lang: en
---

# The G/L Documents category

The G/L Documents category – **GLDOC** – in Continia Document Capture enables you to OCR-process and add documents to G/L entries as attachments, making them searchable. The G/L entries are amended in Microsoft Dynamics 365 Business Central once you register the document.

>[!NOTE]
>The G/L Documents category can't be used to create general journal lines from documents. To do this, you need to use the Purchase Order category. For more information, see [Setting up the registration of documents as general journal lines](@DC-112) and [Registering documents as general journal lines](@DC-67#registering-documents-as-general-journal-lines).

Before you can use the G/L Documents category, you need to set up a new template.

1. Search ({{search}}) for and select **Document Categories**.
2. On the **Document Categories** page, select the G/L Documents category and, on the action bar, click **Edit**.
3. On the **Templates** FastTab, select the master template and, in the related action bar, click **Copy**.
4. In the **Copy Template** dialog box, set the **New Type** field to the blank value. Then, click **OK**.

## To work with the G/L Documents category

With the G/L Documents category set up, you can now process documents imported into it.

1. Search ({{search}}) for and select **Document Categories**.
2. On the **Document Categories** page, click the **GLDOC** code to open the G/L Documents category.
3. In the document journal, select the desired document and, on the action bar, click **Actions > Functions > Create/Select Template**.
4. In the dialog box that opens, select the desired template. Then, click **OK**.
5. On the **Document Header** FastTab, enter the document number in the **Document No.** field. Alternatively, click the three dots by this field to choose the invoice you want to attach the incoming document to. 
6. **Optional**: To recognize text in the **Description** field, select it accordingly in the document.
7.  On the action bar, click **Home > Register** to register the document.

## Related information

[The Purchase Order category](@DC-136)