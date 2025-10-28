---
title: Using rules in Document Capture
date: 23-07-2025
description: How to use rules in template fields in Document Capture
id: DC-245
lang: en
---

# Using rules

This article describes how to use template field rules in Continia Document Capture, either set up with regular expressions or standard operators.

## Why use rules in Document Capture

Using rules in Document Capture allows you to control which values are valid in a template field. During the field recognition process, these rules ensure that only values that match the rule specified for each field are recognized. Therefore, automations are only triggered if your values are fully correct. This is particularly useful if you have vendors who tend to change the layout or content of their documents, making it easier to spot false positives.

Additionally, rules set up on required fields guarantee that documents are only registered if these fields are correctly recognized or filled out.


## Rules, regular expressions, and operators

Template fields with the data type set to **Number** only accept standard operators (such as >, <, and =), and template fields with the data type **Text** support regular expressions – also known as regex. Regular expressions are basically a sequence of digits, letters, and special characters that specify a match pattern. For example, the regular expression `\d{4}-\d{2}-\d{2}` corresponds to the following:

* **\d** - any digit from 0 to 9.
* **{4}** - exactly four of the preceding element, so **\d{4}** matches exactly four digits.
* **-** - a hyphen.
* **\d{2}** - exactly two digits.
* **-** - another hyphen.
* **\d{2}** - exactly two digits.

Therefore, the regular expression shown above can be used to match dates in the format yyyy-mm-dd.

