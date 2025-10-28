---
title: Mit Papier- und PDF-Dokumenten in Document Capture arbeiten
date: 28-03-2025
description:
id: DC-71
lang: de
---

# Mit Papier- und PDF-Belegen arbeiten

Sobald ein Beleg in Continia Document Capture importiert wurde, z. B. als PDF-Datei oder als gescanntes Papierdokument, können Sie [darin enthaltene Textinformationen erfassen](@DC-110) und damit arbeiten. Die Informationen, die Sie erfassen müssen, hängen vom jeweiligen Belegtyp ab. Alle Belege werden, unabhängig vom Typ, am selben Ort verwaltet und verarbeitet – im Belegjournal.

Die Hauptfunktion des Belegjournals besteht darin, Ihnen die Arbeit mit importierten Belegen und die Erfassung der in diesen Belegen enthaltenen Textinformationen zu ermöglichen. Sobald die Informationen im Belegjournal erfasst wurden, müssen Sie den Beleg registrieren. Durch die Registrierung eines Belegs werden alle erfassten Informationen in eine echte Geschäftsentität in Microsoft Dynamics 365 Business Central umgewandelt. Wenn Sie beispielsweise eine Einkaufsrechnung von einem Kreditor registrieren, erstellen Sie eine Business Central-Einkaufsrechnung.

> [!IMPORTANT]
> Sie können Document Capture für viele Belegarten konfigurieren, die sich auf verschiedene Datensätze oder Entitäten in Business Central beziehen. Meist wird Document Capture zur Verarbeitung von Einkaufsrechnungen und Gutschriften verwendet. Es ist aber auch möglich, damit Verkaufsaufträge, Verträge, Artikelzertifikate und viele andere Belegarten zu verarbeiten. Wenn Sie Einkaufsrechnungen und Gutschriften verarbeiten, werden die Belege mit Kreditoren verknüpft. Zur Veranschaulichung konzentriert sich dieser Artikel ausschließlich auf Kreditoren. Es können jedoch auch Debitoren, Artikel, Anlagen etc. verwendet werden.

## Überblick über das Belegjournal

So greifen Sie auf das Belegjournal zu:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, in diesem Fall **EINKAUF**, um das Belegjournal zu öffnen.

Das Belegjournal besteht aus vier Hauptbereichen:

**Belegliste (linke Seite):** Diese Tabelle listet alle Belege auf, die im ausgewählten Journal enthalten sind. Zu jedem Beleg liefert Ihnen die Tabelle Informationen wie die Belegnummer, den Kreditornamen, die verwendete Vorlage und die Anzahl der Seiten. Darüber hinaus zeigt das Feld **OK** an, ob alle erfassten Werte im Beleg gültig sind und ob der jeweilige Beleg zur Registrierung bereit ist.

**Belegfelder (linke Seite):** In diesem Bereich werden unter **Belegkopf** alle Felder angezeigt, die im aktuell ausgewählten Beleg identifiziert wurden, zusammen mit ihren entsprechenden Werten. Die Liste der Felder wird durch die Belegvorlage bestimmt und Document Capture gibt für jedes Feld an, ob der Wert gemäß der Konfiguration des jeweiligen Vorlagenfelds gültig ist.

> [!NOTE]
> Ein Beleg kann erst registriert werden, wenn alle Belegkopffelder in der Spalte **OK** ein Häkchen haben. Wenn alle Belegkopffelder mit OK markiert sind, wird auch der eigentliche Beleg in der Belegliste mit OK markiert.
>
> Beachten Sie, dass **Nr.** für die Belegregistrierung obligatorisch ist und häufig manuell eingegeben werden muss, da sie in importierten Belegen nicht erfasst werden kann. Das Feld steht in engem Zusammenhang mit dem direkt darüber liegenden Feld **Art**, in dem Sie die Art des Kontos für den Beleg auswählen können. Wenn Sie keine Kontoart auswählen, wird für **Nr.** standardmäßig Sachkonto verwendet.

**Bemerkungen (linke Seite):** In diesem Bereich werden Bemerkungen zum ausgewählten Beleg angezeigt. Es gibt drei verschiedene Arten von Bemerkungen: **Information**, **Warnung** und **Fehler**. Weitere Informationen finden Sie unter [Bemerkungsarten und deren Wichtigkeit konfigurieren](Configuring comment types and importance.md).

