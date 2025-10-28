---
title: Belege in Document Capture registrieren
date: 27-05-2025
description: So registrieren Sie Belege in Document Capture.
id: DC-67
lang: de
---

# Belege registrieren

Wenn Sie einen Beleg in Continia Document Capture registrieren, werden alle erkannten Informationen in eine echte Geschäftseinheit in Microsoft Dynamics 365 Business Central umgewandelt. Wenn Sie beispielsweise eine Einkaufsrechnung von einem Kreditor registrieren, erstellen Sie automatisch eine Business Central-Einkaufsrechnung.

Bevor Sie einen Beleg registrieren können, müssen alle Belegfelder erfasst sein und gültige Werte haben. Im Bereich für die Belegfelder (unter **Belegkopf**) können Sie sehen, ob alle Felder korrekt ausgefüllt sind. Falls dies nicht der Fall ist, müssen Sie die Felder ausfüllen, damit Sie den Beleg registrieren können.

In der Belegliste können Sie auch sehen, ob der Beleg bereit ist, registriert zu werden. Dies wird durch ein Häkchen in der Spalte **OK** angezeigt. Wenn der Beleg noch nicht zur Registrierung bereit ist, sehen Sie im Abschnitt **Bemerkungen** unten, welche Aktionen erforderlich sind.

Wenn Sie einen Beleg registrieren, führt Document Capture manchmal eine zusätzliche Validierung durch, die die Registrierung möglicherweise stoppt. In diesem Fall werden Sie darüber informiert, wie Sie die Registrierung abschließen können.

