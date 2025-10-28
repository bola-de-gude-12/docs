---
title: ABBYY und Document Capture-Dienste installieren
date: 04-09-2025
description:
lang: de
---

# ABBYY und Document Capture-Dienste installieren

Der Continia OCR-Dienst umfasst zwei wesentliche Elemente:

- [die ABBYY FineReader-Engine](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/installing-abbyy-and-document-capture-services#die-abbyy-finereader-engine)
- [den Continia Document Capture-Dienst](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/installing-abbyy-and-document-capture-services#der-document-capture-dienst)

In den folgenden Abschnitten finden Sie eine Übersicht über jeden dieser Dienste sowie Einzelheiten zu ihrer Installation.

## Die ABBYY FineReader-Engine

Wenn Sie OCR On-Premises verwenden, führt die ABBYY FineReader Engine die eigentliche OCR-Verarbeitung Ihrer importierten Dokumente durch. Installieren Sie diese nur, wenn Sie Continia Cloud OCR _nicht_ verwenden. Die Anwendung kann entweder auf einem Server oder auf dem Computer installiert werden, der den eigentlichen Scanvorgang durchführt.

Um die ABBYY FineReader-Engine zu installieren, folgen Sie diesen Schritten:

1. Führen Sie setup.exe vom Stammverzeichnis des Softwareverzeichnisses aus, um das Installationsprogramm zu öffnen.
2. Klicken Sie im Installationsprogramm auf **ABBYY FineReader** > **Installieren**.
3. Wenn die Installation abgeschlossen ist, wird der ABBYY FineReader-Lizenzmanager gestartet. Wählen Sie **Lizenz aktivieren**, geben Sie Ihre Seriennummer (SN) ein und folgen Sie den Anweisungen auf dem Bildschirm, um die Lizenz zu aktivieren.

> [!NOTE]
> Die FineReader Engine-Lizenz kann jeweils nur für einen Computer aktiviert werden. Wenn Sie einen Softwareschlüssel verwenden, können Sie die Lizenz nur zweimal deaktivieren und reaktivieren. Danach müssen weitere Aktivierungen freigeschaltet werden. Dieser Vorgang kann mehrere Tage dauern und muss von Ihrem Continia-Partner angefordert werden.

## Der Document Capture-Dienst

Der Document Capture-Dienst wird für das Herunterladen von E-Mails und die Überwachung eingehender Dateien verwendet, die per OCR verarbeitet werden müssen. Installieren Sie diese nur, wenn Sie Continia Cloud OCR _nicht_ verwenden. Der Dienst interagiert mit der FineReader Engine und beide Dienste müssen auf demselben Computer installiert sein. Der Document Capture Service wird als Windows-Dienst mit der Bezeichnung „Document Capture“ installiert und läuft in einigen wichtigen Verzeichnissen, die nach der Installation konfiguriert werden müssen.

> [!IMPORTANT]
> Wenn Sie den Document Capture-Dienst auf eine neuere Version aktualisieren, müssen Sie auch die OCR-Konfigurationsdateien exportieren. Wenn Sie dies nicht tun, funktionieren neue Funktionen, die von Einstellungen in den OCR-Konfigurationsdateien abhängen, nicht wie erwartet (wie etwa der Import von E-Mails mithilfe von EWS oder die Erstellung von PNG-Bilddateien).

Um Document Capture-Dienst zu installieren, führen Sie diese Schritte aus:

1. Führen Sie setup.exe vom Stammverzeichnis des Softwareverzeichnisses aus, um das Installationsprogramm zu öffnen.
2. Klicken Sie im Installationsprogramm auf **Document Capture-Dienst** > **Installieren**.
3. Wenn die Installation abgeschlossen ist, wird der Document Capture Configuration Manager gestartet. Konfigurieren Sie die einzelnen Einstellungen nach Bedarf.
   > [!IMPORTANT]
   > Der in **PDF-Dateien für OCR** eingegebene Pfad muss mit dem Pfad identisch sein, den Sie während der [On-Premises OCR-Einrichtung](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/configuring-on-premises-ocr#on-premises-ocr-einrichten) (Schritt 6) in das Feld **Dateipfad für gescannte PDF** eingeben.
   >
   > Außerdem muss der in **OCR-verarbeitete Dateien für NAV** eingegebene Pfad mit dem Pfad identisch sein, den Sie während der [On-Premises OCR Einrichtung](/continia-document-capture/development-and-administration/on-premises/deployment/configuring-on-premises-ocr/configuring-on-premises-ocr#on-premises-ocr-einrichten) (Schritt 7) in das Feld **Dateipfad für OCR-verarbeitete Dateien** eingeben.
4. Wenn Sie einen oder mehrere Ordner auf einem anderen Computer erstellen, müssen Sie ein gültiges Domänenbenutzerkonto mit Zugriff auf alle Ordner angeben.
5. Starten Sie den Document Capture-Dienst.

> [!NOTE]
> Im Ereignisprotokoll des Document Capture Configuration Managers finden Sie den neuesten Document Capture-Eintrag. Sie müssen sicherstellen, dass beim Starten des Dienstes keine Fehler auftreten.

## Informationen zum Thema

[On-Premises OCR konfigurieren](@DC-150)