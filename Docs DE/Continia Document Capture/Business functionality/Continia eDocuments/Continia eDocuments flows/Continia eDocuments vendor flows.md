---
title: eDocuments-Kreditorflows
date: 15-10-2025
description: So senden Sie Verkaufsrechnungen und Bestellbestätigungen und erhalten Bestellungen.
id: DC-221
lang: de
---

# eDocuments-Kreditorflows

Dieser Artikel beschreibt die Aktionen, die Sie als Kreditor in den Continia eDocuments-Flows ausführen müssen. Die Aktionen sind Teile verschiedener Flows, wie unten beschrieben.

Informationen zu den entsprechenden Debitorflows finden Sie unter [eDocuments-Debitorflows](@DC-220).

## Bestellung

### So importieren und registrieren Sie einen Verkaufsauftrag

So importieren und registrieren Sie einen Verkaufsauftrag:

1. Gehen Sie im Rollencenter unter **Continia Document Capture Aktivitäten** zu **Aktionen** > **Dateien importieren**.

2. Der Verkaufsauftrag steht anschließend im Stapel **Bereit zur Registrierung** zur Verfügung. Wählen Sie diesen Stapel aus, um das Belegjournal zu öffnen.

3. Klicken Sie in der Aktionsleiste auf **Dokument**.
   1. **Optional**: Um alle verfügbaren Informationen für den Verkaufsauftrag anzuzeigen, wählen Sie **eDokumentenkarte** in der Aktionsleiste, um die Seite **eBestellungsdokument** zu öffnen. Schließen Sie die Seite, um zum Belegjournal zurückzukehren, wenn Sie fertig sind.
   2. Wenn der Verkaufsauftrag Bestellzeilen enthält und Sie Übersetzungen oder ähnliches einrichten müssen, wählen Sie **Dokumentenkarte** in der Aktionsleiste aus, um die Dokumentenkarte zu öffnen.

4. Auf der Dokumentenkarte können Sie die üblichen Funktionen von Document Capture ausführen. Wenn Sie mit dem Verkaufsauftrag zufrieden sind und keine Warnungen angezeigt werden, wählen Sie in der Aktionsleiste **Start** > **Registrieren** aus, um den Verkaufsauftrag zu registrieren und einen Verkaufsauftrag zu erstellen.

### So bestätigen Sie einen Verkaufsauftrag

So bestätigen Sie einen Verkaufsauftrag nach der Registrierung:

- Wählen Sie auf der Seite **Verkaufsauftrag** in der Aktionsleiste **Aktionen > eDokumente > Bestätigen** aus.

> [!NOTE]
> Die Aktion heißt **Bestätigen**, auch wenn Sie die Reihenfolge ändern. Stellen Sie daher sicher, dass keine unerwünschten Änderungen vorgenommen wurden. Beispielsweise könnte der Preis eines Artikels auf Ihrer Seite anders sein.

### So lehnen Sie einen Verkaufsauftrag ab

So lehnen Sie einen Verkaufsauftrag ab:

1. Wählen Sie im Belegjournal oder auf der Dokumentenkarte in der Aktionsleiste **Ablehnen** aus.
2. Wählen Sie **Aktionen > Funktionen > eBestellung Ablehnungsantwort senden**, um dem Debitor die Ablehnung mitzuteilen.

### So stornieren Sie einen Verkaufsauftrag

So stornieren Sie einen Verkaufsauftrag nach der Registrierung:

- Wählen Sie auf der Seite **Verkaufsauftrag** in der Aktionsleiste **Aktionen > eDokumente > Stornieren** aus.

> [!TIP]
> Sie können einen Auftrage jederzeit stornieren, auch vor oder nach der Bestätigung.

### So ändern Sie einen Verkaufsauftrag vor der Bestätigung

So ändern Sie einen registrierten Verkaufsauftrag, bevor Sie ihn bestätigen:

1. Nehmen Sie auf der Seite **Verkaufsauftrag** die erforderlichen Änderungen am Auftrag vor.
2. Klicken Sie in der Aktionsleiste auf**Aktionen > eDokumente > Bestätigen**.
3. Wenn der Debitor die von Ihnen vorgeschlagenen Änderungen akzeptiert, registrieren Sie den bestätigten Verkaufsauftrag.

