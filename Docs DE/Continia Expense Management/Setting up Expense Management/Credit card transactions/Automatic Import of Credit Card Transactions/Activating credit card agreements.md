---
title: Kreditkartenvereinbarungen aktivieren
date: 21-11-2024
description: Erfahren Sie, wie Sie eine Bankvereinbarung zum automatischen Empfangen von Transaktionen einrichten.
id: EM-32
lang: de
---

# Kreditkartenvereinbarungen aktivieren

Im Expense Management können Sie Kreditkartentransaktionen importieren. Dadurch wird automatisch eine Ausgabe generiert, die bereits mit allen Informationen der Transaktion, wie Betrag, Währung, Datum und Beschreibung, ausgefüllt ist.

> [!IMPORTANT]
> Bevor Sie versuchen, eine Bankvereinbarung in Expense Management zu aktivieren, muss zuvor eine Vereinbarung mit der Bank bestehen.

Der Import von Kreditkartentransaktionen kann sowohl manuell als auch automatisch erfolgen. Im letzteren Fall müssen Sie eine Vereinbarung mit einer Bank treffen, um Transaktionen automatisch zu empfangen.

Um eine Bankvereinbarung für den automatischen Empfang von Transaktionen einzurichten, gehen Sie wie folgt vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Bankvereinbarungen** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Aktionsleiste **Neue Vereinbarung anfordern** aus.
3. Wählen Sie in der unterstützten Anleitung **Weiter** aus.
4. Füllen Sie auf der nächsten Seite der unterstützten Einrichtung die Felder mit den Transaktionsdetails aus, und wählen Sie dann **Weiter**.
5. Wählen Sie zur Bestätigung **Fertig** aus.

Die Anfrage wird anschließend vom Continia Support bearbeitet, was 1-2 Werktage dauern wird. Wenn die bereitgestellten Informationen mit einer Transaktion übereinstimmen, werden Ihnen die eingehenden Transaktionen im System angezeigt. Wenn die Informationen keiner Transaktion entsprechen, wird die Anfrage abgelehnt. Sie können den aktuellen Status einer Aktivierung jederzeit sehen, indem Sie auf der Seite **Bankvereinbarungen** die Option **Protokoll der Aktivierungsanfrage** auswählen.

> [!IMPORTANT]
> Wenn eine Kreditkartenvereinbarung aktiviert wurde, müssen Sie mit Continia Online synchronisieren, damit die Transaktionen in Expense Management heruntergeladen werden können.
>
> Es wird empfohlen, Synchronisierungen mithilfe einer Aufgabenwarteschlange auszuführen. Weitere Informationen finden Sie unter [Aufgabenwarteschlangen einrichten](@EM-65).

> [!NOTE]
> Sie können eine Bankvereinbarung nur in einer Produktionsumgebung aktivieren. Wenn Sie Transaktionen in einer Demoumgebung importieren möchten, können Sie dies manuell durchführen. Weitere Informationen finden Sie im Artikel [Manueller Dateiimport](Manual file import.md).