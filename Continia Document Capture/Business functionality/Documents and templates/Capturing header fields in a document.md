---
title: Capturing header fields in a document in Document Capture
date: 30-09-2025
description: How to capture header fields in a document using Document Capture.
id: DC-110
lang: en
---

# Capturing header fields in a document

> [!IMPORTANT]
> For descriptive purposes, this article focuses on purchase documents and vendors, although the processes described below also apply to other types of business documents and document sources.

This article describes the overall process of capturing fields at header level. For line recognition, see [Capturing line fields in a document (line recognition)](@DC-147).

When capturing fields, Continia Document Capture uses captions and values to search for and identify textual information in your imported documents. Both captions and values are identifiable text strings that are visible as textual elements in the imported documents, but they differ in function.

Think of a field caption as a sort of label that helps Document Capture to identify the correct value for a template field. Each caption is associated with a corresponding value, which is then the actual text you want to capture and use when registering a document. An example of a caption could be **Invoice No.**, and the associated value could then be the number 1647. In the document viewer on the right side of the document journal, field captions are highlighted using orange boxes – whereas field values are highlighted using blue boxes.

Once a purchase document is linked to a vendor in Business Central, Document Capture automatically checks if there’s a template associated with that vendor. If so, this template is applied to the document, and all fields are captured according to the rules and configuration of that template. All document fields must be captured and have valid values for you to [register the document](@DC-67).

If it’s the first time you receive a document from a vendor, there will be no templates associated with that vendor. To assign a template to the vendor, activate field recognition in the document journal (see step 5 below). This automatically creates a template, links it to the vendor, and captures all fields for that document.

> [!NOTE]
> If a vendor sends you a document for the first time but already has an associated template in another one of your companies, Document Capture copies the template from that company to the current company. This means that you don’t have to repeat any configuration you’ve already carried out in another company for the same vendor.

>[!TIP]
>Document Capture supports Business Central sustainability feature, making it easier for you to calculate and track your company's greenhouse gas (GHG) emissions. The following header fields can be added to your templates:
>
>* **Sustainability Account No.**
>* **Fuel/Electricity***
>* **Distance***
>* **Custom Amount***
>* **Installation Multiplier***
>* **Time Factor***
>* **Emission CO2**
>* **Emission CH4**
>* **Emission N2O**
>
>The fields marked with an asterisk above, known as activity fields, aren't carried over from Document Capture templates to standard purchase invoices. Instead, Document Capture automatically calculates the emission factor fields (i.e.: CO₂, CH₄, N₂O) in the document card. For more information, see [Sustainability management overview](https://learn.microsoft.com/en-us/dynamics365/business-central/finance-manage-sustainability) (Microsoft article).

## To capture fields

