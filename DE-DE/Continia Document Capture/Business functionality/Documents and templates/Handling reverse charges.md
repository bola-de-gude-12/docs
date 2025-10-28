---
title: Verlagerung der Steuerschuld in Document Capture
date: 25-07-2025
description: So können Sie die Verlagerung der Steuerschuld in Document Capture verwalten.
id: DC-446
lang: de
---

# Verlagerung der Steuerschuld

In diesem Artikel wird der Umgang mit der Verlagerung der Steuerschuld in Continia Document Capture beschrieben.

## Definition

Das Verfahren zur Verlagerung der Steuerschuld ist eine Sonderregelung im Mehrwertsteuersystem, bei der die Verantwortung für die Meldung und Zahlung der Mehrwertsteuer vom Verkäufer auf den Empfänger der Artikel oder Dienstleistungen übergeht. Verfahren zur Verlagerung der Steuerschuld werden typischerweise bei grenzüberschreitenden Transaktionen innerhalb der Europäischen Union (EU) verwendet, um die Mehrwertsteuererklärung zu vereinfachen und Mehrwertsteuerbetrug zu reduzieren.

## So bearbeiten Sie eine Verlagerung der Steuerschuld

Bevor Sie die folgenden Schritte ausführen, müssen Sie die MwSt.-Buchungsmatrix in Microsoft Dynamics 365 Business Central für die Bearbeitung der Verlagerung der Steuerschuld konfigurieren. Weitere Informationen finden Sie unter [Berechnungen und Buchungsmethoden für Mehrwertsteuer einrichten](https://learn.microsoft.com/de-de/dynamics365/business-central/finance-setup-vat) (Microsoft-Artikel).

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, zum Beispiel **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, dessen Vorlage Sie bearbeiten möchten.
4. Achten Sie bei der Belegerkennung darauf, dass sowohl der Brutto- als auch der Nettobetrag erfasst wird. Der tatsächliche Mehrwertsteuerbetrag darf weder auf der Rechnung ausgewiesen noch erfasst werden.
5. Klicken Sie in der auf Aktionsleiste **Vorlage > Buchungseinrichtung**, um die Seite **Buchungseinrichtung** zu öffnen.
6. Wählen Sie die gewünschte Kontoart und die Kontonummer aus. Wählen Sie unter **MwSt.-Produktbuchungsgruppe** die Buchungsgruppe aus, die Sie für die Abwicklung der Verlagerung der Steuerschuld erstellt haben. Zum Beispiel: FULL REVERSE.
7. Bei der Registrierung des Belegs werden die entsprechenden Sachposten erstellt.

> [!TIP]
> Alternativ können Sie ein Lookup-Vorlagenkopffeld erstellen (das mit der **MwSt.-Produktbuchungsgruppe**-Herkunftstabelle verknüpft ist), um die FULL REVERSE-Buchungsgruppe direkt im Beleg statt unter **Buchungseinrichtung** auszuwählen.
> Dies sorgt für eine bessere Übersicht und eine schnellere Bearbeitung beim Umgang mit dem Gesamtrechnungsbetrag. Wenn Sie Rechnungsbeträge auf mehrere Konten buchen, verwenden Sie die Methode mit der Buchungseinrichtung.

