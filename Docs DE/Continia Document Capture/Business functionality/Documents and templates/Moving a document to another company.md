---
title: Belege in Document Capture zu anderen Mandanten verschieben
date: 31-03-2025
description:
id: DC-74
lang: de
---

# Belege zu anderen Mandanten verschieben

Wenn Sie in Microsoft Dynamics 365 Business Central mehrere Mandanten eingerichtet haben, müssen Sie möglicherweise manchmal einen Beleg in Continia Document Capture von einem Mandanten zu einem anderen verschieben. Dies kann erforderlich sein, wenn Sie Document Capture so eingerichtet haben, dass alle Belege in einen bestimmten Mandanten importiert werden, oder wenn jemand versehentlich einen Beleg an den falschen Mandanten sendet.

Einige Unternehmen bitten ihre Kreditoren beispielsweise, alle Einkaufsrechnungen an dieselbe E-Mail-Adresse zu senden. Von dieser Adresse aus können die Unternehmen die Belege dann manuell an die vorgesehenen Empfängermandanten verteilen. In Fällen, in denen ein manuelles Verschieben erforderlich ist, kann die [unten beschriebene manuelle Methode](/continia-document-capture/business-functionality/documents-and-templates/moving-a-document-to-another-company#belege-manuell-zu-anderen-mandanten-verschieben) angewendet werden.

Es ist auch möglich, [eingehende Belege automatisch zu anderen Mandanten zu verschieben](/continia-document-capture/business-functionality/documents-and-templates/moving-a-document-to-another-company#belege-automatisch-zu-anderen-mandanten-verschieben). Dies wird weiter unten beschrieben.

Bei App-Versionen von Business Central wird die Kreditor- und Felderkennung automatisch für jeden Beleg durchgeführt, der von einem Mandanten zu einem anderen verschoben wird, unabhängig davon, welche der beiden Methoden Sie verwenden.

## Belege manuell zu anderen Mandanten verschieben

> [!IMPORTANT]
> Die folgende Anleitung setzt voraus, dass Sie in Business Central mindestens zwei Mandanten eingerichtet haben. Andernfalls ist die Aktion **In anderen Mandanten verschieben** nicht verfügbar. Außerdem muss Document Capture in allen Mandanten, zwischen denen Sie Belege verschieben möchten, installiert, aktiviert und korrekt eingerichtet sein.

So verschieben Sie einen Beleg manuell von einem Mandanten zu einem anderen:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, zum Beispiel **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, den Sie verschieben möchten. Wählen Sie die Belegzeile aus, _nicht_ die Nummer in der Spalte **Nr.**, da dadurch die Dokumentenkarte geöffnet wird.
4. Klicken Sie in der Aktionsleiste auf **Aktionen > Funktion > Verschiebe in Mandant**.
5. Wählen Sie auf der Seite **Verschiebe in Mandant** in der Spalte **Name** den Namen des Mandanten aus, zu dem Sie den ausgewählten Beleg verschieben möchten.
6. Wählen Sie in der Spalte **Belegkategorie** den Kategoriecode aus, zu dem Sie den ausgewählten Beleg verschieben möchten. Wenn die gleiche Belegkategorie im Zielmandanten vorhanden ist, wird der Kategoriecode automatisch ausgefüllt.
7. Wenn der Beleg verschoben wurde, wird in einem Dialogfeld bestätigt, dass der ausgewählte Beleg in den ausgewählten Mandanten verschoben wurde. Wählen Sie **OK**, um das Dialogfeld zu schließen und zum Belegjournal zurückzukehren.

Wenn der Beleg in Schritt 7 oben nicht erfolgreich verschoben werden konnte, wird stattdessen ein Dialogfeld mit einer Fehlermeldung angezeigt. Mögliche Gründe hierfür sind:

- Document Capture wurde im Zielmandanten nicht aktiviert oder nicht richtig eingerichtet. Wählen Sie in diesem Fall **OK**, um das Dialogfeld zu schließen, und stellen Sie dann sicher, dass Document Capture in allen relevanten Mandanten aktiviert und voll funktionsfähig ist.
- Die Konfiguration des Felds **E-Mails importieren und archivieren** unterscheidet sich zwischen den Ausgangs- und Zielkategorien. Passen Sie in diesem Fall die Konfiguration des Felds **E-Mails importieren und archivieren** auf den jeweiligen Seiten der **Dokumentkategorie** im Abschnitt **Herkunftstabelle und Felder** an.

## Belege automatisch zu anderen Mandanten verschieben

Sie können Belege nicht nur manuell verschieben, sondern Document Capture auch so einrichten, dass eingehende Belege unmittelbar nach dem Import automatisch an die entsprechenden Empfängermandanten weitergeleitet werden. Gehen Sie dazu folgendermaßen vor:

So richten Sie die automatische Weiterleitung von Belegen ein:

1. Folgen Sie der Anleitung unter [Mandantensuchtexte einrichten](@DC-443#so-richten-sie-mandantensuchtexte-ein), um Mandantensuchtexte einzurichten. Dies sind Suchbegriffe, die Sie bestimmten Mandanten zuordnen können.
2. Stellen Sie sicher, dass Document Capture in beiden Mandanten, zwischen denen Sie Belege verschieben möchten, aktiviert und eingerichtet ist.
3. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
4. Öffnen Sie die entsprechende Belegkategorie. Um beispielsweise die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**, da dadurch das Belegjournal geöffnet wird), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
5. Aktivieren Sie im Inforegister **OCR-Verarbeitung** die Einstellung **Automatische Verschiebung nach Mandant**.

## Informationen zum Thema

[Die Document Capture-App installieren](/Continia Document Capture/Development and Administration/Online/Installing the Document Capture app.md)\
[Mandantensuchtexte einrichten](/Continia Document Capture/Setting up Document Capture/Setting up general business functionality/Setting up company identification texts.md)