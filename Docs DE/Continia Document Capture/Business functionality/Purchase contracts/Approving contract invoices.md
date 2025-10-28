---
title: Vertragsrechnungen in Document Capture genehmigen
date: 15-07-2025
description: So richten Sie die automatische Genehmigung von Vertragsrechnungen ein.
id: DC-89
lang: de
---

# Vertragsrechnungen genehmigen

Mit dem Einkaufsverträge-Modul können Sie Vertragsrechnungen (das heißt Einkaufsrechnungen, die mit einem Einkaufsvertrag verknüpft sind) automatisch genehmigen lassen, wenn die Rechnung registriert wird. Sie können auch für jede Vertragszeile einen Abweichungsbetrag oder -prozentsatz festlegen. So können Rechnungen, deren Vertragsbeträge innerhalb der angegebenen Abweichung liegen, bei der Registrierung automatisch genehmigt werden.

Der Einfachheit halber werden in diesem Artikel Rechnungen als Beispiel verwendet. Die Funktion gilt jedoch auch für Vertragsgutschriften.

> [!NOTE]
> Wenn Sie einen Abweichungsbetrag oder -prozentsatz einrichten möchten, muss die Zeilenerkennung in der entsprechenden Vorlage aktiviert sein. Ohne aktivierte Zeilenerkennung funktioniert die automatische Genehmigung nur, wenn die Beträge der Rechnungs- und Vertragszeilen genau übereinstimmen.

## So aktivieren Sie die automatische Genehmigung von Vertragsrechnungen

Bevor Document Capture Vertragsrechnungen automatisch genehmigen kann, müssen Sie diese Funktion sowohl auf der Seite **Einkaufsverträge** als auch auf der **Vorlagenkarte** aktivieren.

### Auf der Seite „Einkaufsverträge“

So aktivieren Sie die automatische Genehmigung auf der Seite **Einkaufsverträge**:

1. Suchen Sie ({{search}}) nach **Einkaufsverträge** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie in der Liste der Verträge in der Spalte **Nr.** auf die Nummer des Vertrags, dessen verknüpfte Rechnungen Sie genehmigen möchten. Dadurch wird die Seite **Einkaufsvertrag** geöffnet.
3. **Optional**: Klicken Sie auf dem Inforegister **Allgemein** auf das Feld **Preistyp** und wählen Sie dann **Variabler Betrag** aus. Anschließend können Sie in den Schritten 5–6 Abweichungen hinzufügen.
4. Klicken Sie im Feld **Autom. bestätigen innerhalb der Abweichung** auf **Ja**.
5. **Optional**: Um einen Abweichungsprozentsatz für eine Zeile einzurichten, wählen Sie die entsprechende Zeile im Inforegister **Zeilen**,  aus und geben Sie dann den Prozentsatz unter **Max. erlaubte Zeilenabweichung %** ein. Wiederholen Sie diesen Schritt für alle weiteren Zeilen, für die Sie eine Abweichung einrichten möchten.
6. **Optional**: Um einen Abweichungsbetrag für eine Zeile einzurichten, wählen Sie die entsprechende Zeile im Inforegister **Zeilen** aus und geben Sie dann den Betrag unter **Max. erlaubte Zeilenabweichung** ein. Wiederholen Sie diesen Schritt für alle weiteren Zeilen, für die Sie eine Abweichung einrichten möchten.

   > [!NOTE]
   > Das Feld **Max. erlaubte Zeilenabweichung** muss möglicherweise zuerst hinzugefügt werden, damit es sichtbar ist. [Personalisieren Sie dazu die Seite](https://docs.microsoft.com/de-de/dynamics365/business-central/ui-personalization-user) folgendermaßen:
   >
   > 1. Klicken Sie auf **Einstellungen** {{settings}} > **Personalisieren** > **+ Feld**, um den Bereich **Feld der Seite hinzufügen** zu öffnen.
   > 2. Wählen Sie den Abschnitt **Zeilen** aus und ziehen Sie dann das Feld **Max. erlaubte Zeilenabweichung** aus dem Bereich in die Tabelle im ausgewählten Abschnitt.
   > 3. Klicken Sie auf **Fertig**, um das Banner **Personalisierung** zu schließen.

Standardmäßig können Vertragsrechnungen, die im Vergleich zum Vertragsbeginn (bei der ersten Rechnung) oder zum Datum der letzten Rechnung (bei nachfolgenden Rechnungen) bis zu drei Tage zu früh oder zu spät vorliegen, immer noch automatisch genehmigt werden. So ändern Sie dies:

1. Suchen Sie ({{search}}) nach **Einkaufsvertragseinrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Geben Sie auf dem Inforegister **Genehmigung** die gewünschte Formel in das Feld **Max. zulässige Abweichung vom Genehmigungsdatum** ein. Beispielsweise 5T (fünf Tage).

### Auf der Seite „Vorlagenkarte“

Um registrierte Vertragsrechnungen automatisch zur Genehmigung zu senden, müssen Sie den zweiten Schritt für die Registrierung auf der Seite **Vorlagenkarte** konfigurieren. Gehen Sie hierzu wie folgt vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste die Rechnung aus, deren Vorlage Sie bearbeiten möchten.
4. Klicken Sie in der Aktionsleiste auf **Vorlage** > **Vorlagenkarte**, um die Seite **Vorlagenkarte** zu öffnen.
5. Wählen Sie im Inforegister **Einkaufsbelege** unter **Registrierung** das Feld **Rechnung Reg. Schritt 2** und anschließend **Bereitstellen für Genehmigung** aus.

   > [!NOTE]
   > Mit der Anleitung oben wird die automatische Genehmigung nur für die Vorlage aktiviert, die der ausgewählten Rechnung zugewiesen ist. Wenn Sie sie stattdessen für die Mastervorlage aktivieren, wird diese Funktion auch in allen neu erstellten Vorlagen automatisch aktiviert. Weitere Informationen finden Sie unter [Mit Vorlagen arbeiten)](@DC-18).

