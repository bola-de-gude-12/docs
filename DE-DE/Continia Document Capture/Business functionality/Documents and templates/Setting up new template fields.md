---
title: Neue Vorlagenfelder einrichten
date: 27-12-2024
description: Erstellen, Anpassen und Hinzufügen von Vorlagenfeldern, einschließlich Mastervorlagenfeldern.
id: DC-19
lang: de
---

# Neue Vorlagenfelder einrichten

Wenn einige der Standardvorlagenfelder Ihren Anforderungen nicht entsprechen, können Sie Felder erstellen oder vorhandene anpassen. Sie können Felder entweder für eine Mastervorlage oder für alle Kreditorenvorlagen erstellen und anpassen. Es wird jedoch grundsätzlich empfohlen, Felder in einer Mastervorlage zu erstellen und sie dann von dort aus in die Kreditorenvorlagen zu kopieren.

In diesem Artikel werden Kreditoren und Einkaufsbelege als Beispiel verwendet. Die Funktionalität ist jedoch für andere Herkünfte und Belegtypen gleich.

## So erstellen Sie ein Mastervorlagenfeld mit dem Einrichtungsassistenten

Mit dem Einrichtungsassistenten können Sie Vorlagenfelder erstellen, ohne das Risiko einzugehen, vorhandene Pflichtfelder zu löschen oder andere Fehler in der Vorlage zu machen. Nur Feldeinstellungen, die häufig konfiguriert werden, stehen im Assistenten zur Verfügung.

So erstellen Sie ein Feld für eine Mastervorlage mit dem Einrichtungsassistenten:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie im Inforegister **Vorlagen** in der Liste die Mastervorlage für PDF-Dateien (**EINKAUF-DE**), und wählen Sie dann **Bearbeiten** aus, um die Vorlagenkarte zu öffnen.
4. Wählen Sie im Inforegister **Felder** > **Neues Vorlagenfeld erstellen**, um den **Vorlagenfeld Einrichtungsassistenten** zu öffnen.
5. Wählen Sie **Weiter**, um den Assistenten zu starten, und folgen Sie dann den Anweisungen auf dem Bildschirm, um das gewünschte Feld einzurichten. Wählen Sie **Beenden**, wenn Sie fertig sind.

Das neue Feld wird der Vorlagenkarte im Inforegister **Felder** hinzugefügt.

## So erstellen Sie ein Mastervorlagenfeld manuell