> [!NOTE]
> Pro Beleg kann nur eine Änderung übermittelt werden. Wenn Sie oder der Debitor beispielsweise eine Preis- oder Mengenänderung übermitteln, kann die andere Partei keine weiteren Änderungen übermitteln. Zusätzliche Änderungen werden als Fehler im Abschnitt **Kommentare** im Belegjournal oder auf der Dokumentenkarte angezeigt.

### So bestätigen Sie einen geänderten Verkaufsauftrag

So bestätigen Sie einen vom Debitor geänderten Verkaufsauftrag:

1. Überprüfen Sie im Belegjournal oder auf der Dokumentenkarte die vom Debitor gewünschten Änderungen im Bereich **Kommentare**.
2. **Optional**: Für eine detailliertere Übersicht über die vom Debitor gewünschten Änderungen wählen Sie in der Aktionsleiste **Start > Bestellabgleich**.
3. Wählen Sie in der Aktionsleiste **Registrieren** aus.
4. Wählen Sie auf der Seite **Verkaufsauftrag** in der Aktionsleiste **Aktionen > eDokumente > Änderungen bestätigen** aus.

### So aktualisieren Sie einen bestätigten Verkaufsauftrag

So aktualisieren Sie einen Verkaufsauftrag, der von beiden Parteien bestätigt wurde:

1. Nehmen Sie auf der Seite **Verkaufsauftrag** die erforderlichen Änderungen am Auftrag vor.
2. Wählen Sie in der Aktionsleiste **Aktionen > eDocuments > Aktualisieren**.
3. Wenn der Debitor die von Ihnen vorgeschlagenen Änderungen akzeptiert, registrieren Sie den bestätigten Verkaufsauftrag.

### So bestätigen Sie die Stornierung eines Verkaufsauftrags

So bestätigen Sie die Stornierung eines Verkaufsauftrags nach der Registrierung:

- Wählen Sie auf der Seite **Verkaufsauftrag** in der Aktionsleiste **Aktionen > eDokumente > Stornierung bestätigen** aus.

### So lehnen Sie die Stornierung eines Verkaufsauftrags ab

So lehnen Sie die Stornierung eines Verkaufsauftrags ab:

1. Wählen Sie im Belegjournal oder auf der Dokumentenkarte in der Aktionsleiste **Start** > **Ablehnen** aus.
2. Wählen Sie in der Aktionsleiste **Aktionen > Funktionen > eBestellung Ablehnungsantwort senden**, um dem Debitor die Ablehnung mitzuteilen.

> [!NOTE]
> Pro Beleg kann nur eine Änderung übermittelt werden. Wenn Sie oder der Debitor beispielsweise eine Preis- oder Mengenänderung übermitteln, kann die andere Partei keine weiteren Änderungen übermitteln. Zusätzliche Änderungen werden als Fehler im Abschnitt **Kommentare** im Belegjournal oder auf der Dokumentenkarte angezeigt.

## Abrechnung

### So senden Sie eine Verkaufsrechnung

So erstellen und versenden Sie eine Verkaufsrechnung:

