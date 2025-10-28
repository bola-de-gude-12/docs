---
title: Digitale Belege automatisch erstellen
date: 07-03-2024
description: null
id: DC-184
lang: de
---

# Digitale Belege automatisch erstellen

In der Buchführung müssen Unternehmen ihre Transaktionen nachweisen, indem sie die entsprechenden Dokumente wie zum Beispiel Rechnungen oder andere Geschäftsbelege zusammen mit allen zugehörigen Dateien speichern. Dies garantiert Rückverfolgbarkeit und einen robusten Audit-Trail. Hierbei handelt es sich nicht nur um eine gesetzliche Anforderung, sondern es wird auch aus Sicherheitsgründen für Ihr Unternehmen empfohlen.

In vielen Unternehmen werden diese Nachweisdokumente – _Belege (Vouchers)_ – aus Effizienzgründen digitalisiert. In manchen Ländern sind digitale Belege sogar gesetzlich vorgeschrieben. In Microsoft Dynamics 365 Business Central werden digitale Belege unter **Eingehende Belege** gespeichert.

## Standardmäßige Business Central-Funktionalität

Mit der Funktion zur [**Einrichtung digitaler Belege**, die im Update 23.2 für Business Central 2023 Release Wave 2 (BC v23.2)](https://learn.microsoft.com/de-de/dynamics365/business-central/across-how-setup-digital-vouchers) enthalten ist, können Sie Business Central so einrichten, dass vor der Buchung geprüft wird, ob unter **Eingehende Belege** ein digitaler Beleg vorhanden ist. Dies kann für alle Transaktionsarten (Verkaufsbeleg, Verkaufs Buch.-Blatt, Einkaufsbeleg, Einkaufs Buch.-Blatt oder Hauptbuch) eingerichtet werden. Wenn Sie diese Funktion aktiviert haben und kein digitaler Beleg vorhanden ist, müssen Sie der Transaktion einen digitalen Beleg manuell hinzufügen, um die Transaktion buchen zu können.

> [!NOTE]
> In Dänemark ist diese Prüfung für dänische Firmen, die Business Central Online verwenden, Pflicht, da Microsoft Business Central Online bei der dänischen Wirtschaftsbehörde (Erhvervsstyrelsen) registriert und als standardmäßiges digitales Buchhaltungssystem genehmigen lassen hat. Wenn sich Ihr Unternehmen in Dänemark befindet, muss unter **Eingehende Belege** ein digitaler Beleg hinzugefügt werden, damit die Transaktionen gebucht werden können.

## Erweiterte Document Capture-Funktionalität

Ab dem Document Capture 2023 R2 Service Pack 2 kann Document Capture digitale Belege für eingehende Einkaufsbelege automatisch erstellen. Diese werden basierend auf den Document Capture-Dateien erstellt, die zusammen mit dem primären Einkaufsbeleg in Document Capture importiert oder gezogen wurden, sodass Sie die Dateien nicht selbst manuell anhängen müssen. Wenn ein Beleg als Einkaufsbeleg oder Buch.-Blatt registriert wird, erstellt Document Capture automatisch eine Kopie aller Document Capture-Dateien und hängt sie als digitale Belege unter **Eingehende Belege** an, sofern Sie Document Capture entsprechend eingerichtet haben. Die Einrichtung hängt von Ihrer Version von Business Central ab:

<br>

| Business Central-Version                                                                                                                    | Einrichtung                                                                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [Business Central April 2019 (BC v14) bis BC v23.1](#document-capture-einrichtung-fur-bc-v14-to-bc-v231) | Die Funktion wird in der **Document Capture Einrichtung** konfiguriert.                                                                                                          |
| [BC v23.2 und spätere Versionen](#document-capture-einrichtung-fur-bc-v232-und-spatere-versionen)                           | Document Capture verwendet die Einstellungen unter **Einrichtung des digitalen Gutscheinpostens**, um zu prüfen, ob die Funktion für den registrierten Belegtyp aktiviert wurde. |

> [!NOTE]
> In allen Versionen von Business Central wurde eine optionale Funktion hinzugefügt, mit der Sie Document Capture zum Erstellen digitaler Belege für [Einkaufszuordnungen](@DC-41) einrichten können. Diese Funktion ist optional, da einige Unternehmen Einkaufszuordnungen als reine Finanzaufzeichnungen betrachten, die nicht unbedingt digital dokumentiert werden müssen.

Wenn Sie die Funktion aktivieren und einen Einkaufsbeleg registrieren, kopiert Document Capture automatisch alle angehängten Dateien in die **Eingehende Belege**-Infobox im offenen Einkaufsbeleg, wo sie als digitale Belege aufgeführt werden. Die hier aufgeführten Dateien sind standardmäßig dieselben wie die Dateien, die im Inforegister **Allgemein** unter **Anhänge** aufgeführt sind. Es besteht jedoch keine weitere Verbindung zwischen diesen beiden Bereichen. Wenn Sie eine Datei löschen, wird der andere Bereich nicht automatisch entsprechend aktualisiert. Die gelöschte Datei wird weiterhin angezeigt.

Weitere Informationen zum Einrichtungsprozess finden Sie in einem der folgenden Abschnitte für Ihre jeweilige Version von Business Central.

## Document Capture-Einrichtung für BC v14 bis BC v23.1

Um das automatische Erstellen digitaler Belege in älteren Versionen von Business Central (BC v14 bis BC v23.1) einzurichten, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Document Capture Einrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Gehen Sie im Inforegister **Allgemein** zu **Digitale Gutscheine**.
3. Damit Document Capture automatisch digitale Belege aus primären Einkaufsbelegen erstellt (wie etwa eingehenden Einkaufsrechnungen), wählen Sie **Erstellen Sie einen digitalen Gutschein aus dem Primärdokument**.
4. Damit Document Capture digitale Belege auch aus allen zusätzlichen Anhängen automatisch erstellt, wählen Sie **Fügen Sie Anhänge hinzu**.
5. Wenn Document Capture automatisch digitale Belege für [Einkaufszuordnungen](@DC-41) erstellen soll, wählen Sie **Für Einkaufszuordnung erstellen** aus.

Anschließend erstellt Document Capture für alle Belege, die registriert werden, automatisch digitale Belege entsprechend Ihren Einstellungen.

## Document Capture-Einrichtung für BC v23.2 und spätere Versionen

> [!NOTE]
> Document Capture prüft in der standardmäßigen Business Central **Einrichtung des digitalen Gutscheinpostens**, ob die digitale Belegfunktion für die Belegart aktiviert wurde, die registriert werden soll. Wenn dies der Fall ist, überträgt Document Capture automatisch alle Document Capture-Dateien in **Eingehende Belege**.

Um Document Capture so einzurichten, dass in neueren Versionen von Business Central (BC v23.2 und später) automatisch digitale Belege für [Einkaufszuordnungen](@DC-41) erstellt werden, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Document Capture Einrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Gehen Sie im Inforegister **Allgemein** zu **Digitale Gutscheine**.
3. Wählen Sie **Für Einkaufszuordnung erstellen** aus.

Anschließend erstellt Document Capture für alle Belege, die registriert werden, automatisch digitale Belege entsprechend Ihren Einstellungen.

## Informationen zum Thema

[Konformität mit dem Danish Bookkeeping Act](@DC-169)