For more examples of valid expressions, see [Using rules in header fields](#using-rules-in-header-fields) and [Using rules in line fields](#using-rules-in-line-fields) below.

>[!IMPORTANT]
>Rules are case insensitive.

## Using rules in header fields

When using rules on header fields, you can filter the recognized value – that is, the value is only recognized if its data complies with the rule.

To add a rule to a header field:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the **PURCHASE** code to open the document journal.
1. In the list of documents, select the document whose template field you want to set up a rule for.
1. In the **Document Header** section, click the three dots by the header field you want to set up a rule for.
1. On the action bar, click **Rules**. Alternatively, you can edit the **Rule** field on the **General** FastTab.

Below are some examples of regular expressions that can be used in header fields.

| **Expression**       | **Description**                                              | **Example**s                               | **Result**s                                                 |
| -------------------- | ------------------------------------------------------------ | ------------------------------------------ | ----------------------------------------------------------- |
| P[0-9]{8}            | The field value must start with 'P', followed by 8 digits ranging from 0 to 9. | P12345678<br/>P12345<br/>P-12345678        | P12345678<br/>[not recognized]<br/>[not recognized]         |
| [FR]-[0-9]{3,}       | The field value must start with either 'F' or 'R' and '-', followed by at least 3 digits ranging from 0 to 9. | R-123<br/>F-12345<br/>F-1234567<br/>O-7611 | R-123<br/>F-12345<br/>F-1234567<br/>[not recognized]        |
| [FR]-[0-9]{3,5}      | The field value must start with either 'F' or 'R' and '-', followed by 3 to 5 digits ranging from 0 to 9. | R-123<br/>F-12345<br/>F-1234567<br/>O-7611 | R-123<br/>F-12345<br/>[not recognized]<br/>[not recognized] |
| I[0-9]{8}            | The field value must start with 'I', followed by 8 digits ranging from 0 to 9. | I12345678<br/>I12345<br/>I-12345678        | I12345678<br/>[not recognized]<br/>[not recognized]         |
| INV[0-9]{5}X[0-1]{1} | The field value must start with 'INV', followed by 5 digits ranging from 0 to 9, then 'X', followed by 1 digit ranging from 0 to 1. | INV12345X1<br/>INV12345X2<br/>INV12345H1   | INV12345X1<br/>[not recognized]<br/>[not recognized]        |
| <>ABC&<>DEF          | The field value must be different from 'ABC' and 'DEF'.      | ABC<br/>DEF<br/>GHI                        | [not recognized]<br/>[not recognized]<br/>GHI               |
| Invoice\|Credit Memo | The field value must be either 'Invoice' or 'Credit Memo'.   | Invoice<br/>Credit Memo<br/>Credit Note    | Invoice<br/>Credit Memo<br/>[not recognized]                |
| \*AY\*               | The field value must be either an 8- or 13-digit number.     | 12345678<br/>1234567891011<br/>12345       | 12345678<br/>1234567891011<br/>[not recognized]             |
|                      \\d{8}\|\\d{13}| The field value must be either an 8- or 13-digit number. | 12345678<br/>1234567891011<br/>12345 | 12345678<br/>1234567891011<br/>[not recognized] |
| [a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,} | The field value must be a valid email address. | info@continia.com<br/>some_example@domain.co<br/>contact.us@domain.green<br/>sales@company | info@continia.com<br/>some_example@domain.co<br/>contact.us@domain.green<br/>[not recognized] |

## Using rules in line fields

When using rules in line fields, you can filter which values should be kept and which should remain blank. When combined with the **Required** checkbox, this enables you to include only lines with certain content – or leave out lines that otherwise would conflict with the line structure in the document.

To add a rule to a line field:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the **PURCHASE** code to open the document journal.
1. In the list of documents, select the document whose template field you want to set up a rule for.
1. In the **Lines** section, click the three dots by the value of the line field you want to set up a rule for.
1. On the action bar, click **Rules**. Alternatively, you can edit the **Rule** field on the **General** FastTab.

Below are some examples of regular expressions that can be used in line fields, as long as these fields are marked as required or line recognition is using AI. Otherwise, the field value is skipped – but the rest of the line is still recognized.<br>

| **Expression**       | **Description** |
| -------------------- | --------------- |
| Invoice              | Recognize lines where the field value is 'Invoice'. |
| Invoice\|Credit Memo | Recognize lines where the field value is either 'Invoice' or 'Credit Memo'. |
| <>Subtotal           | Skip lines where the field value is 'Subtotal'. |
| <>Freight*           | Skip lines where the field value begins with the word 'Freight'. |
| <>\*A\*&*E\*            | Skip lines where the field value contains the letter 'A', and only recognize lines where the letter 'E' is present. |
| POS[0-9]{3} | Recognize lines where the field value starts with 'POS' followed by 3 digits. |
| [a-z ]{10,20}panel | Recognize lines where the field value has 10-20 characters, contains letters and spaces, and ends with 'panel' – though 'panel' doesn't count toward the character limit. |

## Using automatically generated rules

Instead of manually entering rules for each template field that requires them, it's possible to let Document Capture generate rules based on the captured values. If the format of a captured value for a field changes, Document Capture generates a new rule to match the latest format.

To enable rule generation:

1. Search ({{search}}) for and select **Document Categories**.
1. Click the **PURCHASE** code to open the document journal.
1. In the list of documents, select the document whose template field you want to set up a rule for.
1. In the **Document Header** section, click the three dots by the header field you want to set up a rule for. Alternatively, in the **Lines** section, click the three dots by the value of the line field you want to set up a rule for.
1. On the **General** FastTab, turn on the **Enable Rule Generation** setting.

>[!NOTE]
>It’s only possible to enable automatic rule generation for template fields with the data type set to **Date** or **Text**.

>[!TIP]
>To capture only the part of the value that matches a certain rule, such as digits but no letters or special characters, use the **Capture Only Match** feature. For more information, see [To capture only the parts of values that match a specific rule](@DC-191#to-capture-only-the-parts-of-values-that-match-a-specific-rule).

## Resources

The following resources are useful when building or tweaking regular expressions:

* [Microsoft Copilot](https://copilot.cloud.microsoft/) - or an equivalent generative artificial intelligence chatbot. These tools are good at creating and testing custom rules, but make sure to double check their output.
* [RegExr](https://regexr.com/) - a tool to help you build and test regular expressions.
* [Regex101](https://regex101.com/) - another tool to help you build and test regular expressions.