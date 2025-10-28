---
title: E-Mail-Benachrichtigungen
date: 27-02-2025
description: Einrichten, Anpassen und Senden von Status- und Erinnerungs-E-Mails
id: EM-297
lang: de
---

# E-Mail-Benachrichtigungen

Stellen Sie sicher, dass Genehmiger per E-Mail benachrichtigt werden, wenn sie Dokumente im Expense Management oder im Continia Web Approval Portal genehmigen, ablehnen oder stornieren müssen. Sie können Genehmiger manuell oder automatisch über Aufgabenwarteschlangen benachrichtigen. Außerdem können Sie die ausgehenden Benachrichtigungs-E-Mails anpassen.

## Voraussetzungen

Bevor Expense Management Benachrichtigungs-E-Mails senden kann, müssen Sie zunächst ein E-Mail-Konto konfigurieren.
So konfigurieren Sie ein E-Mail-Konto mit Expense Management:

1. Suchen {{search}} Sie in Expense Management nach **E-Mail einrichten** und wählen Sie dann den entsprechenden Link aus.
2. Befolgen Sie die Anweisungen auf dem Bildschirm im unterstützten Setup, um das E-Mail-Konto zu konfigurieren.

## Status-E-Mails manuell senden

Sie können Status-E-Mails ad hoc an alle Genehmiger senden, deren Genehmigungsanforderungen ausstehen, wenn Sie sie über Dokumente informieren müssen, deren Genehmigung auf sie wartet. Jede Status-E-Mail enthält eine Tabelle mit einer Liste aller Dokumente, deren Genehmigung noch aussteht, sowie einen Link zum Genehmigungs-Client, in dem alle verbleibenden Genehmigungsanfragen für den Tag aufgeführt sind.

Stellen Sie vor dem Versenden von Status-E-Mails sicher, dass alle E-Mail-Empfänger so eingerichtet sind, dass sie Dokumente in Expense Management oder im Web Approval Portal genehmigen können, siehe [Expense-Benutzer für Expense Management einrichten](@EM-36).

So senden Sie Status-E-Mails manuell:

1. Suchen {{search}} Sie nach **Status E-Mail an Genehmiger senden**.
2. Wählen Sie **Status E-Mail an Genehmiger senden (Expense Management)** aus.

Anschließend zeigt der Genehmigungs-Client alle verbleibenden Genehmigungsanfragen an, die für den Tag noch nicht bearbeitet wurden.

Um zu bestimmen, wann zusätzliche Benachrichtigungen versendet werden sollen, protokolliert Expense Management, wann eine Status-E-Mail an einen Genehmiger gesendet wird. Die erste Status-E-Mail des Tages (manuell oder automatisch) enthält alle Dokumente, deren Genehmigung durch den Genehmiger aussteht. Alle nachfolgenden E-Mails, die an diesem Tag an den Genehmiger gesendet werden, beziehen sich auf neue Genehmigungsanfragen, die nach dem Senden der ersten E-Mail hinzugefügt wurden.

## Senden von Status-E-Mails mithilfe von Aufgabenwarteschlangen

Expense Management unterstützt standardmäßige Microsoft Dynamics NAV/Business Central-Benachrichtigungen nicht. Sie können jedoch mithilfe von Aufgabenwarteschlangen automatisch Status-E-Mails an Genehmiger senden.

So senden Sie in Expense Management automatisch Status-E-Mails an Genehmiger:

1. Folgen Sie den im Artikel [Aufgabewarteschlangen einrichten](@EM-65) beschriebenen Schritten.
2. Geben Sie im Feld **ID des auszuführenden Objekts** die Codeunit 6086313 ein, um eine Status-E-Mail-Aufgabenwarteschlange einzurichten.
3. Stellen Sie die Wiederholungsrate auf alle 10–15 Minuten ein.