## So registrieren Sie einen Beleg

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, zum Beispiel **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, den Sie registrieren möchten. Wählen Sie die Belegzeile aus, nicht die Nummer in der Spalte **Nr.**, da dadurch die Dokumentenkarte geöffnet wird.
4. Überprüfen Sie im Abschnitt der Belegfelder (unter **Belegkopf**), ob alle Felder in der Spalte **OK** mit einem Häkchen versehen sind. Wenn ja, sind alle Felder gültig. Wenn nicht, folgen Sie den Anweisungen zum Erfassen von Feldern in den Abschnitten [So erfassen Sie Felder](@DC-110#so-erfassen-sie-felder) und [Document Capture zum Erkennen von Werten trainieren](@DC-110#document-capture-zum-erkennen-von-werten-trainieren) im Artikel [Kopffelder in einem Beleg erfassen](@DC-110). So stellen Sie sicher, dass alle Felder richtig erfasst werden und gültige Werte haben.
5. Nicht alle Feldwerte werden aus dem Beleg eingelesen; einige müssen stattdessen manuell hinzugefügt werden. Der wichtigste Wert ist dabei die Sachkontonummer, die in den meisten Fällen obligatorisch ist. Um diesen Wert hinzuzufügen, gehen Sie zu **Nr.** und wählen Sie die drei Punkte in der Spalte **Wert** aus, um die **Sachkontenübersicht** zu öffnen. Wählen Sie das entsprechende Konto in der Liste aus, indem Sie dessen Nummer in der Spalte **Nr.** auswählen.
6. Es wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob Sie das ausgewählte Konto als Standardkonto konfigurieren möchten. Wählen Sie **Ja**, wenn Document Capture dieses Konto allen Belegen zuweisen soll, die dieselbe Herkunftsvorlage verwenden. Wählen Sie andernfalls **Nein**. Anschließend wird das Dialogfeld geschlossen und der ausgewählte Wert wird im Feld **Nr.** hinzugefügt
7. Überprüfen Sie in der Belegliste, ob in der Spalte **OK** für den ausgewählten Beleg ein Häkchen vorhanden ist. Wenn ja, kann der Beleg registriert werden. Wenn nicht, können Sie im Abschnitt **Bemerkungen** unten im Belegjournal sehen, welche Aktionen erforderlich sind.
8. Wenn keine weiteren Bemerkungen vorhanden sind und in der Spalte **OK** für den ausgewählten Beleg in der Belegliste ein Häkchen angezeigt wird, wählen Sie in der Aktionsleiste **Start** und dann **Registrieren** aus.

Der Beleg wird anschließend als Business Central-Beleg registriert, und die Belegseite wird automatisch geöffnet, sofern Sie in der Einrichtung keine besonderen Einstellungen vorgenommen und Document Capture zum Beispiel eingerichtet haben, um [Belege als Fibu. Buch-Blattzeilen oder Einkaufs Buch.-Blattzeilen zu registrieren](#belege-als-fibu-buch-blattzeilen-oder-einkaufs-buch-blattzeilen-registrieren).

> [!NOTE]
> Abhängig von Ihrer Konfiguration erhalten Sie möglicherweise bestimmte Warnungen während der Registrierung, beispielsweise in Bezug auf Ihre Sachkonten oder Ihre Mehrwertsteuer-Buchungseinrichtung. Die Ursachen für solche Warnungen müssen behoben werden, damit Sie Ihre Belege registrieren können. Gleiches gilt für doppelte Transaktionen aus Continia Expense Management, die anhand des Belegdatums (+/- 3 Tage), des Währungscodes und des Betrags einschließlich Mehrwertsteuer ermittelt werden.

Wenn durch die Registrierung eines Belegs eine Aktualisierung einer bestehenden Bestellung/Reklamation erfolgt, archiviert Document Capture diese automatisch, bevor die Aktualisierung angewendet wird. So können Sie ältere Versionen der Bestellung/Reklamation über [die integrierte Archivierungsfunktion in Business Central](https://learn.microsoft.com/de-de/dynamics365/business-central/across-how-to-archive-documents) (Microsoft-Artikel) anzeigen.

Document Capture archiviert aktualisierte Bestellungen und Reklamation in den folgenden Szenarien automatisch:

- Kategorie Einkauf: Wenn Sie ein Document Capture-Dokument mit den Registrierungsoptionen **Bestellung zuordnen und aktualisieren** oder **Reklamation zuordnen und aktualisieren** als Rechnung oder Gutschrift registrieren.
- Kategorie Bestellung: Wenn Sie ein Document Capture-Dokument mit den Registrierungsoptionen **Bestellung erstellen oder aktualisieren**, **Bestellung aktualisieren** oder **Aktualisiere Bestellempfangsbestätigung** registrieren.

Außerdem wird der archivierten Bestellung ein Kommentar hinzugefügt, der angibt, welcher Beleg die Archivierung ausgelöst hat (zusammen mit der **Belegnr.** und/oder **Kreditoren-Bestellnr.**).

### So aktivieren Sie automatische Registrierung

So können Sie in Document Capture die automatische Registrierung von Belegen ermöglichen, die an eine bestimmte Vorlage gebunden sind, vorausgesetzt, dass die Belege keine Fehler oder Warnungen enthalten:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, zum Beispiel **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste ein Dokument aus, das mit der Vorlage verknüpft ist, für die Sie automatische Registrierungen aktivieren möchten. Wählen Sie die Belegzeile aus, nicht die Nummer in der Spalte **Nr.**, da dadurch die Dokumentenkarte geöffnet wird.
4. Klicken Sie in der Aktionsleiste auf **Vorlage** > **Vorlagenkarte**.
5. Aktivieren Sie im Inforegister **Allgemein** der Vorlagenkarte die Einstellung **Dokumente automatisch registrieren**.

## Belege als Fibu. Buch-Blattzeilen oder Einkaufs Buch.-Blattzeilen registrieren

Außer der standardmäßigen Registrierung ist es auch möglich, Belege entweder als Fibu Buch.-Blattzeilen oder als Einkaufs Buch.-Blattzeilen zu registrieren, jedoch ohne Kreditornamen und andere Standardinformationen. Wenn Sie [dies eingerichtet haben](@DC-112), erstellt Document Capture bei der Belegregistrierung automatisch Zeilen im Fibu Buch.-Blatt oder Einkaufs Buch.-Blatt anstelle von Rechnungen oder Gutschriften.

Dies eignet sich besonders für Unternehmen, die für bestimmte Einkaufsbelege keine Dokumentengenehmigung oder detaillierten Buchungsinformationen benötigen. Bei einigen Belegen, oft von einmaligen Kreditoren, ist eine vollständige Registrierung in Document Capture nicht erforderlich, da sie so wenige Details enthalten.

Der Ablauf ist ähnlich wie beim standardmäßigen Registrierungsprozess. Es gibt jedoch einige nennenswerte Unterschiede. Obwohl sich die folgenden Informationen auf allgemeine Fibu Buch.-Blätter konzentrieren, gilt das Gleiche auch für Einkaufs Buch.-Blätter.

- Nach der Registrierung wird anstelle der Belegseite die Seite **Fibu Buch.-Blätter** geöffnet (da kein Beleg erstellt wird).
  > [!NOTE]
  > Diese Seite wird geöffnet, wenn Sie die folgenden Standardeinstellungen auf der **Vorlagenkarte** beibehalten haben: **Beleg nach Registrierung anzeigen** ist auf **Immer** eingestellt und **Rechnung Reg. Schritt 2** und **Gutschrift Reg. Schritt 2** bleiben leer.
- Wenn Sie im Belegjournal in der Aktionsleiste **Dokument** > **Posten finden** auswählen, hängt das Suchergebnis davon ab, ob Sie das Fibu Buch.-Blatt gebucht haben (z. B. indem Sie **Rechnung Reg. Schritt 2**/**Gutschrift Reg. Schritt 2** in der [Einrichtung](@DC-112) auf **Buchen** gesetzt haben):
  - **Buch.-Blatt gebucht:** Die Seite **Posten suchen** wird geöffnet, und es werden alle zugehörigen Posten aufgelistet.
  - **Buch.-Blatt nicht gebucht:**  Die Seite **Fibu Buch.-Blätter** wird geöffnet.
- Die folgenden Funktionen sind nicht verfügbar, wenn Sie Belege als Fibu Buch.-Blattzeilen registrieren:
  - Belegabgleich
  - Genehmigungen
  - Einkaufszuordnung
  - Rechnungen

> [!TIP]
> Sie können alle registrierten Belege in der Dokumentenvorschau auf der Seite **Fibu Buch.-Blätter** anzeigen, falls Sie die Originalversion sehen möchten.

## So registrieren Sie Vorauszahlungsrechnungen

Document Capture erweitert die standardmäßige Business Central-Funktion für Vorauszahlungen und kann so eingehende Rechnungen automatisch als Vorauszahlungsrechnung für eine Bestellung buchen. Hierfür muss die eingehende Rechnung entweder als Vorauszahlungsrechnung identifiziert oder markiert werden. Wenn Document Capture bestimmte Begriffe im Beleg erkennt, die auf eine Vorauszahlungsrechnung hinweisen, wird der Beleg automatisch entsprechend gekennzeichnet.

So registrieren Sie eine Rechnung als Vorauszahlungsrechnung:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie den Code **EINKAUF** aus, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste die Rechnung aus, die Sie als Vorauszahlungsrechnung registrieren möchten. Wählen Sie die Belegzeile aus, nicht die Nummer in der Spalte **Nr.**.
4. Gehen Sie im Abschnitt für Belegfelder (unter **Belegkopf**) zu **Bestellnummer** und überprüfen Sie, ob in der Spalte **Wert** eine Bestellnummer angezeigt wird. Wenn nicht, klicken Sie auf die drei Punkte rechts, um die **Einkaufsübersicht** zu öffnen, und wählen Sie dann die Bestellung aus, die Sie mit der Rechnung verknüpfen möchten.
   > [!NOTE]
   > Es muss eine Bestellnummer eingegeben oder erfasst werden, damit Document Capture die Rechnung als Vorauszahlungsrechnung registrieren kann.
5. Gehen Sie zu **[R]echnung / [G]utschrift  / [V]orauszahlung**, und prüfen Sie, ob der Buchstabe **V** in der Spalte **Wert** angezeigt wird. Wenn nicht, geben Sie den Wert manuell ein und drücken Sie dann die **Eingabetaste**.
6. [Bei Fehlern werden entsprechende Bemerkungen](#automatische-validierung-und-vorauszahlungsprozentsatz-aktualisieren) in fetter roter Schrift im Abschnitt **Bemerkungen** unten angezeigt. Beheben Sie diese Fehler, um die Belegregistrierung zu aktivieren.
7. Wenn keine Fehlerkommentare mehr angezeigt werden, können Sie mit der Registrierung der Rechnung fortfahren: Wählen Sie in der Aktionsleiste **Start** > **Registrieren**.

Document Capture bucht die Rechnung anschließend als Vorauszahlungsrechnung, die mit der in Schritt 4 oben angegebenen Bestellung verknüpft ist.

### Automatische Validierung und Vorauszahlungsprozentsatz aktualisieren

Wie oben erwähnt, kann Document Capture die Registrierung einer Vorauszahlungsrechnung blockieren, wenn bei der Validierung Fehler auftreten. Häufig liegt der Fehler darin, dass keine zugehörige Bestellung vorliegt oder dass der Betrag der Vorauszahlungsrechnung den Betrag der Bestellung übersteigt. Solche Fehler müssen behoben werden, damit Sie die Vorauszahlungsrechnung registrieren können.

Andere Bemerkungen zu den Vorauszahlungen hindern Sie nicht daran, die Rechnung zu registrieren; sie weisen Sie jedoch auf wichtige Details hin, die Sie beachten müssen. Dies ist beispielsweise bei der folgenden Warnung der Fall:

_Auf Bestellung [Bestellnummer] wurden keine Vorauszahlungen verarbeitet. Die aktuelle Vorauszahlungsrechnung erhöht die Vorauszahlungshöhe und beträgt [Prozentsatz (Betrag)]_.

> [!TIP]
> Obwohl diese Bemerkung die Registrierung standardmäßig nicht verhindert, können Sie sie so konfigurieren, dass statt einer Warnung ein Fehler angezeigt wird. Weitere Informationen finden Sie unter [Bemerkungsarten und deren Wichtigkeit konfigurieren](@DC-72).

Grundlage für diese Bemerkungen ist das Bestellungskopffeld **Vorauszahlung %**, das sich im Inforegister **Vorauszahlung** der Bestellung befindet. Wenn dieses Feld beispielsweise in einer Bestellung mit einem Gesamtbetrag von 5.000 $ ohne Steuern auf 10 % gesetzt wurde und der Betrag der Vorauszahlungsrechnung höher als 500 $ (10 % von 5.000 $) ist, wird die oben genannte Warnung im Belegjournal für die Vorauszahlungsrechnung angezeigt. Der Vorauszahlungsprozentsatz der Bestellung wird automatisch auf den neuen, tatsächlichen Prozentsatz geändert, wenn die Rechnung registriert wird:

<br>

| Dokument<br></br>      |    Betrag ohne Steuer   |                                                                                                                                                                                                                                                                                  Vorauszahlung %                                                                                                                                                                                                                                                                                  | Bemerkungen<br></br> |
| ---------------------- | :---------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | -------------------- |
| Einkaufsbestellung     | 5.000 $ | 10 % <br>(ursprünglicher Prozentsatz) <td rowspan="2">Da der Rechnungsbetrag ein Fünftel des Bestellbetrags beträgt (d. h. 20 %), wird der ursprüngliche Vorauszahlungsprozentsatz von 10 % entsprechend angepasst. Vor der Belegregistrierung wird im Belegjournal eine Warnung angezeigt, die darauf hinweist, dass die Beträge nicht übereinstimmen. Nach der Registrierung ändert Document Capture **Vorauszahlung %** für die Bestellung in 20 %.</td> |                      |
| Vorauszahlungsrechnung | 1.000 $ |                                                                                                                                                                                                                                                               20 % <br>(angepasster Prozentsatz)                                                                                                                                                                                                                                                               |                      |

Hinweis: Wenn der Betrag der Vorauszahlungsrechnung niedriger als 500 $ (10 % von 5.000 $) ist, werden die Zeilenbeträge entsprechend geändert. Der Vorauszahlungsprozentsatz bleibt jedoch auf Kopf- und Zeilenebene unverändert. In solchen Fällen wird im Belegjournal der Vorauszahlungsrechnung eine entsprechende Warnung angezeigt.

Wenn der Betrag der Vorauszahlungsrechnung mehr als 100 % des Bestellbetrags beträgt, wird anstelle einer Warnung ein Fehler angezeigt und Sie können die Rechnung nicht registrieren:

<br>

| Dokument<br></br>      |    Betrag ohne Steuer   |                                                                                                                                                                                                                     Vorauszahlung %                                                                                                                                                                                                                     | Bemerkungen<br></br> |
| ---------------------- | :---------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | -------------------- |
| Einkaufsbestellung     | 5.000 $ | 10 % <br>(ursprünglicher Prozentsatz) <td rowspan="2">Da der Rechnungsbetrag den Betrag der Einkaufsbestellung übersteigt (was 120 % entspricht), wird der ursprüngliche Vorauszahlungsprozentsatz von 10 % nicht angepasst. Im Belegjournal weist eine Fehlermeldung darauf hin, dass die Beträge nicht übereinstimmen, wodurch die Rechnung nicht registriert werden kann.</td> |                      |
| Vorauszahlungsrechnung | 6.000 $ |                                                                                                                                                                                                120 % <br>(entsprechender Prozentsatz)                                                                                                                                                                                                |                      |

> [!NOTE]
> Alle Vorauszahlungsfunktionen von Document Capture gelten auf Kopfebene, da **Vorauszahlung %** ein Kopffeld von Einkaufsbestellungen ist. Derzeit ist es nicht möglich, Vorauszahlungsrechnungen mit Bestellungen auf Zeilenebene zu verknüpfen.

## Informationen zum Thema

[Mit Papier- und PDF-Belegen arbeiten](Working with paper and PDF documents.md)