---
title: Belege in Document Capture importieren
date: 09-05-2025
description: So importieren Sie Belege in Document Capture.
id: DC-82
lang: de
---

# Belege importieren

Bevor Sie in Continia Document Capture mit Belegen arbeiten können, müssen die Belege in das System importiert werden. Dieser Artikel beschreibt, welche Möglichkeiten hierfür zur Verfügung stehen.

> [!NOTE]
> Wenn ein Beleg importiert wird, bleibt der ursprüngliche Dateiname erhalten. Außerdem wird eine eindeutige Kennung hinzugefügt, die sicherstellt, dass das Originaldokument unverändert bleibt und nicht überschrieben wird – auch wenn dasselbe Dokument mehrmals importiert wird.

## Per E-Mail

Sie können Belege in Document Capture importieren, indem Sie sie als PDF- oder XML-Dateien an eine E-Mail anhängen und diese E-Mail an eine spezielle E-Mail-Adresse senden, die von Document Capture überwacht wird. In Document Capture gibt es verschiedene Belegkategorien, beispielsweise **Einkauf** für Einkaufsbelege und **Verkauf** für Verkaufsbelege, und jede Belegkategorie verfügt über eine eigene E-Mail-Adresse. Stellen Sie daher sicher, dass Sie Ihre Belege an die richtige Belegkategorie senden. Sie können die Belege, die Sie erhalten, entweder selbst an die jeweilige E-Mail-Adresse weiterleiten oder die ursprünglichen Absender (meist Ihre Kreditoren) bitten, sie direkt an diese E-Mail-Adresse zu senden.

> [!NOTE]
> Zum Beispiel bietet es sich zum Importieren von Belegen in Document Capture an, eine E-Mail-Adresse in Ihrer eigenen Domäne einzurichten und dann alle E-Mails, die an diese Adresse gesendet werden, automatisch an die vom System erstellte und von Document Capture überwachte E-Mail-Adresse weiterzuleiten.

So importieren Sie einen Beleg per E-Mail:

1. Gehen Sie im Microsoft Dynamics 365 Business Central-Rollencenter unter **Continia Document Capture Aktivitäten** zu **Aktionen** und wählen Sie **Beleg senden**.
2. Auf der Seite **Wie kann man Dokumente senden** werden unter **E-Mail-Adresse** die Document Capture-Adressen für die jeweiligen Belegkategorien angezeigt. Kopieren Sie die entsprechende E-Mail-Adresse, zum Beispiel aus der Kategorie **Eingangsrechnungen und -gutschriften**, wenn Sie eine Rechnung importieren möchten.
3. Erstellen Sie in Ihrem E-Mail-Programm eine neue E-Mail, hängen Sie einen Beleg (in diesem Fall eine Einkaufsrechnung) als PDF an und senden Sie die E-Mail an die Adresse, die Sie in Schritt 2 oben kopiert haben. Die E-Mail muss [eine Reihe von Anforderungen erfüllen](/continia-document-capture/getting-started/frequently-asked-questions/minimum-requirements/additional-guidelines#technische-e-mail-anforderungen).
4. Schließen Sie in Business Central die Seite **Wie kann man Dokumente senden**, um zum Rollencenter zurückzukehren.
5. Der von Ihnen gesendete Beleg wird jetzt [von Continia automatisch mit OCR verarbeitet](OCR-processing a document.md) und anschließend im Bereich **Continia Document Capture Aktivitäten** in Ihrem Rollencenter im Stapel **Warten auf OCR** angezeigt.
6. Nach der OCR-Verarbeitung erscheint der Beleg im Stapel **Bereit zum Import**. Von hier aus können Sie den Beleg importieren und sehen, wie viele andere Dateien mit OCR verarbeitet wurden und für den Import bereit sind.
7. Um Ihren Beleg (zusammen mit allen anderen mit OCR verarbeiteten Belegen) zu importieren, gehen Sie zu **Aktionen** und wählen Sie **Dateien importieren**.
8. Wenn der Import abgeschlossen ist, wird in einer Meldung die Anzahl der importierten Dateien angezeigt. Wählen Sie **OK**.

Der Beleg kann jetzt registriert werden und ist im Stapel **Bereit zur Registrierung** verfügbar.

> [!NOTE]
> Dateien, die zur Verarbeitung mit OCR gesendet wurden, werden in der Reihenfolge in die Warteschlange gestellt, in der sie in Continia Online (Cloud OCR) eingegangen sind. In Spitzenzeiten kann die Bearbeitung etwas mehr Zeit als sonst in Anspruch nehmen. Sie können die Seite aktualisieren, um zu sehen, ob eine Datei verarbeitet wurde.

## Einen Netzwerkscanner verwenden (Multifunktionsdrucker, MFP)

Die meisten Netzwerkscanner können so eingerichtet werden, dass sie Belege scannen und als PDF-Dateien an eine festgelegte E-Mail-Adresse senden. Dazu richten Sie Ihren Scanner einfach so ein, dass alle gescannten Dateien als PDF an die E-Mail-Adresse gesendet werden, die von Document Capture überwacht wird, wie oben beschrieben. Es ist keine zusätzliche Konfiguration erforderlich, da Document Capture alle eingehenden E-Mails und deren Anhänge automatisch einliest, wie im obigen Abschnitt beschrieben.

## Einen Desktopscanner verwenden

Document Capture unterstützt das Scannen von Dokumenten mit einem Desktopscanner, der direkt an den PC eines Endbenutzers angeschlossen ist. Document Capture kann mit dem Scanner kommunizieren und den Scanvorgang direkt von Microsoft Dynamics 365 Business Central aus starten. Weitere Informationen zum Anschließen eines Desktopscanners finden Sie unter [Einen Desktopscanner anschließen](/Continia Document Capture/Setting up Document Capture/Setting up general business functionality/Connecting a desktop scanner.md).

Sobald Sie Ihren Desktopscanner angeschlossen haben, können Sie mit dem Scannen von Dokumenten beginnen, indem Sie die folgenden Schritte ausführen:

1. Legen Sie das Dokument, das Sie scannen möchten, auf das Scannerglas oder legen Sie es in den Dokumenteneinzug, je nach Scannertyp. Folgen Sie dann allen weiteren Anweisungen Ihres Scannerherstellers.
2. Wählen Sie in Business Central das Symbol {{search}}, geben Sie **Scannen & OCR** ein, und wählen Sie dann den zugehörigen Link.
3. Gehen Sie im Fenster **Scannen & OCR**, das sich öffnet, zu **Scanner** und wählen Sie Ihren Scanner im Feld aus.
4. Klicken Sie in der Aktionsleiste auf **Scannen**, um das Dokument zu scannen.

## Über das Continia Delivery Network

Das Continia Delivery Network verbindet Sie mit Netzwerken wie dem globalen Peppol eDelivery Network und dem dänischen NemHandel, wodurch Sie elektronische Dokumente direkt in Business Central importieren können. Weitere Informationen finden Sie unter [Grundlegendes zum Continia Delivery Network](@DC-53).

## Informationen zum Thema

[Technische E-Mail-Anforderungen](/continia-document-capture/getting-started/frequently-asked-questions/minimum-requirements/additional-guidelines#technische-e-mail-anforderungen)  
[OCR-Verarbeitung von Belegen](OCR-processing a document.md)  
[Einen Desktopscanner anschließen](/Continia Document Capture/Setting up Document Capture/Setting up general business functionality/Connecting a desktop scanner.md)  
[Grundlegendes zum Continia Delivery Network](@DC-53)