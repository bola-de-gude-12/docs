---
title: Datenhosting
date: 07-04-2025
description: Wo sich die Server von Continia befinden und welche Art von Daten diese Server verarbeiten.
id: DC-399
lang: de
---

# Datenhosting

In diesem Artikel wird beschrieben, wo sich die Server von Continia befinden und welche Art von Daten diese Server verarbeiten.

Informationen zur Auswahl des Rechenzentrums, in dem Ihre Daten gespeichert werden, was ab Continia Document Capture 2024 R1 möglich ist, finden Sie unter [Rechenzentren](@DC-215).

## Cloud OCR und Web Approval Portal

Continias Cloud-OCR-Service wird von Microsoft Azure gehostet. Während die Produktionsumgebungen in den von Microsoft als Australien-Ost (Australia East) und Nordeuropa (North Europe) bezeichneten Regionen gehostet werden, befinden sich die Demo-Umgebungen in Westeuropa (West Europe).

Das Web Approval Portal von Continia wird ebenfalls von Microsoft Azure gehostet. Während die Produktionsumgebungen in den von Microsoft als Australien-Ost (Australia East), Zentral-USA (Centrals USA) und Nordeuropa (North Europe) bezeichneten Regionen gehostet werden, befinden sich die Demo-Umgebungen in Westeuropa (West Europe).

Die einzigen Continia bekannten Standortdaten sind der Azure-Server, dem der Business Central-Benutzer zugewiesen ist. Beispiel: Wenn einem Business Central-Benutzer ein geografischer Standort in Kanada zugewiesen ist, erfolgt die Verarbeitung seiner Daten im Rechenzentrum Central USA, da dies der nächstgelegene Azure-Server zu diesem Standort ist.

Beachten Sie Folgendes:

- OCR-verarbeitete Dokumente werden nur bis zum Download gespeichert, Continia behält jedoch 30 Tage lang eine Kopie der Original-E-Mail.

- Wenn diese OCR-verarbeiteten Dokumente nicht heruntergeladen werden, werden sie innerhalb von 180 Tagen automatisch gelöscht.

- Das Abrufen und die Speicherung von E-Mails wird von Amazon Web Service (AWS) in Dublin, Irland, gehostet. Microsoft Azure bietet einen solchen Dienst nicht an.

- Für das Web Approval Portal werden PDFs 24–48 Stunden lang zwischengespeichert, abhängig davon, wann die PDF hochgeladen wird und wann der Cleanup-Job ausgeführt wird.

- Die Aktivierungsdaten für Mandanten werden in Continia-Datenbanken gespeichert, die in Dublin, Irland, gehostet werden.

Weitere Informationen zur globalen Infrastruktur von Microsoft finden Sie unter [Azure-Geografien](https://azure.microsoft.com/de-de/explore/global-infrastructure/geographies) (Microsoft-Artikel).

## Informationen zum Thema

[Rechenzentren](@DC-215)