---
title: Einkaufsverträge in Document Capture genehmigen
date: 23-07-2025
description: So können Sie Einkaufsverträge in Document Capture genehmigen
id: DC-87
lang: de
---

# Einkaufsverträge genehmigen

Der Genehmigung von Einkaufsverträgen ist ein zentraler Bestandteil des Einkaufsverträge-Moduls. Mit Vertragsgenehmigungen soll sichergestellt werden, dass ein Mitarbeitender im Unternehmen (der Genehmiger) die aktuellen Verträge des Unternehmens prüft und darauf achtet, dass sie auf dem neuesten Stand sind oder bei Bedarf verlängert, gekündigt oder geändert werden. Sie können für die einzelnen Verträge verschiedene Genehmiger oder einen Genehmiger für alle Verträge bestimmen, je nachdem, was für Ihr Unternehmen am sinnvollsten ist.

Vor der Veröffentlichung von Continia Document Capture 25.00 wurde dieser Prozess als Überprüfung von Einkaufsverträgen bezeichnet. Dieser wurde jetzt überarbeitet, um ihn der Genehmigung von Einkaufsrechnungen anzupassen. Beachten Sie Folgendes:

- Die folgenden Funktionen des Moduls **Genehmigungen** werden derzeit nicht unterstützt: Erweiterte Genehmigung, Vier-Augen-Genehmigung und Genehmigungsabläufe.
- Nach dem Upgrade auf 25.00 wird der Status bestehender und bereits geprüfter Einkaufsverträge auf **Freigegeben** gesetzt; alle anderen erhalten den Status **Genehmigung erforderlich**. Daher müssen diese überprüft werden.
- Wenn das Modul für die Beleggenehmigung in Ihrer Umgebung nicht aktiviert ist, ist die Funktionalität für Einkaufsverträge eingeschränkt. Daher sind viele der in diesem Artikel beschriebenen Funktionen nicht verfügbar.

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src=https://player.vimeo.com/video/1028406654?h=c686b4ad1c&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479 frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="DC_purchase_contracts approvals_produced"></iframe></div><script src=https://player.vimeo.com/api/player.js></script>

## So verwenden Sie die Genehmigungsfunktion

So verwenden Sie die Genehmigungsfunktion:

1. Suchen Sie {{search}} nach **Einkaufsvertragseinrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Aktivieren Sie im Inforegister **Genehmigung** die Einstellung **Einkaufsvertragsgenehmigung aktivieren** und bei Bedarf die Einstellung **Erzwungene Einkaufsvertragsgenehmigung aktivieren**.
3. Klicken Sie in der Aktionsleiste auf **Workflows und Benutzer** > **Continia-Benutzereinrichtung** und konfigurieren Sie die Felder **Grenzbetrag für Einkaufsverträge**, **Unbegrenzte Genehmigung von Einkaufsverträgen** und **Einkaufsvertrags-Genehmiger-ID** entsprechend Ihren Anforderungen.

Ein Einkaufsvertragsadministrator – normalerweise ein Controller – startet den Prozess, indem er entweder einen Vertrag oder mehrere Verträge auf einmal an den Genehmiger sendet. Bei jeder Genehmigung kann der Genehmiger Kommentare hinzufügen, die der Controller berücksichtigen muss.

## Zusätzliche Genehmigungsfunktionen

Beachten Sie, dass die folgende Genehmigungsfunktion für Einkaufsverträge nur verfügbar ist, wenn das Modul Genehmigungen aktiv und die Einkaufsvertragsgenehmigung aktiviert ist.

- Genehmigung erzwingen und Geteilte Genehmigung.

- Zusätzliche Felder auf der Karte **Einkaufsverträge**:
  - **Genehmigung durch:** Gibt die Benutzer an, die Teil des Genehmigungsablaufs für dieses Dokument sind.
  - **Genehmigungsbemerkungen**: Gibt den letzten Kommentar an, der diesem Dokument hinzugefügt wurde. Sie können die Suche verwenden, um alle Kommentare anzuzeigen.

- Zusätzliche Felder auf der Seite **Einkaufsverträge**:
  - **Genehmigung durch:** Gibt die Benutzer an, die Teil des Genehmigungsablaufs für dieses Dokument sind.
  - **Bemerkungen**: Zeigt an, ob Genehmigungskommentare zum Einkaufsvertrag vorhanden sind.

- Zusätzliche Aktionen auf der Karte **Einkaufsverträge**:
  - **Erzwinge Genehmigung**: Erzwingt die Genehmigung des Einkaufsvertrags und umgeht den Genehmigungsablauf.
  - **Bemerkungen**: Öffnet die Seite **Genehmigungsbemerkungen**.

