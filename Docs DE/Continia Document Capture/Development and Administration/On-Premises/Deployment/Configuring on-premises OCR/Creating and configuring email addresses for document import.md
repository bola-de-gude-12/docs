---
title: E-Mail-Adressen für den Dokumentenimport erstellen und konfigurieren
date: 22-12-2022
description:
id: DC-114
lang: de
---

# E-Mail-Adressen für den Dokumentenimport erstellen und konfigurieren

Wenn Sie On-Premises OCR verwenden, müssen Sie für jede relevante Belegkategorie E-Mail-Adressen erstellen und konfigurieren, um Ihre Dokumente in Document Capture zu importieren. Document Capture unterstützt derzeit die folgenden beiden Protokolle:

- Internet Message Access Protocol (IMAP)
- Exchange Web Services (EWS)

Die eigentliche Konfiguration der E-Mail-Adressen hängt davon ab, welches dieser Protokolle Sie verwenden. Beide Methoden werden nachfolgend beschrieben.

> [!WARNING]
> Beachten Sie bitte die folgenden wichtigen Hinweise:
>
> - Es werden nur ungelesene E-Mails verarbeitet.
> - Sie dürfen kein benutzerzugängliches Postfach verwenden.
> - Sie sollten jegliche andere Software deinstallieren oder deaktivieren, die E-Mails verarbeitet.

## E-Mail-Adressen mit IMAP konfigurieren

Um eine E-Mail-Adresse für den Dokumentenimport mit IMAP zu konfigurieren, gehen Sie folgendermaßen vor:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Öffnen Sie die Belegkategorie, die Sie mit dem Document Capture-Dienst einrichten möchten. Um beispielsweise die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Geben Sie im Inforegister **E-Mail** im Feld **Serveradresse** den Namen oder die IP-Adresse des Mailservers ein, den Sie verwenden möchten.
4. Geben Sie in **Server Port** die Nummer des Ports ein, über den die Verbindung zum Mailserver hergestellt werden soll. Der IMAP-Port ist normalerweise 993 bei einer SSL-Verbindung und 143 ohne SSL.
5. Geben Sie unter **Benutzername** die E-Mail-Adresse des Kontos ein, das für die ausgewählte Belegkategorie verwendet werden soll, z. B. invoice@company.com. Dadurch wird es mit der Document Capture-E-Mail-Adresse für diese Kategorie verknüpft.
6. Geben Sie unter **Passwort** das Passwort ein, das mit der unter **Benutzername** eingegebenen E-Mail-Adresse verknüpft ist.
7. Optional: Wenn Sie möchten, dass eingehende Dokumente nach dem Download automatisch vom Mailserver gelöscht werden, aktivieren Sie **Nach Download löschen**.
8. Optional: Wenn Document Capture alle Dokumentimport-E-Mails einschließlich der angehängten Dokumente archivieren soll, aktivieren Sie **E-Mails importieren und archivieren**. Auf diese Weise haben Buchhalter, Wirtschaftsprüfer und andere Benutzer von Document Capture direkten Zugriff auf die E-Mails.
9. Wiederholen Sie die Schritte für all zusätzlichen Kategorien, die Sie mit dem Document Capture-Dienst einrichten möchten.
10. Wenn Sie alle Kategorien eingerichtet haben, wählen Sie das Symbol {{search}}, geben Sie **OCR Konfigurationsdateien exportieren** ein, und wählen Sie dann den zugehörigen Link. Ein Dialogfeld bestätigt, dass eine Reihe von Konfigurationsdateien exportiert wurde. Wählen Sie **OK**, um es zu schließen.

## E-Mail-Adressen mit EWS konfigurieren

> [!IMPORTANT]
> Bevor Sie die folgende Anleitung abschließen können, müssen Sie [EWS gemäß dieser Anleitung einrichten](Setting up Exchange Web Services, EWS.md). Während des EWS-Einrichtungsprozesses erhalten Sie eine Client-ID, eine Tenant-ID und entweder den Fingerabdruck eines Zertifikats oder einen Client Secret-Wert, die verwendet werden müssen, wenn Sie EWS-E-Mail-Adressen für den Dokumentimport konfigurieren.

Um eine E-Mail-Adresse für den Dokumentenimport mit EWS zu konfigurieren, gehen Sie folgendermaßen vor:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Öffnen Sie die Belegkategorie, die Sie mit dem Document Capture-Dienst einrichten möchten. Um beispielsweise die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie im Inforegister **E-Mail** unter **E-Mail-Protokoll** die Option **EWS** aus.
4. Geben Sie unter **E-Mail-Adresse** oder **Geteilte E-Mail-Adresse** die vollständige Adresse des Postfachs ein, das der Dienst überwachen soll.
5. Geben Sie unter **Client ID** und **Tenant ID** die Werte ein, die Sie aus dem Bereich **Übersicht** in Azure kopiert haben, wie [in dieser Anleitung](Setting up Exchange Web Services, EWS.md) beschrieben).
6. Füllen Sie je nach den von Ihnen gewählten Anmeldeinformationen entweder **Client Secret** oder **Fingerabdruck des Zertifikats** aus.
7. Optional: Wenn Sie möchten, dass eingehende Dokumente nach dem Download automatisch vom Mailserver gelöscht werden, aktivieren Sie **Nach Download löschen**.
8. Optional: Wenn Document Capture alle Dokumentimport-E-Mails einschließlich der angehängten Dokumente archivieren soll, aktivieren Sie **E-Mails importieren und archivieren**. Auf diese Weise haben Buchhalter, Wirtschaftsprüfer und andere Benutzer von Document Capture direkten Zugriff auf die E-Mails.
9. Wiederholen Sie die Schritte für all zusätzlichen Kategorien, die Sie mit dem Document Capture-Dienst einrichten möchten.
10. Wenn Sie alle Kategorien eingerichtet haben, wählen Sie das Symbol {{search}}, geben Sie **OCR Konfigurationsdateien exportieren** ein, und wählen Sie dann den zugehörigen Link. Ein Dialogfeld bestätigt, dass eine Reihe von Konfigurationsdateien exportiert wurde. Wählen Sie **OK**, um es zu schließen.

Der Document Capture-Dienst ist jetzt für die Authentifizierung bei EWS unter Verwendung von OAuth 2.0 eingerichtet.
Wenn die Authentifizierung fehlschlägt, wird im Ereignisprotokoll der Serveranwendung ein Eintrag mit Informationen zur Ursache des Authentifizierungsfehlers erstellt.

## Informationen zum Thema

[Exchange Web Services (EWS) einrichten](Setting up Exchange Web Services, EWS.md)