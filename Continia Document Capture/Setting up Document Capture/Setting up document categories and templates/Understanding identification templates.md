---
title: Understanding identification templates in Document Capture
date: 27-06-2025
description: An introduction to identification templates and how to customize them.
id: DC-471
lang: en
---

# Understanding identification templates

For illustrative purposes, the following explanation of identification templates focuses on purchase documents and vendors, although the processes described below may as well involve other types of business documents and document sources.

Identification templates are used for identifying the source of imported documents, in this case the vendor. When an identification template identifies a VAT registration number for an incoming purchase document, Continia Document Capture searches through the vendor table for a vendor with a corresponding VAT registration number and, if successful, then applies the identified vendor and its associated default template to the document. For a more detailed account of how this works, along with information on how to customize certain parts of the identification template, see the sections below.

> [!NOTE]
> The use of identification templates is one of three steps when identifying the source of a document. To learn more, see [Finding the document source and template](@DC-109).

## The underlying logic

Each document category in Document Capture has one identification template. When you import a document into Document Capture, the identification template attempts to link a matching record in the source table to this document. For the **PURCHASE** document category, it does so by capturing the document's VAT number and searching through the vendor table for a vendor with a matching VAT number.

The identification template consists of a single field, **VAT Registration No.**, which uses multiple different captions and rules to identify the correct VAT registration number of each incoming document. The captions and the rules can both be customized, as described below under [To modify search captions](#to-modify-search-captions) and [To modify search rules](#to-modify-search-rules), and together they form the basis of the identification process: When the identification template, based on your selection of captions, recognizes a caption in an imported document, it searches for a corresponding value to capture to the right of or below that caption. If it finds one, it then validates that value against the selected rules to ensure that the value's format is correct – in other words, it confirms that the captured value is indeed a VAT number.

Once a VAT number has been captured, Document Capture runs the codeunit **CDC Purch Doc. - Identificat.** to identify a vendor with a matching VAT number in the vendor table. You can view the codeunit on the identification template card, on the **Codeunits** FastTab, under **After Capture**.

>[!TIP]
>To see the list of templates associated with a vendor, use the **Document Templates** action from the list of vendors or the **Vendor Card**. To reveal this action, which is hidden by default:
>
>1. Search ({{search}}) for and select **Vendors**.
>2. On the list of vendors, click **Settings** ({{settings}}) > **Personalize** in the top-right corner.
>3. On the action bar, expand the action group **Related**.
>4. Hover the cursor over **Vendors > Document Templates**, then click **Show** to make the action available.

## To modify search captions

It's possible to determine exactly what captions Document Capture should search for in order to identify VAT registration numbers in incoming documents. To do this:

1. Search ({{search}}) for and select **Document Categories**.
1. Open the relevant document category. For example, to open the purchase document category, click the **PURCHASE** line (not the **PURCHASE** code itself), and then click **Edit** on the action bar.
1. On the **Templates** FastTab, in the list of templates, locate the **PURCHASE-ID** template. Click the {{vertical-dots}} icon and then **Edit** to open the template card.
1. On the **Fields** FastTab, in the **Field Name** column, click **VAT Registration No.** to open the template field card.
1. On the action bar, click **Captions** to open the **Edit** page.
1. Edit the list of captions as needed, for example using the **New** and **Delete** buttons on the action bar.
1. Click **Close** when you're done.

Document Capture will then search every single incoming document for the captions included in this list in order to identify each document's VAT registration number, which can be used to identify the document source.

## To modify search rules

You can also determine the exact rules to be used by Document Capture when identifying VAT registration numbers in incoming documents. To do this:

1. Search ({{search}}) for and select **Document Categories**.
1. Open the relevant document category. For example, to open the purchase document category, click the **PURCHASE** line (not the **PURCHASE** code itself), and then click **Edit** on the action bar.
1. On the **Templates** FastTab, in the list of templates, locate the **PURCHASE-ID** template. Click the {{vertical-dots}} icon and then **Edit** to open the template card.
1. On the **Fields** FastTab, in the **Field Name** column, click **VAT Registration No.** to open the template field card.
1. On the action bar, click **Rules** to open the **Edit** page.
1. Edit the list of rules as needed, for example using the **New** and **Delete** buttons on the action bar.
1. Click **Close** when you're done.

Document Capture will then search every single incoming document using the rules included in this list in order to identify each document's VAT registration number. Whenever at least one rule matches the format of a captured value, that value is accepted as a valid VAT number. As mentioned above, this VAT number can then be used by Document Capture to identify the document source.