1. Erstellen Sie eine Verkaufsrechnung, indem Sie beispielsweise einen Verkaufsauftrag buchen, den Sie im Rahmen eines Bestellflows von einem Debitor erhalten haben.
2. Wählen Sie auf der Seite **Gebuchte Verkaufsrechnung** in der Aktionsleiste **Drucken/Senden** > **Senden** aus, um das Dialogfeld **Dokument senden an** zu öffnen.
3. Wählen Sie im Dropdown-Menü **Elektronischer Beleg** die Option **Über Continia Delivery Network** aus. Wählen Sie zur Bestätigung **OK** und dann erneut **OK**, um zur Seite **Gebuchte Verkaufsrechnung** zurückzukehren.
4. Aktivieren Sie im Inforegister **Allgemein** [das Feld **eDokumentenstatus**](@DC-183#das-edokumentenstatus-feld):
   - **Gesendet** – die Verkaufsrechnung wurde an den Debitor gesendet.
   - **In Bearbeitung** – die Verkaufsrechnung wurde an das Netzwerk gesendet, es liegt jedoch keine Empfangs- oder Fehlerbestätigung vor.
   - **Fehlgeschlagen** – das Senden der Verkaufsrechnung ist aufgrund eines Netzwerkproblems fehlgeschlagen.
   - **Ungültig** – wählen Sie diesen Text aus, um entweder die Seite **eAbrechnungsdokument** (wenn der Rechnung keine zugehörige eBestellung zugeordnet ist) oder die Seite **eDokument Übersicht** (wenn eine zugehörige eBestellung vorhanden ist) zu öffnen. Wenn die Seite **eDokument Übersicht** geöffnet wird, suchen Sie das eAbrechnungsdokument und wählen Sie es aus, um die Seite **Abrechnungsdokument** zu öffnen. Gehen Sie dann wie folgt vor:
     1. Klicken Sie in der Aktionsleiste auf **Validierungsprotokoll**, um die Seite **eValidierungsprotokoll** zu öffnen, auf der Validierungsfehler aufgelistet sind.
     2. Beachten Sie die **detaillierte Fehlermeldung**, schließen Sie das Protokoll, um zur Seite **eAbrechnungsdokument** zurückzukehren, und beheben Sie dann die aufgeführten Validierungsfehler.
     3. Wenn Sie fertig sind, wählen Sie in der Aktionsleiste **Erneut senden** aus, um die überarbeitete Verkaufsrechnung an den Debitor zu senden.

Die Verkaufsrechnung wurde anschließend an den Debitor gesendet, der sie wie unter [So empfangen Sie eine Rechnung und senden eine Rechnungsantwort](@DC-220#so-empfangen-sie-eine-rechnung-und-senden-eine-rechnungsantwort) beschrieben verarbeiten kann.

**So senden Sie ein eAbrechnungsdokument erneut**

In bestimmten Fällen ist es möglicherweise erforderlich, ein bereits erfolgreich versendetes eAbrechnungsdokument erneut zu versenden. Zum Beispiel, wenn ein Empfänger eine Kopie des Dokuments benötigt. So senden Sie ein eAbrechnungsdokument erneut:

> [!NOTE]
> Diese Aktion ist nur in elektronischen Dokumentformaten mit dem **Copy Indicator**-Feld verfügbar, beispielsweise im dänischen OIOUBL-Format.

1. Suchen Sie ({{search}}) nach **Gesendete Netzwerkdokumente** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie das Dokument aus, das Sie erneut senden möchten. Beachten Sie, dass nur Dokumente mit dem **eDokumentenstatus** „Erfolgreich“ erneut gesendet werden können.
3. Klicken Sie in der Aktionsleiste auf **Aktionen** > **Erneut senden**. Alternativ können Sie auf **eDokumentenkarte** klicken und auf der Seite **eBestellungsantwort** in der Aktionsleiste auf **Erneut senden** klicken.

Es wird ein zusätzlicher eDocument-Datensatz im Continia Delivery Network (CDN) erstellt und die Kopie automatisch gesendet.

> [!TIP]
> Um zu überprüfen, ob ein gesendetes eDokument eine Kopie ist, gehen Sie auf die Seite **Gesendete Netzwerkdokumente** und suchen Sie den Wert in der Spalte **Kopie**.

## So antworten Sie automatisch über eDocuments

Anstatt auf jede Bestellung oder Rechnung manuell zu antworten, können Sie Continia eDocuments so konfigurieren, dass basierend auf einer Aktion automatisch eine Antwort gesendet wird.

So konfigurieren Sie Ihre automatischen eDocuments-Antworten:

1. Suchen Sie {{search}} nach **Continia eDokument Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Konfigurieren Sie auf dem Inforegister **eDokument Antwort** unter **eBestellungsantwort** die folgenden Einstellungen:

   - **Aktualisierungen senden** – wählen Sie diese Option, wann Sie benachrichtigt werden möchten, dass die Bestellung aktualisiert wurde. Beispielsweise bei der Registrierung der Bestellung.
   - **Abgelehnt senden** – wählen Sie diese Option, wann Sie benachrichtigt werden möchten, dass die Bestellung abgelehnt wurde.

## Informationen zum Thema

[Continia eDocuments-Flows](@DC-183)\
[Continia eDocuments-Debitorflows](@DC-220)