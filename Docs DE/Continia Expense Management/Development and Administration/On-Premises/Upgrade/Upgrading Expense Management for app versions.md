---
title: Upgrade von Continia Expense Management für App-Versionen von Business Central
date: 17-09-2025
description: Erfahren Sie, wie Sie Expense Management für App-Versionen von Microsoft Dynamics 365 Business Central aktualisieren
id: EM-254
lang: de
---

# Upgrade von Continia Expense Management für App-Versionen von Business Central

> [!NOTE]
> In diesem Artikel wird beschrieben, wie Sie Expense Management für App-Versionen von Microsoft Dynamics 365 Business Central aktualisieren. Informationen zum Aktualisieren von Expense Management für _FOB_ Versionen von Business Central finden Sie unter [Unterstützte Upgradepfade für Continia Expense Management (FOB)](@EM-103)

Alle Upgrade-Pakete sind kostenlos. Als bewährte Vorgehensweise empfehlen wir Ihnen, regelmäßig ein Upgrade durchzuführen, um von allen neuen Funktionen zu profitieren, die der Anwendung regelmäßig hinzugefügt werden. Stellen Sie sicher, dass Ihr Continia-Partner Sie bei jedem Upgrade unterstützt.

## Upgrade von Expense Management

Um den Aktualisierungsprozess zu vereinfachen, hat Continia ein PowerShell-Skript entwickelt, das sicherstellt, dass Expense Management korrekt aktualisiert wird und alle Abhängigkeiten wie vorgesehen funktionieren.

Wenn Sie Expense Management mit dem PowerShell-Skript aktualisieren, wird die Expense Management OnPremises-App automatisch zusammen mit der Continia Expense Management-Basis-App aktualisiert.

Das Skript durchsucht automatisch den Ordner, in dem es ausgeführt wird (einschließlich aller Unterordner), nach vorhandenen Instanzen von Expense Management und anderen Continia-Apps. Wenn eine frühere Version einer App erkannt wird, aktualisiert es die App und alle Abhängigkeiten und deinstalliert alle alten Versionen. Wenn keine App erkannt wird, installiert das Skript die App automatisch zusammen mit allen anderen erforderlichen Apps.

So aktualisieren Sie Expense Management mit diesem Skript:

1. Gehen Sie zur [Continia PartnerZone](https://partnerzone.continia.com).

2. Klicken Sie im Menü oben auf **Help Center** > **Download Center**.

3. Verwenden Sie die Filter, um die neueste Version von Expense Management zu finden, und klicken Sie auf **Download**, um das Upgrade-Paket herunterzuladen.

4. Nachdem Sie das Installationspaket heruntergeladen haben, müssen Sie es entsperren, um es ordnungsgemäß extrahieren zu können:

   1. Klicken Sie mit der rechten Maustaste auf die heruntergeladene Datei und klicken Sie auf **Eigenschaften**, um das Fenster mit den Dateieigenschaften zu öffnen.
   2. Klicken Sie auf der Registerkarte **Allgemein** unter **Sicherheit** auf **Entsperren** und dann auf **Übernehmen**.
   3. Schließen Sie das Fenster.

5. Extrahieren Sie das Produktpaket in einen Ordner auf Ihrem Computer. Führen Sie in diesem Ordner die Datei setup.exe aus, um das Expense Management-Installationsprogramm zu öffnen.

6. Klicken Sie im Installationsprogramm auf **Server Components** und wählen Sie dann Ihre Version von Business Central aus.

   > [!NOTE]
   > Das Installationsprogramm aktualisiert den Ordner **Add-ins** (Client und/oder Server) im Standardinstallationspfad. Wenn Ihr Installationspfad jedoch vom Microsoft-Standardpfad abweicht, müssen Sie den neuen Ordner **Add-ins** in den Ordner kopieren, in dem sich Ihre Installation befindet.

7. Wählen Sie im App-Ordner den Ordner aus, der Ihrer Business Central-Version (Ihrer Plattform) entspricht, einschließlich des richtigen kumulativen Updates. Da Continia-Apps als Runtime Packages verteilt werden, müssen Sie die richtige Version auswählen. Die Funktionsfähigkeit von Runtime Packages wird nur dann garantiert, wenn sie auf einer Plattform mit derselben Version veröffentlicht werden, auf der sie erstellt wurden.

8. Verwenden Sie eine der folgenden Methoden, um das Installationsskript auszuführen. Wenn Sie unterschiedliche Versionen von Business Central installiert haben, wählen Sie im Skript die entsprechende Version aus.

   - Klicken Sie in dem Ordner, den Sie im vorherigen Schritt ausgewählt haben, mit der rechten Maustaste auf **Install.ps1** und wählen Sie **Mit PowerShell ausführen**.

   - Führen Sie das Skript mit PowerShell aus.

   > [!IMPORTANT]
   > Das Skript **Install.ps1** unterstützt keine Aktualisierung in Multi-Tenant-Umgebungen. Um Expense Management in Multi-Tenant-Umgebungen zu aktualisieren, müssen Sie die Befehle im Installationsskript manuell für Ihre installierten Continia-Lösungen ausführen. Weitere Informationen finden Sie unter [Continia-Apps in Multi-Tenant-Umgebungen installieren oder aktualisieren](@EM-253).

9. Wählen Sie **Expense Management** für die Lösung aus, die Sie installieren möchten.

10. Wählen Sie die Serverinstanz aus, auf der die App aktualisiert werden soll.

11. Dadurch wird die Aktualisierung von Expense Management gestartet, die je nach Größe Ihrer Datenbank 1-2 Minuten dauern kann. Wenn Sie fertig sind, drücken Sie zum Beenden eine beliebige Taste. Wenn das Upgrade abgeschlossen ist, ist die vorherige Version von Expense Management nicht mehr verfügbar.

12. Nach dem Upgrade müssen Sie eine neue und aktualisierte Kundenlizenzdatei von Microsoft herunterladen und verwenden.

## Informationen zum Thema

Weitere Informationen zu Upgradepfaden finden Sie im folgenden Artikel:
[Unterstützte Upgradepfade für Continia Expense Management (FOB)](@EM-103)