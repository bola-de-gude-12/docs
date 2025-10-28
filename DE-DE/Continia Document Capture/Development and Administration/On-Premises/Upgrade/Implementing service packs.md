---
title: Service Packs implementieren
description:
date: 03-06-2025
id: DC-167
lang: de
---

# Service Packs implementieren

> [!NOTE]
> Dieser Artikel beschreibt den Prozess der Implementierung von Service Packs für FOB-Versionen von Microsoft Dynamics NAV/365 Business Central. Informationen zum Upgrade von Document Capture für App-Versionen von Business Central finden Sie unter [Upgrade von Continia Document Capture für App-Versionen von Business Central](@DC-6).

Seit der Veröffentlichung von Continia Document Capture Version 4.50 hat Continia regelmäßig Service Packs mit Codekorrekturen veröffentlicht. Die Service Packs sind einfach zu implementieren, erfordern keine Datenkonvertierung und Sie müssen lediglich neue Objekte importieren. Daher empfehlen wir allen Continia-Partnern dringend, sie regelmäßig zu implementieren.

Jedes Service Pack bringt viele neue Funktionen und Fehlerbehebungen für Document Capture und verbessert Ihr allgemeines Benutzererlebnis erheblich. Beispielsweise enthielten die Service Packs 1 bis 3 für Document Capture 2022 R2 (v10.00) mehr als 170 Verbesserungen, was zu einem deutlich stabileren und funktionsreicheren System im Vergleich zu früheren Versionen führte.

Continia veröffentlicht im Allgemeinen neue Service Packs in den folgenden Fällen:

- Es wurden genügend Probleme behoben, um die Veröffentlichung eines Service Packs zu rechtfertigen.
- Ein kritisches Problem wurde identifiziert und behoben.

Nach jeder Veröffentlichung einer neuen Hauptversion von Document Capture werden Service Packs in Abständen von 2–3 Monaten oder immer dann veröffentlicht, wenn kritische Probleme behoben wurden. Allerdings nimmt die Häufigkeit der Veröffentlichung von Service Packs im Laufe der Zeit normalerweise ab. Continia veröffentlicht weiterhin Service Packs für die beiden neuesten Versionen von Document Capture, solange kritische Probleme erkannt werden.

## So implementieren Sie ein Service Pack

Sie können ein Service Pack implementieren, indem Sie die folgenden Schritte ausführen:

1. Gehen Sie zur [Continia PartnerZone](https://partnerzone.continia.com/downloads/) (nur für Partner verfügbar).
2. Identifizieren Sie im Abschnitt **Downloads** das Service Pack, das Sie herunterladen möchten, und klicken Sie dann auf **Download**.
3. Die heruntergeladene ZIP-Datei enthält den gesamten Produktordner. Gehen Sie zum Ordner **..\Objects\Document Capture**, um die Document Capture-Objekte zu suchen. Beachten Sie, dass die Objektdateien alle Dokumentobjekte enthalten.
4. Extrahieren Sie die Service Pack-Objekte aus den Objektdateien.
5. Importieren Sie die Objekte in NAV/Business Central mit dem **Object Designer**.

Das Service Pack ist jetzt implementiert und einsatzbereit.

## Informationen zum Thema

[Upgrade auf die neueste Version](@DC-58)  
[Software Lifecycle-Richtlinie und Continia Document Capture On-Premises](@DC-13)  
[Ereignisse und externe Funktionen anfordern](@DC-27)