---
title: Häufig gestellte Fragen zu Belegen
date: 31-01-2025
description: Häufig gestellte Fragen zu Belegen
id: EM-244
lang: de
---

# Häufig gestellte Fragen zu Belegen

In diesem Abschnitt finden Sie Antworten auf einige der am häufigsten gestellten Fragen zur Verarbeitung von Belegen in Expense Management. Die Antworten geben Auskunft über Themen wie etwa das Festlegen einer Standardwährung und das Einschränken auswählbarer Feldwerte.

## Kann ich für einen Expense-Benutzer eine Standardwährung festlegen?

Diese Aktion wird derzeit nicht unterstützt. Dies ist nur möglich, die Währung ist gesperrt (und vom Expense-Benutzer nicht geändert werden kann).

Die Continia Expense App verwendet jedoch Standortdaten, um die Währung für das Land anzuzeigen, in dem sich der Expense-Benutzer befindet. Wenn der Expense-Benutzer eine andere Währung wählt, merkt sich die Continia Expense App diese für den nächsten Beleg und behält diesen Wert bei. Wenn die Continia Expense App geschlossen wird, wird die aus den Standortdaten abgeleitete Währung wieder verwendet. Sie können diese Einschränkung umgehen, indem Sie mit der Lookup-Funktion eine bestimmte Währung zuweisen. Dies bedeutet, dass der ausgewählte Expense-Benutzer oder die ausgewählte Gruppe (oder beide) nur auf eine bestimmte Währung zugreifen können, die auch standardmäßig ausgewählt wird, wenn sie einen neuen Beleg erstellen.

So weisen Sie einem Expense-Benutzer oder einer Gruppe eine bestimmte Währung zu:

1. Wählen Sie das Symbol ![Search](https://docs.continia.com/images/search_small.png), geben Sie **Konfigurierte Felder** ein und wählen Sie dann den zugehörigen Link aus.
2. Wählen Sie in der Tabelle unter **Feldcode** die Option **Währung** aus.
3. Wählen Sie in der Aktionsleiste **Kopffelder** > **Feldtyp** aus.
4. Wählen Sie in der Aktionsleiste **Feldtyp Karte** > **Feldtyp** > **Lookup Wert Zugriff** aus.
5. Wählen Sie in der Spalte **Wert Code** der Tabelle eine Währung aus. **Wert Beschreibung** wird automatisch mit der von Ihnen ausgewählten Währung ausgefüllt.
6. Optional: Wählen Sie unter **Art** einen Typ aus. Der Standardwert ist _Benutzer_.
7. Wählen Sie unter **Code** einen bestimmten Benutzer oder eine Gruppe aus.
8. Um diese Änderungen zu aktualisieren, müssen Sie eine Synchronisierung mit Continia Online erzwingen. Wählen Sie in der Aktionsleiste **Feld Typ Karte** > **Continia Online** > **Erzwinge Synchronisation mit Continia Online**.

## Kann ich einschränken, welche Feldwerte Expense-Benutzer in der Expense App auswählen können?

Ja, das können Sie. Um festzulegen, welche Feldwerte für Expense-Benutzer in Business Central verfügbar sind, _erlauben_ Sie den Zugriff auf bestimmte Feldwerte. So beschränken Sie den Zugriff der Expense-Benutzer auf die angegebenen Feldwerte.

Weitere Informationen finden Sie unter [Beschränkungen für den Feldwertzugriff einrichten](@EM-296).
