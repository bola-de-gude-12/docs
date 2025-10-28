---
title: Continia eDocuments einrichten
date: 10-09-2025
description: So richten Sie Continia eDocuments in Document Capture ein.
id: DC-179
lang: de
---

# Continia eDocuments einrichten

In diesem Artikel wird beschrieben, wie Sie Continia eDocuments in Continia Document Capture einrichten.

## Definitionen

Bei der Einrichtung von Continia eDocuments sind verschiedene Begriffe und Konzepte relevant. Hierzu zählen die verschiedenen Dokumenttypen:

<br>

| Dokumenttyp                  | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| eAbrechnungsdokumente        | Dazu gehören sowohl eingehende Einkaufsrechnungen/Gutschriften als auch ausgehende Verkaufsrechnungen/Gutschriften.                                                                                                                                                                                                                                                                                                                                              |
| eBestellungsdokumente        | Dazu gehören sowohl ausgehende Einkaufsbestellungen als auch eingehende Verkaufsaufträge.                                                                                                                                                                                                                                                                                                                                                                        |
| eDocuments-Antwortdokumente  | Dies kann entweder eine technische Antwort sein (zum Beispiel die empfangene XML-Datei ist ungültig oder die Regeln wurden verletzt) oder eine geschäftliche Antwort (zum Beispiel die Artikel und/oder Preise unterscheiden sich von den Vereinbarungen). Eine Geschäftsantwort ist ein Dokument, das als Antwort auf eine Rechnung oder eine Gutschrift (Einkauf oder Verkauf) dient. |
| eBestellung-Antwortdokumente | Dazu gehören sowohl Antworten auf eingehende Einkaufsbestellungen als auch Antworten auf ausgehende Verkaufsaufträge.                                                                                                                                                                                                                                                                                                                                            |

## XML-Strukturen

Eine XML-Struktur definiert die Dateistruktur für ein bestimmtes elektronisches Format (wie zum Beispiel **PEPPOL BIS3** und **OIOUBL**) und für bestimmte Geschäftsdokumente, beispielsweise eine Rechnung, eine Gutschrift, eine Rechnungsantwort, eine Bestellung oder eine Bestellantwort. Hierzu gehören beispielsweise **Peppol BIS3 Invoice**, **Peppol BIS3 Credit Memo** und **Peppol BIS3 Order**. Es gibt jedoch noch viele andere für unterschiedliche Belegarten und elektronische Formate.

Jede XML-Struktur ist verknüpft mit:

