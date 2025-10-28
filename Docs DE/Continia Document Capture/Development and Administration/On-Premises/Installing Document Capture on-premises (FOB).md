---
title: Continia Document Capture On-Premises (FOB) installieren
date: 31-03-2025
description: So installieren Sie Document Capture in FOB-Versionen von NAV/Business Central (On-Premises).
id: DC-17
lang: de
---

# Continia Document Capture On-Premises (FOB) installieren

In diesem Artikel wird beschrieben, wie Sie Document Capture in FOB-Versionen von Microsoft Dynamics 365 Business Central installieren. Beachten Sie, dass Sie bei der Installation der Software stets die Unterstützung Ihres Continia-Partners benötigen.

> [!IMPORTANT]
> Die letzte FOB-Version von Document Capture ist 2024 R2 (25.00). On-Premises-Benutzer können die App-Version von Document Capture 2025 R1 (26.00) installieren.

Um Document Capture in einer FOB-Version von NAV/Business Central zu installieren, müssen Sie die folgenden Schritte in der angegebenen Reihenfolge ausführen:

1. [Laden Sie das Installationspaket herunter und führen Sie das Installationsprogramm aus](#so-fuhren-sie-das-document-capture-installationsprogramm-aus).
2. [Importieren Sie die in Schritt 1 heruntergeladenen Objekte in Ihre Business Central-Datenbank](#so-importieren-sie-die-objekte).
3. [Kompilieren Sie alle Objekte in der Datenbank](#so-kompilieren-sie-alle-objekte-in-der-datenbank).

Diese Aktionen werden in den folgenden Anleitungen ausführlicher beschrieben.

## So führen Sie das Document Capture-Installationsprogramm aus

> [!NOTE]
> Für alle Versionen zwischen NAV 2017 und Business Central April 2019 (BC v14) werden sowohl Server- als auch Clientkomponenten automatisch installiert, sodass Sie die Schritte 5-6 in der folgenden Anleitung überspringen können. Für alle vorherigen Versionen von NAV müssen Sie diese Komponenten manuell installieren, wie in der Anleitung beschrieben.

1. Gehen Sie zur [Continia PartnerZone](https://partnerzone.continia.com).
2. Wählen Sie im Menü oben **Downloads** aus.
3. Verwenden Sie die Filter, um die neueste Version von Document Capture zu finden, und wählen Sie **Download**, um das Installationspaket herunterzuladen.
4. Extrahieren Sie das Produktpaket in einen Ordner auf dem Computer mit der Business Central Service-Tier. Führen Sie in diesem Ordner die Datei setup.exe aus, um das Document Capture-Installationsprogramm zu öffnen.
5. Wählen Sie im Installationsprogramm unter **Dynamics NAV Server** die Option **Serverkomponenten** und dann Ihre Version von Business Central > **Installieren** aus.
   > [!NOTE]
   > Das Installationsprogramm aktualisiert den Ordner **Add-ins** (Client und/oder Server) im Standardinstallationspfad. Wenn Ihr Installationspfad also vom Microsoft-Standardpfad abweicht, müssen Sie den neuen Ordner **Add-ins** in den Ordner kopieren, in dem sich Ihre Installation befindet.
6. Wählen Sie je nach Ihrer Version von NAV/Business Central **Dynamics NAV RoleTailored Client** oder **Dynamics NAV Classic Client** und dann **Client Components** aus. Wenn Sie einen RoleTailored-Client haben und im entsprechenden Abschnitt **Client Components** ausgewählt haben, müssen Sie auch Ihre Version von Business Central auswählen. Wählen Sie **Installieren**, um die Clientkomponenten zu installieren.
7. **Optional:** Wenn Sie Dokumente vom eigentlichen NAV/Business Central-Client aus scannen möchten, wählen Sie **Dynamics NAV RoleTailored Client** oder **Dynamics NAV Classic Client** und wählen Sie dann **Scanner Components**. Wählen Sie für RoleTailored-Clients Ihre Version von Business Central aus. Wählen Sie **Installieren**, um die Scannerkomponenten zu installieren.

> [!IMPORTANT]
> Die obige Anleitung beschreibt die erforderlichen Schritte auf dem Computer, auf dem die Business Central-Dienstebene installiert ist. Die Schritte 6 bis 7 gelten jedoch für alle Computer, auf denen Document Capture verwendet wird. Um auf diesen Computern Clientkomponenten und ggf. Scannerkomponenten zu installieren, müssen Sie diese beiden Schritte für jeden einzelnen Computer einzeln durchführen, indem Sie beispielsweise das heruntergeladene Produktpaket auf alle betroffenen Computer verteilen und das Installationsprogramm anschließend lokal ausführen. Überspringen Sie Schritt 5 auf allen anderen Computern und führen Sie ihn nur auf dem Computer aus, auf dem die Business Central-Dienstebene ausgeführt wird.

## So importieren Sie die Objekte

> [!NOTE]
> Für NAV 2015 und höher müssen die Schritte 6-8 der folgenden Anleitung durchgeführt werden. Bei allen anderen Versionen sind diese Schritte nicht erforderlich.

1. Gehen Sie in der Microsoft Dynamics NAV-Entwicklungsumgebung zu **Tools** und wählen Sie **Object Designer**.
2. Wählen Sie in der Menüleiste **File** > **Import...**, um das Fenster **Import Objects** zu öffnen.
3. Suchen Sie das Installationspaket, das Sie in Schritt 3 [der obigen Anleitung](#so-fuhren-sie-das-document-capture-installationsprogramm-aus) heruntergeladen haben, und wählen Sie den Ordner **Objects** aus.
4. Wählen Sie die FOB-Datei aus, die Ihrer Business Central-Version entspricht, und wählen Sie dann **Open** aus.
   > [!IMPORTANT]
   > Sie müssen die FOB-Datei auswählen, die der Datenbank-Version von NAV/Business Central entspricht, auch wenn Sie ein Runtime-Upgrade von NAV/Business Central ausführen.
5. Ein Dialogfeld wird angezeigt, das Sie über mögliche Konflikte informiert. Sie haben die folgenden Optionen:
   - Wenn Konflikte vorhanden sind, wählen Sie **OK** aus, um das Fenster **Import Worksheet** zu öffnen, und lösen Sie dann alle Konflikte. Diese sind in der Spalte **Warning** durch ein Ausrufezeichen gekennzeichnet. Wählen Sie **OK**, wenn Sie fertig sind.
   - Wenn keine Konflikte vorliegen, wählen Sie **Yes**, um alle FOB-Dateiobjekte zu importieren.
6. Das Fenster **Import fob** wird geöffnet. Wählen Sie unter **Synchronize Schema** die Option **Now - with validation** > **OK**.
7. Ein Dialogfeld wird angezeigt, in dem Sie gefragt werden, ob Sie fortfahren möchten. Wählen Sie **Yes**, um das Feld zu schließen und die Synchronisierung der Tabellenänderungen zu starten.
8. Wenn im Fenster **Synchronize Schema Changes** der Status **Operational** angezeigt wird, wählen Sie **Close** aus.
9. Ein Dialogfeld bestätigt, dass der Import abgeschlossen ist. Wählen Sie **OK**, um es zu schließen.

## So kompilieren Sie alle Objekte in der Datenbank

Dieser Schritt des Prozesses variiert geringfügig je nach Ihrer Version von NAV/Business Central, wie in den beiden Anleitungen unten beschrieben. Beide Anleitungen sind eine direkte Fortsetzung [der obigen Anleitung zum Objektimport](#so-importieren-sie-die-objekte).

> [!NOTE]
> Der Unterschied zwischen den Anleitungen besteht darin, ob Sie die Server- und Clientkomponenten beim [Ausführen des Document Capture-Installationsprogramms](#so-fuhren-sie-das-document-capture-installationsprogramm-aus) manuell installiert haben oder nicht:
>
> - Wenn Sie dies _nicht manuell_ durchgeführt haben (Versionen NAV 2017 bis BC v14), müssen Sie vor dem Kompilieren den unterstützten Installationsleitfaden ausführen, um die Komponenten automatisch zu installieren und Kompilierungsfehler zu vermeiden.
> - Wenn Sie die Komponenten _manuell_ installiert haben (alle Versionen vor NAV 2017), müssen Sie sie kompilieren, bevor Sie das unterstützte Setup für Document Capture ausführen.

### Für Versionen vor NAV 2017:

1. Wählen Sie in der Microsoft Dynamics NAV-Entwicklungsumgebung in der Tabelle **Object Designer** die Spalte **Version List** und wählen Sie dann **View** > **Field Filter...**, um das Filterfenster zu öffnen.
2. Geben Sie im Filterfeld die Zeichenfolge **\*DC\*|\*EM\*|\*CC\*|\*DN\*** ein und wählen Sie dann **OK**, um den eingegebenen Filter anzuwenden und um das Fenster zu schließen.
3. Wählen Sie in der Tabelle **Object Designer** alle Einträge aus (z. B. durch Drücken von **Strg+A**) und wählen Sie dann **Tools** > **Compile**.
4. Das Fenster **Compile** wird geöffnet. Wählen Sie unter **Synchronize Schema** die Option**Now - with validation** > **OK**.
5. Wenn der Kompilierungsprozess abgeschlossen ist, wird möglicherweise eine Fehlerliste angezeigt. Für die skandinavischen Länder werden wahrscheinlich die folgenden Codeunits als fehlgeschlagen angezeigt:
   - **6085715** (nur für Dänemark)
   - **6085745** (für Dänemark, Norwegen und Schweden)
   - **6085767** (nur für Norwegen)
   - **6085768** (nur für Schweden)
     Wenn Sie Continia Payment Management nicht installiert haben, können Sie dies ignorieren und die Liste schließen, sofern keine anderen Fehler aufgeführt sind.
6. Führen Sie in NAV/Business Central das **Unterstützte Setup für Document Capture** aus und folgen Sie den Anweisungen auf dem Bildschirm. Sie können das Setup entweder beim [Aktivieren von Document Capture](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-activate-a-solution) ausführen oder indem Sie nach **Document Capture Konfigurationsassistent** suchen und den entsprechenden Link auswählen.

### Für Versionen von NAV 2017 bis einschließlich BC v14:

1. Führen Sie in NAV/Business Central das **Unterstützte Setup für Document Capture** aus und folgen Sie den Anweisungen auf dem Bildschirm. Sie können das Setup entweder beim [Aktivieren von Document Capture](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-activate-a-solution) ausführen oder indem Sie nach **Document Capture Konfigurationsassistent** suchen und den entsprechenden Link auswählen.
2. Wählen Sie in der Microsoft Dynamics NAV-Entwicklungsumgebung in der Tabelle **Object Designer** die Spalte **Version List** und wählen Sie dann **View** > **Field Filter...**, um das Filterfenster zu öffnen.
3. Geben Sie im Filterfeld die Zeichenfolge **\*DC\*|\*EM\*|\*CC\*|\*DN\*** ein und wählen Sie dann **OK**, um den eingegebenen Filter anzuwenden und um das Fenster zu schließen.
4. Wählen Sie in der Tabelle **Object Designer** alle Einträge aus (z. B. durch Drücken von **Strg+A**) und wählen Sie dann **Tools** > **Compile**.
5. Das Fenster **Compile** wird geöffnet. Wählen Sie unter **Synchronize Schema** die Option**Now - with validation** > **OK**.
6. Wenn der Kompilierungsprozess abgeschlossen ist, wird möglicherweise eine Fehlerliste angezeigt. Für die skandinavischen Länder werden wahrscheinlich die folgenden Codeunits als fehlgeschlagen angezeigt:
   - **6085715** (nur für Dänemark)
   - **6085745** (für Dänemark, Norwegen und Schweden)
   - **6085767** (nur für Norwegen)
   - **6085768** (nur für Schweden)
     Wenn Sie Continia Payment Management nicht installiert haben, können Sie dies ignorieren und die Liste schließen, sofern keine anderen Fehler aufgeführt sind.