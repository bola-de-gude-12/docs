---
title: Abgleichprüfungen vor der Registrierung einrichten
date: 24-08-2022
description: So richten Sie Document Capture ein, um zu prüfen, ob Belege vor der Registrierung abgeglichen wurden
id: DC-84
lang: de
---

# Abgleichprüfungen vor der Registrierung einrichten

Sie möchten Benutzer möglicherweise vor der Restrierung benachrichtigen, wenn Belege nicht übereinstimmen, oder verhindern, dass Benutzer nicht übereinstimmende Belege registrieren können. In diesem Fall können Sie Continia Document Capture so einrichten, dass Übereinstimmungen bei der Registrierung von Belegen automatisch geprüft werden. Für den Fall, dass keine Übereinstimmungen gefunden werden, sind in Document Capture folgende Optionen möglich:

- **Wenn Zeilenerkennung aktiviert ist**, zeigt Document Capture eine Fehlermeldung im Abschnitt **Bemerkungen** im Belegjournal an. Sie können den Beleg dann nicht registrieren.
- **Wenn Zeilenerkennung deaktiviert ist**, zeigt Document Capture im ersten Schritt der Registrierung ein Dialogfeld an, das Sie darüber informiert, dass keine Übereinstimmungen vorhanden sind. Sie werden gefragt, ob Sie trotzdem mit der Registrierung des Belegs fortfahren möchten.

> [!NOTE]
> Wenn Zeilenerkennung deaktiviert ist, ist es trotz der Prüfung möglich, nicht übereinstimmende Belege zu registrieren. Das angezeigte Dialogfeld fordert Sie jedoch ausdrücklich auf, die Registrierung aktiv zu bestätigen.

Wie beim Abgleich werden Abgleichprüfungen in der jeweiligen Vorlage konfiguriert. Wenn Sie diese Prüfungen für eine bestimmte Vorlage aktivieren, werden sie auf alle Belege angewendet, die diese Vorlage verwenden.

Um Abgleichprüfungen einzurichten, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie auf der Seite **Belegkategorie** im Inforegister **Vorlagen** die Vorlage aus, die Sie konfigurieren möchten.
4. Wählen Sie in der Titelleiste des Inforegisters **Bearbeiten** aus, um die Vorlagenkarte zu öffnen.
5. Nehmen Sie im Inforegister **Einkaufsbelege** unter **Registrierung** die folgenden Änderungen vor:
   - Wählen Sie im Feld **Rechnung Reg. Schritt 1** die Option **Bestellung zuordnen & Rechnung erzeugen**.
   - Wählen Sie im Feld **Gutschrift Reg. Schritt 1** die Option **Reklamation zuordnen & Gutschrift erzeugen**.

Je nach Ihren Einstellungen in der Vorlage wird verhindert, dass Sie nicht übereinstimmende Belege, die diese Vorlage verwenden, registrieren können, oder es wird im ersten Schritt der Registrierung nicht übereinstimmender Belege ein Dialogfeld angezeigt, in dem Sie bestätigen müssen, dass Sie trotz der fehlenden Übereinstimmungen mit der Registrierung fortfahren möchten.

## Informationen zum Thema

[Automatischer Belegabgleich](@DC-70)