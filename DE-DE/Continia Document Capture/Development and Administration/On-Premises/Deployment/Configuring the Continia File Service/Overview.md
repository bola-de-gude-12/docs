---
title: Überblick über den Continia File Service
date: 16-10-2023
description:
id: DC-123
lang: de
---

# Überblick über den Continia File Service

Der Continia File Service ist ein Speichertyp, der es Ihnen ermöglicht, weiterhin lokalen Dateisystemspeicher und On-Premises OCR in Continia Document Capture zu verwenden und gleichzeitig die Konformität mit der Business Central Universal Code-Initiative von Microsoft sicherzustellen.

> [!IMPORTANT]
> Der Continia File Service funktioniert nur mit On-Premises-Installationen von Document Capture.

Der Dienst dient als Ersatz für den älteren Speichertyp **Dateisystem**, der nicht Cloud-kompatibel ist. Der Continia File Service hingegen ist Cloud-optimiert und hostet einen Webdienst, der als eine Art Vermittler zwischen Microsoft Dynamics 365 Business Central und Ihrem Dateisystem dient. Der Webdienst lädt oder speichert Dateien in vordefinierten Repositories. Dabei handelt es sich um in sich geschlossene Einheiten, die auf einen bestimmten Ordner verweisen, auf den der Benutzer zugreifen kann, der den Continia File Service ausführt. Dabei kann es sich um einen lokalen oder freigegebenen Ordner handeln.

Um unbefugten Zugriff zu verhindern, ist jedes Repository durch einen eigenen, eindeutigen Namen und Autorisierungsschlüssel gesichert. Sowohl den Namen als auch den Autorisierungsschlüssel legen Sie im Rahmen der Konfiguration frei fest.

Um den Continia File Service einzurichten, müssen Sie die folgenden Aktionen in der angegebenen Reihenfolge ausführen:

- [Den Continia File Service installieren](@DC-124).
- [Den Continia File Service konfigurieren](@DC-125).
- [Den Continia File Service in Business Central einrichten](@DC-126).

Klicken Sie für weitere Informationen auf die oben stehenden Links, um ausführliche Artikel mit Anleitungen für jeden einzelnen Prozessschritt zu öffnen.

## Informationen zum Thema

[Dokumentenspeicher einrichten](@DC-3)\
[Überlegungen bei der Migration in die Cloud](@DC-106#uberlegungen-bei-der-migration-in-die-cloud)