Sie können ein Feld für eine Mastervorlage auch manuell erstellen. Gehen Sie dazu folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie im Inforegister **Vorlagen** in der Liste die Mastervorlage für PDF-Dateien (**EINKAUF-DE**), und wählen Sie dann **Bearbeiten** aus, um die Vorlagenkarte zu öffnen.
4. Wählen Sie im Inforegister **Felder** > **Neu** aus, um die **Vorlagenfeldkarte** des neuen Felds zu öffnen.
5. Geben Sie im Inforegister **Allgemein** einen Code für das neue Vorlagenfeld ein (obligatorisch), und füllen Sie die verbleibenden Konfigurationsfelder nach Bedarf aus. Wenn Sie ein Dimensionsfeld erstellen, stellen Sie sicher, dass der **Code** des Felds genau mit dem Namen der zugehörigen Dimension übereinstimmt.

   > [!WARNING]
   > Leerzeichen und die folgenden Sonderzeichen sind in Vorlagenfeldcodes nicht zulässig: /\*-+()|\<\>%^&=.?$#@'". Wenn Sie eine Formel einrichten, die ein oder mehrere Feld(er) enthält, deren Codes Leerzeichen oder Sonderzeichen enthalten (zum Beispiel „BETRAG 1 + BETRAG 2“), funktioniert die Formel nicht. Wenn Sie Leerzeichen und/oder eines der genannten Zeichen in Ihrem Code verwenden, werden diese automatisch entfernt, wenn das Vorlagenfeld erstellt wird.

   > [!NOTE]
   > Auf der **Vorlagenfeldkarte** werden unterschiedliche Konfigurationsfelder angezeigt, je nachdem, welche Einstellung Sie unter **Datentyp** gewählt haben. Weitere Informationen finden Sie unter [Die Vorlagenfeldkarte](#die-vorlagenfeldkarte).
6. **Optional**: Wenn das neue Feld automatisch in alle neuen Kreditorenvorlagen eingefügt werden soll, die auf Grundlage der Mastervorlage erstellt werden, aktivieren Sie **In neue Vorlage einfügen** mit dem entsprechenden Schalter. Wenn Sie diese Option nicht aktivieren, kann das Feld später auch manuell einzelnen Vorlagen hinzugefügt werden, [wie unten beschrieben](#so-fugen-sie-einer-kreditorenvorlage-ein-neues-feld-hinzu).
7. Geben Sie im Inforegister **Feldübersetzungen** den Text ein, der für dieses Feld übersetzt werden soll, damit Document Capture das Feld erkennen kann. Aktivieren Sie das Kontrollkästchen in der Spalte **Groß-/Kleinschreibung beachten**, wenn beim eingegebenen Text zwischen Groß- und Kleinschreibung unterschieden werden soll.
   > [!TIP]
   > Wenn Sie in der Spalte **Übersetze nach** nichts eingeben, wird der Text, den Sie in der Spalte **Übersetze von** eingegeben haben, aus allen relevanten Werten entfernt, die von Document Capture identifiziert wurden. Wenn Sie beispielsweise unter **Übersetze von** den Text **Dr.** eingeben und **Übersetze nach** leer lassen, entfernt Document Capture diesen Titel, wenn er in einem Beleg erfasst wird. Dadurch kann Document Capture den richtigen Benutzer im System identifizieren.

Das neue Feld wird der Vorlagenkarte im Inforegister **Felder** hinzugefügt. Es wird direkt unter dem Listeneintrag eingefügt, der ausgewählt war, als Sie in Schritt 4 oben die Vorlagenfeldkarte geöffnet haben.

## Die Vorlagenfeldkarte

Auf der Vorlagenfeldkarte können Sie die Eigenschaften eines bestimmten Vorlagenfelds bearbeiten. Zum Beispiel können Sie den Datentyp festlegen, nach welchen Suchtexten Document Capture suchen soll, welche Regeln zur Validierung der erfassten Daten verwendet werden sollen und ob das Feld allen neuen Vorlagen hinzugefügt werden soll. Sie konfigurieren diese Eigenschaften mithilfe von verschiedenen Konfigurationsfeldern und Schaltern, die alle über erklärende Tooltips in der Business Central-Benutzeroberfläche verfügen.

Auf der **Vorlagenfeldkarte** werden unterschiedliche Konfigurationsfelder und Schalter angezeigt, je nachdem, welche Einstellung Sie unter **Datentyp** gewählt haben. Die meisten Felder und Schalter sind für alle Datentypen gleich. Daher wird in der folgenden Tabelle nur auf die Unterschiede zwischen den einzelnen Typen eingegangen:

<br>

| Datentyp     | Verfügbare Einstellungen                                                                                                                                                                                                                                                                |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Text**     | Für diesen Datentyp ist **Regelerzeugung aktivieren** als zusätzlicher Schalter unter **Regeln und Suchbegriffe** verfügbar.                                                                                                                                            |
| **Nummer**   | Für diesen Datentyp ist **Nummerierung Einstellungen** als zusätzlicher Abschnitt mit verschiedenen Nummernkonfigurationsfeldern und Schaltern verfügbar.                                                                                                               |
| **Datum**    | Für diesen Datentyp ist **Regelerzeugung aktivieren** als zusätzlicher Schalter unter **Regeln und Suchbegriffe** verfügbar. Außerdem ist **Datumseinstellungen** als zusätzlicher Abschnitt mit einer Reihe von Datumskonfigurationsfeldern verfügbar. |
| **Boolesch** | Für diesen Datentyp ist das Konfigurationsfeld **Nach Wert suchen** deaktiviert und das Feld **Formel** muss entweder den Wert **'Ja'** oder **'Nein'** haben. Der Standardwert ist **'Nein'**.                                                         |
| **Lookup**   | Für diesen Datentyp ist **Lookup Werte** als zusätzlicher Abschnitt mit einer Reihe von Lookup-Konfigurationsfeldern verfügbar.                                                                                                                                         |

Für den Datentyp **Datum** können Sie im Feld **Formel** die Schlüsselwörter **HEUTE** (**H**) oder **ARBEITSDATUM** (**A**) eingeben. Dadurch wird bei der Felderkennung für alle Belege, die diese Vorlage verwenden, automatisch das aktuelle Datum bzw. das angegebene Arbeitsdatum in das entsprechende Vorlagenfeld eingefügt. Wenn Sie dies beispielsweise für das Vorlagenfeld **Fälligkeitsdatum** einrichten und das Arbeitsdatum der 30. September 2024 ist, wird im Feld **Fälligkeitsdatum** unter **Belegkopf** im Belegjournal aller eingehenden Belege mit dieser Vorlage **30.09.24** angezeigt.

## So erstellen Sie ein Kreditorenvorlagenfeld

Um ein Kreditorenvorlagenfeld mit dem Einrichtungsassistenten zu erstellen, folgen Sie der [Anleitung für Mastervorlagenfelder oben](#so-erstellen-sie-ein-mastervorlagenfeld-mit-dem-einrichtungsassistenten). Wählen Sie jedoch in Schritt 3 eine Kreditorenvorlage aus.

Das manuelle Erstellen von Kreditorenvorlagenfeldern ist auch dem für Mastervorlagenfelder ähnlich, [wie oben beschrieben](#so-erstellen-sie-ein-neues-mastervorlagenfeld-manuell). Es gibt jedoch folgende Unterschiede:

 - In Schritt 3 müssen Sie eine Kreditorenvorlage auswählen.
 - Schritt 6 gilt nicht für Kreditorenvorlagen und sollte daher übersprungen werden.

Es wird grundsätzlich empfohlen, alle Felder in Mastervorlagen zu erstellen. Gelegentlich kann es jedoch erforderlich sein, Felder zu erstellen, die nur für einen bestimmten Kreditor zutreffen.

## So fügen Sie einer Kreditorenvorlage ein neues Feld hinzu

Nachdem Sie ein neues Feld in der Mastervorlage mit der Anleitung oben erstellt haben, kann es jeder beliebigen Kreditorenvorlage hinzugefügt werden. Wenn Sie beim Erstellen des Mastervorlagenfelds (Schritt 6 in [der obigen Anleitung](#so-erstellen-sie-ein-mastervorlagenfeld-manuell)) die Option **In neue Vorlagen einfügen** aktiviert haben, wird das Feld automatisch allen neuen Kreditorenvorlagen hinzugefügt, die als Kopien der Mastervorlage erstellt werden. Wenn Sie beim Erstellen des Felds nicht die Option **In neue Vorlagen einfügen** aktiviert haben, können Sie das Feld einer Kreditorenvorlage folgendermaßen manuell hinzufügen:

 - Mit dem Belegjournal, wie unter [So passen Sie Mastervorlagenfelder an](#so-passen-sie-mastervorlagenfelder-an) beschrieben.
 - Mit der Vorlagenkarte, wie unten beschrieben.

Um einer Kreditorenvorlage mithilfe der Vorlagenkarte ein Feld hinzuzufügen, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie im Inforegister **Vorlagen** die Vorlage in der Liste aus, der Sie das Feld hinzufügen möchten, und wählen Sie dann **Bearbeiten** aus, um die Vorlagenkarte zu öffnen.
4. Wählen Sie im Inforegister **Felder** die Option **Vorlagenfeld hinzufügen**, um die Liste der **Vorlagenfelder** zu öffnen.
5. Wählen Sie in der Feldliste das relevante Feld aus.

Das Feld wird dann der Liste der Vorlagenfelder hinzugefügt und auf der Vorlagenkarte im Inforegister **Felder** angezeigt.

## So passen Sie Mastervorlagenfelder an

Um Mastervorlagenfelder anzupassen, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie im Inforegister **Vorlagen** in der Liste die Mastervorlage für PDF-Dateien (**EINKAUF-DE**), und wählen Sie dann **Bearbeiten** aus, um die Vorlagenkarte zu öffnen.
4. Passen Sie im Inforegister **Felder** die einzelnen Vorlagenfelder und deren Verfügbarkeit an:
    - Um festzulegen, dass ein Feldwert in einem importierten Beleg vorhanden sein muss, damit der Beleg registriert werden kann, aktivieren Sie das Kontrollkästchen für das Feld in der Spalte **Erforderlich**.
    - Um ein Feld zu verschieben oder zu löschen, wählen Sie die entsprechende Feldzeile aus, und wählen Sie anschließend die gewünschte Aktion. Wenn Sie ein Feld löschen, haben Sie die Option, es in allen zugehörigen Vorlagen zu löschen.
    - Um die Eigenschaften eines Feldes zu bearbeiten, einschließlich des Datentyps, nach welchen Suchtexten gesucht werden soll, welche Regeln verwendet werden sollen und ob das Feld allen neuen Vorlagen hinzugefügt werden soll, wählen Sie in der Spalte **Feldname** den Namen des Feldes aus, um die entsprechende **Vorlagenfeldkarte** zu öffnen, und nehmen Sie dort die erforderlichen Änderungen vor.
   > [!NOTE]
   > Auf der **Vorlagenfeldkarte** werden unterschiedliche Konfigurationsfelder angezeigt, je nachdem, welche Einstellung Sie unter **Datentyp** gewählt haben. Weitere Informationen finden Sie unter [Die Vorlagenfeldkarte](#die-vorlagenfeldkarte).
5. **Optional**: Um ein Vorlagenfeld in alle Vorlagen, die auf Grundlage der Mastervorlage erstellt wurden, zu kopieren (wie beispielsweise das Feld, das Sie gerade angepasst haben), wählen Sie auf der Registerkarte **Felder** in der Feldliste das entsprechende Feld aus, und wählen Sie dann **Feld kopieren** aus.

   > [!IMPORTANT]
   > Das Feld wird nur in Vorlagen kopiert, in denen es noch nicht vorhanden ist; es aktualisiert keine bereits kopierten Felder des gleichen Typs. Wenn Sie das Feld bereits in alle Vorlagen kopiert haben, es aber aktualisieren müssen, müssen Sie dies manuell durchführen.

## So passen Sie Kreditorenvorlagenfelder an

Das Anpassen von Feldern für Kreditorenvorlagen funktioniert ähnlich wie das Anpassen von Feldern für Mastervorlagen; es gibt jedoch einige wichtige Unterschiede, auf die unten eingegangen wird.

Um Kreditorenvorlagenfelder anzupassen, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie im Inforegister **Vorlagen** in der Liste der Vorlagen die Vorlage aus, die Sie bearbeiten möchten, und wählen Sie dann **Bearbeiten** aus, um die Vorlagenkarte zu öffnen.
4. Passen Sie im Inforegister **Felder** die einzelnen Vorlagenfelder und deren Verfügbarkeit an:
    - Um festzulegen, dass ein Feldwert in einem importierten Beleg vorhanden sein muss, damit der Beleg registriert werden kann, aktivieren Sie das Kontrollkästchen für das Feld in der Spalte **Erforderlich**.
    - Um ein Feld zu verschieben oder zu löschen, wählen Sie die entsprechende Feldzeile aus, und wählen Sie anschließend die gewünschte Aktion.
    - Um ein Feld aus der Mastervorlage hinzuzufügen, wählen Sie **Vorlagenfeld hinzufügen**.
    - Um die Eigenschaften eines Feldes zu bearbeiten, einschließlich des Datentyps, nach welchen Suchtexten gesucht werden soll, und welche Regeln verwendet werden sollen, wählen Sie in der Spalte **Feldname** den Namen des Feldes aus, um die entsprechende **Vorlagenfeldkarte** zu öffnen, und nehmen Sie dort die erforderlichen Änderungen vor.
   > [!NOTE]
   > Auf der **Vorlagenfeldkarte** werden unterschiedliche Konfigurationsfelder angezeigt, je nachdem, welche Einstellung Sie unter **Datentyp** gewählt haben. Weitere Informationen finden Sie unter [Die Vorlagenfeldkarte](#die-vorlagenfeldkarte).

## Informationen zum Thema

[Mit Vorlagen arbeiten](Working with templates.md)