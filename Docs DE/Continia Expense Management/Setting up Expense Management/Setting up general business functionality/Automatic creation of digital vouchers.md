---
title: Expense Management Digitale Belege automatisch erstellen
date: 04-04-2024
description: null
id: EM-223
lang: de
---

# Digitale Belege automatisch erstellen

In der Buchführung müssen Unternehmen ihre Transaktionen nachweisen, indem sie die entsprechenden Dokumente wie zum Beispiel Rechnungen oder andere Geschäftsbelege zusammen mit allen zugehörigen Dateien speichern. Dies garantiert Rückverfolgbarkeit und einen robusten Audit-Trail. Hierbei handelt es sich nicht nur um eine gesetzliche Anforderung, sondern es wird auch aus Sicherheitsgründen für Ihr Unternehmen empfohlen.

In vielen Unternehmen werden diese Nachweisdokumente – _Belege (Vouchers)_ – aus Effizienzgründen digitalisiert. In manchen Ländern sind digitale Belege sogar gesetzlich vorgeschrieben. In Microsoft Dynamics 365 Business Central werden digitale Belege unter **Eingehende Belege** gespeichert.

> [!NOTE]
> In Document Capture gibt es die gleiche Funktionalität. Weitere Informationen finden Sie im Document Capture-Artikel [Digitale Belege automatisch erstellen](@DC-184).

## Standardmäßige Business Central-Funktionalität

Mit der Funktion zur [**Einrichtung digitaler Belege**, die im Update 23.2 für Business Central 2023 Release Wave 2 (BC v23.2)](https://learn.microsoft.com/de-de/dynamics365/business-central/across-how-setup-digital-vouchers) enthalten ist, können Sie Business Central so einrichten, dass vor der Buchung geprüft wird, ob unter **Eingehende Belege** ein digitaler Beleg vorhanden ist. Dies können Sie für jede Transaktionsart einrichten. Wenn Sie diese Funktion aktiviert haben und kein digitaler Beleg in Spesenabrechnungen vorhanden ist, müssen Sie der Transaktion einen digitalen Beleg manuell hinzufügen, um die Transaktion buchen zu können. Für Pauschalen und Fahrstrecken werden digitale Belege automatisch erstellt, sodass Sie nichts selbst hinzufügen müssen.

> [!NOTE]
> In Dänemark ist diese Prüfung für dänische Firmen, die Business Central Online verwenden, aufgrund des neuen dänischen Buchhaltungsgesetzes (in Kraft seit dem 1. Juli 2024) Pflicht, da Microsoft Business Central Online bei der dänischen Wirtschaftsbehörde (Erhvervsstyrelsen) registriert und als standardmäßiges digitales Buchhaltungssystem genehmigen lassen hat. Wenn sich Ihr Unternehmen in Dänemark befindet, muss unter **Eingehende Belege** ein digitaler Beleg hinzugefügt werden, damit die Transaktionen gebucht werden können.

## Erweiterte Expense Management-Funktionalität

Ab Expense Management 2023 R2 Service Pack 2 kann Expense Management auf Basis der Expense Management-Dateien (der Dateien, die in Expense Management importiert wurden) automatisch digitale Belege für eingehende Dokumente erstellen, sodass Sie Dateien nicht mehr manuell anhängen müssen. Wenn ein Beleg als Einkaufsbeleg oder Buch.-Blatt registriert wird, erstellt Expense Management automatisch eine Kopie aller Expense Management-Dateien und hängt sie als digitale Belege unter **Eingehende Belege** an, sofern Sie Expense Management entsprechend eingerichtet haben. Die Einrichtung hängt von Ihrer Version von Business Central ab:

<br>

| Business Central-Version                                                                                                                          | Einrichtung                                                                                                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [Ab Business Central April 2019 (BC v14) bis BC v23.1](#expense-management-einrichtung-fur-bc-v14-bis-bc-v231) | Die Funktion wird in der **Expense Management Einrichtung** konfiguriert.                                                                                                          |
| [BC v23.2 und spätere Versionen](#expense-management-einrichtung-fur-bc-v232-und-spatere-versionen)                               | Expense Management verwendet die Einstellungen unter **Einrichtung des digitalen Gutscheinpostens**, um zu prüfen, ob die Funktion für den registrierten Belegtyp aktiviert wurde. |

Wenn Sie die Funktion aktivieren und einen Einkaufsbeleg registrieren, kopiert Expense Management automatisch alle angehängten Dateien in die **Eingehende Belege**-Infobox im offenen Einkaufsbeleg, wo sie als digitale Belege aufgeführt werden. Die hier aufgeführten Dateien sind standardmäßig dieselben wie die Dateien, die im Inforegister **Allgemein** unter **Anhänge** aufgeführt sind. Es besteht jedoch keine weitere Verbindung zwischen diesen beiden Bereichen. Wenn Sie eine Datei löschen, wird der andere Bereich nicht automatisch entsprechend aktualisiert. Die gelöschte Datei wird weiterhin angezeigt.

Weitere Informationen zum Einrichtungsprozess finden Sie in einem der folgenden Abschnitte für Ihre jeweilige Version von Business Central.

## Expense Management-Einrichtung für BC v14 bis BC v23.1

Um das automatische Erstellen digitaler Belege in älteren Versionen von Business Central (BC v14 bis BC v23.1) einzurichten, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Expense Management Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Gehen Sie im Inforegister **Allgemein** zu **Digitale Anhänge**.
3. Um zu prüfen ob Anlagen vorhanden sind, aktivieren Sie **Vor dem Buchen des Einkaufsbelegs Anhänge erstellen**.
4. Damit Expense Management automatisch digitale Belege erstellen kann, aktivieren Sie **Digitalen Beleg aus Dokument erstellen**.

Anschließend erstellt Expense Management für alle Belege, die registriert werden, automatisch digitale Belege entsprechend Ihren Einstellungen.

## Expense Management-Einrichtung für BC v23.2 und spätere Versionen

> [!NOTE]
> Expense Management prüft in der standardmäßigen Business Central **Einrichtung des digitalen Gutscheinpostens**, ob die digitale Belegfunktion für die Belegart aktiviert wurde, die registriert werden soll. Wenn dies der Fall ist, überträgt Expense Management automatisch alle Expense Management-Dateien in **Eingehende Belege**.

Um Expense Management so einzurichten, dass in neueren Versionen von Business Central (BC v23.2 und später) automatisch digitale Belege für [Einkaufszuordnungen](@DC-41) erstellt werden, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Expense Management Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Gehen Sie im Inforegister **Allgemein** zu **Digitale Anhänge**.
3. Wählen Sie unter **Status** **Nicht konfiguriert** aus. Damit gelangen Sie zur Business Central-Standardseite **Einrichtung des digitalen Gutscheinpostens**. Die Microsoft-Anleitung zum Einrichten digitaler Belege finden Sie [hier](https://learn.microsoft.com/de-de/dynamics365/business-central/across-how-setup-digital-vouchers).

Anschließend erstellt Expense Management für alle Belege, die registriert werden, automatisch digitale Belege entsprechend Ihren Einstellungen.