- Geänderte Aktionen auf der Karte **Einkaufsverträge**:
  - **Genehmigungen**: Öffnet die Seite **Einkaufsvertragsgenehmigungsanforderungen**, die über Funktionen wie **Genehmiger hinzufügen** und **Weiterleiten** verfügt.

- Wenn Sie eine Genehmigung ablehnen, wird die Seite **Genehmigungsbemerkung** geöffnet. Auf diese Weise können Sie vorherige Genehmigungskommentare anzeigen und einen Ablehnungskommentar hinzufügen.

- Die Weiterleitungsfunktion bietet drei Optionen:
  - **Genehmigen und weiterleiten**
  - **Ohne Genehmigung weiterleiten**
  - **Weiterleiten und Beleg nach Genehmigung an mich zurücksenden**

> [!TIP]
> Außer dem Symbol {{search}}, das in den folgenden Anleitungen verwendet wird, können Genehmiger und Genehmigungsadministratoren den Genehmigungsprozess auch mit den Stapeln in der Stapelgruppe **Einkaufsverträge** im Microsoft Dynamics 365 Business Central-Rollencenter verwalten:
>
> - **Alle**: Enthält alle Verträge und bietet allen Benutzern eine Übersicht.
> - **Genehmigung fällig**: Enthält Verträge, bei denen das **nächste Genehmigungsdatum** auf das aktuelle Datum oder ein beliebiges Datum davor festgelegt ist.
> - **Genehmigung erforderlich**: Enthält Verträge, bei denen der **Genehmigungsstatus** auf **Genehmigung erforderlich** gesetzt ist.
> - **Genehmigung ausstehend**: Enthält Verträge, bei denen der **Genehmigungsstatus** auf **Genehmigung ausstehend** gesetzt ist.

## So richten Sie einen Genehmigungsadministrator ein

Um Genehmigungen zu erzwingen, müssen Sie als Genehmigungsadministrator eingerichtet sein. Gehen Sie hierzu wie folgt vor:

1. Suchen Sie {{search}} nach **Continia Benutzereinrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie in der Liste der Continia-Benutzer auf die ID des Benutzers, den Sie als Genehmigungsadministrator einrichten möchten. Dadurch wird die **Continia Benutzereinrichtung Karte** geöffnet.
3. Aktivieren Sie im Inforegister **Allgemein** die Einstellung **Genehmigungsadministrator**.

## So senden Sie einen einzelnen Vertrag zur Genehmigung

Als Genehmigungsadministrator können Sie einen Vertrag folgendermaßen zur Genehmigung senden:

1. Suchen Sie {{search}} nach **Einkaufsverträge** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie in der Vertragsliste den Vertrag aus, den Sie zur Genehmigung senden möchten.
3. Klicken Sie in der Aktionsleiste auf **Genehmigen** > **Genehmigungsanfrage senden**.

Dadurch wird der Vertrag zur Genehmigung gesendet und das Feld **Status** im Inforegister **Genehmigungen** zeigt dann **Genehmigung ausstehend** an.

## So senden Sie mehrere Verträge zur Genehmigung

Als Genehmigungsadministrator können Sie mehrere Verträge folgendermaßen zur Genehmigung senden:

1. Suchen Sie {{search}} nach **Einkaufsverträge** und wählen Sie dann den entsprechenden Link aus.

2. Klicken Sie in der Aktionsleiste auf **Start** > **Genehmigungsanforderung senden**, um die Seite **Einkaufsverträge zur Genehmigung senden** zu öffnen.

3. Im Inforegister **Filter: Einkaufsvertragskopf** wird der Filter **Nächste Genehmigung am** hinzugefügt und mit dem Datumsbereich **..[heute]** automatisch gefüllt. So werden alle Verträge, die noch nicht überprüft wurden, und deren Datum in **Nächste Genehmigung am** überschritten wurde, alle zusammen zur Genehmigung gesendet. Sie können den automatisch ausgefüllten Datumsbereich auch ändern.

4. **Optional:** Um einen weiteren Filter hinzuzufügen, klicken Sie auf **+ Filter**.

5. **Optional:** Um den Stapelbericht zu einem späteren Zeitpunkt auszuführen, klicken Sie auf **Plan…** und wählen Sie dann ein Startdatum/eine Startzeit und ein Ablaufdatum/eine Ablaufzeit aus. Sie können auch eine Datumsformel eingeben, die das Feld **Früheste(s) Startdatum/-uhrzeit** automatisch ausfüllt.

   > [!NOTE]
   > Wenn Sie **Datumsformel für nächste Ausführung** auswählen, müssen Sie eine Formel in Form einer Ganzzahl gefolgt von **T** (Tage), **WT** (Wochentage), **W** (Wochen), **M** (Monaten), **Q** (Quartale) oder **J** (Jahre) eingeben, zum Beispiel **2W** (zwei Wochen). Für komplexere Formeln können Sie auch die mathematischen Symbole + und – verwenden oder den Buchstaben **L** (laufend) als Präfix für eine der zuvor genannten Zeiteinheiten eingeben – zum Beispiel **LM+10T** (der laufende Monat plus zehn Tage).

