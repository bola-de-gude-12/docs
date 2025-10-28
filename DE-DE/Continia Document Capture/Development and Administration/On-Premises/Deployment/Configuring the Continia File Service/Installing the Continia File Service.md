---
title: Den Continia File Service installieren
date: 16-10-2023
description:
id: DC-124
lang: de
---

# Den Continia File Service installieren

> [!IMPORTANT]
> Der Continia File Service funktioniert nur mit On-Premises-Installationen von Document Capture.

Um den Continia File Service zu installieren, führen Sie diese Schritte aus:

1. Stellen Sie sicher, dass Sie eine Version von Continia Document Capture ausführen, die den Continia File Service unterstützt (Document Capture 2023 R1 (11.00) oder höher).
2. Gehen Sie zur [Continia PartnerZone](https://partnerzone.continia.com/) > **Downloads** (nur für Continia-Partner verfügbar) und laden Sie das entsprechende Produktpaket herunter.
3. Extrahieren Sie das Produktpaket in einen Ordner auf Ihrem Computer.
4. Führen Sie setup.exe vom Stammverzeichnis des Softwareverzeichnisses aus, um das Installationsprogramm zu öffnen.
5. Wählen Sie im Installationsprogramm **File Service** > **Install**. Beachten Sie, dass der Continia File Service auf einem Server mit Zugriff auf die Dateien installiert sein muss.
6. Wählen Sie **Schließen**, um das Installationsprogramm zu schließen und den Installationsvorgang abzuschließen.
7. Stellen Sie sicher, dass alle relevanten TCP-Ports in den entsprechenden Firewalls geöffnet sind.
   > [!NOTE]
   > Die TCP-Ports müssen dieselben sein wie die, die Sie im Continia File Service Configuration-Tool eingeben, wenn Sie [den Continia File Service konfigurieren](@DC-125).

Jetzt können Sie ein Repository und einen Autorisierungsschlüssel für den Dienst konfigurieren. Informationen hierzu finden Sie unter [Den Continia File Service konfigurieren](@DC-125).