**Dokumentenvorschau (rechte Seite):** Das Bild rechts zeigt eine visuelle Darstellung des gescannten Originalbelegs (entweder PDF oder XML), nachdem dieser mit Texterkennung (OCR) verarbeitet wurde. Weitere Informationen finden Sie unter [Dokumentenvorschau](#dokumentenvorschau) weiter unten.

## Dokumentenvorschau

Wie oben erwähnt, zeigt die Dokumentenvorschau PDF- oder XML-Belege an, die von Document Capture gescannt, importiert und mit OCR verarbeitet wurden. Bei PDF-Belegen ist das Dokumentenbild interaktiv, d. h. Sie können Text an einer beliebigen Stelle im Bild manuell auswählen, um ihn als den Wert zu erfassen, der einem bestimmten Feld zugeordnet ist. Weitere Informationen finden Sie unter [Felder in einem Beleg erfassen](@DC-110).

> [!NOTE]
> Während der OCR-Verarbeitung eines Belegs wird eine visuelle Darstellung des Belegs zu Anzeigezwecken erstellt, die weniger Farben und einer geringere Auflösung als der Originalbeleg haben kann. Hierdurch wird die Leistung und Benutzerfreundlichkeit für Sie optimiert, wenn Sie mit dem Beleg in Business Central arbeiten. Was Sie in der Dokumentenvorschau sehen, ist die mit OCR verarbeitete Version des Belegs und nicht der Originalbeleg, der möglicherweise etwas anders aussieht. Der eigentliche OCR- und Erkennungsprozess des Originalbelegs wird jedoch trotzdem mit höchster Detailgenauigkeit durchgeführt. Weitere Informationen finden Sie unter [OCR-Verarbeitung von Belegen](OCR-processing a document.md).

In der oberen linken Ecke der Dokumentenvorschau befindet sich ein Dropdown-Menü, mit dem Sie alle angehängten Dateien des Belegs anzeigen oder herunterladen können. Das Dropdown-Menü ist auch für alle anderen Seiten verfügbar, die die Dokumentenvorschau enthalten, mit Ausnahme der Seite **Dokumente (UIC)**, da die auf dieser Seite angezeigten Belege noch nicht verarbeitet wurden.

Die meisten der im Menü aufgeführten Anhänge können in der Benutzeroberfläche angezeigt werden, einige jedoch nicht (z. B. .xlsx- und .docx-Dateien). Diese können jedoch direkt aus dem Menü heruntergeladen werden. Die Anhänge sind in folgende Gruppen eingeteilt:

- **Original** – der ursprüngliche Beleg, der in Document Capture importiert wurde
- **Verknüpfte Dokumente** (OIOUBL/OIOUTS)
- **Anhänge** (.bmp, .jpeg, .jpg, .pdf, .png, .tif und .tiff)
- **XML-Anhänge** (.bmp, .jpeg, .jpg, .pdf, .png, .tif und .tiff)
- **Herunterladbare Formularanhänge** (alle anderen Dateitypen)

Wenn Sie einen XML-Beleg anzeigen, der über eine eingebettete PDF-Datei verfügt, können Sie diese PDF-Datei anstelle der ursprünglichen XML-Datei in der Dokumentenvorschau anzeigen lassen. Dies muss jedoch zuerst [für die entsprechende XML-Mastervorlage eingerichtet](@DC-144) werden. Wenn eine Datei in einem anderen Format als PDF in das importierte XML eingebettet wurde, wird sie standardmäßig nicht angezeigt. In solchen Fällen zeigt die Dokumentenvorschau stattdessen das Original-XML an.

Sie können die Größe der Dokumentenvorschau ändern, indem Sie den vertikalen Ziehbalken auf der linken Seite der FactBox der Dokumentenvorschau ziehen. Dies gilt auch für alle anderen Seiten, auf denen die Dokumentenvorschau verfügbar ist (z. B. **Einkaufsrechnung**, **Verkaufsauftrag**, **Kreditorenposten**, **Fibu Buch.-Blätter** und **Sachposten**).

## Den mit einem Beleg verknüpften Kreditor ändern

Standardmäßig verknüpft Document Capture alle Belege mit vorhandenen Datensätzen in Business Central. Einkaufsbelege sind mit Kreditoren verknüpft, d. h. jedem Einkaufsbeleg ist ein bestimmter Kreditor zugeordnet. Im Belegjournal zeigen die ersten Spalten in der Belegliste (**Kreditor** und **Name**) die Nummer und den Namen des Kreditors an, mit dem der jeweilige Beleg verknüpft ist. Beim Importieren von Belegen identifiziert Document Capture den Kreditor automatisch anhand verschiedener Parameter. Weitere Informationen zu diesen Parametern finden Sie unter [Belegherkunft und -vorlage identifizieren](Finding the document source and template.md).

Falls Document Capture keinen Kreditor identifizieren kann oder Sie den identifizierten Kreditor ändern möchten, können Sie einen neuen Kreditor im Belegjournal zuweisen. Gehen Sie hierzu wie folgt vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, in diesem Fall **EINKAUF**, um das Belegjournal zu öffnen.
3. Gehen Sie in der Belegliste in die Zeile des importierten Belegs, dessen Kreditor Sie ändern möchten, und wählen Sie das Feld **Kreditor** aus. Wählen Sie dann die drei angezeigten Punkte aus, um das Fenster **Kreditoren** zu öffnen.
4. Wählen Sie den Kreditor, den Sie zuweisen möchten, indem Sie die entsprechende Nummer in der Spalte **Nr.** auswählen.

> [!NOTE]
> Sie können auch Suchtexte einrichten, damit Document Capture den richtigen Kreditor besser identifizieren kann. Weitere Informationen finden Sie unter [Belegherkunft und Vorlage identifizieren](/Continia Document Capture/Business functionality/Documents and templates/Finding the document source and template.md).

## Die Kategorie eines Belegs ändern

So ändern Sie die Kategorie eines Belegs im Belegjournal:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, in diesem Fall **EINKAUF**, um das Belegjournal zu öffnen.
3. Klicken Sie in der Aktionsleiste auf **Dokument** > **Kategorie ändern**, um die Liste der Kategorien zu öffnen. Anschließend können Sie den bzw. die Beleg(e) in die gewünschte Kategorie verschieben, wobei auch eine automatische Felderkennung erfolgt.

Beachten Sie, dass eine Änderung der Kategorie nur bei Belegen mit dem Status „offen“ möglich ist, das heißt keine abgelehnten oder registrierten Belege. Außerdem funktioniert dies nur bei PDF-Dateien.

Die Alternative zum oben beschriebenen Ansatz ist:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, in diesem Fall **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie das Symbol {{settings}} > **Personalisieren**.
4. Wählen Sie in der oberen linken Ecke **+ Feld** aus, um den Bereich **Feld der Seite hinzufügen** zu öffnen.
5. Suchen Sie nach dem Feld **Belegkategorie** und ziehen Sie es vor oder nach einer vorhandenen Spalte im Belegjournal.
6. Wählen Sie im Personalisierungsbanner **Fertig** aus.

Sie können nun unter der **Belegkategorie** einen neuen Wert auswählen, um die Kategorie des entsprechenden Belegs zu ändern.

## Registrierte und abgelehnte Belege anzeigen

Wenn Sie das Belegjournal öffnen, zeigt der Filter nur offene Belege an. Sie können den Filter aber problemlos anpassen, um registrierte oder abgelehnte Belege anzuzeigen. Gehen Sie hierzu wie folgt vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, in diesem Fall **EINKAUF**, um das Belegjournal zu öffnen.
3. Gehen Sie in der oberen rechten Ecke über der Aktionsleiste zu **Statusfilter**, um die Filteroptionen anzuzeigen. Die Standardoption ist **Offen**, sodass nur Belege mit dem Status „Offen“ in der Belegliste angezeigt werden. Sie können dies nach Bedarf ändern, indem Sie Ihre bevorzugte Filteroption auswählen.

Die Belegliste wird aktualisiert und zeigt nur Belege mit dem von Ihnen ausgewählten Status an. Wenn Sie **Alle** ausgewählt haben, werden alle Belege unabhängig vom Status in der Liste angezeigt.

## Informationen zum Thema

[Felder in einem Beleg erfassen](@DC-110)  
[Bemerkungsarten und deren Wichtigkeit konfigurieren](@DC-72)  
[OCR-Verarbeitung von Belegen](@DC-145)  
[Belegherkunft und -vorlage identifizieren](@DC-109)  
[Belege registrieren](@DC-67)  
[Mit Vorlagen arbeiten](@DC-18)  
[Neue Vorlagenfelder einrichten](@DC-19)