---
title: Debitoren und Kreditoren für Continia eDocuments einrichten
date: 17-09-2025
description: So richten Sie Debitoren und Kreditoren für die Verwendung von Continia eDocuments ein.
id: DC-180
lang: de
---

# Debitoren und Kreditoren für Continia eDocuments einrichten

Nachdem Sie [Continia eDocuments aktiviert](@DC-178) und [eingerichtet](@DC-179) haben, müssen Sie Ihre Kreditoren und/oder Debitoren einrichten. Dies wird in den folgenden Abschnitten beschrieben.

## Überprüfen, ob ein Geschäftspartner eDokumente empfangen kann

Obwohl Sie davon ausgehen können, dass ein Debitor oder Kreditor, mit dem Sie Geschäfte machen, in der Regel Dokumente empfangen kann, ist nicht immer klar, ob dieser auch eDokumente empfangen kann. Mit Continia eDocuments können Sie überprüfen, ob der Debitor/Kreditor, dem Sie ein eDokument senden müssen, dieses auch empfangen kann.

So aktivieren Sie diese Funktion:

1. Suchen Sie {{search}} nach **Continia eDokument Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Aktivieren Sie im Inforegister **Automatisierungen** die Einstellung **Aktualisierung der Funktionen für den Empfang von Dokumenten**.
3. Der Status von **Aktualisierung der Funktionen für den Empfang von Dokumenten** ändert sich anschließend in **Bereit** und zeigt damit an, dass die Aufgabe, die für die Aktualisierung des eDocuments-Teilnahmecaches zuständig ist, ausgeführt wird.

Sie können jetzt überprüfen, ob ein Debitor oder Kreditor Teil eines eDocuments-Netzwerks ist. Die folgenden Anweisungen verwenden Kreditoren als Beispiel:

1. Suchen Sie ({{search}}) nach **Kreditoren** und wählen Sie den entsprechenden Link aus.
2. Klicken Sie auf der Seite **Kreditoren** auf **Zugehörig** > **Kreditor** > **Continia eDokumente Einrichtung**.
3. Wenn die Infobox **eDocuments Empfangsmöglichkeiten** leer ist, klicken Sie in der Aktionsleiste auf **eDocuments Empfangsmöglichkeiten erneut prüfen** aus. Sobald die Infobox Informationen enthält, können Sie die Dokumenttypen sehen, die der Kreditor empfangen kann und über welches Netzwerk.

Wenn Sie versuchen, ein eDokument an einen Debitor oder Kreditor zu senden, der es nicht empfangen kann, wird eine Fehlermeldung mit Angaben zum Grund angezeigt. Beispielsweise könnte der Empfänger nicht im Netzwerk registriert sein.

## Debitoren und Kreditoren einrichten

Es gibt zwei Möglichkeiten, Geschäftspartner so einzurichten, dass ihre Netzwerkverbindungseinstellungen mit Ihren konfigurierten Einstellungen übereinstimmen.

