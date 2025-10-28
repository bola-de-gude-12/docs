---
title: Regeln in Document Capture verwenden
date: 23-07-2025
description: So verwenden Sie Regeln in Vorlagenfeldern in Document Capture
id: DC-245
lang: de
---

# Regeln verwenden

In diesem Artikel wird beschrieben, wie Sie in Continia Document Capture Vorlagenfeldregeln verwenden, die entweder mit regulären Ausdrücken oder Standardoperatoren eingerichtet werden.

## Wozu können Regeln in Document Capture verwendet werden?

Mit Regeln können Sie in Document Capture festlegen, welche Werte in einem Vorlagenfeld gültig sind. Diese Regeln stellen während der Felderkennung sicher, dass nur Werte erkannt werden, die der für das jeweilige Feld angegebenen Regel entsprechen. Daher werden Automatisierungen nur ausgelöst, wenn Ihre Werte vollständig korrekt sind. Dies bietet sich besonders bei Kreditoren an, die das Layout oder den Inhalt ihrer Belege häufiger ändern, da dadurch Fehlalarme leichter erkannt werden können.

Darüber hinaus garantieren Regeln, die für Pflichtfelder eingerichtet sind, dass Belege nur dann registriert werden, wenn diese Felder korrekt erkannt oder ausgefüllt sind.

## Regeln, reguläre Ausdrücke und Operatoren

Vorlagenfelder mit dem Datentyp **Zahl** akzeptieren nur Standardoperatoren (wie >, < und =), und Vorlagenfelder mit dem Datentyp **Text** unterstützen reguläre Ausdrücke – auch als Regex bekannt. Reguläre Ausdrücke sind grundsätzlich eine Folge von Ziffern, Buchstaben und Sonderzeichen, die ein Übereinstimmungsmuster angeben. Beispielsweise entspricht der reguläre Ausdruck `\d{4}-\d{2}-\d{2}` Folgendem:

- **\d** – eine beliebige Ziffer von 0 bis 9.
- **{4}** – Anzahl des vorhergehenden Elements, also entspricht **\d{4}** genau vier Ziffern.
- **-** – ein Bindestrich.
- **\d{2}** – zwei Ziffern.
- **-** – ein weiterer Bindestrich.
- **\d{2}** – zwei Ziffern.

Daher kann der oben gezeigte reguläre Ausdruck verwendet werden, um Datumsangaben im Format JJJJ-MM-TT abzugleichen.

