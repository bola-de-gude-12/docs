---
title: Betrugsprüfungen einrichten
date: 19-04-2024
description: null
id: DC-213
lang: de
---

# Betrugsprüfungen einrichten

Um Betrug zu minimieren, können Sie Continia Document Capture so einrichten, dass bestimmte Daten in den eingehenden Belegen der Kreditoren überprüft werden. Document Capture kann die folgenden Daten überprüfen:

- Bankkontonummern
- Umsatzsteuer-Identifikationsnummern
- Telefonnummern

Wenn Sie beispielsweise die Prüfung von Bankkontonummern einrichten und eine Bankkontonummer in einem importierten Beleg erfasst wird, vergleicht Document Capture die Nummer mit den folgenden Feldern auf der **Kreditor Bankkontokarte**, auf die Sie von der Kreditorenkarte aus zugreifen können:

- **IBAN**
- **Bankleitzahl** (Bankfiliale) + **Bankkontonummer**
- **Bankkontonummer** + **Bankleitzahl** (Bankfiliale)

Wenn die Werte dieser Felder mit dem erfassten Wert übereinstimmen, wird kein Betrug vermutet. Wenn jedoch keine Übereinstimmung vorliegt, wird im Abschnitt **Bemerkungen** unten im Belegjournal ein Fehlerkommentar angezeigt, der darauf hinweist, dass es sich bei dem Beleg möglicherweise um Betrug handelt.

Außerdem werden alle erfassten Umsatzsteuer-Identifikationsnummern anhand des Feldes **USt-IdNr.** und alle erfassten Telefonnummern anhand des Feldes **Telefonnr.** auf der Kreditorenkarte überprüft. Wenn die erfassten Werte nicht vorhanden sind oder sich von den entsprechenden Werten auf der Kreditorenkarte unterscheiden, wird im Belegjournal ein Fehlerkommentar angezeigt, um auf Betrug hinzuweisen.

> [!NOTE]
> Bei dieser Funktion werden nur Ziffern überprüft. Alle anderen Zeichen werden bei der Betrugsprüfung ignoriert, obwohl die Zeichen auch erfasst und den entsprechenden Vorlagenfeldern im Abschnitt **Belegkopf** hinzugefügt werden.

## So richten Sie Betrugsprüfungen in einer Kreditorenvorlage ein

Um Betrugsprüfungen für Bankkontonummern, Umsatzsteuer-Identifikationsnummern oder Telefonnummern in eingehenden Belegen eines bestimmten Kreditors einzurichten, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Belegkategorien** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Code der entsprechenden Belegkategorie, in diesem Fall **EINKAUF**, um das Belegjournal zu öffnen.
3. Wenn Document Capture automatisch einen Kreditor für den Beleg identifiziert hat, wird die Nummer des identifizierten Kreditors im Feld **Kreditor** in der Belegliste angezeigt. Wenn kein Kreditor identifiziert wurde, weisen Sie einen Kreditor manuell zu, wie unter [Den mit einem Beleg verknüpften Kreditor ändern](@DC-71#den-mit-einem-beleg-verknupften-kreditor-andern) beschrieben.
4. Wählen Sie in der Aktionsleiste **Vorlage** > **Vorlagenfeld hinzufügen** aus, um die Seite **Vorlagenfelder** zu öffnen.
5. Gehen Sie in der Feldliste mit dem Bildlauf zum Abschnitt **Kopffelder** und wählen Sie dann die Felder aus, die Sie zur Betrugsprüfung verwenden möchten. Hierfür stehen die folgenden Felder zur Auswahl:
   - **Kreditor Bankkonto-Nr.**
   - **USt-IdNr.**
   - **Telefonnummer des Kreditors**
6. Wählen Sie **OK**, um das bzw. die Feld(er) hinzuzufügen und zum Belegjournal zurückzukehren.
7. Die ausgewählten Felder werden dem Abschnitt **Belegkopf** im Belegjournal hinzugefügt. Wählen Sie zuerst das Feld aus, das Sie einrichten möchten.
8. Sie können mit der Maus genau auswählen, welcher Text im Beleg für das ausgewählte Vorlagenfeld erfasst werden soll: Um den _Suchtext_ festzulegen, klicken Sie mit der rechten Maustaste und halten Sie die Taste gedrückt, um einen orangefarbenen Rahmen um den relevanten Text in der Dokumentenvorschau zu zeichnen.
9. Um den entsprechenden _Wert_ für das ausgewählte Vorlagenfeld festzulegen, klicken Sie mit der linken Maustaste und halten Sie die Schaltfläche gedrückt, um in der Dokumentenvorschau ein blaues Kästchen um den entsprechenden Text zu zeichnen.
10. Der ausgewählte Text wird dem Vorlagenfeld im Abschnitt **Belegkopf** hinzugefügt. Stellen Sie sicher, dass er korrekt erfasst wurde.
11. Wiederholen Sie die Schritte 7 bis 10 für alle weiteren Felder, die Sie oben in Schritt 5 hinzugefügt haben.

Bei allen eingehenden Belegen von diesem Kreditor wird Document Capture anschließend alle erfassten Werte in den hinzugefügten Vorlagenfelder mit den entsprechenden Werten auf der Kreditorenkarte vergleichen, um Betrug zu verhindern.
