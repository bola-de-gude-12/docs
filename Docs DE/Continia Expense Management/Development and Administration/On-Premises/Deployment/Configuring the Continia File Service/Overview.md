---
title: Expense Management Überblick über den Continia File Service
date: 29-03-2023
description:
id: EM-141
lang: de
---

# Überblick über den Continia File Service

Der Continia File Service ist ein Speichertyp, der es Ihnen ermöglicht, weiterhin lokalen Dateisystemspeicher in Continia Expense Management zu verwenden und gleichzeitig die Konformität mit der Business Central Universal Code-Initiative von Microsoft sicherzustellen.

Der Dienst dient als Ersatz für den älteren Speichertyp **Dateisystem**, der nicht Cloud-kompatibel ist. Der Continia File Service hingegen ist Cloud-optimiert und hostet einen Webdienst, der als eine Art Vermittler zwischen Microsoft Dynamics 365 Business Central und Ihrem Dateisystem dient. Der Webdienst lädt oder speichert Dateien in vordefinierten Repositories. Dabei handelt es sich um in sich geschlossene Einheiten, die auf einen bestimmten Ordner verweisen, auf den der Benutzer zugreifen kann, der den Continia File Service ausführt. Dabei kann es sich um einen lokalen oder freigegebenen Ordner handeln.

Um unbefugten Zugriff zu verhindern, ist jedes Repository durch einen eigenen, eindeutigen Namen und Autorisierungsschlüssel gesichert. Sowohl den Namen als auch den Autorisierungsschlüssel legen Sie im Rahmen der Konfiguration frei fest.

Um den Continia File Service einzurichten, müssen Sie die folgenden Aktionen in der angegebenen Reihenfolge ausführen:

- [Den Continia File Service installieren](@EM-140).
- [Den Continia File Service konfigurieren](@EM-139).
- [Den Continia File Service in Business Central einrichten](@EM-142).

Klicken Sie für weitere Informationen auf die oben stehenden Links, um ausführliche Artikel mit Anleitungen für jeden einzelnen Prozessschritt zu öffnen.

## Informationen zum Thema

[Dokumentenspeicher einrichten](@EM-144)  
[Expense Management von Business Central On-Premises zur Cloud migrieren](@EM-112)