To capture the fields of a document:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
1. If Document Capture has automatically identified a vendor for the document whose fields you want to capture, the number of the identified vendor is displayed in the **Vendor** field of the document list. If no vendor has been identified, assign a vendor manually as described under [Changing a document’s associated vendor](@DC-71#changing-a-documents-associated-vendor).

If you've previously received and imported documents from the assigned vendor, the template that's associated with that vendor is automatically used for capturing field captions and values. Otherwise, there's no associated template – but Document Capture creates and assigns one automatically. Field captions and values are then captured and highlighted using orange and blue boxes in the document viewer on the right.

You can always change the identified field values and captions. To learn more, see [Training Document Capture to locate values](#training-document-capture-to-locate-values) below.

>[!TIP]
>PDFs are complex, multi-layered documents. If you encounter odd values when processing a PDF in Document Capture, open the PDF using a modern browser, MS Paint, or equivalent. You can then either print it to PDF or save it as a PDF once again, which should allow Document Capture to process it correctly. Note that this only applies to on-premises setups, as the Cloud OCR is more precise.

## Understanding field captions and values

As mentioned above, Document Capture searches for and identifies textual information in imported documents using field captions and corresponding values. For example, consider the following texts which could be found in any invoice:

| Text sample | Explanation |
| --- | --- |
| “Invoice number: 12345678” | The caption is **Invoice number** and the corresponding value is **12345678**. |
| “Invoice date: 01/01/2021” | The caption is **Invoice date** and the value is **01/01/2021**. |

As is evident in the above, captions and values always work in pairs. Usually, captions don’t change from document to document when the documents have been sent by the same vendor – unless the vendor changes the layout of the invoice. Values, on the other hand, change from document to document. For example, the invoice number typically increases incrementally for each invoice, and the same usually goes for the invoice date.

Captions are defined for each template field, and the values are captured and stored in the document itself. It’s important to note that for captions and values to be captured correctly, the distance between them should remain the same in all documents from the same vendor. For instance, in the examples above, the caption immediately precedes its corresponding value at a certain distance, and if the two elements have the same position and distance between them in all subsequent documents, they're all processed correctly.

Captions and values can also be split into separate lines, for example if an **Invoice number** caption is placed on one line and its corresponding value then follows immediately below it on the next line (a common invoice format). This is also perfectly fine, as long as the distance between the caption and the value is the same for all documents from the same vendor. Even captions that are placed far away from their related values are completely acceptable, provided that the distance between the two remains the same in all documents.

When Document Capture identifies the values of fields in a document, it searches for captions that are defined for each template field and then attempts to capture their associated values. For example, if Document Capture searches for the text string “Invoice number” in an invoice and manages to find this, it can then locate the actual invoice number as well based on the template configuration.

>[!NOTE]
>Although you can define multiple captions for a given template field on the **Field Captions** page, such as Date Invoice and Date Credit Note for the **Invoice Date** field, only the first caption found by Document Capture is kept when fields are recognized. This is done to ensure a precise and reliable recognition across all layers of the document.

### Default field values

When header fields aren’t recognized, default values are often applied to the invoice when registering it. These values are automatically taken from the vendor or template, and aren't visible by default. If the header fields contain a value that’s either recognized from the document or manually selected, the value from the vendor/template card isn’t used.

If the **Show Default Field Value** setting is enabled on the document category card, the default values for the fields listed below are shown in brackets next to the field names in the header field list – both in the document journal and on the document card.

* Purchase category:
  * Approval Flow Code
  * Responsibility Center
  * Vendor Bank Account No.
  * Vendor VAT No.
  * Vendor Phone No.
  * Dimensions 1-8*

* Sales category:
  * Responsibility Center
  * Dimensions 1-8*
  
  \* The dimension values displayed are based on the order determined on the **Default Dimension Priorities** page.

To enable **Show Default Field Value** setting:

1.	Search ({{search}}) for and select **Document Categories**.
2.	To open the purchase document category, select the line of the relevant document category – for example, **PURCHASE** –, and then click **Edit** on the action bar.
3.	On the **General** FastTab, enable the setting **Show Default Field Value**.

> [!NOTE]
> The expected values may be changed or overwritten when the actual invoice is created, depending on the final document data, your own overrides, and any updates to the related fields during processing.


## Training Document Capture to locate values

Document Capture sometimes fails to capture the value of a field in a document, or it may identify an incorrect element as the field’s associated value. If this happens, you can easily train Document Capture by changing the caption and/or showing it where exactly to locate the correct value in the document. To do this:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
1. In the document fields section (under **Document Header**), select the template field that you want to correct – for example, **Posting Description**.
1. Use your mouse to select exactly what text in the document should be captured for the chosen template field. To set the caption, right-click and hold the button to draw an orange box around the relevant text in the document viewer.
1. Similarly, to set the corresponding value for the chosen template field, left-click and hold the button to draw a blue box around the relevant text in the document viewer.
1. The selected text is added to the template field in the document fields section. Verify that it has been captured correctly.
1. To confirm that the text is consistently captured correctly, click **Home** > **Recognize Fields** on the action bar. If the text somehow isn't captured correctly this second time, carry out steps 4-7 again until you get the desired result.

> [!TIP]
   > If the field you want to capture a value for isn't available in the **Document Header** or **Lines** sections, you can add it by selecting the desired value in the document viewer. 
   >
   > 1. Select a header or line field. Header fields can be selected from the document card or the document journal, while line fields can only be selected from the document card.
   > 2. Press **Ctrl** and select the desired value in the document viewer to open the **Assisted Template Field Setup Guide**. Note that values must be recognized with **Ctrl** and the left mouse button, and captions with **Ctrl** and the right mouse button.
   > 3. Click **Next > Template Field** to open the **Template Field List** and choose an existing field from the master template, or **Next > Create New** to create a custom field.
   > 4. When you're done, click **Finish** to return to the document card.

## Related information

[Working with paper and PDF documents](@DC-71)  
[Managing template fields](@DC-241)