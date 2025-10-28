---
title: Continia Expense Management On-Premises installieren
description: So installieren Sie Expense Management On-Premises in Business Central
date: 18-08-2021
id: EM-138
lang: de
---

# Continia Expense Management On-Premises installieren

In diesem Artikel wird beschrieben, wie Sie Expense Management in On-Premises-Bereitstellungen von Microsoft Dynamics 365 Business Central installieren. Beachten Sie, dass Sie bei der Installation der Software stets die Unterstützung Ihres Continia-Partners benötigen.

## So installieren Sie Expense Management

Um den Installationsprozess zu vereinfachen, hat Continia ein PowerShell-Skript entwickelt, das sicherstellt, dass Expense Management korrekt installiert wird und alle Abhängigkeiten wie vorgesehen funktionieren.

Um Expense Management mit diesem Skript zu installieren, führen Sie diese Schritte aus:

1. Gehen Sie zur [Continia PartnerZone](https://partnerzone.continia.com).
2. Wählen Sie im Menü oben **Downloads** aus.
3. Verwenden Sie die Filter, um die neueste Version von Expense Management zu finden, und wählen Sie **Download**, um das Installationspaket herunterzuladen.
4. Extrahieren Sie das Produktpaket in einen Ordner auf dem Computer mit der Business Central Service-Tier. Führen Sie in diesem Ordner die Datei setup.exe aus, um das Expense Management-Installationsprogramm zu öffnen.
5. Wählen Sie im Installationsprogramm **Server Components** und dann Ihre Version von Business Central aus.
   > [!NOTE]
   > Das Installationsprogramm aktualisiert den Ordner **Add-ins** (Client und/oder Server) im Standardinstallationspfad. Wenn Ihr Installationspfad also vom Microsoft-Standardpfad abweicht, müssen Sie den neuen Ordner **Add-ins** in den Ordner kopieren, in dem sich Ihre Installation befindet.
6. Wählen Sie im App-Ordner den Ordner aus, der Ihrer Business Central-Version (Ihrer Plattform) entspricht, einschließlich des richtigen kumulativen Updates.
   > [!NOTE]
   > Da Continia-Apps als Runtime Packages verteilt werden, müssen Sie die richtige Version auswählen. Die Funktionsfähigkeit von Runtime Packages wird nur dann garantiert, wenn sie auf einer Plattform mit derselben Version veröffentlicht werden, auf der sie erstellt wurden.
7. Das Installationsskript kann folgendermaßen ausgeführt werden:
   1. Führen Sie Windows PowerShell als Administrator aus.
   2. Ändern Sie in der PowerShell-Eingabeaufforderung das Verzeichnis in den Ordner, den Sie in Schritt 6 ausgewählt haben, und führen Sie dann **Install.ps1** aus.
8. Wenn Sie unterschiedliche Versionen von Business Central installiert haben, wählen Sie im Skript die entsprechende Version aus.
9. Wenn Sie aufgefordert werden, die zu installierende Lösung auszuwählen, wählen Sie **Expense Management**.
10. Wählen Sie die Serverinstanz aus, auf der die App installiert werden soll.
11. Dadurch wird die Installation von Expense Management gestartet, die je nach Größe Ihrer Datenbank 1–2 Minuten dauern kann. Wenn Sie fertig sind, drücken Sie zum Beenden eine beliebige Taste.

> [!IMPORTANT]
> Wenn Sie Business Central auf eine andere Version oder ein kumulatives Upgrade aktualisieren, müssen Sie Expense Management deinstallieren und dann das Expense Management-Runtime Package installieren, das der neuen Version von Business Central entspricht.
