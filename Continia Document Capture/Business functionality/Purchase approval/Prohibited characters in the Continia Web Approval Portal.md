---
title: Prohibited characters in the Continia Web Approval Portal
date: 01-11-2024
description: A list of the characters that aren't allowed in the Continia Web Approval Portal.
id: DC-243
lang: en
---

# Prohibited Characters in the Web Approval Portal

This article explains why certain characters can't be used in the Continia Web Approval Portal, and lists them accordingly.

Unlike Continia Document Capture, which is built inside Microsoft Dynamics 365 Business Central, the Web Approval Portal is a separate resource. It communicates with Business Central via XML, therefore the content handled by the Web Approval Portal mustn't include characters that interfere in the processing of documents.

>[!NOTE]
>Examples of fields where these characters can't be used include dimension codes, approver names, and vendor names.

## Control characters

Control characters, also known as non-printable characters (NPCs), are characters that represent effects – rather than graphic characters such as letters, symbols, etc. Examples of control characters include backspace and escape, which are respectively represented by the codes U+0008 and U+001B in the Unicode standard.

Apart from the exceptions listed below, all control characters are prohibited in XML.

<br>

| Code (Unicode standard) | Description     |
| ----------------------- | --------------- |
| U+000D                  | Carriage return |
| U+000A                  | Line feed       |
| U+0009                  | Horizontal tab  |

## Special characters

Some special characters are prohibited in XML because they serve a function in its structure, such as defining the beginning and the end of a tag. Therefore, using these characters may result in errors.

Contrary to control characters, though, most special characters are allowed in XML. The exceptions to this rule are listed below.
<br>

| Code (Unicode standard) | Description       | Glyph |
| ----------------------- | ----------------- | ----- |
| U+003E                  | Greater-than sign | >     |
| U+003C                  | Less-than sign    | <     |
| U+0026                  | Ampersand         | &     |
| U+0027                  | Apostrophe        | '     |
| U+0022                  | Quotation mark    | "     |

>[!NOTE]
>The special characters listed above can be used if escaped, but this is often impractical in documents.

## Related information

[Continia Web Approval Portal](@DC-165)  
[Configuring Users for the Web Approval Portal](@DC-129)