---
title: Continia Document Capture On-Premises installieren
date: 08-07-2025
description: So installieren Sie Document Capture On-Premises in Business Central.
id: DC-51
lang: de
---

# Continia Document Capture On-Premises installieren

In diesem Artikel wird beschrieben, wie Sie Document Capture in On-Premises-Bereitstellungen von Microsoft Dynamics 365 Business Central installieren. Beachten Sie, dass Sie bei der Installation der Software stets die Unterstützung Ihres Continia-Partners benötigen.

Der Installationsprozess umfasst Runtime Packages, da alle Continia-Apps so herausgegeben werden. So kann jede Erweiterung in einem Runtime Package – in diesem Fall die Document Capture-App – auf Servern installiert werden kann, die über keine Entwicklerlizenz verfügen. Weitere Informationen finden Sie unter [Create runtime packages for Business Central on-premises](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/developer/devenv-creating-runtime-packages) (Microsoft-Artikel).

Beachten Sie, dass Continia Code für alle verfügbaren kumulativen Updates (CUs) für Business Central veröffentlicht, wenn eine Version von Document Capture veröffentlicht wird (gilt sowohl für Hauptversionen als auch für Service Packs). Jedes neu veröffentlichte CU von Microsoft wird erst ab dem nächsten von Continia veröffentlichten Service Pack unterstützt. Wenn Sie auf ein derzeit nicht unterstütztes Business Central CU aktualisieren müssen – beispielsweise auf das neueste – und nicht warten können, bis Continia ein Document Capture-Service Pack veröffentlicht, das dies unterstützt, wenden Sie sich bitte an das Continia-Supportteam, indem Sie ein Supportticket erstellen. Continia stellt Ihnen dann ein voll funktionsfähiges Paket bereit, das das entsprechende Business Central CU unterstützt.

## So installieren Sie Document Capture

Um den Installationsprozess zu vereinfachen, hat Continia ein PowerShell-Skript entwickelt, das sicherstellt, dass Document Capture korrekt installiert wird und alle Abhängigkeiten wie vorgesehen funktionieren.

Wenn Sie das Skript ausführen, durchsucht es automatisch den Ordner, in dem es ausgeführt wird (einschließlich aller Unterordner), nach vorhandenen Instanzen von Document Capture und anderen Continia-Apps. Wenn eine frühere Version einer App erkannt wird, werden die App und alle Abhängigkeiten aktualisiert und alle alten Versionen deinstalliert. Wenn keine App erkannt wird, installiert das Skript die App automatisch zusammen mit allen anderen erforderlichen Apps.

> [!NOTE]
> Document Capture besteht aus zwei Apps:
>
> - **Continia Document Capture** – die Basis-App, die die meisten Funktionen enthält. Diese App ist identisch mit der in Business Central Online veröffentlichten App.
> - **Continia Document Capture OnPremise** – eine App, die Ihnen Zugriff auf Funktionen gibt, die nur in On-Premises-Installationen von Business Central verfügbar sind. Diese App ist erforderlich, wenn Sie den Dokumentspeichertyp **Dateisystem** oder den On-Premises OCR-Dienst verwenden möchten, der ebenfalls Zugriff auf das Dateisystem erfordert.
>   Wenn Sie Document Capture mit dem PowerShell-Skript installieren, wie in dieser Anleitung beschrieben, **wird die Document Capture OnPremise-App _nicht_ standardmäßig installiert**. Befolgen Sie zur Installation Schritt 12 in der Anleitung. Beachten Sie außerdem, dass Sie die Document Capture-Serverkomponenten (Service Tier-Bibliotheken) installieren müssen, bevor Sie die OnPremise-App veröffentlichen und installieren.

So installieren Sie Document Capture mit diesem Skript:

