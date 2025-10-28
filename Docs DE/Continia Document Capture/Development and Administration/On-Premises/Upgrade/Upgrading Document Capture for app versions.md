---
title: Upgrade von Continia Document Capture für App-Versionen von Business Central
date: 19-09-2025
description: So führen Sie ein Upgrade von Continia Document Capture für App-Versionen von Business Central durch.
id: DC-6
lang: de
---

# Upgrade von Continia Document Capture für App-Versionen von Business Central

In diesem Artikel wird beschrieben, wie Sie Continia Document Capture für App-Versionen von Microsoft Dynamics 365 Business Central aktualisieren. Informationen zum Aktualisieren von Document Capture für FOB Versionen von Business Central finden Sie unter [Unterstützte Upgradepfade für Continia Document Capture (FOB)](@DC-8).

Alle Upgradepakete sind völlig kostenlos und es wird empfohlen, regelmäßig ein Upgrade durchzuführen, um von allen neuen Funktionen zu profitieren, die der Anwendung kontinuierlich hinzugefügt werden. Beachten Sie, dass Sie bei der Aktualisierung der Software stets die Unterstützung Ihres Continia-Partners benötigen.

## So aktualisieren Sie Document Capture

Um den Aktualisierungsprozess zu vereinfachen, hat Continia ein PowerShell-Skript entwickelt, das sicherstellt, dass Document Capture korrekt aktualisiert wird und alle Abhängigkeiten wie vorgesehen funktionieren.

Wenn Sie das Skript ausführen, durchsucht es automatisch den Ordner, in dem es ausgeführt wird (einschließlich aller Unterordner), nach vorhandenen Instanzen von Document Capture und anderen Continia-Apps. Wenn eine frühere Version einer App erkannt wird, werden die App und alle Abhängigkeiten aktualisiert und alle alten Versionen deinstalliert. Wenn keine App erkannt wird, installiert das Skript die App automatisch zusammen mit allen anderen erforderlichen Apps.

> [!NOTE]
> Wenn Sie Document Capture mit dem PowerShell-Skript mit dieser Anleitung aktualisieren, wird die Document Capture OnPremise-App automatisch zusammen mit der Document Capture-Basis-App aktualisiert.

So aktualisieren Sie Document Capture mit diesem Skript:

1. Gehen Sie zur [Continia PartnerZone](https://partnerzone.continia.com).
2. Klicken Sie im Menü oben auf **Help Center** > **Download Center**.
3. Verwenden Sie die Filter, um die neueste Version von Document Capture zu finden, und klicken Sie auf **Download**, um das Upgradepaket herunterzuladen.

   > [!IMPORTANT]
   > Nachdem Sie das Installationspaket heruntergeladen haben, müssen Sie es entsperren, um es ordnungsgemäß extrahieren zu können:
   >
   > 1. Klicken Sie mit der rechten Maustaste auf die heruntergeladene Datei und klicken Sie dann auf **Eigenschaften**, um das Fenster mit den Dateieigenschaften zu öffnen.
   > 2. Klicken Sie auf der Registerkarte **Allgemein** unter **Sicherheit** auf **Entsperren** > **Übernehmen**. Schließen Sie das Fenster, wenn Sie fertig sind.
4. Extrahieren Sie das Produktpaket in einen Ordner auf Ihrem Computer. Führen Sie in diesem Ordner die Datei **setup.exe** aus, um das Document Capture-Installationsprogramm zu öffnen.
5. Klicken Sie im Installationsprogramm auf **Server Components** und wählen Sie dann Ihre Version von Business Central aus.
   > [!NOTE]
   > Das Installationsprogramm aktualisiert den Ordner **Add-ins** (Client und/oder Server) im Standardinstallationspfad. Wenn Ihr Installationspfad vom Microsoft-Standardpfad abweicht, müssen Sie den neuen Ordner **Add-ins** in den Ordner kopieren, in dem sich Ihre Installation befindet.
6. Wählen Sie im App-Ordner den Ordner aus, der Ihrer Business Central-Version (Ihrer Plattform) entspricht, einschließlich des richtigen kumulativen Updates.
   > [!IMPORTANT]
   > Da Continia-Apps als Runtime Packages verteilt werden, müssen Sie die richtige Version auswählen. Die Funktionsfähigkeit von Runtime Packages wird nur dann garantiert, wenn sie auf einer Plattform mit derselben Version veröffentlicht werden, auf der sie erstellt wurden.
7. Das Installationsskript kann folgendermaßen ausgeführt werden:
   - Klicken Sie in dem Ordner, den Sie im vorherigen Schritt ausgewählt haben, mit der rechten Maustaste auf **Install.ps1** und wählen Sie **Mit PowerShell ausführen**.
   - Führen Sie das Skript in einer PowerShell-Shell aus.
   > [!IMPORTANT]
   > Das Skript **Install.ps1** unterstützt keine Aktualisierung in Multi-Tenant-Umgebungen. Um Document Capture in Multi-Tenant-Umgebungen zu aktualisieren, müssen Sie die Befehle im Installationsskript manuell für Ihre installierten Continia-Lösungen ausführen. Weitere Informationen finden Sie unter [Continia-Apps in Multi-Tenant-Umgebungen installieren oder aktualisieren](@DC-116).
8. Wenn Sie unterschiedliche Versionen von Business Central installiert haben, wählen Sie im Skript die entsprechende Version aus.
9. Wenn Sie aufgefordert werden, die zu installierende Lösung auszuwählen, wählen Sie **Document Capture**.
10. Wählen Sie die Serverinstanz aus, auf der die App aktualisiert werden soll.
11. Dadurch wird die Aktualisierung von Document Capture gestartet, die je nach Größe Ihrer Datenbank 1–2 Minuten dauern kann. Wenn Sie fertig sind, drücken Sie zum Beenden eine beliebige Taste.

Wenn das Upgrade abgeschlossen ist, ist die vorherige Version von Document Capture nicht mehr verfügbar.

> [!IMPORTANT]
> Nach dem Upgrade müssen Sie eine neue und aktualisierte Kundenlizenzdatei von Microsoft herunterladen und verwenden.

## Informationen zum Thema

[Unterstützte Upgradepfade für Continia Document Capture (FOB)](@DC-8)