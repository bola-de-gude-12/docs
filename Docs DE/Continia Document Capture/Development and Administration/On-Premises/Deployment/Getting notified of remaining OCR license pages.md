---
title: Benachrichtigung über verbleibende OCR-Lizenzseiten
date: 06-09-2023
description: null
id: DC-153
lang: de
---

# Benachrichtigung über verbleibende OCR-Lizenzseiten

Sie können in Document Capture On-Premises Benachrichtigungen einrichten, um Benutzer in Ihrem Unternehmen zu warnen, wenn die Seiten in Ihrer OCR-Lizenz aufgebraucht werden. So können Sie rechtzeitig Maßnahmen ergreifen und vermeiden, dass Dokumente aufgrund des erreichten Limits in den Fehlerordner verschoben werden.

> [!NOTE]
> Solche Benachrichtigungen werden nur für Benutzer von [On-Premises-OCR](#on-premises-ocr) angezeigt, da es für Continia Cloud OCR kein Limit für die Anzahl der verarbeiteten Seiten gibt. Da die Continia Cloud OCR-Basislizenz jedoch maximal 1.000 OCR-Seiten pro Monat umfasst und Ihnen für alle darüber hinaus verarbeiteten Seiten eine geringe Gebühr berechnet wird, kann es für Sie dennoch wichtig sein, Ihren Seitenverbrauch im Auge zu behalten. Sie können dies ganz einfach in der **Document Capture Einrichtung** konfigurieren, wie unten unter [Continia Cloud OCR](#continia-cloud-ocr) beschrieben.

## On-Premises OCR

Um einen Überblick über Ihren OCR-Lizenzstatus zu erhalten und einen Seitenschwellenwert festzulegen, bei dem Benachrichtigungen angezeigt werden, führen Sie die folgenden Schritte aus:

1. Wählen Sie das Symbol {{search}}, geben Sie **Document Capture Einrichtung** ein, und wählen Sie dann den zugehörigen Link.

2. Im Inforegister **OCR-Lizenzseiten** können Sie die folgenden Informationen zu Ihrem OCR-Seitenverbrauch überprüfen:

   <br>

   | Feld                      | Beschreibung                                                                                                                                                                                                                                            |
   | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | **Seitenwarnung**         | Ermöglicht Ihnen, einen Schwellenwert für die Anzeige von Benachrichtigungen festzulegen.                                                                                                                                               |
   | **Verbleibende Seiten**   | Gibt an, wie viele Seiten Sie in Ihrer Lizenz noch zu verarbeiten haben. Zusammen mit **Seitenwarnung** bestimmt dieses Feld, wann Benachrichtigungen angezeigt werden.                                                 |
   | **Seiten insgesamt**      | Gibt an, wie viele Seiten insgesamt in Ihrer Lizenz enthalten sind. Standardmäßig sind 10.000 Seiten pro Monat für On-Premises OCR enthalten; Sie können jedoch bei Bedarf zusätzliche Seiten erwerben. |
   | **Letzte Aktualisierung** | Gibt das genaue Datum und die Uhrzeit der letzten Aktualisierung der oben genannten Felder an.                                                                                                                                          |

   <br>

3. Geben Sie unter **Seitenwarnung** die Anzahl der Dokumente ein, ab der eine Benachrichtigung ausgelöst wird.

Wenn die Anzahl der verbleibenden Seiten Ihrer Lizenz gleich oder niedriger als die Zahl ist, die Sie unter **Seitenwarnung** eingeben, werden Benutzer benachrichtigt, dass die Lizenz ihr Limit erreicht. Diese Benachrichtigung wird den Benutzern angezeigt, wenn sie im Rollencenter **Dateien importieren** auswählen oder wenn sie zu einer der Seiten **Bereit zum Importieren**, **Belegjournal** oder **Document Capture Einrichtung** gehen.

## Continia Cloud OCR

Um einen Überblick über Ihren OCR-Lizenzstatus zu erhalten, folgen Sie diesen Schritten:

1. Wählen Sie das Symbol {{search}}, geben Sie **Document Capture Einrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Im Inforegister **OCR-Lizenzseiten** können Sie die folgenden Informationen zu Ihrem OCR-Seitenverbrauch überprüfen:

   <br>

   | Feld                      | Beschreibung                                                                                                                                                                                                            |
   | ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | **Verwendete Seiten**     | Gibt an, wie viele Seiten Sie in Ihrer Lizenz verarbeitet haben.                                                                                                                                        |
   | **Seiten insgesamt**      | Gibt an, wie viele Seiten insgesamt in Ihrer Lizenz enthalten sind. Standardmäßig sind 1.000 Seiten ohne zusätzliche Kosten pro Monat für Continia Cloud OCR enthalten. |
   | **Letzte Aktualisierung** | Gibt das genaue Datum und die Uhrzeit der letzten Aktualisierung der oben genannten Felder an.                                                                                                          |

Wenn die unter **Verwendete Seiten** angezeigte Zahl die unter **Gesamtzahl Seiten** angegebene Zahl überschreitet, wird Ihnen eine geringe Gebühr für jede zusätzliche Seite berechnet.

## Informationen zum Thema

[Cloud OCR konfigurieren](@DC-141)\
[On-Premises OCR konfigurieren](@DC-150)\
[Continia-Benachrichtigungen](@DC-131)

<style>
.content table tr td:nth-child(1) {
width: 80px;
}
.content table tr td:nth-child(2) {
width: 520px;
}
</style>
