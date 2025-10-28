---
title: Der Document Capture-Bereich im Business Central-Rollencenter
date: 17-04-2025
description: Eine Übersicht über die im Rollencenter verfügbaren Funktionen für Document Capture.
id: DC-172
lang: de
---

# Der Document Capture-Bereich im Business Central-Rollencenter

Continia Document Capture verbessert die Benutzeroberfläche und Funktionalität von Microsoft Dynamics 365 Business Central, indem einige der Standard-Rollencenter in Business Central erweitert werden. Dabei wird ein Bereich mit einer Reihe von Stapeln und Aktionskacheln hinzugefügt, die Ihnen die Verarbeitung Ihrer eingehenden Belege erleichtern.

Dieser Bereich, **Continia Document Capture Aktivitäten**, ist in mehrere Gruppen von Stapeln unterteilt, von denen jede mehrere relevante Stapel oder Aktionskacheln enthält. Diese werden weiter unten im Abschnitt [Der Bereich „Continia Document Capture Aktivitäten“](#der-bereich-continia-document-capture-aktivitaten) beschrieben.

Die folgenden Standard-Rollencenter in Business-Central werden mit diesem Bereich erweitert:

- **Buchhalter (ACCOUNTANT)**
- **Buchhaltungs-Manager (ACCOUNTING MANAGER)**
- **Kreditorenkoordinator (AP COORDINATOR)**
- **Buchhalter (BOOKKEEPER)**
- **Geschäftsführer (BUSINESS MANAGER)**

> [!NOTE]
> Außer den oben genannten Rollencentern, die standardmäßig mit dieser Funktionalität erweitert werden, können Continia-Partner den Bereich **Continia Document Capture Aktivitäten** auch beliebigen anderen Business Central-Rollencentern hinzufügen. Verwenden Sie hierfür die Seite **6085573 CDC Doc. Capture Activities**. Wenn dies für Sie relevant ist, wenden Sie sich bitte an [Ihren Continia-Partner](@DC-15).

## Der Bereich „Continia Document Capture Aktivitäten“

Der Bereich **Continia Document Capture Aktivitäten** im Rollencenter umfasst fünf Stapelgruppen:

- [**Belege**](#die-gruppe-belege)
- [**Einkaufsgenehmigung - Rechnungen**](#die-gruppe-einkaufsgenehmigung---rechnungen)
- [**Einkaufsgenehmigung - Gutschriften**](#die-gruppe-einkaufsgenehmigung---gutschriften)
- [**Einkaufsverträge**](#die-gruppe-einkaufsvertrage)
- [**Aktionen**](#die-gruppe-aktionen)

Jede dieser Stapelgruppen enthält mehrere relevante Stapel oder Aktionskacheln. Diese werden in den folgenden Abschnitten beschrieben.

### Die Gruppe „Belege“

Die Stapelgruppe **Belege** bietet einen Überblick darüber, wie viele Belege auf die OCR-Verarbeitung warten, wie viele zum Import und zur Registrierung bereit sind und wie viele Ihnen zugewiesen sind.

Wenn Sie **Warten auf OCR** oder **Bereit zum Import** auswählen, wird eine entsprechende Seite geöffnet, auf der alle Belegkategorien aufgeführt sind. In der Spalte **Belege für OCR** können Sie sehen, wie viele Belege für jede Kategorie auf die OCR-Verarbeitung warten. Wenn ein Beleg mit OCR verarbeitet wurde, wird er in die Spalte **Belege für Import** verschoben. Wenn bei der OCR-Verarbeitung ein Problem mit einem Beleg aufgetreten ist, wird dieser in die Spalte **Fehlerhafte Belege** verschoben, wo Sie ihn dann manuell verarbeiten müssen.

> [!TIP]
> Wenn Sie die Details der Belege in einer der Spalten anzeigen oder verschiedene Aktionen für einen der Belege ausführen möchten, wählen Sie die Nummer in der entsprechenden Spalte für die entsprechende Belegkategorie aus, um die Seite **Belegübersicht** zu öffnen. Darin werden alle Belege in der ausgewählten Spalte und Kategorie aufgelistet sind. Auf dieser Seite können Sie nach einem bestimmten Beleg in der Liste suchen (**Suchen**), eine Datei öffnen, um sie außerhalb von Business Central anzuzeigen (**Datei zeigen**), eine Datei vollständig löschen (**Löschen**) und eine OCR-verarbeitete Datei importieren (**Importiere Datei**).
>
> In der Spalte **Von** können Sie auch die E-Mail-Adresse des ursprünglichen Absenders eines Belegs anzeigen (normalerweise ein Kreditor), anstatt beispielsweise eine zwischengeschaltete E-Mail.

Durch Auswählen von **Bereit zur Registrierung** wird das Belegjournal geöffnet, wo importierte Belege verarbeitet und die darin enthaltenen Textinformationen erfasst werden. Weitere Informationen zum Belegjournal und seiner Verwendung finden Sie unter [Mit Papier- und PDF-Belegen arbeiten](@DC-71).

Durch Auswählen von **Mir zugewiesen** wird die Seite **Zugewiesene Dokumente** geöffnet, auf der Sie Ihnen zugewiesene Belege anzeigen, bearbeiten und neu zuweisen sowie deren Zuweisung aufheben können. Die hier angezeigten Belege wurden Ihnen von Mitarbeitenden aus einem bestimmten Grund zugewiesen, z. B. weil Sie sich besser damit auskennen. Es handelt sich hierbei nicht um Belege, die genehmigt werden müssen.

### Die Gruppe „Einkaufsgenehmigung - Rechnungen“

Die Stapelgruppe **Einkaufsgenehmigung – Rechnungen** ist für Einkaufsrechnungen vorgesehen und enthält drei Stapel: **Offene Rechnungen**, **Rechnungen zur Genehmigung** und **Freigegebene Rechnungen**. Sie bietet einen Überblick darüber, wie viele Rechnungen offen sind, wie viele zur Genehmigung bereit sind und wie viele jeweils freigegeben wurden.

Durch Auswählen einer der Stapel wird die Seite **Einkaufsrechnungen** geöffnet. Der Name und der Filter sind je nach Auswahl unterschiedlich; das Gesamtlayout ist jedoch gleich.

### Die Gruppe „Einkaufsgenehmigung - Gutschriften“

Die Stapelgruppe **Einkaufsgenehmigung – Gutschriften** ist für Einkaufsgutschriften vorgesehen und enthält drei Stapel: **Offene Gutschriften**, **Gutschriften zur Genehmigung** und **Freigegebene Gutschriften**. Sie bietet einen Überblick darüber, wie viele Gutschriften offen sind, wie viele zur Genehmigung bereit sind und wie viele jeweils für den nächsten Verarbeitungsschritt freigegeben wurden.

Durch Auswählen einer der Stapel wird die Seite **Einkaufsgutschriften** geöffnet. Der Name und der Filter sind je nach Auswahl unterschiedlich; das Gesamtlayout ist jedoch gleich.

> [!NOTE]
> Weitere Informationen zur standardmäßigen Business Central-Funktionalität für Einkaufsfunktionen im Zusammenhang mit den oben beschriebenen Seiten finden Sie unter [Einkauf](https://learn.microsoft.com/de-de/dynamics365/business-central/purchasing-manage-purchasing) (Microsoft-Artikel). <br><br> Weitere Informationen über die Einkaufsgenehmigung finden Sie unter [Überblick über Einkaufsgenehmigung](@DC-34).

### Die Gruppe „Einkaufsverträge“

Mit der Stapelgruppe **Einkaufsverträge** werden Einkaufsverträge verwaltet und sie enthält vier Stapel: **Alle**, **Genehmigung fällig**, **Genehmigung erforderlich** oder **Genehmigung ausstehend**. Diese geben einen Überblick darüber, wie viele Verträge insgesamt vorliegen, wie viele bis zum nächsten Genehmigungstermin fällig sind, wie viele den Status **Genehmigung erforderlich** haben bzw. wie viele den Status **Genehmigung ausstehend** haben.

Durch Auswählen einer der Stapel wird die Seite **Einkaufsverträge** geöffnet. Der Name und der Filter sind je nach Auswahl unterschiedlich; das Gesamtlayout ist jedoch gleich.

> [!NOTE]
> Weitere Informationen über Einkaufsverträge finden Sie unter [Überblick über Einkaufsverträge](@DC-85).

### Die Gruppe „Aktionen“

Die Stapelgruppe **Aktionen** enthält fünf Aktionskacheln, mit denen Sie verschiedene Aufgaben und Vorgänge ausführen können:

<br>

| Aktion                                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| ------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Beleg senden**                                       | Wählen Sie diese Aktion aus, um eine Seite mit einer Liste von E-Mail-Adressen für die jeweilige Belegkategorie zu öffnen. Um einen Beleg in Document Capture zu importieren, wählen Sie eine E-Mail-Adresse aus der Liste aus (möglicherweise möchten Sie die Seite vergrößern), und senden Sie dann eine E-Mail mit dem entsprechenden Beleg als Anhang an die ausgewählte E-Mail-Adresse. Weitere Informationen finden Sie unter [Belege importiereren](@DC-82#per-e-mail).                                                                                                                                                                 |
| **Dateien importieren**                                | Wählen Sie diese Aktion aus, um alle Dateien aus dem Stapel **Bereit zum Import** in [der Stapelgruppe **Belege**](#die-gruppe-belege) zu importieren. Die Dateien werden dann in den Stapel **Bereit zur Registrierung** verschoben. Weitere Informationen finden Sie unter [Belege importiereren](@DC-82#per-e-mail).                                                                                                                                                                                                                                                                                                                                           |
| **Beleg suchen**                                       | Wählen Sie diese Option, um in Ihren PDF- und XML-Belegen nach beliebigem Text zu suchen. Es werden alle Textinhalte in den Belegen durchsucht, unabhängig davon, ob der Text erfasst wurde oder nicht. Mit **Posten finden** werden alle Einträge gefunden, die sich auf die von Ihnen gesuchte Transaktion beziehen, einschließlich nicht gebuchter Belege (z. B. Rechnungen, deren Genehmigung noch aussteht oder die noch nicht registriert wurden. Weitere Informationen finden Sie in diesem Video zum [Suchen nach beliebigen Dokumenten](https://www.youtube.com/watch?v=if9Vjx_IeEg). |
| **Status E-Mail an Genehmiger senden**                 | Wählen Sie diese Aktion aus, um eine E-Mail-Benachrichtigung an alle Genehmiger zu senden, die ausstehende Genehmigungsanforderungen haben. Weitere Informationen finden Sie unter [So senden Sie Status-E-Mails manuell](@DC-26#so-senden-sie-status-e-mails-manuell).                                                                                                                                                                                                                                                                                                                                                                                                           |
| **Status E-Mail an Einkaufsvertragsgenehmiger senden** | Wählen Sie diese Aktion aus, um eine E-Mail-Benachrichtigung an alle Genehmiger von Einkaufsverträgen zu senden, deren Verträge zur Genehmigung anstehen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |

## Informationen zum Thema

[OCR-Verarbeitung von Belegen](@DC-145)