## So genehmigen Sie Vertragsrechnungen

Wenn Sie die beiden Schritte des Einrichtungsprozesses wie oben beschrieben abgeschlossen haben, können Sie alle Vertragsrechnungen automatisch genehmigen lassen, indem Sie sie einfach registrieren:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie den Code **EINKAUF** aus, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste die Rechnung aus, die Sie registrieren möchten.
4. Klicken Sie in der Aktionsleiste auf **Start** > **Registrieren**.

Dadurch wird die Rechnung registriert und automatisch genehmigt, und die Seite **Einkaufsrechnung** wird geöffnet. Im Inforegister **Allgemein** wird im Feld **Genehmigungsbemerkungen** der Text **Die Rechnung wurde automatisch genehmigt** angezeigt.

## Szenarien

Die folgenden Szenarien veranschaulichen die Logik der automatischen Genehmigung.

### Erste Vertragsrechnung

Wenn keine anderen Rechnungen im Zusammenhang mit dem Einkaufsvertrag vorliegen (weder gebucht noch ungebucht), genehmigt Document Capture die neue Rechnung nur dann automatisch, wenn ihr Buchungsdatum entweder mit dem Startdatum des Vertrags übereinstimmt oder nach diesem liegt.

### Eine nicht gebuchte Einkaufsrechnung ist vorhanden

Wenn es eine oder mehrere nicht gebuchte Rechnungen im Zusammenhang mit dem Einkaufsvertrag gibt, genehmigt Document Capture die neue Rechnung nicht automatisch, da die erforderliche Datumsprüfung nicht durchgeführt werden kann.

### Eine gebuchte Einkaufsrechnung ist vorhanden

Wenn eine oder mehrere gebuchte Rechnungen zum Einkaufsvertrag vorliegen, genehmigt Document Capture die neue Rechnung automatisch – vorausgesetzt, diese Rechnung besteht die Datumsprüfung.

### Es sind gebuchte und nicht gebuchte Rechnungen vorhanden

Wenn sowohl gebuchte als auch nicht gebuchte Rechnungen zum Einkaufsvertrag gehören, ignoriert Document Capture die nicht gebuchten Rechnungen, führt die Datumsprüfung auf Grundlage der zuletzt gebuchten Rechnung durch und genehmigt die neue Rechnung automatisch – vorausgesetzt, diese Rechnung besteht die Datumsprüfung.

## Informationen zum Thema

[Einkaufsverträge erstellen](@DC-86)  
[Genemigung von Einkaufsverträgen](@DC-87)  
[Vertragsrechnungen erstellen](@DC-88)  
[Das Einkaufsvertragsarchiv anzeigen](@DC-90)