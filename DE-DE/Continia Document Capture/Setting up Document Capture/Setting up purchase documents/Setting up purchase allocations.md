---
title: Einkaufszuordnungen einrichten
date: 14-03-2025
description:
id: DC-41
lang: de
---

# Einkaufszuordnungen einrichten

Bei einer Einkaufszuordnung werden die Beträge eines Einkaufsbelegs (einer Rechnung oder einer Gutschrift) vorübergehend im Hauptbuch gebucht. Wenn der Einkaufsbeleg zur Genehmigung gesendet wird, wird eine Einkaufszuordnung, d. h. eine Kopfzeile mit mehreren Zeilen, erstellt. Durch die manuelle oder automatische Buchung dieser Einkaufszuordnung werden dann sowohl Zuordnungseinträge als auch entsprechende Sachposten generiert. Diese temporären Einträge werden später rückgängig gemacht und im Hauptbuch dauerhaft gemacht, sobald der Beleg genehmigt und gebucht wurde. Auf diese Weise können Sie mit der Einkaufszuordnung Belegbeträge vorläufig vormerken, die dann später in eigentliche Sachposten umgewandelt werden können.

Wenn Sie beispielsweise eine Einkaufsrechnung erhalten, sind die Rechnungsbeträge nicht sofort im Hauptbuch sichtbar, aber Sie können sie mithilfe von Einkaufszuordnungen im Hauptbuch anzeigen lassen. Dies kann für Buchprüfungen oder andere Zwecke sinnvoll oder sogar notwendig sein. Wenn Sie automatische Einkaufszuordnung aktivieren, werden ein oder mehrere vorläufige Einkaufszuordnungsposten erstellt und im Hauptbuch gebucht, sobald Sie die Rechnung zur Genehmigung senden. Wenn die Rechnung genehmigt und gebucht wird, storniert Continia Document Capture diese vorläufigen Einträge und ersetzt sie durch eigentliche Einträge im Hauptbuch.