6. Klicken Sie auf **OK**, wenn Sie fertig sind.

Dadurch werden alle Verträge innerhalb des angegebenen Datumsbereichs zusammen zur Genehmigung gesendet, und das Feld **Status** im Inforegister **Genehmigungen** zeigt dann für alle Verträge **Genehmigung ausstehend** an.

## Automatische Aktualisierung des Genehmigungsstatus

Wenn Sie eine Änderung an einem oder mehreren der folgenden Zeilenfelder vornehmen, wird der Status eines Einkaufsvertrags ebenfalls automatisch auf **Genehmigung erforderlich** gesetzt:

- Kreditorennr.
- Einkäufercode
- Währungs- code
- Preistyp
- Abrechnungszeit-Code
- Vertragsbeginn
- Vertragsenddatum
- Autom. bestätigen innerhalb der Abweichung
- Genehmigung
- Datumsformel Genehmigung

Wenn Sie eine Änderung an einem oder mehreren der folgenden Kopffelder vornehmen, wird der Status eines Einkaufsvertrags automatisch auf **Genehmigung erforderlich** gesetzt:

- Art
- Nr.
- Preistyp
- Währungscode
- Menge
- Einstandspreis
- Betrag
- Status
- Preise inkl. MwSt.
- Betrag inkl. MwSt.
- Startdatum
- Enddatum
- Abrechnungsperiode

> [!NOTE]
> Das Löschen einer aktiven Einkaufsvertragszeile löst auch die Änderung des Genehmigungsstatus aus.

## So stornieren Sie eine Vertragsgenehmigungsanforderung

So brechen Sie eine von Ihnen gestartete Genehmigungsanforderung ab:

1. Suchen Sie {{search}} nach **Einkaufsverträge** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie in der Vertragsliste den Vertrag aus, dessen Genehmigung Sie abbrechen möchten.
3. Klicken Sie in der Aktionsleiste auf **Genehmigen** > **Genehmigungsanforderung stornieren**.

Auf der Seite **Einkaufsvertrag** wird im Feld **Genehmigungsstatus** im Inforegister **Genehmigungen** nicht mehr **Genehmigung ausstehend** angezeigt, sondern **Genehmigung erforderlich**.

## So reichen Sie eine Vertragsgenehmigung ein

Sobald Ihnen ein Vertrag von einem Genehmigungsadministrator zur Genehmigung zugesandt wurde, können Sie den Vertrag genehmigen. Sie können dies entweder in Business Central oder im Continia Web Approval Portal vornehmen.

### Mit Business Central

So führen Sie eine Genehmigung mit Business Central aus:

1. Suchen Sie {{search}} nach **Einkaufsverträge** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie in der Liste der Verträge in der Spalte **Nr.** auf die Nummer des Vertrags, den Sie genehmigen möchten. Dadurch wird die Seite **Einkaufsvertrag** geöffnet.
3. Überprüfen Sie den Vertrag.
4. Klicken Sie in der Aktionsleiste auf **Genehmigung anfordern** > **Genehmigen**.

Dadurch wird die Anforderung genehmigt und das Feld **Genehmigungsstatus** im Inforegister **Genehmigungen** zeigt anschließend **Freigegeben** an.

### Mit dem Web Approval Portal

So führen Sie eine Genehmigung mit dem Web Approval Portal aus:

1. Melden Sie sich am Web Approval Portal an.
2. Klicken Sie auf der Registerkarte auf **Einkauf** auf **Verträge**, um die Seite **Meine ausstehenden Genehmigungen** zu öffnen.
3. Wählen Sie in der Liste der zu genehmigenden Verträge den Vertrag aus, den Sie genehmigen möchten.
4. Genehmigen Sie den Vertrag.
5. Geben Sie im Textfeld oben rechts Ihre Kommentare ein und klicken Sie auf **Speichern**, wenn Sie fertig sind. Wiederholen Sie diesen Schritt, wenn Sie weitere Bemerkungen hinzufügen möchten.
6. Klicken Sie in der Aktionsleiste auf **Genehmigung einreichen**.

Dadurch wird Ihre Genehmigung an den Einkaufsgenehmigungsadministrator übermittelt. Außerdem wird in Business Central auf der Seite **Einkaufsvertrag** im Feld **Status** im Inforegister **Genehmigung** > **Genehmigung eingereicht** angezeigt.

## Informationen zum Thema

[Einkaufsverträge erstellen](@DC-86)\
[Vertragsrechnungen erstellen](@DC-88)\
[Vertragsrechnungen genehmigen](@DC-89)\
[Das Einkaufsvertragsarchiv anzeigen](@DC-90)