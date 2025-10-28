---
title: Transaktionsvorlagen einrichten
date: 06-12-2021
description: Erfahren Sie, wie Sie eine Transaktionsvorlage einrichten, um festzulegen, wie Banktransaktionsdateien verarbeitet werden.
id: EM-42
lang: de
---

# Transaktionsvorlagen einrichten

Bevor Sie Banktransaktionen von Ihrer Bank in Expense Management importieren, müssen Sie eine Transaktionsvorlage einrichten. Jede Vorlage ist einer Bank zugeordnet und es ist möglich, mehrere Vorlagen für die gleiche Bank zu haben. Jede Vorlage umfasst mehrere Regeln und Konfigurationen und diese bestimmen, wie Banktransaktionsdateien verarbeitet werden.

Um eine neue Transaktionsvorlage einzurichten, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Banken** ein, und wählen Sie dann den zugehörigen Link.

2. Wählen Sie eine Bank aus der Liste. Wenn Sie die Bank, von der Sie die Transaktionen importieren möchten, nicht in der Liste finden, müssen Sie eine neue erstellen.

3. Wählen Sie in der Aktionsleiste **Zugehörig** > **Bank** > **Transaktionsvorlage** aus.

4. Füllen Sie im Inforegister **Allgemein** die Felder nach Bedarf aus.

5. Die Felder werden unten beschrieben:

   - **Datenformate** – Wählen Sie ein vordefiniertes Datenformat für die Datums- und Dezimalfelder. Sollte das gewünschte Datums- oder Dezimalformat in der Lookup-Liste nicht definiert sein, können Sie es direkt als Text eingeben.

   - **Zu ignorierende Zeilen** - In den Feldern **Anzahl der Kopfzeilen** und **Anzahl der Fußzeilen** können Sie festlegen, ob bestimmte Zeilen am Anfang oder Ende der Datei beim Import ignoriert werden sollen, z. B. Zeilen mit Kopfzeileninformationen.

   - **Vorlagenregeln aktivieren/deaktivieren** – Mit dieser Option können Sie festlegen, ob die Kartennummer aus dem Namen der Transaktionsdatei gelesen werden soll. Wenn die Kreditkartennummer im Dateinamen und nicht in der Transaktion angegeben ist, wird durch Aktivieren der **Kartennummer im Dateinamen** die Kartennummer unter Verwendung der Startposition und Länge der Kartennummer aus dem Dateinamen extrahiert. Im Abschnitt **Zeilenregeln** können Sie Zeilen aus der Datei ausschließen, z. B. Zeilen, die das Wort „Gesamt“ enthalten. Diese Zeilen werden dann nicht importiert.

   - **Feldzuordnung** – dieser Abschnitt ermöglicht Ihnen die Zuordnung von Bankdateifeldern zu Expense Management-Feldern. Wenn beispielsweise Transaktionen aus der Bankdatei in das Expense Management-System importiert werden, kann das Feld _Beschreibung_ in der Bankdatei Details zur Transaktion enthalten, wie etwa den Namen des Kreditors, den Transaktionstyp oder eine kurze Beschreibung der Ausgabe. Durch die Zuordnung des Felds _Beschreibung_ aus der Bankdatei zum Feld _Firmenname_ in der Transaktionsvorlage unter Verwendung der Spaltennummer kann das System das Feld _Firmenname_ während des Importvorgangs automatisch mit den relevanten Informationen aus der Bankdatei füllen.

     > [!NOTE]
     >
     > Beim Umgang mit Dateien, die negative Beträge enthalten, ist es wichtig, die Option zum Umkehren von Vorzeichen manuell zu aktivieren. Dies ist erforderlich, da Kredittransaktionen als positive Beträge in das Transaktionsjournal importiert werden sollten.
