---
title: Setting up Identification Fields 
date: 19-08-2022
description:  
id: DC-81
lang: en
---

# Setting up Identification Fields

For illustrative purposes, the following explanation of identification fields will focus on vendors, but note that identification fields are always configured according to the source table that’s set up in the relevant document category.

Identification fields are used when identifying the source of an imported document, in this case the vendor. In the vendor table, you basically select one or more fields that can help Document Capture to identify the vendor (for example, name, address, phone number, or VAT registration number). When Document Capture attempts to determine what vendor should be associated with a certain document, it runs through all vendors in the vendor table to search for the values of the selected identification fields (name, address, etc.) within the document. The document is then assigned the vendor whose field values best match the values identified in the document.

When identifying the vendor of a document, there may be multiple vendors that fully or to some extent match the vendor in the document. In order to determine which is the correct one, Document Capture assigns each vendor a confidence score that ultimately determines which vendor is assigned to the document.

> [!NOTE]
> The use of identification fields is one of three steps when identifying the source of a document. To learn more, see [Finding the Document Source and Template](/Continia Document Capture/Business functionality/Documents and templates/Finding the document source and template.md).

## Configuring identification fields for purchase documents

You can configure identification fields for all document categories. To do this, follow these steps:

1. Search ({{search}}) for and select **Document Categories**.
1. Open the relevant document category. For example, to open the purchase document category, select the **PURCHASE** line (not the **PURCHASE** code itself, as this will open the document journal), and then choose **Edit** on the action bar.
1. On the **Document Category** page, on the action bar, click **Identification Fields**.
1. The **Identification Fields** page opens, displaying the current selection of identification fields. To add a new field, select **New** on the action bar, and then under **Field No.**, select the three dots on the new line that's added.
1. This will open the **Fields Lookup** page, which displays all fields in the vendor table. Add the field you want by selecting the relevant number in the **No.** column. 
1. The **Fields Lookup** page is closed, and you're returned to the **Identification Fields** page, where the selected identification field has now been added.
1. On the **Identification Fields** page, you can also delete existing identification fields by selecting the relevant field(s) and then choosing **Delete** on the action bar. Note that on a computer, you can select multiple entries by pressing Ctrl+Click.
1. The **Identification Fields** page also allows you to edit any existing identification fields: Choose the **Field No.** field for the identification field you want to edit, and then select the three dots to open the **Fields Lookup** page. Here, add the field you want by selecting the relevant number in the **No.** column.
1. For any of the selected identification fields, you can edit the assigned rating by entering a number in the **Rating** column. The higher the number, the more weight the field is assigned when Document Capture attempts to identify the source of an imported document. To learn more, see [Calculating confidence scores](/continia-document-capture/setting-up-document-capture/setting-up-document-categories-and-templates/setting-up-identification-fields#calculating-confidence-scores).

> [!NOTE]
> When you create a new identification field or edit an existing one, you can't choose an identification field that's already included in the current selection, i.e. the list displayed on the **Identification Fields** page.

## Calculating confidence scores

For each vendor, Document Capture calculates a confidence score by searching for each field configured as an identification field and then multiplying the number of characters of the identified field value with the configured rating. Consider the following:

| Field | Value | Rating | Confidence score |
| --- | --- | --- | --- |
| **Name** | Microsoft | 1 | 9 (1 × 9 characters) |
| **Address** | One Microsoft Road | 1 | 18 (1 × 18 characters) |
| **Bank Account No.** | 1212-1928381887231 | 2 | 36 (2 × 18 characters) |
| *Total score* | | | 63 |

The reason why some fields may be assigned higher ratings is that some values are more likely to be unique than others. For example, the address of a company may be the same as that of another company, but a company’s bank account number is unique, as it would only ever belong to one company.

Document Capture doesn’t always find all vendor identification fields in imported documents. In some documents, it may identify several vendors that could all potentially be assigned as the correct one. Consider the following scenario, which involves one document but two vendors that could both match the document vendor:

Vendor 1:

| Field | Value in document | Value for vendor 1 | Rating | Confidence score |
| --- | --- | --- | --- | --- |
| **Name** | Microsoft | Microsoft | 1 | 9 |
| **Address** | One Microsoft Road | One Microsoft Road | 1 | 18 |
| **Bank Account No.** | 1212-1928381887231 | 1212-1928381887231 | 2 | 36 |
| *Total score* | | | | 63 |

Vendor 2:

| Field | Value in document | Value for vendor 2 | Rating | Confidence score |
| --- | --- | --- | --- | --- |
| **Name** | Microsoft | Microsoft | 1 | 9 |
| **Address** | One Microsoft Road | One Microsoft Road | 1 | 18 |
| **Bank Account No.** | 1212-1928381887231 | 0000-0000000000000 | 2 | 0 |
| *Total score* | | | | 27 |

In this example, vendor 1 has the highest confidence score and will therefore be assigned to the document.

> [!NOTE]
> To prevent unreliable results, the minimum confidence score that must be obtained in order for a vendor to be assigned to a document is 15. For example, if the only match between a document and a vendor is the vendor’s city, it’s uncertain that the right vendor has been identified, seeing that multiple other vendors may very well be located in the same city.

## Related information

[Finding the Document Source and Template](@DC-109)  