1. Gehen Sie zur [Continia PartnerZone](https://partnerzone.continia.com).

2. Klicken Sie im Menü oben auf **Downloads**.

3. Verwenden Sie die Filter, um die neueste Version von Document Capture zu finden, und klicken Sie auf **Download**, um das Installationspaket herunterzuladen.

   > [!IMPORTANT]
   > Nachdem Sie das Installationspaket heruntergeladen haben, müssen Sie es entsperren, um es ordnungsgemäß extrahieren zu können:
   >
   > 1. Klicken Sie mit der rechten Maustaste auf die heruntergeladene Datei und wählen Sie **Eigenschaften**, um das Fenster mit den Dateieigenschaften zu öffnen.
   > 2. Wählen Sie auf der Registerkarte **Allgemein** unter **Sicherheit** die Option **Entsperren** und dann **Übernehmen**. Schließen Sie das Fenster, wenn Sie fertig sind.

4. Extrahieren Sie das Produktpaket in einen Ordner auf dem Computer mit der Business Central Service-Tier. Führen Sie in diesem Ordner die Datei **setup.exe** aus, um das Document Capture-Installationsprogramm zu öffnen.

5. Wählen Sie im Installationsprogramm **Server Components** und dann Ihre Version von Business Central aus.
   > [!NOTE]
   > Das Installationsprogramm aktualisiert den Ordner **Add-ins** (Client und/oder Server) im Standardinstallationspfad. Wenn Ihr Installationspfad also vom Microsoft-Standardpfad abweicht, müssen Sie den neuen Ordner **Add-ins** in den Ordner kopieren, in dem sich Ihre Installation befindet.

6. Wählen Sie im App-Ordner den Ordner aus, der Ihrer Business Central-Version (Ihrer Plattform) entspricht, einschließlich des richtigen kumulativen Updates.
   > [!IMPORTANT]
   > Da Continia-Apps als Runtime Packages verteilt werden, müssen Sie die richtige Version auswählen. Die Funktionsfähigkeit von Runtime Packages wird nur dann garantiert, wenn sie auf einer Plattform mit derselben Version veröffentlicht werden, auf der sie erstellt wurden.

7. Das Installationsskript kann folgendermaßen ausgeführt werden:
   - Klicken Sie in dem Ordner, den Sie im vorherigen Schritt ausgewählt haben, mit der rechten Maustaste auf **Install.ps1** und wählen Sie **Mit PowerShell ausführen**.
   - Führen Sie das Skript in einer PowerShell-Shell aus.
   > [!IMPORTANT]
   > Das Skript **Install.ps1** unterstützt keine Installation in Multi-Tenant-Umgebungen. Um Document Capture in Multi-Tenant-Umgebungen zu installieren, müssen Sie die Befehle im Installationsskript manuell ausführen. Weitere Informationen finden Sie unter [Continia-Apps in Multi-Tenant-Umgebungen installieren oder aktualisieren](@DC-116).

8. Wenn Sie unterschiedliche Versionen von Business Central installiert haben, wählen Sie im Skript die entsprechende Version aus.

9. Wenn Sie aufgefordert werden, die zu installierende Lösung auszuwählen, wählen Sie **Document Capture**.

10. Wählen Sie die Serverinstanz aus, auf der die App installiert werden soll.

11. Dadurch wird die Installation von Document Capture gestartet, die je nach Größe Ihrer Datenbank 1–2 Minuten dauern kann. Wenn Sie fertig sind, drücken Sie zum Beenden eine beliebige Taste.

12. **Optional:** Wenn Sie On-Premises-Funktionalität (wie Dateisystemspeicher und On-Premises OCR) verwenden möchten, müssen Sie die Continia Document Capture OnPremise-App installieren. Gehen Sie hierzu wie folgt vor:

    1. Wiederholen Sie die Schritte 7–11 oben, verwenden Sie jedoch **Install-onprem.ps1** statt **Install.ps1**.
    2. Wenn Sie OCR vor Ort verwenden möchten, befolgen Sie [diese Anleitung](https://continia.zendesk.com/hc/en-us/article_attachments/13795227122450), um den Continia Document Capture OCR-Dienst zu installieren.

> [!IMPORTANT]
> Wenn Sie Business Central auf eine andere Version oder ein kumulatives Upgrade aktualisieren, müssen Sie Document Capture deinstallieren und dann das Document Capture-Runtime Package installieren, das der neuen Version von Business Central entspricht.
>
> Weitere Informationen finden Sie unter [Upgrades für Business Central On-Premises installieren](@DC-59).
