---
title: Using field translations in Document Capture
date: 30-09-2025
description: How to use the field translation functionality in Document Capture.
id: DC-460
lang: en
---

# Using field translations

Field translations help you with values that would be either difficult to capture or require manual work. This is one of the simplest and yet most flexible features in Continia Document Capture, so learning how to use it can save plenty of time and hassle.

The field translations feature converts values captured for the field in which it's configured into different values – or into no values at all, removing the captured value either fully or partially. In fact, removing parts of captured values is such a common scenario that fields such as **Amount Incl. VAT** are configured by default to remove certain currency symbols and special characters.

<a href="/images/DC/DocumentsAndTemplates/Field translations A.png" target="_blank">
</images/DC/DocumentsAndTemplates/Field translations A.png" alt="Field translations">
</a>

## To use field translations

1. Search ({{search}}) for and select **Document Categories**.
2. Select the relevant document category code – for example, **PURCHASE** – to open the document journal.
3. In the list of documents, select the one you want to work with.
4. On the **Document Header** or **Lines** FastTab, select the three dots by the field to which you want to apply field translations.
5. On the **Field Translations** FastTab, enter the value you want to translate under the **Translate From** column.
6. Under the **Translate to** column, enter the value you want as a result. Note that you can leave this field blank, resulting in the removal of the value entered under **Translate From**.
7. If the field translation should only occur when the case of the captured values is the same as the case entered under **Translate From**, select the **Case-sensitive** box. E.g.: Hazel, but not hazel or HAZEL.

>[!TIP]
>If the data type of a template field is set to **Lookup**, the **Translate To** field on the **Template Field Card** also works as a lookup field. This allows you to select values dynamically, rather than entering them manually. To enable this functionality, configure lookup values for both the source table and source field of the template field.

## To use a wildcard in field translations

Much like when [using rules](@DC-245), it's possible to use the asterisk ( * ) as a wildcard in field translations. This allows you to translate the data before and/or after a certain number, term, or special character – even if this data varies or is unknown to you.

For example, if only the first six digits of the invoice number 555002-20250723 are relevant to you, use the wildcard preceded by a hyphen (i.e.: -*) to translate the unwanted data into an empty value. In this example, the result of the translation would be 555002.

<a href="/images/DC/DocumentsAndTemplates/Field translations B.png" target="_blank">
</images/DC/DocumentsAndTemplates/Field translations B.png" alt="Wildcards in field translations">
</a>