Empfohlen wird die [Verwendung der eCandidates-Funktion](#to-automatically-set-up-customers-and-vendors), die eine automatische Erkennung und Netzwerkregistrierung der Teilnehmer ermöglicht. Identifizierte Teilnehmer können dann einzeln oder in Gruppen verbunden werden, was den Prozess erheblich beschleunigt.

Es ist jedoch auch möglich, [Debitoren](#to-manually-set-up-customers) und [Kreditoren](#to-manually-set-up-vendors) manuell einzurichten. Beide Methoden werden hier behandelt.

### So richten Sie Debitoren und Kreditoren automatisch ein

1. Suchen Sie ({{search}}) nach **eCandidates** und wählen Sie den entsprechenden Link aus.
2. Wenn in der Tabelle keine eCandidates angezeigt werden, klicken Sie in der Aktionsleiste auf **Liste aktualisieren**.

> [!NOTE]
> Wenn Sie in der Tabelle immer noch keine eCandidates sehen, klicken Sie auf **Show all eCandidates**, um diejenigen aufzulisten, die derzeit in keinem der Netzwerke registriert sind, an denen Sie teilnehmen.

3. Bevor Sie eine Verbindungsmethode auswählen, überprüfen Sie die Werte in der Spalte **Netzwerkregistrierungen**, da Ihre eCandidates möglicherweise in verschiedenen Netzwerken registriert sind.
4. Wählen Sie die gewünschten eCandidates aus und klicken Sie in der Aktionsleiste auf **Verbinden**. Alternativ können Sie in der Aktionsleiste auf **Batch Connect** klicken, um alle aufgelisteten eCandidates auf einmal zu verbinden.

> [!TIP]
> Um schnell einen Debitor oder Kreditor zu suchen, wählen Sie ihn aus und klicken Sie in der Aktionsleiste auf **Debitor anzeigen** oder **Kreditor anzeigen**, um die zugehörige Karte zu öffnen.

5. Überprüfen Sie im Dialogfeld **Connect eCandidates** unter **eDocuments** den Wert des Felds **Von Teilnahme** und wählen Sie einen Wert für das Feld **Elektronisches Format** aus. Beachten Sie, dass bei Verwendung der Batch-Connect-Methode alle eCandidates im selben Netzwerk registriert sein müssen, das unter **Von der Teilnahme** ausgewählt wurde – und dass sie das unter **Elektronisches Format** festgelegte Format empfangen können müssen.

6. Passen Sie unter **eDocuments automatisch senden** bei Bedarf die Werte der Felder **Debitor** und **Kreditor** an. Wenn Sie fertig sind, klicken Sie auf **OK**.

7. Ein Dialogfeld bestätigt, wie viele eCandidates (falls vorhanden) verbunden wurden. Führen Sie den Vorgang bei Bedarf erneut durch und verwenden Sie dabei andere Werte für **Von Teilnahme** und/oder **Elektronisches Format**.

Sie können jetzt Continia eDocuments verwenden, um elektronische Dokumente an die verbundenen Geschäftspartner zu senden.

> [!NOTE]
> Wenn viele Debitoren und Kreditoren mit Ihrem Unternehmen verknüpft sind, kann die Überprüfung, ob sie über aktive Registrierungen in den unterstützten Netzwerken verfügen, zeitaufwändig sein. Um diesen Vorgang zu beschleunigen, befolgen Sie die ersten Anweisungen unter [Überprüfen der eDocument-Empfangsfunktionen](#checking-a-business-partners-edocument-receiving-capabilities).

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src=https://player.vimeo.com/video/1116129248?h=fce8677bab&badge=0&autopause=0&player_id=0&app_id=58479%22 frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="DC_Welcome_to_Document_Capture"></iframe></div><script src=https://player.vimeo.com/api/player.js></script>

### So richten Sie Debitoren manuell ein

1. Suchen Sie ({{search}}) nach **Debitoren** und wählen Sie den entsprechenden Link aus.

> [!TIP]
> Alternativ klicken Sie auf **Debitoren** in der Navigationsleiste im Rollencenter.

<ol start="2">
<li>Klicken Sie auf der Seite <strong>Debitoren</strong> auf den Namen des Debitors, den Sie für Continia eDocuments einrichten möchten. Dadurch wird die <strong>Debitorenkarte</strong> geöffnet.</li>
<li>Klicken Sie in der Aktionsleiste auf <strong>Zugehörig</strong>> <strong>Debitor</strong> > <strong>Continia eDocuments Einrichtung</strong>, um die Seite <strong>Continia eDokument Debitoreinrichtung</strong> zu öffnen.</li>
<li>Geben Sie im Inforegister <strong>Allgemein</strong> mithilfe der Felder auf der linken Seite an, wie Sie als Kreditor Dokumente mit dem ausgewählten Debitor austauschen möchten:</li>
<ul>
<li>Im elektronischen Format senden: Wählen Sie das elektronische Format aus, das Sie zum Senden elektronischer Dokumente an diesen Debitor verwenden möchten.</li>
<li>Sende von Teilnahme: Wählen Sie die Teilnahme aus, die Sie beim Senden elektronischer Dokumente an diesen Debitor verwenden möchten. Weitere Informationen zu Teilnahmen finden Sie unter <a href="https://docs.continia.com/en-us/continia-document-capture/setting-up-document-capture/setting-up-general-business-functionality/setting-up-the-continia-delivery-network#the-list-of-participations">Das Continia Delivery Network einrichten</a>.</li>
<li>E-Dokumente automatisch senden: Wählen Sie aus, welche Dokumente ggf. beim Buchen automatisch gesendet werden sollen.</li>
</ul>
</ol>
<ol start="5">
<li>Geben Sie auf der rechten Seite im Inforegister unter <strong>Debitoridentifikation</strong> an, wie der Debitor identifiziert werden soll:</li>
<ol type="a">
<li>Wählen Sie unter <strong>Empfängertyp</strong> die Art der ID aus, die Sie zur Identifizierung des Debitors verwenden möchten.</li>
<li>Wenn Sie in Schritt 5a oben unter <strong>Empfängertyp</strong> > <strong>Sonstiges</strong> ausgewählt haben, klicken Sie auf die drei Punkte auf der rechten Seite des Felds <strong>Empfänger-ID Art</strong>, um die Seite <strong>Continia Delivery Network Kennzeichen</strong> zu öffnen. Wählen Sie in der Liste die Kennungen aus, die Sie für diesen Debitor verwenden möchten, und klicken Sie dann auf <strong>OK</strong>, um zur Seite <strong>Continia eDokument Debitoreinrichtung</strong> zurückzukehren.</li>
</ol>
</ol>

> [!NOTE]
> Wenn Sie in Schritt 5a **USt.-IdNr.** oder **GLN** ausgewählt haben, ist das Feld **Empfänger-ID Art** nicht verfügbar und wird automatisch mit der richtigen Kennung basierend auf Ihrer Auswahl und den zugehörigen Metadaten ausgefüllt, die im Continia Delivery Network verfügbar sind.

<ol>
<ol type="a" start="3">
<li>Geben Sie unter <strong>Empfänger-ID</strong> die genaue ID des Debitors ein, sofern diese nicht automatisch ausgefüllt wurde.</li>
</ol>
</ol>

> [!NOTE]
> Wenn Sie wie in Schritt 5b in Schritt 5a **USt-IdNr.** oder **GLN** ausgewählt haben, wird das Feld **Empfänger-ID** automatisch mit der richtigen ID ausgefüllt, sofern dies für den ausgewählten Debitor verfügbar ist.

<ol start="6">
<li><strong>Optional</strong>: Nehmen Sie im Inforegister <strong>Exporteinrichtung</strong> bei Bedarf die gewünschten Anpassungen an den Einstellungen vor.</li>
<li>Gehen Sie zurück zur <strong>Debitorenkarte</strong>.</li>
<li>Gehen Sie im Inforegister <strong>Allgemein</strong> zu <strong>Belegsendeprofil</strong> und wählen Sie <strong>CONTINIAEDOCUMENTS</strong> aus.</li>
<li>Wiederholen Sie die Schritte 2–8 für alle weiteren Debitoren, die Sie einrichten möchten.</li>
</ol>
Die Einrichtung ist jetzt vollständig abgeschlossen und Sie können mit Continia eDocuments elektronische Dokumente an die ausgewählten Debitoren senden. Bei Bedarf können Sie auch später jederzeit andere Debitoren hinzufügen.

### So richten Sie Kreditoren manuell ein

1. Suchen Sie ({{search}}) nach **Kreditoren** und wählen Sie den entsprechenden Eintrag aus.

> [!TIP]
> Alternativ klicken Sie auf **Kreditoren** in der Navigationsleiste im Rollencenter.

<ol start="2">
<li>Wählen Sie auf der Seite <strong>Kreditoren</strong> den Namen des Kreditors aus, den Sie für Continia eDocuments einrichten möchten. Dadurch wird die <strong>Kreditorenkarte</strong> geöffnet.</li>
<li>Klicken Sie in der Aktionsleiste auf <strong>Zugehörig</strong>> <strong>Kreditor</strong> > <strong>Continia eDokumente Einrichtung</strong>, um die Seite <strong>Continia eDokument Kreditoreinrichtung</strong> zu öffnen.</li>
<li>Geben Sie im Inforegister <strong>Allgemein</strong> mithilfe der Felder auf der linken Seite an, wie Sie als Debitor Dokumente mit dem ausgewählten Kreditor austauschen möchten:</li>
<ul>
<li>Im elektronischen Format senden: Wählen Sie das elektronische Format aus, das Sie zum Senden elektronischer Dokumente an diesen Kreditor verwenden möchten.</li>
<li>Sende von Teilnahme: Wählen Sie die Teilnahme aus, die Sie beim Senden elektronischer Dokumente an diesen Kreditor verwenden möchten. Weitere Informationen zu Teilnahmen finden Sie unter <a href="https://docs.continia.com/en-us/continia-document-capture/setting-up-document-capture/setting-up-general-business-functionality/setting-up-the-continia-delivery-network#the-list-of-participations">Das Continia Delivery Network einrichten</a>.</li>
<li>Bestellungen automatisch senden: Aktivieren Sie dies, wenn Bestellungen nach Freigabe automatisch gesendet werden sollen.</li>
</ul>
</ol>
<ol start="5">
<li>Geben Sie auf der rechten Seite im Inforegister unter <strong>Kreditoridentifikation</strong> an, wie der Kreditor identifiziert werden soll:</li>
<ol type="a">
<li>Wählen Sie unter <strong>Empfängertyp</strong> die Art der ID aus, die Sie zur Identifizierung des Kreditors verwenden möchten.</li>
<li>Wenn Sie in Schritt 5a oben unter <strong>Empfängertyp</strong> > <strong>Sonstiges</strong> ausgewählt haben, klicken Sie auf die drei Punkte auf der rechten Seite des Felds <strong>Empfänger-ID Art</strong>, um die Seite <strong>Continia Delivery Network Kennzeichen</strong> zu öffnen. Wählen Sie in der Liste die Kennungen aus, die Sie für diesen Kreditor verwenden möchten, und klicken Sie dann auf <strong>OK</strong>, um zur Seite <strong>Continia eDokument Kreditoreinrichtung</strong> zurückzukehren.</li></ol>
</ol>

> [!NOTE]
> Wenn Sie in Schritt 5a **USt.-IdNr.** oder **GLN** ausgewählt haben, ist das Feld **Empfänger-ID Art** nicht verfügbar und wird automatisch mit der richtigen Kennung basierend auf Ihrer Auswahl und den zugehörigen Metadaten ausgefüllt, die im Continia Delivery Network verfügbar sind.

<ol>
<ol type="a" start="3">
<li>Geben Sie unter <strong>Kreditor ID Wert</strong> die genaue ID des Kreditors ein, sofern diese nicht automatisch ausgefüllt wurde.</li></ol>
</ol>

> [!NOTE]
> Wenn Sie wie in Schritt 5b in Schritt 5a **USt-IdNr.** oder **GLN** ausgewählt haben, wird das Feld **Kreditor ID Wert** automatisch mit der richtigen ID ausgefüllt, sofern dies für den ausgewählten Kreditor verfügbar ist.

<ol start="6">
<li>Gehen Sie zurück zur <strong>Kreditorenkarte</strong>.</li>
<li>Gehen Sie im Inforegister <strong>Allgemein</strong> zu <strong>Belegsendeprofil</strong> und wählen Sie <strong>CONTINIAEDOCUMENTS</strong> aus.</li>
<li>Wiederholen Sie die Schritte 2–7 für alle weiteren Kreditoren, die Sie einrichten möchten.</li></ol>
Die Einrichtung ist jetzt vollständig abgeschlossen und Sie können mit Continia eDocuments elektronische Dokumente an die ausgewählten Kreditoren senden. Bei Bedarf können Sie auch später jederzeit andere Kreditoren hinzufügen.