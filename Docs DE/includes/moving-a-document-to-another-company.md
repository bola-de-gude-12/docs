Wenn Sie mehrere Mandanten in Microsoft Dynamics 365 Business Central eingerichtet haben, kann es vorkommen, dass Sie {param1} in Continia Expense Management von einem Mandanten in einen anderen übertragen müssen. Dies kann in Situationen relevant sein, in denen Sie Expense Management so konfiguriert haben, dass alle {param2} in einen bestimmten Mandanten importiert werden, oder wenn jemand versehentlich {param1} an den falschen Mandanten sendet.

> [!NOTE]
> Die folgende Anleitung setzt voraus, dass Sie in Business Central mindestens zwei Mandanten eingerichtet und aktiviert haben. Andernfalls ist das Feld **In anderen Mandanten verschieben** nicht verfügbar. Stellen Sie außerdem sicher, dass Expense Management in allen relevanten Mandanten, zwischen denen Sie {param2} verschieben möchten, installiert, aktiviert und ordnungsgemäß eingerichtet ist.

Um {param1} manuell von einem Mandanten zu einem anderen zu verschieben, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Belege** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Belegliste den Beleg aus, den Sie verschieben möchten.
3. Wählen Sie in der Aktionsleiste **Aktionen** > **Funktion** > **In anderen Mandanten verschieben**.
4. Wählen Sie auf der Seite **Verschiebe in Mandant** in der Spalte **Name** den Namen des Mandanten aus, zu dem Sie den ausgewählten Beleg verschieben möchten.
5. Wenn der Beleg verschoben wurde, wird dies in einem Dialogfeld bestätigt. Wählen Sie **OK**, um das Dialogfeld zu schließen und zur Belegseite zurückzukehren.

Wenn der Beleg in Schritt 5 oben nicht erfolgreich verschoben werden konnte, wird stattdessen ein Dialogfeld mit einer Fehlermeldung angezeigt. Dies kann daran liegen, dass Expense Management im Zielmandanten nicht aktiviert oder nicht richtig eingerichtet ist. Wählen Sie in diesem Fall **OK**, um das Dialogfeld zu schließen, und stellen Sie dann sicher, dass Expense Management in allen relevanten Mandanten aktiviert und voll funktionsfähig ist.
