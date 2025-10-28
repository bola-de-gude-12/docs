---
title: Geschäftsfunktionen in Document Capture
date: 14-07-2025
description: Detaillierte Informationen über die in der neuesten Version von Document Capture enthaltenen Funktionen.
id: DC-49
lang: de
---

# Geschäftsfunktionen

Als End-to-End-Lösung für den Import, die Verarbeitung, Registrierung, Genehmigung und Archivierung von PDF-Rechnungen oder Rechnungen in elektronischem Format und anderen Geschäftsbelegen bietet Continia Document Capture erhebliche Vorteile für eine Vielzahl von Unternehmen. Sie können damit Prozesse vereinfachen und die Kosten für die Eingabe von Daten in Unternehmen in so unterschiedlichen Sektoren wie Finanzen, Gesundheitswesen, Fertigung, Transport usw. senken.

Document Capture ist modular aufgebaut und kann an Ihre speziellen Geschäftsanforderungen angepasst werden. Jedes der verfügbaren Module stellt einen Funktionsbereich dar. Sie können mithilfe der unterstützten Einrichtung, auf die Sie direkt über Ihr Rollencenter in Microsoft Dynamics 365 Business Central zugreifen können, beliebige Module hinzufügen.

> [!IMPORTANT]
> Nicht alle Funktionen sind in allen Versionen von Document Capture verfügbar. Informationen zu den in den einzelnen Versionen von Document Capture verfügbaren Funktionen finden Sie unter [Funktionsvergleich in verschiedenen Versionen von Document Capture](@DC-46).

Im Folgenden finden Sie eine Beschreibung der einzelnen Module sowie einen Überblick über ihre jeweiligen Funktionen.

## Basis

Mit dem obligatorischen **Basis**-Modul können Sie Einkaufsrechnungen und Gutschriften in Business Central importieren. Importiert werden können gescannte Belege oder mit Texterkennung (OCR) verarbeitete PDF-Dateien sowie XML-Dateien in verschiedenen Formaten, beispielsweise Peppol und XRechnung, über das Continia Delivery Network (CDN).

Das Modul ermöglicht es Ihnen, Kopffelder in Belegen mithilfe von OCR zu erkennen und die erkannten Daten der eigentlichen Position im Belegtext zuzuordnen. Mit dieser einmaligen Zuordnung kann der Prozess für alle zukünftigen Belege, die vom selben Kreditor eingehen, automatisiert werden.

