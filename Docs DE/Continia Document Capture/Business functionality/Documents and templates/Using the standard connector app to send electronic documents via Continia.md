---
title: Verwenden der Standard-Connector-App zum Senden elektronischer Belege über Continia
date: 26-08-2025
description: So konfigurieren Sie die E-Document Connector-Anwendung von Continia.
id: DC-173
lang: de
---

# Die Standard-Connector-App zum Senden elektronischer Belege über Continia verwenden

Microsoft Dynamics 365 Business Central enthält eine Standard-Connector-App, mit der Sie elektronische Belege senden können, ohne direkt auf Erweiterungen von Drittanbietern angewiesen zu sein.

Dies ist mit dem **E-Document Connector – Continia** möglich, der Continia als E-Belegdienstanbieter verwendet und auf der Seite **Erweiterungsverwaltung** verfügbar ist.

Weitere Informationen finden Sie unter [Übersicht über Connectors](https://learn.microsoft.com/de-de/connectors/overview) (Microsoft-Artikel).

## Überlegungen zur Verwendung des Connectors

- Die Konfiguration verwendet die Standardlogik von Business Central zum Generieren von XML-Dokumenten, nicht Continia-Apps. Continia dient lediglich als Transportebene und stellt sicher, dass Belege von Business Central über das elektronische Netzwerk zum Empfänger gelangen – und umgekehrt.
- Die Teilnahmegenehmigung dauert ca. 1-2 Werktage. Um den Genehmigungsstatus zu überprüfen, gehen Sie zu **E-Belegdienste > Continia >Dienstintegration einrichten > Anzahl der Teilnahmen > Registrierungsstatus**.
- Für die Abwicklung der Empfangsseite ist der Empfänger verantwortlich.

## So richten Sie den E-Document Connector – Continia ein

Die folgenden Schritte beschreiben, wie Sie Continia mithilfe des Standard-Connectors als Standard-Dienstanbieter für elektronische Belegformate konfigurieren.

1. Suchen Sie ({{search}}) nach **Erweiterungsverwaltung** und wählen Sie den entsprechenden Link aus. Suchen Sie dann nach **E-Document Connector - Continia** und installieren Sie die Erweiterung.
2. Erstellen Sie einen E-Belegdienst, indem Sie der Dokumentation von Microsoft folgen, und wählen Sie dann **Continia** im Feld **Dienstintegration** aus.
3. Klicken Sie in der Aktionsleiste auf **Dienstintegration einrichten** und klicken Sie auf der Seite **Continia E-Document External Connection Setup** auf **Neue Teilnahme registrieren**, um den Onboarding-Prozess zu starten.

> [!NOTE]
> Sie müssen diesen Prozess wiederholen, um zusätzliche Teilnahmen zu registrieren. Beispielsweise einmal zur Registrierung von Peppol und einmal zur Registrierung von NemHandel.

4. Geben Sie die PartnerZone-Anmeldeinformationen Ihres Partners ein. Dies ist nur beim ersten Onboarding erforderlich.
5. Geben Sie die rechtlichen Informationen Ihres Unternehmens ein. Stellen Sie sicher, dass diese Informationen korrekt sind, da sie über KYC-Prozesse (Know Your Customer) validiert werden.
6. Geben Sie die Rechnungsdaten Ihres Unternehmens ein. Wenn Sie dies zu einem späteren Zeitpunkt bearbeiten müssen, gehen Sie zu **E-Belegdienste > Continia > Dienstintegration einrichten > Abonnement > Bearbeiten**.
7. Wählen Sie die Belegarten aus, die Sie senden und empfangen möchten. Wenn Sie unsicher sind, wählen Sie alle verfügbaren Arten aus.
8. **OPTIONAL:** Wenn Sie mehr Details benötigen, klicken Sie auf **Erweiterte Einrichtung**, um die gewünschten Netzwerkprofile auszuwählen und jedem von ihnen einen E-Beleg-Dienstcode zuzuordnen. Dies ist auch nach Abschluss des Onboarding-Einrichtungsassistenten durch Bearbeiten der Teilnahme möglich.
9. Kehren Sie nach Abschluss des Onboardings zur erstellten E-Belegdienstseite zurück (z. B.: CONTINIA) und wählen Sie den Wert im Feld **Anzahl von Netzwerkprofilen** unter dem Inforegister **Allgemein** aus.
10. Klicken Sie im Dialogfeld **E-Document Service Network Profiles** in der Aktionsleiste auf **Hinzufügen**. Für jedes Netzwerk, an dem Sie teilnehmen (z. B. Peppol, NemHandel), müssen Sie E-Belegdienste konfigurieren, da jeder Dienst nur ein Format verarbeiten kann. Beispiel: Wenn Sie einen E-Belegdienst einrichten, der XRechnung-Dokumente sendet und empfängt, wählen Sie XRechnung-Profile aus.
11. Kehren Sie zur Seite **E-Belegdienst** zurück und klicken Sie in der Aktionsleiste auf **Zu exportierende Dokumente konfigurieren**. Überprüfen Sie die Liste der Herkunftsbelegarten und fügen Sie bei Bedarf Typen hinzu, indem Sie in der Aktionsleiste auf **Neu** klicken.

> [!TIP]
> Informationen zum Einrichten von Sendeprofilen und Workflows finden Sie unter [E-Belege einrichten](https://learn.microsoft.com/de-de/dynamics365/business-central/finance-how-setup-edocuments) (Microsoft-Artikel).

## So bearbeiten Sie eine Connector-Teilnahme

So bearbeiten Sie eine bereits im Connector eingerichtete Teilnahme:

1. Suchen Sie ({{search}}) nach **E-Belegdienste** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code des gewünschten Dienstes. Zum Beispiel: CONTINIA.
3. Klicken Sie in der Aktionsleiste auf **Dienstintegration einrichten**.
4. Klicken Sie auf den Wert im Feld **Anzahl der Teilnahmen** und klicken Sie dann in der Aktionsleiste auf **Bearbeiten**.
5. Bestätigen Sie mit dem Schalter unten im Dialogfeld und klicken Sie dann auf **Weiter**.
6. Nehmen Sie die erforderlichen Änderungen vor.