Weitere Beispiele für gültige Ausdrücke finden Sie weiter unten unter [Regeln in Kopffeldern verwenden](#regeln-in-kopffeldern-verwenden) und [Regeln in Zeilenfeldern verwenden](#regeln-in-zeilenfeldern-verwenden).

> [!IMPORTANT]
> Bei Regeln wird nicht zwischen Groß- und Kleinschreibung unterschieden.

## Regeln in Kopffeldern verwenden

Wenn Sie Regeln für Kopffelder verwenden, können Sie den erkannten Wert filtern. Das heißt, der Wert wird nur erkannt, wenn seine Daten der Regel entsprechen.

So fügen Sie einem Kopfeld eine Regel hinzu:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, in dessen Vorlagenfeld Sie eine Regel einrichten möchten.
4. Klicken Sie im Abschnitt **Belegkopf** auf die drei Punkte neben dem Kopffeld, für das Sie eine Regel einrichten möchten.
5. Klicken Sie in der Aktionsleiste auf **Regeln**. Alternativ können Sie das Feld **Regel** auf dem Inforegister **Allgemein** bearbeiten.

Nachfolgend finden Sie einige Beispiele für reguläre Ausdrücke, die in Kopffeldern verwendet werden können.

| **Ausdruck**                                                                                                                                                                                                                                                                                  | **Beschreibung**                                                                                                                               | **Beispiele**                                                                                                                                                                                              | **Ergebnisse**                                                                                                                                                                                                                                      |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| P[0-9]{8}                                                                                                                                                                                                                                 | Der Feldwert muss mit „P“ beginnen, gefolgt von 8 Ziffern im Bereich von 0 bis 9.                                              | P12345678<br/>P12345<br/>P-12345678                                                                                                                                                                        | P12345678<br/>[nicht erkannt]<br/>[nicht erkannt]                                                                                           |
| [FR]-[0-9]{3,}                                                                                                                                                                        | Der Feldwert muss entweder mit „F“ oder „R“ und „-“ beginnen, gefolgt von mindestens 3 Ziffern im Bereich von 0 bis 9.         | R-123<br/>F-12345<br/>F-1234567<br/>O-7611                                                                                                                                                                 | R-123<br/>F-12345<br/>F-1234567<br/>[nicht erkannt]                                                                                                                                             |
| [FR]-[0-9]{3,5}                                                                                                                                                                       | Der Feldwert muss entweder mit „F“ oder „R“ und „-“ beginnen, gefolgt von 3 bis 5 Ziffern im Bereich von 0 bis 9.              | R-123<br/>F-12345<br/>F-1234567<br/>O-7611                                                                                                                                                                 | R-123<br/>F-12345<br/>[nicht erkannt]<br/>[nicht erkannt]                                                                                   |
| I[0-9]{8}                                                                                                                                                                                                                                 | Der Feldwert muss mit „I“ beginnen, gefolgt von 8 Ziffern im Bereich von 0 bis 9.                                              | I12345678<br/>I12345<br/>I-12345678                                                                                                                                                                        | I12345678<br/>[nicht erkannt]<br/>[nicht erkannt]                                                                                           |
| INV[0-9]{5}X[0-1]{1}                                                                                                                                                                  | Der Feldwert muss mit „INV“ beginnen, gefolgt von 5 Ziffern zwischen 0 und 9, dann „X“, gefolgt von 1 Ziffer zwischen 0 und 1. | INV12345X1<br/>INV12345X2<br/>INV12345H1                                                                                                                                                                   | INV12345X1<br/>[nicht erkannt]<br/>[nicht erkannt]                                                                                          |
| <>ABC&<>DEF                                                                                                                                                                                                             | Der Feldwert muss sich von „ABC“ und „DEF“ unterscheiden.                                                                      | ABC<br/>DEF<br/>GHI                                                                                                                                                                                        | [nicht erkannt]<br/>[nicht erkannt]<br/>GHI                                                                                                 |
| Rechnung\\|Gutschrift                                                                                                                                                                                                                                                                        | Der Feldwert muss entweder „Rechnung“ oder „Gutschrift“ sein.                                                                  | Rechnung<br/>Gutschrift<br/>Erstattung                                                                                                                                                                     | Rechnung<br/>Gutschrift<br/>[nicht erkannt]                                                                                                                                                     |
| \*AY\*                                                                                                                                                                                                                                                                                        | Der Feldwert muss entweder eine 8- oder 13-stellige Zahl sein.                                                                 | 12345678<br/>1234567891011<br/>12345                                                                                                                                                                       | 12345678<br/>1234567891011<br/>[nicht erkannt]                                                                                                                                                  |
| \\d{8}\\|\\d{13}                                                                                                                                                                                                                                                                           | Der Feldwert muss entweder eine 8- oder 13-stellige Zahl sein.                                                                 | 12345678<br/>1234567891011<br/>12345                                                                                                                                                                       | 12345678<br/>1234567891011<br/>[nicht erkannt]                                                                                                                                                  |
| [a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,} | Der Feldwert muss eine gültige E-Mail-Adresse sein.                                                                            | info@continia.com<br/>beispiel@domain.co<br/>contact.us@domain.green<br/>sales@company | info@continia.com<br/>beispiel@domain.co<br/>contact.us@domain.green<br/>[nicht erkannt] |

## Regeln in Zeilenfeldern verwenden

Bei der Verwendung von Regeln in Zeilenfeldern können Sie filtern, welche Werte beibehalten werden und welche leer bleiben sollen. In Kombination mit dem Kontrollkästchen **Erforderlich** können Sie so nur Zeilen mit bestimmten Inhalten einfügen – oder Zeilen weglassen, die sonst mit der Zeilenstruktur im Beleg in Konflikt geraten würden.

So fügen Sie einem Zeilenfeld eine Regel hinzu:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, in dessen Vorlagenfeld Sie eine Regel einrichten möchten.
4. Klicken Sie im Abschnitt **Zeilen** auf die drei Punkte neben dem Wert des Zeilenfeldes, für das Sie eine Regel einrichten möchten.
5. Klicken Sie in der Aktionsleiste auf **Regeln**. Alternativ können Sie das Feld **Regel** auf dem Inforegister **Allgemein** bearbeiten.

Nachfolgend finden Sie einige Beispiele für reguläre Ausdrücke, die in Zeilenfeldern verwendet werden können, sofern diese Felder als erforderlich markiert sind oder die Zeilenerkennung KI verwendet. Andernfalls wird der Feldwert übersprungen; der Rest der Zeile wird jedoch weiterhin erkannt.<br>

| **Ausdruck**                                                           | **Beschreibung**                                                                                                                                                                                   |
| ---------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Rechnung                                                               | Zeilen werden erkannt, bei denen der Feldwert „Rechnung“ ist.                                                                                                                      |
| Rechnung\\|Gutschrift                                                 | Zeilen werden erkannt, bei denen der Feldwert entweder „Rechnung“ oder „Gutschrift“ ist.                                                                                           |
| <>Zwischensumme                               | Zeilen werden übersprungen, bei denen der Feldwert „Zwischensumme“ ist.                                                                                                            |
| <>Fracht\*                                    | Zeilen werden übersprungen, in denen der Feldwert mit dem Wort „Fracht“ beginnt.                                                                                                   |
| <>\*A\*&\*E\*             | Zeilen werden übersprungen, in denen der Feldwert den Buchstaben „A“ enthält, und es werden nur Zeilen erkannt, in denen der Buchstabe „E“ vorhanden ist.                          |
| POS[0-9]{3}        | Zeilen werden erkannt, bei denen der Feldwert mit „POS“ beginnt, gefolgt von 3 Ziffern.                                                                                            |
| [a-z ]{10,20}panel | Zeilen werden erkannt, bei denen der Feldwert 10–20 Zeichen umfasst, Buchstaben und Leerzeichen enthält und mit „panel“ endet – wobei „panel“ nicht zur Zeichenbeschränkung zählt. |

## Verwenden automatisch generierter Regeln

Anstatt Regeln für jedes erforderliche Vorlagenfeld manuell einzugeben, können Sie Document Capture Regeln basierend auf den erfassten Werten generieren lassen. Wenn sich das Format eines erfassten Werts für ein Feld ändert, generiert Document Capture eine neue Regel, die dem neuesten Format entspricht.

So aktivieren Sie die Erstellung von Regeln:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, in dessen Vorlagenfeld Sie eine Regel einrichten möchten.
4. Klicken Sie im Abschnitt **Belegkopf** auf die drei Punkte neben dem Kopffeld, für das Sie eine Regel einrichten möchten. Alternativ können Sie im Abschnitt **Zeilen** auf die drei Punkte neben dem Wert des Zeilenfeldes klicken, für das Sie eine Regel einrichten möchten.
5. Aktivieren Sie auf dem Inforegister **Allgemein** die Einstellung **Regelerzeugung aktivieren**.

> [!NOTE]
> Die automatische Regelgenerierung kann nur für Vorlagenfelder aktiviert werden, deren Datentyp auf **Datum** oder **Text** eingestellt ist.

> [!TIP]
> Um nur den Teil des Werts zu erfassen, der einer bestimmten Regel entspricht, z. B. Ziffern, aber keine Buchstaben oder Sonderzeichen, verwenden Sie die Funktion **Nur Übereinstimmung erfassen**. Weitere Informationen finden Sie unter [So erfassen Sie nur die Teile von Werten, die einer bestimmten Regel entsprechen](@DC-191#so-erfassen-sie-nur-die-teile-von-werten-die-einer-bestimmten-regel-entsprechen).

## Ressourcen

Die folgenden Ressourcen sind beim Erstellen oder Optimieren regulärer Ausdrücke hilfreich:

- [Microsoft Copilot](https://copilot.cloud.microsoft/) – oder ein gleichwertiger Chatbot mit generativer künstlicher Intelligenz. Diese Tools eignen sich gut zum Erstellen und Testen benutzerdefinierter Regeln, aber überprüfen Sie ihre Ausgabe unbedingt noch einmal.
- [RegExr](https://regexr.com/) – ein Tool, das Ihnen beim Erstellen und Testen regulärer Ausdrücke hilft.
- [Regex101](https://regex101.com/) – ein weiteres Tool, das Ihnen beim Erstellen und Testen regulärer Ausdrücke hilft.