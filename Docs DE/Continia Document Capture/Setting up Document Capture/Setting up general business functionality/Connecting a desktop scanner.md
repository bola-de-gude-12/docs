---
title: Einen Desktopscanner in Document Capture anschließen
date: 04-07-2025
description:
id: DC-119
lang: de
---

# Einen Desktopscanner anschließen

Continia Document Capture unterstützt das Scannen von Dokumenten mit einem Desktopscanner, der direkt an Ihren Laptop oder Desktop-PC angeschlossen ist. Sobald ein Desktopscanner angeschlossen ist, kann Document Capture mit dem Scanner kommunizieren und den Scanvorgang direkt aus Microsoft Dynamics 365 Business Central heraus starten.

> [!NOTE]
> Bei der Verwendung von Desktopscannern kann das Scannen nur von den Computern aus durchgeführt werden, an die der Scanner angeschlossen ist, weshalb dies für die meisten Unternehmen nicht die erste Wahl ist. Stattdessen werden Dokumente normalerweise entweder per E-Mail empfangen oder mit einem Netzwerkscanner gescannt. Es steht Ihrer Organisation jedoch frei, eine Kombination dieser Methoden zu nutzen. Die Verwendung eines Desktopscanners hindert Sie nicht daran, Dokumente auch per E-Mail oder mit einem Netzwerkscanner zu importieren.

Bevor Sie einen Desktopscanner verwenden können, müssen Sie sicherstellen, dass sowohl der Scanner als auch Ihr Computer die Mindestanforderungen erfüllen. Weitere Informationen finden Sie unter den Anforderungen für lokale Desktopscanner für [Business Central Online](@DC-482#lanforderungen-fur-lokale-scanner) oder für [Business Central On-premises](@DC-135#anforderungen-fur-lokale-scanner), je nachdem, welche Version Sie verwenden.

Um Ihren Scanner einzurichten, nachdem Sie ihn an einen Benutzer-PC angeschlossen haben, folgen Sie diesen Schritten:

1. Installieren Sie die erforderliche Software. Sie erhalten die entsprechende Software von Ihrem [Continia-Partner](/Continia Document Capture/Getting Started/Resellers and Partners/Overview.md).
2. Führen Sie die von Ihrem Partner bereitgestellte Software aus. Wählen Sie im Installationsassistenten das Installationsprogramm aus, das der von Ihnen verwendeten Version von Microsoft Dynamics NAV/Business Central entspricht, und klicken Sie dann auf **Installieren**.
3. Suchen Sie in Business Central ({{search}}) nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.
4. Aktivieren Sie auf dem Inforegister **Allgemein** die Verwendung Ihres angeschlossenen Scanners, indem Sie die Einstellung**Lokalen Scanner aktivieren** einschalten.
5. Um zu überprüfen, ob der Scanner aktiviert wurde, suchen Sie ({{search}}) nach **Scannen & OCR** und wählen Sie den entsprechenden Link aus. Im Fenster **Scannen & OCR** sollte Ihr Scanner jetzt im Feld **Scanner** angezeigt werden.
6. Klicken Sie in der Aktionsleiste auf **Scannen**, um ein Dokument zu scannen.

Laden Sie die erforderlichen Treiber von der Website Ihres Scannerherstellers herunter.

> [!NOTE]
> Wenn Sie mit Microsoft Edge auf Business Central zugreifen, müssen Sie Edge erlauben, mit lokalen HTTP-Diensten zu kommunizieren. Andernfalls wird im Fenster **Scannen & OCR** die Meldung „Der Document Capture-Scannerdienst wird nicht ausgeführt“ anstelle des Namens Ihres Scanners angezeigt. Scannen ist dann nicht möglich. Um Microsoft Edge die Kommunikation mit dem Document Capture-Scannerdienst zu ermöglichen, öffnen Sie eine Eingabeaufforderung mit Administratorrechten und geben Sie den folgenden Befehl ein:
>
> **CheckNetIsolation LoopbackExempt -a -n=Microsoft.MicrosoftEdge_8wekyb3d8bbwe**
>
> Ihr Scanner sollte jetzt im Fenster **Scannen & OCR** im Feld **Scanner** angezeigt werden und Sie sollten Dokumente scannen können.