> [!NOTE]
> Das **Basis**-Modul ist auf die Erkennung von Daten im Belegkopf sowie auf Einkaufsrechnungen und Gutschriften beschränkt. Um Felder auf der Zeilenebene zu erkennen und weitere Arten von Geschäftsbelegen zu verarbeiten, müssen Sie ein Upgrade auf das [Modul **Erweitert**](/continia-document-capture/getting-started/business-functionality#erweitert) durchführen.

Mit dem **Basis**-Modul erhalten Sie Zugriff auf die folgenden Hauptfunktionen:

| Funktion                                                                                                                                                                                                                                                 |   Enthalten   |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-----------: |
| Anzeigen und Überprüfen von Bildern in Business Central                                                                                                                                                                                                  | {{checkmark}} |
| Hinzufügen von Anhängen zu beliebigen Datensätzen per Drag & Drop                                                                                                                                                                    | {{checkmark}} |
| Erkennung und Verarbeitung von Einkaufsrechnungen und Gutschriften                                                                                                                                                                                       | {{checkmark}} |
| Erkennung von benutzerdefinierten Feldern und dynamische Übertragung erkannter Werte in Einkaufsbelege                                                                                                                                                   | {{checkmark}} |
| Erkennung unterschiedlicher Beträge (zum Beispiel für Kosten plus Fracht)                                                                                                                                                             | {{checkmark}} |
| Erkennung unterschiedlicher Mehrwertsteuer-/Steuersätze und Zuordnung zu den entsprechenden Sachkonten                                                                                                                                                   | {{checkmark}} |
| Verwenden fester Werte in beliebigen Feldern                                                                                                                                                                                                             | {{checkmark}} |
| Leichtes Anpassen des Erkennungsbereichs auf gescannten Belegen                                                                                                                                                                                          | {{checkmark}} |
| Konfigurieren von Regeln für Felder, damit die richtigen Werte erkannt werden (z. B. spezielles Format, nur positive Beträge)                                                                         | {{checkmark}} |
| Kreditorenspezifische Einstellungen und Vorlagen für Erkennung und Validierung                                                                                                                                                                           | {{checkmark}} |
| Suchtextvorschläge für Felder von Mastervorlagen, einschließlich der Möglichkeit, diese Vorschläge zu ignorieren                                                                                                                                         | {{checkmark}} |
| Unterstützte Einrichtung zum Erstellen von Vorlagenfeldern                                                                                                                                                                                               | {{checkmark}} |
| Konfigurieren, ob Beträge Mehrwertsteuer/Steuer enthalten oder nicht                                                                                                                                                                                     | {{checkmark}} |
| Manuelles Aufteilen von PDF-Dateien in Business Central (z. B. bei mehreren Rechnungen in einer PDF-Datei)                                                                                            | {{checkmark}} |
| Direkte Integration in Business Central zur Erweiterung der App-Funktionalität                                                                                                                                                                           | {{checkmark}} |
| Sicheres digitales Archiv mit Volltextsuchfunktion                                                                                                                                                                                                       | {{checkmark}} |
| Automatisierte Prüfung von Bankkonten, Umsatzsteuer-Identifikationsnummern und Telefonnummern zur Vermeidung von Betrug                                                                                                                                  | {{checkmark}} |
| Erfassung von QR-Codes und Extrahieren der Daten                                                                                                                                                                                                         | {{checkmark}} |
| Registrieren von Belegen direkt in Fibu Buch.-Blättern unter Verwendung eines Kreditors, einer Bank oder eines Sachkontos als Gegenkonto                                                                                                 | {{checkmark}} |
| Anzeigen von Belegen in Zahlungsausgangs Buch.-Blättern                                                                                                                                                                                  | {{checkmark}} |
| Dokumentenvorschau auf der Seite **Kreditorenposten**                                                                                                                                                                                                    | {{checkmark}} |
| Betragsverteilungscodes, um festzulegen, wie Beträge beim Erstellen von Einkaufszeilen Konten und Dimensionen zugeordnet werden                                                                                                                          | {{checkmark}} |
| Konfigurieren von Kommentartypen und automatische Zuweisung von Belegen zu bestimmten Benutzern bei Fehlern                                                                                                                                              | {{checkmark}} |
| Benachrichtigung über verbleibende Seiten in OCR-Lizenzen                                                                                                                                                                                                | {{checkmark}} |
| Automatische Erkennung von Kreditoren und Feldern beim Verschieben von Belegen in andere Mandanten                                                                                                                                                       | {{checkmark}} |
| Automatische Deaktivierung von Continia-Lösungen beim Kopieren von Mandanten                                                                                                                                                                             | {{checkmark}} |
| Anzeigen des Originalabsenders der E-Mail in **Bereit zum Import** bei Verwendung von Cloud OCR (anstelle einer anderen, zwischengeschalteten E-Mail)                                                                                 | {{checkmark}} |
| Benachrichtigungen über offene, nicht registrierte Belege an die zuständigen Mitarbeitenden                                                                                                                                                              | {{checkmark}} |
| Automatisches Einfügen des Arbeitsdatums bzw. des aktuellen Datums in allen Belegen durch Eingabe von **ARBEITSDATUM** und **HEUTE** (bzw. Stichwörtern wie Arbeits, Heu/Heut) in Vorlagenfeldformeln | {{checkmark}} |
| Secure Archive, ein Archiv, das Ihre digitalen Buchhaltungsbelege automatisch und sicher im Original speichert                                                                                                                                           | {{checkmark}} |
| Continia Hub, eine zentrale Hilfsplattform direkt in der App, die auf Benutzerfreundlichkeit abzielt und wo Sie Feedback geben können                                                                                                                    | {{checkmark}} |
| Unterstützung für die QR-Bill Management App von Microsoft                                                                                                                                                                                               | {{checkmark}} |
| Dokumentenkontrollprotokoll: Bietet einen zentralen Überblick über Dokumente, die aufgrund von Problemen mit der Dateiprüfsumme oder Änderungen nach der Genehmigung besondere Aufmerksamkeit erfordern                                  | {{checkmark}} |
| Unterstützung für Multi-Entity-Management (MEM) von Binary Stream Software                                                                                                                                                            | {{checkmark}} |
| Automatisierte Datenpflegeprozesse zum Löschen erfasster Wörter, generierter Werte und ganzer Datensätze basierend auf Dokumentstatus und -alter, um die Einhaltung der DSGVO sowie die Wahrung von Datenschutz und Datenintegrität zu gewährleisten     | {{checkmark}} |
| Continia eDokumente: proprietäre Funktionen, mit denen Sie eAbrechnungs- und eBestelldokumente (XML) direkt aus Business Central verwalten und austauschen können.                                    | {{checkmark}} |
| Continia Delivery Network: ein Service, der mit dem Peppol eDelivery Network und dem NemHandel-Netzwerk integriert ist und Ihnen das Senden und den Empfang elektronischer Dokumente in Business Central ermöglicht.     | {{checkmark}} |
| Unterstützung von Rechnungsrabatten und Umlagekonten                                                                                                                                                                                                     | {{checkmark}} |
| Berechnung von Fälligkeitsdaten basierend auf Zahlungstagen (Spanien)                                                                                                                                                                 | {{checkmark}} |
| Warnungen bei Rechnungen, die bereits über Continia Expense Management bezahlt und registriert wurden                                                                                                                                                    | {{checkmark}} |
| Verwaltung von Zahlungsmitteln in Continia eDocuments                                                                                                                                                                                                    | {{checkmark}} |

## Erweitert

Mit dem Modul **Erweitert** können Sie außer Einkaufsrechnungen und Gutschriften auch weitere Geschäftsbelege importieren und mit OCR verarbeiten, unter anderem auch benutzerdefinierte Dokumente. Außerdem können damit sowohl Daten in den Kopffeldern als auch auf Zeilenebene erfasst und Geschäftsbelege beim Import ggf. automatisch aufgeteilt werden. Das Modul bietet sich besonders an, wenn Sie komplexe Dokumente, große Mengen an Belegen von mehreren Kreditoren importieren müssen.

Das Modul **Erweitert** umfasst die folgenden Hauptfunktionen:

| Funktion                                                                                                                                                                                                                                                           |   Enthalten   |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | :-----------: |
| Erkennung beliebiger Belegarten (z. B. Aufträge, Einkaufsbelege, mitarbeiterbezogene Dokumente, Lieferscheine usw.) und Anpassen von Feldern, die in diesen Belegarten ausgelesen werden sollen | {{checkmark}} |
| Zeilenerkennung, einschließlich KI-unterstützter Zeilenerfassung, Kombination von KI mit manueller Erfassung, Erfassung von Zeilen über mehrere Reihen, relative Zeilenerfassung und Erfassung von Feldsuchtexten auf Zeilenebene                                  | {{checkmark}} |
| Artikelreferenz für Zeilenübersetzung                                                                                                                                                                                                                              | {{checkmark}} |
| Automatische Aufteilung von PDF-Dateien in Business Central, beispielsweise anhand von Barcodes oder Rechnungsnummer                                                                                                                                               | {{checkmark}} |
| Automatisches Verschieben von Belegen zum richtigen Mandanten anhand von Mandantensuchtexten                                                                                                                                                                       | {{checkmark}} |
| Automatische Überprüfung von Artikelpreisen                                                                                                                                                                                                                        | {{checkmark}} |
| Unterstützung für Vorauszahlungen (zum Beispiel Advance Letters) in der Tsche­chi­schen Re­pu­b­lik                                                                                                                                             | {{checkmark}} |
| Eigene Kategorie zum Erstellen und Aktualisieren von Bestellungen                                                                                                                                                                                                  | {{checkmark}} |
| Automatische Zuweisung von Zu-/Abschlägen bei der Belegregistrierung                                                                                                                                                                                               | {{checkmark}} |
| Dokumentenvorschau auf den Seiten **Sachposten** und **Fibu. Buch-Blätter**                                                                                                                                                                        | {{checkmark}} |
| Ändern importierter Beträge in Fibu. Buch- und Einkaufs Buch.-Blättern                                                                                                                                                             | {{checkmark}} |
| Aktualisieren von Bestellungen auf Basis von Lieferscheinen und anderen Empfangsdokumenten, um den Wareneingangsprozess zu automatisieren                                                                                                                          | {{checkmark}} |

## Bestellabgleich

Mit dem Modul **Bestellabgleich** können Sie eingehende Geschäftsbelege wie Einkaufsrechnungen und Gutschriften mit den entsprechenden Belegen wie Bestellungen, Reklamationen oder Rücklieferungen abgleichen. Die Belege werden verglichen, um sicherzustellen, dass sie übereinstimmen. Stimmen die Belege überein (z. B. hinsichtlich des Preises oder der Stückzahl), können sie automatisch verarbeitet und genehmigt werden. Ist dies nicht der Fall, müssen die entsprechenden Abweichungen abgeklärt werden. Sie können die Toleranzgrenzen für solche Abweichungen manuell konfigurieren.

Mit dem Modul **Bestellabgleich** erhalten Sie Zugriff auf die folgenden Hauptfunktionen:

| Funktion                                                                                                                                          |   Enthalten   |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | :-----------: |
| Integrierte Dokumentenvorschau als Teil des Abgleichprozesses                                                                                     | {{checkmark}} |
| Manueller Abgleich mit Eingangslieferungen und Reklamationen                                                                                      | {{checkmark}} |
| Abgleich mit ungebuchten Bestellungen und ungebuchten Rücklieferungen                                                                             | {{checkmark}} |
| Automatischer Abgleich mit Bestellungen, Eingangslieferungen, Reklamationen und Rücklieferungen                                                   | {{checkmark}} |
| Abgleich basierend auf Lieferungsnummer und Bestellnummer von Kreditoren                                                                          | {{checkmark}} |
| Konfigurierbarer und automatischer Abgleich Zeile für Zeile<a href="#footnote-1.1"><sup>1</sup></a>                                               | {{checkmark}} |
| Automatisierte, durch Regeln festgelegte Toleranz für die zulässige Differenz zwischen Bestell- und Rechnungsbeträgen sowie anschließende Buchung | {{checkmark}} |
| Automatisches Kopieren von Dimensionen aus dem Belegkopf der Bestellung in die Rechnung                                                           | {{checkmark}} |
| Aktualisieren bestehender Bestellungen oder Reklamationen anstelle von Rechnungen oder Gutschriften                                               | {{checkmark}} |
| Unterstützung von Serien- und Chargennummern beim Abgleichprozess                                                                                 | {{checkmark}} |
| Einbeziehung der Paketverfolgung beim Bestell- und Lieferungsabgleich                                                                             | {{checkmark}} |
| Anwendung von Toleranzbeträgen/-prozentsätzen auf Zeilenebene                                                                                     | {{checkmark}} |
| Hinzufügen fehlender Bestellzeilen beim Abgleich                                                                                                  | {{checkmark}} |
| Automatischer Abgleich über Aufgabenwarteschlangen                                                                                                | {{checkmark}} |
| Abgleich von Einkaufsrechnungen mit unterschiedlichen Einheiten in der Bestellung                                                                 | {{checkmark}} |

<br>

<small style><div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.1">Beachten Sie, dass für diese Funktion auch die Installation des Moduls „Erweitert“ erforderlich ist.</li>
  </ol>
</div>
</small>

## Genehmigungen

Das Modul **Genehmigungen** bietet Ihnen einen vollständigen Genehmigungsworkflow, mit dem Sie Geschäftsdokumente genehmigen, Genehmiger zuweisen und Genehmigungslimits festlegen können. Sie können die Genehmigung von Dokumenten erzwingen, sie auf Abwarten setzen oder automatisch genehmigen lassen. Außerdem ist es möglich, Dokumente weiterzuleiten und Genehmigungen zu delegieren, wenn Sie beispielsweise für einen bestimmten Zeitraum nicht im Büro sind.

Das Modul **Genehmigungen** bietet Ihnen Zugriff auf die folgenden Hauptfunktionen:

| Funktion                                                                                                                                                                                    |   Enthalten   |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-----------: |
| Verbesserung mehrerer gängiger Workflow- und Genehmigungsszenarien, die in Business Central standardmäßig nicht unterstützt werden                                                          | {{checkmark}} |
| Integrierte Dokumentenvorschau als Teil des Genehmigungsprozesses                                                                                                                           | {{checkmark}} |
| Automatische Genehmigung und Buchung innerhalb vordefinierter Limits                                                                                                                        | {{checkmark}} |
| Kombinieren und Senden aller zu genehmigenden Rechnungen in einer E-Mail                                                                                                                    | {{checkmark}} |
| Geteilte Genehmigung bei Abwesenheit (z. B. Urlaub)                                                                                      | {{checkmark}} |
| Geteilte Genehmigung, bei der Personen Genehmigungen für andere übernehmen können                                                                                                           | {{checkmark}} |
| Weiterleiten von Rechnungen und Gutschriften zur Genehmigung an eine bestimmte Person                                                                                                       | {{checkmark}} |
| Vier-Augen-Genehmigung (d. h. mindestens zwei Personen prüfen alle Rechnungen)                                                           | {{checkmark}} |
| Prüfung von Dimensionen und Beträgen bei der Genehmigung                                                                                                                                    | {{checkmark}} |
| Betragsprüfung beim Buchen, um gebuchte Beträge mit tatsächlichen Beträgen in zu vergleichen                                                                                                | {{checkmark}} |
| Anfordern vordefinierter Ursachencodes, wenn eine Rechnung oder Gutschrift auf Abwarten gesetzt oder abgelehnt wird                                                                         | {{checkmark}} |
| Vorbuchen von Einkäufen im Hauptbuch vor der Genehmigung von Belegen                                                                                                                        | {{checkmark}} |
| Genehmigungsworkflows basierend auf vorkonfigurierten Genehmigern                                                                                                                           | {{checkmark}} |
| Erweiterte Genehmigung zur Genehmigung von Dokumenten basierend auf Dimensionscodes                                                                                                         | {{checkmark}} |
| Kostenloses Online-Hosting mit Continia Software<a href="#footnote-2.1"><sup>1</sup></a>                                                                                                    | {{checkmark}} |
| Direkte Verbindung zu Business Central über Webdienste (vollständige Übereinstimmung der Daten)<a href="#footnote-2.1"><sup>1</sup></a>                                  | {{checkmark}} |
| Eine intuitive Benutzeroberfläche für Benutzer zum Genehmigen von Einkaufsrechnungen, Gutschriften und anderen Geschäftsbelegen<a href="#footnote-2.1"><sup>1</sup></a>                     | {{checkmark}} |
| Funktionalität, mit der Benutzer problemlos Zeilen ändern, Belege genehmigen und auf Abwarten setzen, Belege an andere Benutzer weiterleiten sowie Anhänge und Kommentare hinzufügen können | {{checkmark}} |
| Konfigurieren von Konten- und Dimensionsbeschränkungen zur Vereinfachung der Auswahl<a href="#footnote-2.1"><sup>1</sup></a>                                                                | {{checkmark}} |
| Genehmigungen durch eingeschränkte Benutzer von Business Central                                                                                                                            | {{checkmark}} |
| Durchsuchbares, sicheres Archiv<a href="#footnote-2.1"><sup>1</sup></a>                                                                                                                     | {{checkmark}} |
| Vordefinierte Vorlagen zum automatischen Erstellen von Zeilen in Rechnungen und Gutschriften                                                                                                | {{checkmark}} |
| Genehmigung von Bestellungen und Reklamationen mit Continia-Genehmigungsworkflows, einschließlich des Continia Web Approval Portals                                                         | {{checkmark}} |
| Benutzerspezifische Genehmigerliste für die Weiterleitung von Genehmigungsanforderungen                                                                                                     | {{checkmark}} |
| Verhindern, dass Genehmiger den Abwartestatus zu genehmigender Belege ändern können                                                                                                         | {{checkmark}} |
| Option, mit der beide Benutzertypen bei geteilter Genehmigung Benachrichtigungen empfangen können                                                                                           | {{checkmark}} |
| Ein Beleg kann auf Abwarten gesetzt und gleichzeitig genehmigt werden                                                                                                                       | {{checkmark}} |
| Sortieren nach Fälligkeitsdatum bzw. Fälligkeitsdatum der Genehmigung auf der Seite **Genehmigungsposten**                                                                  | {{checkmark}} |
| Mandantenübergreifende Genehmigung von Dokumenten im Web Approval Portal                                                                                                                    | {{checkmark}} |

<br>

<small style>

<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-2.1">Beachten Sie, dass Sie zur Nutzung dieser Funktion auch das Web Approval Portal benötigen.</li>
  </ol>
</div>

</small>

## Einkaufsverträge

Mit dem Modul **Einkaufsverträge** können Sie Ihre Einkaufsverträge einfach verwalten und regelmäßig überprüfen lassen, um sie stets auf dem neuesten Stand zu halten. Es ermöglicht Ihnen einen Überblick über Ihre Verträge und Abonnements und vereinfacht den Prozess zum Überprüfen von Verträgen. Außerdem können Einkaufsbelege bei der Registrierung automatisch genehmigt werden, wenn deren Beträge den Vertragsbeträgen innerhalb vorgegebener Abweichungen entsprechen.

Mit dem Modul **Einkaufsverträge** erhalten Sie Zugriff auf die folgenden Hauptfunktionen:

| Funktion                                                                                                                                                   |   Enthalten   |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------- | :-----------: |
| Zentralisierte Verwaltung und Speicherung aller Einkaufsverträge, Abonnements und anderer wiederkehrender Kosten                                           | {{checkmark}} |
| Erstellen von Verträgen mit allen relevanten Informationen wie Kreditor, Preisen, Vertragsbeginn und -ende sowie detaillierten Vertragszeilen              | {{checkmark}} |
| Umfangreiches Archiv mit allen vertragsrelevanten Dokumenten und Dateien der Einkaufsverträge                                                              | {{checkmark}} |
| Erstellen von Verträgen basierend auf wiederkehrenden Rechnungen                                                                                           | {{checkmark}} |
| Automatisches Ausfüllen der Vertragsdetails beim Verarbeiten von Rechnungen im Belegjournal                                                                | {{checkmark}} |
| Unkomplizierte und regelmäßige Überprüfung, damit Sie nur für das bezahlen, was Sie auch brauchen                                                          | {{checkmark}} |
| Automatisches Starten der Überprüfung in regelmäßigen Abständen basierend auf Unternehmensrichtlinien                                                      | {{checkmark}} |
| Möglichkeit zur Überprüfung aller Verträge vor Beginn eines neuen Geschäftsjahres                                                                          | {{checkmark}} |
| Überblick über Verträge, die zur Genehmigung gesendet werden müssen                                                                                        | {{checkmark}} |
| E-Mail-Benachrichtigungen an Vertragsgenehmiger wenn Verträge zur Genehmigung anstehen                                                                     | {{checkmark}} |
| Eine intuitive Benutzeroberfläche, die eine einfache Genehmigung von Verträgen in Business Central oder im Web Approval Portal ermöglicht                  | {{checkmark}} |
| Vertragsgenehmiger können problemlos Zeilen ändern, Verträge genehmigen und stornieren sowie Anhänge und Kommentare hinzufügen                             | {{checkmark}} |
| Automatische Genehmigung wiederkehrender Rechnungen innerhalb zulässiger Toleranzen basierend auf genehmigten Verträgen                                    | {{checkmark}} |
| Automatische Erstellung von Einkaufsverträgen, ein System, das die Erstellung von Verträgen basierend auf Mustern in wiederkehrenden Rechnungen vorschlägt | {{checkmark}} |

## Informationen zum Thema

[Veröffentlichungsplan](@DC-56)\
[Funktionsverwaltung](@DC-455)

<style>
  .content table tr td:nth-child(1) {
    width: 500px;
  }
  .content table tr td:nth-child(2) {
    width: 50px;
  }  
  .content table tr td:nth-child(3) {
    width: 50px;
  }  
</style>