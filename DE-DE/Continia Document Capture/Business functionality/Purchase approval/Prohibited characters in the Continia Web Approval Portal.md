---
title: Unzulässige Zeichen im Continia Web Approval Portal
date: 01-11-2024
description: Eine Liste der Zeichen, die im Continia Web Approval Portal nicht zulässig sind.
id: DC-243
lang: de
---

# Unzulässige Zeichen im Continia Web Approval Portal

In diesem Artikel wird erläutert, warum bestimmte Zeichen im Continia Web Approval Portal nicht verwendet werden können, und sie werden entsprechend aufgelistet.

Im Gegensatz zu Continia Document Capture, das in Microsoft Dynamics 365 Business Central integriert ist, ist das Web Approval Portal eine separate Ressource. Die Kommunikation mit Business Central erfolgt über XML. Daher darf der vom Web Approval Portal verarbeitete Inhalt keine Zeichen enthalten, die die Verarbeitung von Dokumenten beeinträchtigen.

> [!NOTE]
> Beispiele für Felder, in denen diese Zeichen nicht verwendet werden können, sind Dimensionscodes, Genehmigernamen und Kreditornamen.

## Steuerzeichen

Steuerzeichen, auch nicht druckbare Zeichen (NPCs) genannt, sind Zeichen, die Effekte darstellen und keine grafischen Zeichen wie Buchstaben, Symbole usw. Beispiele für Steuerzeichen sind Backspace und Escape, die im Unicode-Standard durch die Codes U+0008 bzw. U+001B dargestellt werden.

Abgesehen von den unten aufgeführten Ausnahmen sind in XML sämtliche Steuerzeichen verboten.

<br>

| Code (Unicode-Standard) | Beschreibung    |
| ------------------------------------------ | --------------- |
| U+000D                                     | Carriage Return |
| U+000A                                     | Line Feed       |
| U+0009                                     | Tabulator       |

## Sonderzeichen

Einige Sonderzeichen sind in XML verboten, da sie in der Struktur eine Funktion erfüllen, beispielsweise den Anfang und das Ende eines Tags definieren. Daher kann die Verwendung dieser Zeichen zu Fehlern führen.

Im Gegensatz zu Steuerzeichen sind die meisten Sonderzeichen in XML jedoch zulässig. Die Ausnahmen von dieser Regel sind unten aufgeführt. <br>

| Code (Unicode-Standard) | Beschreibung        | Glyphe                     |
| ------------------------------------------ | ------------------- | -------------------------- |
| U+003E                                     | Größer-als-Zeichen  | >                          |
| U+003C                                     | Kleiner-als-Zeichen | < |
| U+0026                                     | Ampersand           | &      |
| U+0027                                     | Apostroph           | '                          |
| U+0022                                     | Anführungszeichen   | "                          |

> [!HINWEIS]
> Die oben aufgeführten Sonderzeichen können verwendet werden, wenn sie mit einem Escape-Zeichen versehen sind, was sich jedoch in Dokumenten oft nicht anbietet.

## Informationen zum Thema

[Continia Web Approval Portal](@DC-165)  
[Benutzer für das Web Approval Portal konfigurieren](@DC-129)