---
title: eDocuments-Debitorflows
date: 15-10-2025
description: So senden Sie Bestell- und Rechnungsantworten, erfassen Bestellantworten und empfangen Rechnungen.
id: DC-220
lang: de
---

# eDocuments-Debitorflows

Dieser Artikel beschreibt die Aktionen, die Sie als Debitor in den Continia eDocuments-Flows ausführen müssen. Diese Aktionen sind Teile verschiedener Flows, wie unten beschrieben.

Informationen zu den entsprechenden Kreditorflows finden Sie unter [eDocuments-Kreditorflows](@DC-221).

## Bestellung

### So senden Sie eine Bestellung

So erstellen und senden Sie eine Einkaufsbestellung:

1. Erstellen Sie eine Bestellung, wie unter [Eine Einkaufsrechnung erstellen und buchen](https://learn.microsoft.com/de-de/dynamics365/business-central/purchasing-how-record-purchases?wt.mc_id=d365bc_inproduct_helppane#create-and-post-a-purchase-invoice) (Microsoft-Artikel) beschrieben. Klicken Sie in der Aktionsleiste auf der Seite **Einkaufsbestellungen** auf **Neu**, um die Seite **Einkaufsbestellung** zu öffnen, und geben Sie dann die erforderlichen Details wie beschrieben ein.
2. Klicken Sie in der Aktionsleiste auf **Drucken/Senden** > **Senden**, um das Dialogfeld **Beleg senden an** zu öffnen.
3. Wählen Sie in der Dropdown-Liste **Elektronischer Beleg** die Option **Über Continia Delivery Network** aus. Klicken Sie zur Bestätigung auf **OK** und dann erneut auf **OK**, um zur Seite **Einkaufsbestellung** zurückzukehren.
4. Aktivieren Sie im Inforegister **Allgemein** [das Feld **eDokumentenstatus**](@DC-183#das-edokumentenstatus-feld):
   - **Gesendet** – die Bestellung wurde an den Kreditor gesendet.
   - **In Bearbeitung** – die Bestellung wurde an das Netzwerk gesendet, es liegt jedoch keine Empfangs- oder Fehlerbestätigung vor.
   - **Fehlgeschlagen** – das Senden der Bestellung ist aufgrund eines Netzwerkproblems fehlgeschlagen.
   - **Ungültig** – klicken Sie auf diese Option, um die Seite **eBestellungsdokumente** zu öffnen, und gehen Sie dann wie folgt vor:
     1. Klicken Sie in der Aktionsleiste auf **Validierungsprotokoll**, um die Seite **eValidierungsprotokoll** zu öffnen, auf der Validierungsfehler aufgelistet sind.
     2. Beachten Sie die **detaillierte Fehlermeldung**, schließen Sie das Protokoll, um zur Seite **eBestellungsdokument** zurückzukehren, und beheben Sie dann die aufgeführten Validierungsfehler.
     3. Wenn Sie fertig sind, klicken Sie in der Aktionsleiste auf **Erneut senden**, um die überarbeitete Bestellung an den Lieferanten zu senden.

Die Bestellung wurde anschließend an den Kreditor gesendet, der sie wie unter [So importieren und registrieren Sie einen Verkaufsauftrag](@DC-221#so-importieren-und-registrieren-sie-einen-verkaufsauftrag) beschrieben verarbeiten kann.

### So registrieren Sie eine Bestellantwort

So importieren und registrieren Sie die Bestellantwort eines Kreditors:

1. Gehen Sie im Rollencenter unter **Continia Document Capture Aktivitäten** zu **Aktionen** und klicken Sie auf **Dateien importieren**.
2. Die Bestellantwort kann jetzt registriert werden und ist im Stapel **Bereit zur Registrierung** verfügbar. Klicken Sie auf diesen, um das Belegjournal zu öffnen.
3. Klicken Sie in der Aktionsleiste auf **Dokument** > **Dokumentenkarte**, um die Dokumentenkarte zu öffnen.
4. Wenn der Kreditor Änderungen an Zeilen vorgenommen hat, werden diese im Inforegister **Zeilen** angezeigt.
   > [!NOTE]
   > Hier werden nur die tatsächlichen Änderungen angezeigt; weitere Zeilendetails bezüglich Menge, Preis, Maßeinheit und ähnlichem sind nicht sichtbar.> Um den vollständigen Kontext der Zeilenänderungen (vorher und nachher) zu sehen, wählen Sie in der Aktionsleiste **Vorschau Bestelländerungen** aus, um die Seite **Vorschau Bestelländerungen** zu öffnen.
   > Um den vollständigen Kontext der Zeilenänderungen (vorher und nachher) zu sehen, klicken Sie in der Aktionsleiste auf **Vorschau Bestelländerungen**, um die Seite **Vorschau Bestelländerungen** zu öffnen.
5. Der Abschnitt **Bestellzeilen** bietet eine Übersicht über die ursprünglichen Positionen und ihre Details, während der Abschnitt **Geänderte Zeilen** die Zeilen so auflistet, wie sie nach der Änderung durch den Kreditor aussehen. Überprüfen Sie die Änderungen und schließen Sie dann die Seite, um zur Dokumentenkarte zurückzukehren.
6. Klicken Sie in der Aktionsleiste auf **Start** > **Registrieren**, um die neue Bestellantwort zu registrieren.

Die Bestellantwort wird registriert und die Bestellung automatisch geöffnet und mit den Änderungen aus der Bestellbestätigung aktualisiert.

> [!NOTE]
> Pro Beleg kann nur eine Änderung übermittelt werden. Wenn Sie oder der Kreditor beispielsweise eine Preis- oder Mengenänderung übermitteln, kann die andere Partei keine weiteren Änderungen übermitteln.

> [!TIP]
> Um eine Übersicht über die vom Kreditor vorgenommenen Änderungen zu erhalten, klicken Sie in der Aktionsleiste der Dokumentkarte oder des Belegjournals auf **Start** > **Bestellabgleich**.

### So ändern Sie eine bestätigte Einkaufsbestellung

So ändern Sie eine vom Kreditor bestätigte Bestellung, nachdem Sie die Bestellantwort registriert haben:

1. Nehmen Sie auf der Seite **Bestellung** die erforderlichen Änderungen an der Bestellung vor.
2. Klicken Sie in der Aktionsleiste auf **Aktionen > eDokumente > Aktualisieren**.

### So bestätigen Sie eine geänderte Bestellung

So bestätigen Sie eine vom Kreditor geänderte Bestellung, nachdem Sie die Bestellantwort registriert haben:

- Klicken Sie auf der Seite **Bestellung** in der Aktionsleiste auf **Aktionen** > **eDokumente** > **Änderungen bestätigen**.

### So stornieren Sie eine geänderte Bestellung

So stornieren Sie eine vom Kreditor geänderte Bestellung, nachdem Sie die Bestellantwort registriert haben:

1. Klicken Sie auf der Seite **Bestellung** in der Aktionsleiste auf **Aktionen** > **eDokumente** > **Stornieren**.
2. Die Seite **eBestellungsdokument** wird geöffnet. Geben Sie auf dem Inforegister **Allgemein** im Feld **Stornierungshinweis** einen Grund ein.
3. Klicken Sie in der Aktionsleiste auf **Senden**.

> [!NOTE]
> Obwohl eine vom Kreditor übermittelte Stornierung endgültig ist, können von einem Debitor übermittelte Stornierungen vom Kreditor entweder akzeptiert oder abgelehnt werden.

## Abrechnung

### So empfangen Sie eine Rechnung und senden eine Rechnungsantwort

Als Debitor können Sie eine Einkaufsrechnung importieren und eine Rechnungsantwort zurücksenden, indem Sie die folgenden Schritte ausführen:

1. Gehen Sie im Rollencenter unter **Continia Document Capture Aktivitäten** zu **Aktionen** und klicken Sie auf **Dateien importieren**.
2. Die Einkaufsrechnung steht anschließend im Stapel **Bereit zur Registrierung** zur Verfügung. Klicken Sie auf diesen Stapel, um das Belegjournal zu öffnen.
3. Klicken Sie in der Aktionsleiste auf **Dokument**.
   1. **Optional**: Um alle verfügbaren Informationen zur Einkaufsrechnung anzuzeigen, klicken Sie auf **eDokumentkarte**, um die Seite **eBestellungsdokument** zu öffnen. Schließen Sie die Seite, um zum Belegjournal zurückzukehren, wenn Sie fertig sind.
   2. Wenn die Einkaufsrechnung Rechnungszeilen enthält und Sie zum Beispiel Übersetzungen einrichten müssen, wählen Sie **Dokumentenkarte** aus, um die Dokumentenkarte zu öffnen.
4. Auf der Dokumentenkarte können Sie die üblichen Funktionen von Document Capture ausführen, wie zum Beispiel den [Belegabgleich](@DC-61). Um den Abgleich durchzuführen, wählen Sie **Start** > **Zeilen abgleichen**. Nehmen Sie alle erforderlichen Anpassungen vor, um den Abgleichvorgang abzuschließen.
5. Wenn Sie mit der Einkaufsrechnung fertig sind und keine Warnungen angezeigt werden, klicken Sie in der Aktionsleiste auf **Registrieren**, um die Einkaufsrechnung zu registrieren.
6. Die Seite **Einkaufsrechnung** wird geöffnet. Von hier aus können Sie dem Kreditor manuell mitteilen, dass Sie die Rechnung angenommen, abgelehnt oder bezahlt haben, dass Sie sie bearbeiten oder Fragen haben.

   1. Klicken Sie in der Aktionsleiste auf **Rechnung** > **Elektronische Bestätigung senden**.
   2. Klicken Sie im sich öffnenden Dialogfeld auf die entsprechende Option, z. B. **Akzeptiert**, und klicken Sie anschließend auf **OK**, um das Dialogfeld zu schließen.
   3. Die Seite **eAbrechnungsantwort** wird geöffnet. Wählen Sie auf der Inforegisterkarte **Antwort** unter **Antwortcode** bei Bedarf einen Antwortcode aus.
   4. Wählen Sie auf der Inforegisterkarte **Grund** einen Ursachencode aus und geben Sie ggf. Ihre Kommentare für den Kreditor ein. In manchen Fällen wird das Dokument erst versendet, wenn Sie hier einen Kommentar eingeben.
   5. Klicken Sie in der Aktionsleiste auf **Senden**, um Ihre Antwort an den Kreditor zu senden.

   ## So antworten Sie automatisch über eDocuments

   Anstatt auf jede Bestellung oder Rechnung manuell zu antworten, können Sie Continia eDocuments so konfigurieren, dass basierend auf einer Aktion automatisch eine Antwort gesendet wird. Beachten Sie, dass nicht alle Antworten automatisierbar sind.

   So konfigurieren Sie Ihre automatischen eDocuments-Antworten:

   1. Suchen Sie {{search}} nach **Continia eDokument Einrichtung** und wählen Sie dann den entsprechenden Link aus.
   2. Konfigurieren Sie auf dem Inforegister **eDokument Antwort** unter **eAbrechnungsantwort** die folgenden Einstellungen:

   - **Senden in Bearbeitung** – wählen Sie diese Option, wann Sie benachrichtigt werden möchten, wenn die Rechnung sich in Bearbeitung befindet. Beispielsweise bei der Freigabe des Dokuments.
   - **Akzeptiert senden** – wählen Sie diese Option, wann Sie benachrichtigt werden möchten, dass die Rechnung akzeptiert wurde. Beispielsweise bei Import des Dokuments.
   - **Abgelehnt senden** – wählen Sie diese Option, wann Sie benachrichtigt werden möchten, dass die Rechnung abgelehnt wurde.

## Informationen zum Thema

[eDocuments-Flows](@DC-183)\
[eDocuments-Kreditorenflows](@DC-221)