- Einer zugehörigen Identifikationsvorlage, die zum Identifizieren der Herkunft Ihrer eingehenden Dokumente verwendet wird (beispielsweise der Debitor oder Kreditor, der die Dokumente gesendet hat).
- Einem Stylesheet, das heißt eine Datei, mit der jedes XML-Dokument in ein besser lesbares und benutzerfreundlicheres Format umgewandelt wird, um es in der [Dokumentenvorschau](@DC-71#dokumentenvorschau) anzuzeigen.

> [!IMPORTANT]
> Wenn Sie ein bestehender Benutzer sind, der zu Continia eDocuments migriert, und Sie zuvor Änderungen an einem XML-Mastervorlagen-Stylesheet vorgenommen haben, müssen Sie das geänderte Stylesheet exportieren und es über die Seite **XML-Struktur Einrichtung** in Continia eDocuments importieren. Weitere Informationen finden Sie in Schritt 5 im Abschnitt [So richten Sie Continia eDocuments ein](#so-richten-sie-continia-edocuments-ein) weiter unten.

Die XML-Struktur funktioniert, indem ein XML-Pfad mit einem Datentyp (wie zum Beispiel **Text**, **Datum** oder **Code**) verknüpft wird und diese Daten dann einem Feld in einem [Datensatz](@DC-181) zugeordnet werden. Auf der Seite **XML-Strukturansicht** wird der Name der Tabelle, in der ein bestimmter Datensatz vorkommt, in der Spalte **Tabellenname** angezeigt, während der Name des zugehörigen Felds in der Spalte **Feldname** zu finden ist. Diese beiden Namen – Tabellenname und Feldname – sind für das Continia eDocuments-Framework von wesentlicher Bedeutung.

Beispielsweise könnte die XML-Struktur für eine eingehende Peppol-Rechnung den XML-Pfad **\/ubl:Invoice\/cbc:IssueDate** mit dem Datentyp **Datum** verknüpfen und diese Daten dann dem Feld **Ausgabedatum** in der Tabelle **eAbrechnungskopf** zuordnen. Eine andere Rechnung in einem anderen elektronischen Format verfügt möglicherweise über einen XML-Pfad, der dem von Peppol entspricht, sieht aber völlig anders aus. Dennoch erkennt die XML-Struktur, dass dieser XML-Pfad auch für dieses Format demselben Feld in derselben Tabelle zugeordnet werden sollte.

Die Formaterkennung erfolgt außerdem innerhalb der XML-Struktur und ist nicht mehr Bestandteil der Identifikationsvorlage. Dies bedeutet, dass die Identifikationsvorlage lediglich zur Parteiidentifikation (also zur Identifikation des Debitors bzw. Weitere Informationen zur Verwendung von Identifikationsvorlagen in Continia eDokumente finden Sie unter [Daten aus eDokumenten erfassen](@DC-182).

### So zeigen Sie eine XML-Struktur an und bearbeiten sie

So zeigen Sie die Struktur einer XML an und bearbeiten sie:

1. Suchen Sie {{search}} nach **XML-Strukturansicht** und wählen Sie dann den entsprechenden Link aus. Klicken Sie alternativ in der Aktionsleiste auf der Seite **Continia eDokument Einrichtung** auf **XML-Struktur**, wählen Sie dann die gewünschte Struktur aus und klicken Sie in der Aktionsleiste auf **Öffne XML-Struktur** klicken.
2. Klicken Sie auf der Seite **XML-Strukturansicht** auf die Dropdown-Liste neben dem Feld **Strukturcode** und wählen Sie die gewünschte Struktur aus. Zum Beispiel.: PEPPOLBIS3ORDER.
3. Um zusätzliche Informationen zu einem bestimmten Knoten in der Struktur anzuzeigen, wählen Sie ihn in der Tabelle aus und überprüfen Sie die Infobox **XML-Struktur Details**.
4. Um einen Wert zu bearbeiten, der auf der Seite **XML-Strukturansicht** nicht bearbeitet werden kann, klicken Sie in der Aktionsleiste auf **Aktionen > Details bearbeiten**, um die Seite **XML-Struktur Details bearbeiten** zu öffnen.

> [!NOTE]
> Sie sollten XML-Strukturen nur bearbeiten, wenn Sie sich gut damit auskennen. Wenden Sie sich an Ihren Partner, falls Sie Unterstützung benötigen.

## So richten Sie Continia eDocuments ein

So richten Sie Continia eDocuments ein:

1. Suchen Sie {{search}} nach **Continia eDokument Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Geben Sie auf der Inforegisterkarte **Allgemein** an, ob eingehende eRechnungsdokumente mit eDocuments verarbeitet werden sollen. Sie können auch den Testmodus einschalten. Weitere Informationen finden Sie unter [So aktivieren Sie den Testmodus](#so-aktivieren-sie-den-testmodus).
3. Geben Sie im Inforegister **Nummerierung** die Nummernserie an, die für die automatische Nummernzuweisung von importierten elektronische Dokumenten verwendet werden soll.
4. Geben Sie im Inforegister **eDokumentantwort** an, ob Sie Statusaktualisierungen von Dokumenten manuell oder automatisch senden möchten und wann automatische Antworten gesendet werden sollen.
   - Die Felder unter **eBestellantwort** sind Kreditorenfelder, die sich auf das Senden von Auftragsaktualisierungen an Debitoren beziehen, die etwas bei Ihnen bestellt haben:

     | Feld                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                               |
     | --------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
     | **Aktualisierungen senden** | Benachrichtigen Sie den Debitor, dass Sie die Bestellung aktualisiert haben (bei Preisänderungen, Artikelersetzungen usw.). Sie können wählen, ob Sie die Antworten manuell senden möchten oder ob sie automatisch gesendet werden sollen, wenn das Dokument freigegeben oder registriert wird oder wenn die Lieferung eingegangen ist. |
     | **Abgelehnt senden**        | Benachrichtigen Sie den Debitor, dass Sie den Verkaufsauftrag abgelehnt haben. Sie können wählen, ob Sie die Antworten manuell senden möchten oder ob sie automatisch gesendet werden sollen, wenn die Bestellung abgelehnt wird.                                                                                                                                          |

   - Die Felder unter **eAbrechnungsantwort** sind Debitorenfelder, die sich auf das Senden von Geschäftsantworten an Kreditoren beziehen, die Ihnen Rechnungen oder Gutschriften gesendet haben:

     | Feld                      | Beschreibung                                                                                                                                                                                                                                                                                      |
     | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
     | **In Bearbeitung senden** | Benachrichtigen Sie den Kreditor, dass Sie das empfangene Dokument bearbeiten. Sie können wählen, ob Sie die Antworten manuell senden möchten oder ob sie automatisch gesendet werden sollen, wenn das Dokument importiert, registriert oder genehmigt wird.      |
     | **Akzeptiert senden**     | Benachrichtigen Sie den Kreditor, dass Sie das empfangene Dokument akzeptiert haben. Sie können wählen, ob Sie die Antworten manuell senden möchten oder ob sie automatisch gesendet werden sollen, wenn das Dokument registriert, freigegeben oder gebucht wird. |
     | **Abgelehnt senden**      | Benachrichtigen Sie den Kreditor, dass Sie das empfangene Dokument abgelehnt haben. Sie können wählen, ob Sie die Antworten manuell senden möchten oder ob sie automatisch gesendet werden sollen, wenn das Dokument abgelehnt wird.                              |
5. **Optional**: Wenn Sie zuvor Änderungen an einem XML-Mastervorlagen-Stylesheet vorgenommen haben, das Sie importieren möchten:

   1. Um das Stylesheet zu exportieren, suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Link aus.
   2. Um die Belegkategorie zu öffnen, deren Stylesheet Sie exportieren möchten, klicken Sie auf die entsprechende Zeile (nicht den Code) und wählen Sie dann **Bearbeiten** in der Aktionsleiste aus.
   3. Klicken Sie im Inforegister **Vorlagen** auf die entsprechende Mastervorlage in der Liste, und wählen Sie dann **Bearbeiten** aus, um die Vorlagenkarte zu öffnen.
   4. Klicken Sie in der Aktionsleiste auf **Aktionen** > **XML** > **Stylesheet exportieren**, um das Stylesheet zu exportieren.
   5. Um das exportierte Stylesheet zu importieren, gehen Sie zur Seite **XML-Struktur Einrichtung**, die Sie in Schritt 4 geöffnet haben.
   6. Klicken Sie auf **Aktionen** > **Stylesheet** > **Stylesheet importieren**, um das Stylesheet zu importieren.
   7. Wenn es sich bei dem Stylesheet um eine ZIP-Datei handelt, gehen Sie zu **XML-Stylesheets Hauptdateiname** und geben Sie den Namen der zu verwendenden Haupt-Stylesheetdatei ein.

Die Einrichtung von Continia eDocuments ist damit abgeschlossen und Sie können anschließend Debitoren und Kreditoren einrichten. Dies wird unter [Debitoren und Kreditoren einrichten](@DC-180) beschrieben. Außerdem muss das [Continia Delivery Network eingerichtet werden](@DC-75), falls dies noch nicht erfolgt ist.

### So aktivieren Sie den Testmodus

Durch Aktivieren des Testmodus können Sie die Continia eDocuments-Funktionalität testen, ohne Dokumente über das Continia Delivery Network (CDN) zu senden.

So aktivieren Sie den Testmodus:

1. Suchen Sie {{search}} nach **Continia eDokument Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Aktivieren Sie im Inforegister **Allgemein** > **Testmodus**.

Wenn der Testmodus aktiviert ist, gilt Folgendes:

- Die gesamte Kommunikation mit dem CDN wird ausgesetzt; es werden keine Dokumente gesendet oder empfangen.
- Alle unterstützten Geschäftsdokumente können erneut gesendet werden – unabhängig von ihrem aktuellen Status. Sowohl eDokumemte (z. B. eAbrechnung, eBestellung und eAntwort) als auch zugehörige Netzwerkdokumente werden neu erstellt und mit dem Status **Test** gekennzeichnet.
- Beim Kopieren eines Mandanten werden alle bestehenden Teilnahmen in den Testmodus versetzt. Dies gilt für Mandanten, die innerhalb des Tenants mithilfe der Kopierfunktionen auf der Seite **Mandanten** oder bei SaaS-Umgebungen aus dem Admin Center erstellt wurden.

### So ändern Sie die Priorität eines Netzwerkprofils

Auf der Seite **Netzwerkprofile** können Sie die Priorität jedes Ihrer Netzwerkprofile festlegen. Continia eDocuments wählt automatisch das oberste registrierte Profil aus, das in der Liste verfügbar ist (z. B. 1). Ist dieses Profil beim Absender nicht registriert, wird das nächste Profil verwendet – und so weiter.

So ändern Sie die Reihenfolge, in der verschiedene Netzwerkprofile verwendet werden:

1. Suchen Sie {{search}} nach **Continia eDokument Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie in der Aktionsleiste auf **XML-Struktur**.
3. Klicken Sie auf der Seite **XML-Struktur** unter der Spalte **Unterstützt von Netzwerkprofilen** auf die Nummer, die dem Netzwerkprofil entspricht, dessen Prioritäten Sie ändern möchten.
4. Wählen Sie auf der Seite **Netzwerkprofile** einen Netzwerkprofilnamen aus und erhöhen oder verringern Sie die Priorität des Netzwerkprofils mithilfe der Aktionen **Nach oben verschieben** und **Nach unten verschieben** in der Aktionsleiste.