Die Codeunit ist so konzipiert, dass nur dann Benachrichtigungs-E-Mails versendet werden, wenn ein neuer Genehmigungsposten erstellt wurde. Dadurch wird sichergestellt, dass die Genehmiger immer über neue Genehmigungseinträge auf dem Laufenden sind. Wenn keine neuen Genehmigungsposten vorliegen, wird 24 Stunden lang keine E-Mail gesendet.

Jede Status-E-Mail enthält eine Tabelle mit einer Liste aller Dokumente, deren Genehmigung noch aussteht, sowie einen Link zum Genehmigungs-Client, in dem alle verbleibenden Genehmigungsanfragen für den Tag aufgeführt sind.

Stellen Sie vor dem automatischen Versenden von Status-E-Mails sicher, dass alle E-Mail-Empfänger so eingerichtet sind, dass sie Dokumente in Expense Management oder im Web Approval Portal genehmigen können, siehe [Expense-Benutzer für Expense Management einrichten](@EM-36).

## Benachrichtigungs-E-Mails anpassen

Sie können Elemente der an Genehmiger gesendeten E-Mails anpassen, beispielsweise die Standardbetreffzeile und den darin enthaltenen Text.

So passen Sie Benachrichtigungs-E-Mails an:

1. Suchen {{search}} Sie nach Expense Management Einrichtung und wählen Sie dann den zugehörigen Link.

2. Sie können die Betreffzeile von Benachrichtigungs-E-Mails unter **E-Mail** > **Erinnerungs-E-Mail** ändern.

3. Wählen Sie **Betreff der Genehmigungs-E-Mail** und geben Sie dann den Text für den E-Mail-Betreff ein.

### Benutzerdefinierte Vorlagen importieren

Sie können eine benutzerdefinierte HTML-Vorlage über die Aktionsleiste importieren.

1. Wählen Sie **Aktionen** > **E-Mail** > **Importiere Genehmigungsvorlage**.
2. Öffnen Sie die HTML-Vorlage, die Sie importieren möchten.
3. Wenn Sie eine benutzerdefinierte Vorlage erstellen, müssen Sie die beiden Schlüsselwörter #DOCUMENTS# und #APPROVALFORMLINK# beibehalten, da Expense Management sie durch eine Liste aller relevanten Dokumente zur Genehmigung und einen Link zum entsprechenden Genehmigungs-Client ersetzt.

> [!TIP]
> Ihr Expense Management-Installationspaket enthält eine HTML-Vorlage für Status-E-Mails. Sie können sie bearbeiten und als Grundlage für Ihre eigene benutzerdefinierte Vorlage verwenden. Sie finden unter: [Laufwerk]\Support Files\Document Capture\Other.

### Wann sollte die Standardvorlage verwendet werden?

Wenn Sie keine eigene benutzerdefinierte HTML-Vorlage importieren, verwendet Expense Management die Standardvorlage, die in einer Textvariablen in der Codeunit **CEM Expense Approval E-mail** hardcodiert wurde.

Falls zuvor eine benutzerdefinierte Vorlage importiert wurde und Sie stattdessen die Standardvorlage verwenden möchten, können Sie die importierte Vorlage löschen.

So löschen Sie eine importierte Vorlage:

1. Wählen Sie auf der Seite **Expense Management Einrichtung** in der Aktionsleiste **Aktionen** > **E-Mail** > **Lösche Genehmigungsvorlage** (nur sichtbar, wenn eine Vorlage importiert wurde).
2. In einem Dialogfeld werden Sie gefragt, ob Sie die Vorlage löschen möchten. Wählen Sie **Ja**, um die zuvor importierte Vorlage zu löschen und die Standardvorlage wiederherzustellen.

## Informationen zum Thema

Weitere Informationen mit Bezug auf diesen Artikel finden Sie unter:

[Expense-Benutzer für Expense Management einrichten](@EM-36)

[Aufgabenwarteschlangen einrichten](@EM-65)
