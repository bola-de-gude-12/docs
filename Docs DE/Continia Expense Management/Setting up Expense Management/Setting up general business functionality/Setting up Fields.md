---
title: Felder einrichten
date: 18-03-2025
description: null
id: EM-80
lang: de
---

# Felder einrichten

Mit Expense Management können Sie beim Erstellen von Belegen, Fahrstrecken, Pauschalen und Spesenabrechnungen ganz einfach die für Ihr Unternehmen relevanten Felder konfigurieren. Für jeden Belegtyp kann definiert werden, welche Felder für Expense-Benutzer in der Expense App und im Expense Portal sichtbar sind.

> [!NOTE]
> Die Reihenfolge, in der Sie die Felder anordnen, bestimmt die Reihenfolge, in der die Felder in der Expense App und im Expense Portal angezeigt werden.

So legen Sie fest, welche Felder angezeigt werden:

1. Suchen Sie {{search}} nach **Konfigurierte Felder**, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Aktionsleiste den Typ des Belegs aus (Pauschale, Fahrstrecken, Beleg oder Abrechnung), den Sie konfigurieren möchten.
3. So fügen Sie ein neues Feld hinzu:
   1. Wählen Sie unter **Kopffelder** > **Neue Zeile** aus, um der Tabelle eine neue Zeile hinzuzufügen.
   2. Wählen Sie in der Spalte **Feldcode** der neuen Zeile das Feld aus, um ein Dropdown-Menü zu öffnen.
   3. Wählen Sie entweder ein Feld direkt aus dem Dropdown-Menü aus oder geben Sie einen Suchbegriff ein, um nach dem Feld zu suchen, das Sie hinzufügen möchten, und wählen Sie dann das Feld aus dem Menü aus, um es hinzuzufügen.
4. Um ein Feld zu löschen, markieren Sie das entsprechende Feld und wählen Sie anschließend **Zeile löschen**. Wählen Sie im Dialogfeld, das geöffnet wird, zur Bestätigung der Löschung **Ja** aus.
5. Um beliebige Felder standardmäßig auszublenden, aktivieren Sie das bzw. die Kontrollkästchen in der Spalte **Sichtbar standardmäßig ausblenden**.
6. Um beliebige Felder bearbeitbar zu machen, aktivieren Sie das bzw. die Kontrollkästchen in der Spalte **Editierbar**.
7. Um beliebige Felder obgligatorisch zu machen, aktivieren Sie das bzw. die Kontrollkästchen in der Spalte **Notwendig**.
   > [!TIP]
   > Wenn das Kontrollkästchen **Notwendig** in der Zeile **Beschreibung** _nicht_ aktiviert ist, wird der Text aus der jeweiligen Belegart in das Feld **Beschreibung** in der Expense App und im Expense Portal kopiert.
8. Wählen Sie in der Aktionsleiste **Continia Online** > **Erzwinge Synchronisation mit Continia Online**, um Ihre Änderungen zu synchronisieren. Die von Ihnen konfigurierten Felder sind erst in der Continia Expense App oder im Continia Expense Portal sichtbar, wenn Sie eine Synchronisierung mit Continia Online durchführen.

## Überlegungen zur Beschriftung von Feldern

Sie haben die Kontrolle darüber, wie Sie Felder beschriften. Durch die Anpassung der Feldbezeichnungen an die verschiedenen Dokumenttypen (Beleg, Fahrstrecke, Pauschale und Abrechnungen) wird die Nachverfolgung von Informationen für Ihr Unternehmen einfacher und präziser.

Die folgenden bewährte Vorgehensweisen tragen dazu bei, Fehler und Missverständnisse zu reduzieren und Klarheit in den Workflow eines Benutzers zu bringen. Wenn Sie Feldbeschriftungen definieren:

- Verwenden Sie spezifische Begriffe, die den Richtlinien und Vorschriften Ihres Unternehmens entsprechen, da dies den Mitarbeitern die korrekte Einreichung von Ausgaben erleichtert.
- Geben Sie für jedes Feld genau an, welche Art von Informationen erforderlich sind. Eine Feldbezeichnung sollte das Feld für den jeweiligen Dokumententyp für Belege, Fahrstrecken und Pauschalen genau beschreiben. Um beispielsweise eine Ausgabenart für Belege zu beschreiben, können Sie das Feld „Beschreibung“ nennen. Für Fahrstrecken könnten Sie denselben Feldtyp „Zweck“ nennen.
- Mit jeder von Ihnen erstellten Feldbeschriftung sorgen Sie für noch mehr Klarheit. Zur besseren Übersichtlichkeit können Sie zum Beispiel „Teilnehmer“ für Belege und „Passagier“ für Fahrstrecken verwenden.

## Benutzerdefinierte Feldtypen einrichten

Die unterstützte Einrichtung von Expense Management lädt eine große Auswahl an Feldtypen herunter, die Sie in den meisten gängigen Szenarien verwenden können. Sie können jedoch weitere Feldtypen hinzufügen, um dies an Ihre jeweiligen Geschäftsanforderungen anzupassen. Die Standardkonfiguration bietet eine große Auswahl der gängigsten Felder, Sie können jedoch auch selbst neue Felder konfigurieren.

Um einen neuen Feldtyp einzurichten, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Konfigurierte Felder**, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie unter **Feldcode** die erste verfügbare Zeile aus und wählen Sie dann **Aus vollständiger Liste auswählen**.
3. Wählen Sie in der Aktionsleiste **Neu** aus.
4. Fügen Sie auf der Seite **Feldtyp Karte** den **Code** und die **Beschreibung** für Ihren neuen Feldtyp hinzu und wählen Sie den **Datentyp** aus. Der ausgewählte Datentyp wirkt sich auf die Feldabhängigkeitsoptionen für den Feldtyp aus. Wenn der Feldtyp beispielsweise einen Wert enthalten muss, können Sie nur die Datentypen _Option_ und _Code_ verwenden.
5. Führen Sie eine Synchronisierung mit Continia Online durch. Die von Ihnen konfigurierten Felder sind erst in der Continia Expense App oder im Continia Expense Portal sichtbar, wenn Sie eine Synchronisierung mit Continia Online durchführen.

> [!NOTE]
> Ein neuer Feldtyp wird nicht automatisch im System aktualisiert. Sie müssen das Feld unter **Konfigurierte Felder** oder **Benutzerdefinierte Felder** hinzufügen. Sie sehen **Benutzerdefinierte Felder** in der Expense Management Einrichtung und können sie auf den jeweiligen Belegseiten in Business Central konfigurieren.

## Benutzerdefinierte Felder im Web Approval Portal

Wenn Sie das Web Approval Portal verwenden, finden Sie unter [Das Web Approval Portal anpassen](@EM-61) Informationen zum Aktivieren benutzerdefinierter Felder.

## Informationen zum Thema

[Feldabhängigkeiten einrichten](@EM-250)\
[Einschränkungen auf Feldwertzugriff einrichten](@EM-296)