Im Folgenden wird beschrieben, wie Sie Document Capture so konfigurieren können, dass Einkaufszuordnungsposten [automatisch](#so-erstellen-und-buchen-sie-einkaufszuordnungsposten-automatisch) oder [manuell](#so-erstellen-und-buchen-sie-einkaufszuordnungsposten-manuell) erstellt und gebucht werden. In diesem Artikel werden Rechnungen als Beispiel verwendet; die Einkaufszuordnung funktioniert jedoch auch mit Gutschriften.

## So erstellen und buchen Sie Einkaufszuordnungsposten automatisch

1. Suchen Sie {{search}} nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.

2. Wählen Sie in der Aktionsleiste **Einrichtung** > **Einkaufsgenehmigung** aus, um die Seite **Document Capture Einrichtung / Einkaufsgenehmigungen** zu öffnen.

3. Aktivieren Sie Einkaufszuordnung unter **Einkaufszuordnung**, indem Sie den Schalter **Aktivieren** umschalten.

4. Geben Sie unter **Beträge** an, ob Document Capture Zeilen aus Einkaufsrechnungen oder importierte Beträge verwenden soll, um die für die Einkaufszuordnung verwendeten Beträge abzurufen. Wenn Sie **Zeilen oder importierte Beträge verwenden** auswählen, haben Einkaufsrechnungszeilen Priorität. Wenn keine Zeilen vorhanden sind, werden stattdessen importierte Beträge verwendet.

  > [!NOTE]
  > Wenn Sie hier **Immer importierte Beträge verwenden** auswählen, kann die **Sachkontoart** nicht in Schritt 5 unten konfiguriert werden und die Einkaufszuordnungskonten, die Sie in **Kreditorenbuchungsgruppen** einrichten, werden für die Erstellung und Buchung von Einkaufszuordnungsposten verwendet. Weitere Informationen finden Sie unter [So konfigurieren Sie Buchungskonten](#so-konfigurieren-sie-buchungskonten) weiter unten.
  >
  > Der Begriff importierter Betrag bezieht sich auf den Gesamtbetrag der Rechnung.

5. Geben Sie unter **Sachkontoart** an, welche Kostenkonten beim Erstellen von Einkaufszuordungsposten verwendet werden sollen. Es gibt folgende Optionen:
  - **Benutze Buchungseinrichtung**: Document Capture verwendet die Einkaufszuordnungskonten, die Sie in der **Buchungsmatrix Einrichtung** eingerichtet haben. Informationen zum Einrichten dieser Konten finden Sie unter [Buchungsmatrix Einrichtung](#buchungsmatrix-einrichtung) weiter unten.
  - **Benutze Herkunftskonto**: Document Capture verwendet die Sachkonten, die jeder Einkaufsrechnungszeile zugewiesen sind. Für die Rechnungszeilen, denen kein Sachkonto zugewiesen ist, wird stattdessen die **Buchungsmatrix Einrichtung** verwendet. Weitere Informationen finden Sie unter [So konfigurieren Sie Buchungskonten](#so-konfigurieren-sie-buchungskonten).

6. Aktivieren Sie die automatische Erstellung und Buchung von Einkaufszuordnungsposten, indem Sie den Schalter \*\*Autom.

7. Wählen Sie unter **Buchungsdatum bei Storno der Eink. Zuordnung** aus, welches Buchungsdatum verwendet werden soll, wenn Einkaufszuordungsposten storniert werden. Sie können entweder das ursprüngliche Datum wählen, an dem die Einkaufszuordnung gebucht wurde, oder das Datum, an dem die Rechnung gebucht wurde.

Diese vorläufigen Einkaufszuordungsposten werden automatisch storniert und durch eigentliche Einträge im Hauptbuch ersetzt, sobald die Rechnung genehmigt und gebucht wurde.

## So erstellen und buchen Sie Einkaufszuordnungsposten manuell

Um Einkaufszuordungsposten manuell erstellen und buchen zu können, müssen Sie zunächst die Einkaufszuordnung in der **Document Capture Einrichtung** aktivieren und konfigurieren. Befolgen Sie dazu die [Anleitung oben](#so-erstellen-und-buchen-sie-einkaufszuordnungsposten-automatisch), aber überspringen Sie Schritt 6, um **Autom. buchen** deaktiviert zu lassen.

Sobald Sie den Konfigurationsassistenten abgeschlossen haben, können Sie Einkaufszuordungsposten manuell erstellen und buchen:

1. Gehen Sie im Rollencenter unter **Continia Document Capture Aktivitäten** zu **Einkaufsgenehmigung - Rechnungen** und wählen Sie **Offene Rechnungen** aus, um die Liste der offenen Einkaufsrechnungen zu öffnen.
2. Wählen Sie in der Liste die Rechnung aus, für die Sie Einkaufszuordungsposten erstellen und buchen möchten.
3. Wählen Sie in der Aktionsleiste **Zugehörig** > **Rechnung** > **Zuordnungen** aus, um die **Einkaufszuordnungübersicht** zu öffnen.
4. Wählen Sie in der Aktionsleiste **Neu** aus, um eine neue Einkaufszuordnung zu erstellen.
5. Wählen Sie auf der Seite **Einkaufszuordnung** in der Aktionsleiste **Zeilen erstellen** aus, um alle erforderlichen Felder mit den relevanten Daten zu füllen. Sie können dies auch manuell unter **Zeilen** vornehmen.
6. Wählen Sie in der Aktionsleiste **Buchen** aus, um die Einkaufszuordnung im Hauptbuch zu buchen.

> [!NOTE]
> Wenn die Rechnung genehmigt und gebucht wurde, wird die Einkaufszuordnung storniert. Diese Stornierung erfolgt automatisch, unabhängig davon, ob die Einkaufszuordnung automatisch oder manuell erstellt und gebucht wurde.

> [!TIP]
> Wenn Sie den Buchungsverlauf einer Einkaufszuordnung anzeigen möchten, gehen Sie zur Seite **Einkaufszuordnung** und wählen Sie in der Aktionsleiste **Posten finden** aus. Dadurch wird die Seite **Posten suchen** geöffnet, die einen Überblick über die ausgewählte Zuordnung bietet.

## So konfigurieren Sie Buchungskonten

Wenn Sie die automatische oder manuelle Erstellung und Buchung von Einkaufszuordnungen wie oben beschrieben einrichten, müssen Sie unter **Beträge** angeben, welche Beträge zugeordnet werden sollen und unter **Sachkontoart**, welche Kostenkonten verwendet werden sollen. Unabhängig davon, was Sie in diesen Feldern angeben, müssen Sie auch Konten in [**Kreditorenbuchungsgruppen**](#kreditorenbuchungsgruppen) einrichten. Die Gegenkonten, die Sie hier zuweisen, werden immer für die Erstellung und Buchung von Einkaufszuordnungen verwendet; die Einkaufszuordnungskonten, die Sie hier zuweisen, werden jedoch nur in bestimmten Szenarien verwendet, so wie die Einkaufszuordnungkonten in der [**Buchungsmatrix Einrichtung**](#buchungsmatrix-einrichtung), die Sie möglicherweise auch einrichten müssen.

Welches der Einkaufszuordnungkonten verwendet wird, hängt davon ab, was Sie unter **Beträge** und **Sachkontoart** in der **Document Capture Einrichtung** auswählen:

<br>

| Ausgewählte Einstellungen                                                                                                                                                                          | Ergebnis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Unter **Beträge**: <ul><li><b>Immer importierte Beträge benutzen</b></li></ul>                                                                                                     | Mit dieser Einstellung (**Sachkontoart** ist hier nicht zutreffend) werden die Einkaufszuordnungskonten verwendet, die Sie in **Kreditorenbuchungsgruppen** zugewiesen haben. Für den gesamten Rechnungsbetrag (auch importierter Betrag genannt) wird, unabhängig von der Anzahl der Rechnungszeilen, nur ein Konto verwendet, und dieses Konto wird anhand der Buchungsgruppe des Kreditors zugeordnet, der die Rechnung gesendet hat. <br><br> Weitere Informationen zum Zuweisen von Konten für Kreditorenbuchungsgruppen finden Sie unter [**Kreditorenbuchungsgruppen**](#kreditorenbuchungsgruppen) weiter unten.                                                                                                                                                                                                                                                                                                                                                                           |
| Unter **Beträge**: <ul><li><b>Zeilen oder importierte Beträge verwenden</b></li></ul> Unter **Sachkontoart**: <ul><li><b>Benutze Buchungseinrichtung</b></li></ul> | Mit dieser Kombination der Einstellungen wird für jede Rechnungszeile ein Einkaufszuordungsposten gebucht, wobei die Konten verwendet werden, die bereits in den einzelnen Rechnungszeilen angegeben sind. Für jede Rechnungszeile wird ein Einkaufszuordnungseintrag gebucht, und Document Capture weist dann jeder einzelnen Rechnungszeile das Einkaufszuordnungskonto zu, das der Kombination aus **Geschäftsbuchungsgruppe** Für jede Rechnungszeile wird ein Einkaufszuordnungseintrag gebucht, und Document Capture weist dann jeder einzelnen Rechnungszeile das Einkaufszuordnungskonto zu, das der Kombination aus **Geschäftsbuchungsgruppe** und **Produktbuchungsgruppe** der jeweiligen Rechnungszeile entspricht, gemäß Ihren Einstellungen. und **Produktbuchungsgruppe** und **Produktbuchungsgruppe** der jeweiligen Rechnungszeile entspricht, gemäß Ihren Einstellungen. <br><br> Weitere Informationen finden Sie unter [**Buchungsmatrix Einrichtung**](#buchungsmatrix-einrichtung) weiter unten. |
| Unter **Beträge**: <ul><li><b>Zeilen oder importierte Beträge verwenden</b></li></ul> Unter **Sachkontoart**: <ul><li><b>Benutze Herkunftskonto</b></li></ul>      | Mit dieser Kombination der Einstellungen wird für jede Rechnungszeile ein Einkaufszuordungsposten gebucht, wobei die Konten verwendet werden, die bereits in den einzelnen Rechnungszeilen angegeben sind. <br><br> Wenn Rechnungszeilen jedoch kein Sachkonto zugewiesen ist, wird stattdessen die **Buchungsmatrix Einrichtung** verwendet. In solchen Fällen bucht Document Capture einen Einkaufszuordungsposten für jede Rechnungszeile, der kein Sachkonto zugewiesen ist, und verwendet dabei das Einkaufszuordnungskonto, das der Kombination aus **Geschäftsbuchungsgruppe** und **Produktbuchungsgruppe** und **Produktbuchungsgruppe** der jeweiligen Rechnungszeile entspricht, gemäß Ihren Einstellungen. <br><br> Weitere Informationen finden Sie unter [**Buchungsmatrix Einrichtung**](#buchungsmatrix-einrichtung) weiter unten.                                                                                                                                                                       |

### Buchungsmatrix Einrichtung:

So richten Sie Einkaufszuordnungskonten in der **Buchungsmatrix Einrichtung** ein:

1. Wählen Sie das Symbol {{search}}, geben Sie **Buchungsmatrix Einrichtung** ein, und wählen Sie dann den zugehörigen Link.

2. Wählen Sie in der Aktionsleiste **Liste bearbeiten** aus.

  > [!NOTE]
  > Bei der Liste handelt es sich um eine Tabelle und jede Zeile der Tabelle stellt eine Kombination aus einer allgemeinen Geschäftsbuchungsgruppe (für den Kreditor einer Rechnung) und einer allgemeinen Produktbuchungsgruppe (für das Sachkonto oder den Posten einer Rechnungszeile) dar. Wenn die Kombination einer Tabellenzeile mit der einer Rechnungszeile übereinstimmt, wird das Einkaufszuordnungskonto, das Sie dieser Tabellenzeile zugewiesen haben, als Kostenkonto der entsprechenden Rechnungszeile eingerichtet.

3. Aktivieren Sie die automatische Erstellung und Buchung von Einkaufszuordnungsposten, indem Sie den Schalter **Autom. buchen** umschalten.

4. Wählen Sie die drei Punkte rechts neben dem Feld **Einkaufskonto (Zuweisung)** aus, um die **Sachkontenübersicht** zu öffnen. Wählen Sie in der Liste unter **Nr.** das Konto aus, das Sie der ausgewählten Tabellenzeile zuordnen möchten.

5. Wiederholen Sie Schritte 3–4 für jede weitere Tabellenzeile, der Sie Konten zuweisen möchten.

Die von Ihnen zugewiesenen Konten werden dann für die Einkaufszuordungsposten verwendet, die im Hauptbuch erstellt und gebucht werden, wenn Sie eine Rechnung zur Genehmigung senden, jedoch nur, wenn die folgenden Bedingungen erfüllt sind:

- In der **Document Capture Einrichtung** muss unter **Einkaufszuordnung** > **Beträge** die Option **Zeilen oder importierte Beträge verwenden** ausgewählt sein.
- Die Rechnung muss mindestens eine Zeile enthalten.
- Eine der folgenden Einstellungen muss zutreffen:
  - In der **Document Capture Einrichtung** muss unter **Einkaufszuordnung** > **Sachkontoart** die Option **Benutze Buchungseinrichtung** ausgewählt sein.
  - Die jeweilige(n) Einkaufsrechnungszeile(n) muss/müssen einen anderen Typ als Sachkonto haben.

### Kreditorenbuchungsgruppen:

Um Konten in **Kreditorenbuchungsgruppen** einzurichten, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Kreditorenbuchungsgruppen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Aktionsleiste **Liste bearbeiten** aus.
3. Suchen Sie die Tabellenzeile, der Sie ein Konto zuweisen möchten, und wählen Sie **Zahlungskonto (Zuweisung)** aus.
4. Wählen Sie die drei Punkte rechts neben dem Feld **Zahlungskonto (Zuweisung)** aus, um die **Sachkontenübersicht** zu öffnen. Wählen Sie in der Liste unter **Nr.** das Konto aus, das Sie der ausgewählten Tabellenzeile zuordnen möchten.
5. Wählen Sie unter **Einkaufskonto (Zuweisung)** die drei Punkte rechts im Feld aus, um die **Sachkontenübersicht** zu öffnen. Wählen Sie in der Liste unter **Nr.** das Konto aus, das Sie der ausgewählten Tabellenzeile zuordnen möchten.
6. Wiederholen Sie Schritte 3–5 für jede weitere Tabellenzeile, der Sie Konten zuweisen möchten.

Die von Ihnen zugewiesenen Konten werden dann wie folgt für die Einkaufszuordungsposten verwendet, die erstellt und gebucht werden, wenn Sie eine Rechnung zur Genehmigung senden:

- **Zahlungskonto (Zuweisung)**: das Gegenkonto wird immer verwendet.
- **Einkaufskonto (Zuweisung)**: das Kostenkonto wird nur verwendet, wenn **Immer importierte Beträge benutzen** in der **Document Capture Einrichtung** ausgewählt wurde.

<style>
  .content table tr td:nth-child(1) {
    width: 180px;
  }
  .content table tr td:nth-child(2) {
    width: 550px;
  }  
</style>