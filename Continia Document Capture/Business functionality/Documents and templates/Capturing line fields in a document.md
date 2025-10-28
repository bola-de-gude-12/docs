---
title: Capturing line fields in a document (line recognition) in Document Capture
date: 30-09-2025
description: How line recognition works in Document Capture.
id: DC-147
lang: en
---

# Capturing line fields in a document (line recognition)

> [!IMPORTANT]
> For descriptive purposes, this article focuses on purchase documents and vendors, although the processes described below might as well be centered around other types of business documents and document sources.

The process of capturing line fields in an imported document is very similar to that of [capturing header fields](@DC-110), and you have to go through many of the same steps for both processes. The main difference between the two is that header field recognition disregards the lines of the document, and only checks the document header when capturing [field captions and values](@DC-110#understanding-field-captions-and-values) – whereas line recognition captures field captions and values in the document lines in addition to the captured header fields. This ensures a higher level of captured detail for each document, which may be useful in some contexts and unnecessary in others – depending on what data is needed in your organization.

The line recognition process is described in detail below. Note that if it’s the first time you receive a document from a vendor, there are no templates associated with that vendor. To assign a template to the vendor, you have to activate field recognition in the document journal (see [step 4 below](#to-capture-line-fields)). This automatically creates a template, links it to the vendor, and captures all fields for that document.

> [!NOTE]
> If a vendor sends you a document for the first time but already has an associated template in another one of your companies, Continia Document Capture copies the template from that company to the current company. This means that you don’t have to repeat any configuration you’ve already carried out in another company for the same vendor.

>[!TIP]
>Document Capture supports Business Central sustainability feature, making it easier for you to calculate and track your company's greenhouse gas (GHG) emissions. The following line fields can be added to your templates:
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

## To capture line fields

To capture the fields of a document, including line fields:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the code of the relevant document category – in this case **PURCHASE** – to open the document journal.
1. If Document Capture has automatically identified a vendor for the document whose fields you want to capture, the number of the identified vendor is displayed in the **Vendor** field of the document list. If no vendor has been identified, assign a vendor manually as described under [Changing a document’s associated vendor](@DC-71#changing-a-documents-associated-vendor).
1. Provided that this is the first document you receive and import from the assigned vendor, there's no associated template, so you must assign one by activating field recognition. On the action bar, click **Home** > **Recognize Fields**. Field captions and values are then captured and highlighted using orange and blue boxes in the document viewer on the right.
   >[!NOTE]
   >If you've previously received and imported documents from the assigned vendor, the template associated with that vendor is automatically used for capturing field captions and values.
1. On the action bar, click **Document** > **Document Card** to open the document card.
1. On the **Lines** FastTab, for the first line in the table, select the field in the **No.** column. In the document viewer, locate the line column header that corresponds to the selected **No.** field (it could be named **Item**, **Item \#**, **Number** or similar), and then right-click and hold the button to draw an orange box around the located header in the document viewer.
   > [!NOTE]
   > If the imported document doesn't contain a line column header that corresponds to **No.**, move on to the first field that does (typically **Description**). Then, right-click to draw an orange box around the header in the document viewer.
   > 
   > However, note that the **No.** field is typically mandatory (as is the case in the default template), meaning that the document can't be registered if this field contains no value. If so, you must manually enter a value in the field. The same goes for any other fields that have been set to **Required** on the template card.
1. Repeat step 6 above for all fields that have a matching column header in the document. All column headers in the line section of the document should now be enclosed in orange boxes in the document viewer.
1. On the action bar, click **Home** > **Recognize Fields**. The values below each of the boxed column headers are automatically transferred to their corresponding fields on the **Lines** FastTab, for each line in the document.
1. For each of the lines, select the relevant values in **Translate to Type** and **Translate to No.** to let Document Capture know how to translate the vendor's account references into account types and numbers that can be used internally.

   > [!IMPORTANT]
   > To change the order in which columns are presented in the **Lines** section, select **Template** > **Template Card** on the action bar and, in the **Fields** section, use the **Move Up** or **Move Down** actions to shift the position of the selected field. Don't attempt to achieve the same result by moving line columns via **Settings** > **Personalize** on the **Document Card**, as this breaks the link between the column in focus and the related value highlighted in the document viewer. Personalizing non-template field columns, such as **Translate to No.**, also breaks this link.

All document lines have now been captured, and line recognition has been automatically activated for the assigned template.

> [!TIP]
> You can change the identified field values and captions. To learn more, see [Training Document Capture to locate values](@DC-110#training-document-capture-to-locate-values).

## To configure line recognition

When you've activated line recognition for a document template as described above, you can configure it in various ways. To do this:

1. In the document journal, select the document whose template you want to configure in terms of line recognition.
1. On the action bar, click **Template** > **Template Card** to open the template card.
1. On the **General** FastTab, **Recognize Lines** has been enabled automatically if you've manually [captured line fields following the guide above](#to-capture-line-fields). If you haven't captured line fields yet, enable **Recognize Lines** to activate line recognition. This displays the following configuration fields:
   * **Vendor uses your Item Nos.** - enable this if you use the same item numbers as the vendor.
   * **First Table Line Has Captions** - enable this if the top line in the document line table functions as a header with captions for each column, which is typically the case. This is enabled by default once you [capture line fields manually](#to-capture-line-fields).
   * **Check Item Prices** - if enabled, Document Capture automatically checks the item prices of all recognized document lines against the vendor's calculated item prices.
   > [!NOTE]
   > If a recognized price differs from the vendor item price, a warning is displayed in the comments section of the document journal. Prices are only checked if no related purchase orders exist. The feature takes into account whether any special vendor purchase prices or discounts apply to the checked item numbers.

   >[!TIP]
   >PDFs are complex, multi-layered documents. If you encounter odd values when processing a PDF in Document Capture, open the PDF using a modern browser, MS Paint, or equivalent. You can then either print it to PDF or save it as a PDF once again, which should allow Document Capture to process it correctly. Note that this only applies to on-premises setups, as the Cloud OCR is more precise.

## Prioritization of filters

For the **Description** and **No.** line fields, filters with operators such as .. and | (as well as filters without any operators) take precedence over filters with wildcards. For example, if the following filters are configured, filter b takes precedence over filter a because it doesn’t contain wildcards.

a. \*FREIGHT\* -> G/L Account 1000
b. EXPRESS FREIGHT|NORMAL FREIGHT -> G/L Account 2000

The full order of priorities is, with 1 being the highest and 15 the lowest:

1.	Item field GTIN
2.	Number exact match
3.	Number exact match with operators (e.g.: 'AiP&12' or 'TM>Y')
4.	Number operators (e.g.: 100..109 or Freight|Delivery)
5.	Number operator using * (e.g.: 10* or *freight)
6.	Item Reference table
7.	Item Vendor table
8.	Item table field Vendor Item No.
9.	Item No. field from Item table (template setting "Use Vendor/Customer Item Nos.“)
10.	Number * translation only
11.	Description exact match
12.	Description exact match with operators (e.g.: 'Anderson & co.')
13.	Description filters (e.g.: Apple iMac|Apple iPhone)
14.	Description filters using * (e.g.: Apple*)
15.	Description * translation only 

> [!NOTE]
> Although it’s possible to encase terms that include most operators reserved for filtering in Microsoft Dynamics 365 Business Central with single quotation marks (i.e.:  ( ) | < > = .. ? &), this doesn’t apply to @ and *.

For more information, see [Filter criteria and operators](https://learn.microsoft.com/en-us/dynamics365/business-central/ui-enter-criteria-filters#FilterCriteria) (Microsoft article).

## Related information

[Working with paper and PDF documents](@DC-71)  
[Capturing header fields in a document](@DC-110)  