---
title: Verbesserte Zeilenerkennung in Document Capture
date: 26-09-2025
description: Eine Beschreibung der verbesserten Zeilenerkennung in Document Capture.
id: DC-191
lang: de
---

# Verbesserte Zeilenerkennung

Basierend auf den Zeilendaten, die durch künstliche Intelligenz (KI) erfasst werden, kann Continia Document Capture mehr Daten in den Zeilen eingehender Dokumente erfassen, und die erfassten Daten sind erheblich genauer als zuvor.

> [!IMPORTANT]
> Die in diesem Artikel beschriebene Funktionalität steht Ihnen nur zur Verfügung, wenn Sie die Codeunit für die Zeilenerfassung **CDC Line Capture 2.0** verwenden. Um dies zu überprüfen, öffnen Sie die Vorlagenkarte der entsprechenden Vorlage, gehen Sie zum Inforegister **Codeunits** und überprüfen Sie die unter **Zeilencapture** angezeigte Codeunit. Ab Document Capture 2024 R1 verwenden alle neu erstellten Vorlagen standardmäßig diese Codeunit, während vorhandene Vorlagen die ältere Codeunit beibehalten.
>
> Sie können die neue Codeunit auch den vorhandenen Vorlagen zuordnen, wenn Sie sich über die möglichen Auswirkungen bewusst sind. Dies sollte in den allermeisten Fällen gut funktionieren, kann jedoch unter bestimmten Umständen die Ergebnisse und die Qualität der Zeilenerfassung beeinträchtigen. Wenn dies der Fall ist, können Sie die ältere Codeunit wieder anwenden, um die vorherige Funktionalität wiederherzustellen.

Das folgende Video beschreibt die wichtigsten Funktionen der verbesserten Zeilenerkennung:

<br>

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src=https://player.vimeo.com/video/924666894?h=023c3cda09&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479 frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="DC_Sales documents_Notification_produced"></iframe></div><script src=https://player.vimeo.com/api/player.js></script>

## So wenden Sie Verbesserungsvorschläge an

Um Ihnen einen schnellen Einstieg in diese Funktionen zu ermöglichen und Sie bei deren Anwendung zu unterstützen, bietet Document Capture einen KI-basierten Assistenten, der automatisch verbesserungswürdige Bereiche der Zeilenerkennung identifiziert und Sie dann darüber informiert. Wenn Sie die Benachrichtigung auswählen, wird Ihnen eine Liste mit Vorschlägen zum Aktualisieren der zugewiesenen Vorlage angezeigt, um mehr Zeilendetails präzise zu erfassen. Sie können dann frei entscheiden, ob Sie diese Vorschläge anwenden möchten.

> [!NOTE]
> Wenn Sie KI zur Zeilenerkennung auf der Dokumentenkarte verwenden, werden weiterhin Vorschläge zur Verbesserung der Erkennung angezeigt – sofern die Belegwerte einen Vorschlag erfordern und der jeweilige Vorschlag nicht deaktiviert wurde.

Bei allen Vorschlägen handelt es sich um Schnellanleitungen, um Ihnen die gewünschte Zeilenerkennung mit Document Capture zu ermöglichen. Die jeweiligen Verbesserungsvorschläge können jedoch auch auf herkömmliche Weise in der Einrichtung konfiguriert werden, wie in anderen Abschnitten weiter unten beschrieben.

> [!NOTE]
> Diese Anleitung beschreibt nicht alle möglichen Vorschläge im Detail, sondern nur, wie sie angewendet werden. Beispiele für mögliche Vorschläge sind:
>
> - **KI als Zeilenerkennungsmethode verwenden** – siehe [So verwenden Sie KI-Zeilenerkennung](#so-verwenden-sie-ki-zeilenerkennung) weiter unten.
> - **Zeilen erfassen, die sich über mehrere Reihen erstrecken** – siehe [So erfassen Sie Zeilen, die sich über mehrere Reihen erstrecken](#so-erfassen-sie-zeilen-die-sich-uber-mehrere-reihen-erstrecken) weiter unten.
> - **Regel zum Abgleichen von Artikelnummern hinzufügen** – hiermit lässt sich beispielsweise eine Vorlagenfeldregel erstellen, die nur auf **Nr.**-Werte zutrifft, die Großbuchstaben und ggf. Ziffern enthalten und mindestens sieben Zeichen lang sind.
> - **Regel zum Abgleichen von Dezimalwerten hinzufügen** – hiermit können Sie beispielsweise eine Vorlagenfeldregel erstellen, die nur mit Zahlen übereinstimmt, die Kommas als Dezimaltrennzeichen verwenden, und zwar für die Felder **Rabattbetrag**, **Zeilenbetrag** und **Einstandspreis**.

So wenden Sie Vorschläge des Assistenten für die Zeilenerkennung an:

1. Führen Sie die Schritte 1-5 der [Anleitung zur herkömmlichen Zeilenerkennung](@DC-147#so-erfassen-sie-zeilenfelder) aus, um die Dokumentenkarte zu öffnen.
2. Wenn die Funktion Verbesserungen hinsichtlich der Zeilenerkennung identifiziert, erscheint oben eine Benachrichtigung mit einigen Vorschlägen. Klicken Sie auf **Vorschläge anzeigen**, um die Seite **Vorlagenvorschläge** zu öffnen.
3. Suchen Sie in der Liste der Vorschläge den/die Vorschläg(e), den/die Sie anwenden möchten, und aktivieren Sie dann das/die entsprechende(n) Kästchen in der Spalte **Übernehmen**.
   > [!TIP]
   > Wenn Sie mehr über einen Vorschlag erfahren möchten, bevor Sie ihn anwenden, klicken Sie in der Spalte ganz rechts für diesen Vorschlag auf **Details anzeigen**, um ein Dialogfeld mit weiteren Informationen zu öffnen. Klicken Sie auf **OK**, um das Dialogfeld zu schließen und zur Seite **Vorlagenvorschläge** zurückzukehren.
4. Um die Seite zu schließen und die Einstellungen anzuwenden, klicken Sie auf **Fertig**.

Die vom KI-basierten Assistenten vorgeschlagenen Verbesserungen werden jetzt angewendet. Um eine Übersicht aller von Ihnen angewendeten Vorschläge anzuzeigen, klicken Sie auf die Aktionsleiste und wählen Sie **Aktionen** > **Funktionen** > **Angewendete Vorschläge anzeigen**. Dadurch wird die Seite **Vorlagenvorschläge** geöffnet, die einen vollständigen Überblick bietet.

## So verwenden Sie KI-Zeilenerkennung

Wenn Document Capture mehrere Beträge erkennt, die mit dem Gesamtbetrag des Belegs übereinstimmen, wird Ihnen vorgeschlagen, die KI-Zeilenerkennung zu verwenden, um den Vorgang zu vereinfachen und zu beschleunigen. Die KI-Zeilenerkennungsfunktion ist jedoch völlig optional und kann in Kombination mit [der herkömmlichen Methode](@DC-147) verwendet werden. Dies bedeutet, dass Sie alle Suchtextn und Werte, die die KI-gestützte Zeilenerkennungsfunktion nicht identifizieren konnte, manuell erfassen und Werte überschreiben können, die von der KI falsch erfasst wurden.

> [!NOTE]
> Diese Funktion steht allen Kunden zur Verfügung, die die Continia Cloud OCR-Engine verwenden.

So erfassen Sie die Felder eines Belegs mit der KI-Zeilenerkennung:

1. Führen Sie die Schritte 1-5 der [Anleitung zur herkömmlichen Zeilenerkennung](@DC-147#so-erfassen-sie-zeilenfelder) aus, um die Dokumentenkarte zu öffnen.
2. Klicken Sie in der Benachrichtigung oben auf der Seite auf **Vorschläge anzeigen**, um die Seite **Vorlagenvorschläge** zu öffnen.
3. Suchen Sie in der Liste der Vorschläge nach **Verwenden Sie KI als Methode zur Zeilenerkennung** und aktivieren Sie anschließend das entsprechende Kontrollkästchen in der Spalte **Übernehmen**.
   > [!TIP]
   > Sie können die KI-Zeilenerkennung auch direkt im Inforegister **Allgemein** aktivieren: Gehen Sie zu **Zeilen erkennen** und wählen Sie **KI** im Dropdown-Menü.
4. Klicken Sie anschließend auf **Fertig**, um die Seite zu schließen und die Einstellung anzuwenden.
5. Wenn die KI-Zeilenerkennungsfunktion einige Zeilendaten nicht erkennt, können Sie die Daten manuell auswählen, indem Sie die Schritte 6 bis 9 der [Anleitung zur herkömmlichen Zeilenerkennung](@DC-147#so-erfassen-sie-zeilenfelder) befolgen.

Wenn alle Zeilendaten durch die KI-Funktion und/oder manuell von Ihnen korrekt erfasst wurden, ist der Beleg zur weiteren Verarbeitung bereit.

So überschreiben Sie von der KI falsch erfasste Werte:

1. Wählen Sie im Inforegister **Zeilen** das Zeilenfeld aus, dessen Wert Sie überschreiben möchten.
2. Klicken Sie mit der linken Maustaste auf den Bereich im Dokument, der den richtigen Wert enthält.
3. Nachdem Sie manuell einen neuen Wert ausgewählt haben, können Sie auch einen anderen Zeilensuchtext erfassen.

   > [!NOTE]
   > Das Erfassen einer anderen Zeilenüberschrift oder das Überschreiben aller Zeilenfelder mit manuell ausgewählten Werten deaktiviert die KI-gesteuerte Zeilenerkennung für das gesamte Dokument.

## So erfassen Sie Zeilen, die sich über mehrere Reihen erstrecken

Einige Zeilen in Einkaufsbelegen enthalten mehrere Textreihen. Beispielsweise kann die Artikelnummer in einer höheren Reihe stehen als die Artikelmenge. Mit der herkömmlichen Zeilenerkennung lassen sich derartige Layouts nur schwer erfassen. Wenn Document Capture ein mögliches Problem mit Zeilen erkennt, die sich über mehrere Zeilen erstrecken, wird Ihnen vorgeschlagen, diese Funktion zu aktivieren, um das Problem zu beheben.

So erfassen Sie Zeilen, die sich über mehrere Reihen erstrecken:

1. Folgen Sie der [Anleitung zur herkömmlichen Zeilenerkennung](@DC-147#so-erfassen-sie-zeilenfelder), um die Dokumentenkarte zu öffnen, orangefarbene Kästchen um die Überschriften zu zeichnen und die Zeilenerkennung durchzuführen.
2. Wenn Document Capture feststellt, dass sich eine oder mehrere Zeilen im Beleg über mehrere Reihen erstrecken können, wird oben auf der Seite eine Benachrichtigung mit Vorschlägen zur Verbesserung der Zeilenerkennung angezeigt. Klicken Sie in der Benachrichtigung auf **Vorschläge anzeigen**, um die Seite **Vorlagenvorschläge** zu öffnen.
3. Suchen Sie in der Liste der Vorschläge nach **Aktivieren Sie die Zeilenerfassung, um mehrere Textzeilen zu umfassen** und aktivieren Sie anschließend das entsprechende Kontrollkästchen in der Spalte **Übernehmen**.
4. Klicken Sie anschließend auf **Fertig**, um die Seite zu schließen und die Einstellung anzuwenden.
   > [!NOTE]
   > Dadurch wird das Feld **Zeilenwert geht über mehrere Zeilen** auf der Vorlagenkarte aktiviert. Sie können dies auch direkt aktivieren, ohne die Benachrichtigung des Assistenten zu verwenden: Klicken Sie auf der Dokumentenkarte in der Aktionsleiste auf **Vorlage** > **Vorlagenkarte**, um die Vorlagenkarte zu öffnen. Aktivieren Sie im Inforegister **Allgemein** den Schalter **Zeilenwerte geht über mehrere Zeilen**.

Die relevanten Werte unter den orange-umrahmten Spaltenüberschriften werden dann automatisch für jede Zeile im Beleg in die entsprechenden Felder im Inforegister **Zeilen** übertragen. Außerdem werden dieselben Werte in der Dokumentenvorschau von blauen Kästchen umrahmt. Beachten Sie, dass Sie in Schritt 3 oben möglicherweise zusätzliche Vorschläge anwenden müssen (z. B. eine oder mehrere Regeln), damit Document Capture genau bestimmen kann, welche Werte für die Erfassung relevant sind.

## So verwenden Sie relative Zeilenerfassung

Nachdem Sie durch Erfassen der wichtigsten Details (beispielsweise mithilfe der oben beschriebenen Funktion zum Erfassen mehrerer Zeilen) definiert haben, wo sich die Zeilen im Beleg befinden, können Sie die verbleibenden Zeilendetails für eine der Zeilen manuell erfassen, damit Document Capture weiß, wo in den anderen Zeilen danach gesucht werden soll. Document Capture kann dann an den gleichen Positionen relativ zu den zuvor erfassten Daten die entsprechenden Details in den anderen Zeilen erfassen.

Nachdem Sie durch Erfassen der wichtigsten Details (beispielsweise mithilfe der oben beschriebenen Funktion zum Erfassen mehrerer Zeilen) definiert haben, wo sich die Zeilen im Beleg befinden, können Sie die verbleibenden Zeilendetails für eine der Zeilen manuell erfassen, damit Document Capture weiß, wo in den anderen Zeilen danach gesucht werden soll. Document Capture kann dann an den gleichen Positionen relativ zu den zuvor erfassten Daten die entsprechenden Details in den anderen Zeilen erfassen.

Sie können jetzt auch Feldsuchtexte definieren und Werte auf Reihenebene statt auf Spaltenebene für jede Zeile erfassen. Dies bietet eine größere Flexibilität als die herkömmliche spaltenbasierte Zeilenerfassung und ermöglicht Ihnen in einigen Fällen, genauer anzugeben, was Sie erfassen möchten.

So erfassen Sie einen Wert mithilfe der relativen Zeilenerfassung:

1. Folgen Sie der [Anleitung zur herkömmlichen Zeilenerkennung](@DC-147#so-erfassen-sie-zeilenfelder), um die Dokumentenkarte zu öffnen, orangefarbene Kästchen um die Überschriften zu zeichnen und die Zeilenerkennung durchzuführen.
2. Wenn einige Zeilendetails aufgrund eines ungewöhnlichen Beleglayouts nicht erfasst werden, können Sie sie mithilfe der relativen Zeilenerfassung erfassen: Wählen Sie im Inforegister **Zeilen** in der Zeilenliste das Feld aus, dessen Wert Sie erfassen möchten, z.
3. Suchen Sie in der Dokumentenvorschau den entsprechenden Text, den Sie erfassen möchten, und klicken Sie dann mit der linken Maustaste und halten Sie die Taste gedrückt, um ein blaues Kästchen um den Text zu zeichnen.

   > [!NOTE]
   > Damit die relative Zeilenerfassung funktioniert, darf für den Wert, um den Sie ein blaues Kästchen zeichnen, kein Suchtext für die Spaltenüberschrift definiert sein. Um den zugehörigen Suchtext zu löschen, markieren Sie das gewünschte Zeilenfeld und klicken Sie mit der rechten Maustaste auf eine leere Stelle im Dokument.

   > [!TIP]
   > Wenn das Feld, für das Sie einen Wert erfassen möchten, in den Abschnitten **Belegkopf** oder **Zeilen** nicht verfügbar ist, können Sie es hinzufügen, indem Sie den gewünschten Wert in der Dokumentenvorschau auswählen.
   >
   > 1. Wählen Sie ein Kopf- oder Zeilenfeld aus. Kopffelder können aus der Dokumentenkarte oder dem Belegjournal ausgewählt werden, während Zeilenfelder nur aus der Dokumentenkarte ausgewählt werden können.
   > 2. Drücken Sie **Strg** und wählen Sie den gewünschten Wert in der Dokumentenvorschau aus, um den **Vorlagenfeld-Einrichtungsassistenten** zu öffnen. Beachten Sie, dass Werte mit **Strg** und der linken Maustaste und Suchtexte mit **Strg** und der rechten Maustaste erkannt werden müssen.
   > 3. Klicken Sie auf **Weiter > Vorlagenfeld**, um die **Vorlagenfeldliste** zu öffnen und ein vorhandenes Feld aus der Mastervorlage auszuwählen, oder auf **Weiter > Neu erstellen**, um ein benutzerdefiniertes Feld zu erstellen.
   > 4. Wenn Sie fertig sind, klicken Sie auf **Beenden**, um zur Dokumentenkarte zurückzukehren.
4. Klicken Sie in der Aktionsleiste auf **Start** > **Felder erkennen**. Document Capture merkt sich nun die Position Ihres blau umrahmten Werts im Verhältnis zu anderen, zuvor erfassten Werten und sucht dann für andere Zeilen nach entsprechenden Werten an den gleichen relativen Positionen. Die ermittelten Werte werden in der Dokumentenvorschau von blauen Kästchen umrahmt und für jede Zeile im Beleg automatisch in das entsprechende Feld im Inforegister **Zeilen** übertragen.
5. Wenn einige der ermittelten Werte falsch sind, können Sie diese möglicherweise mithilfe der neu eingeführten Funktion zum Definieren von Feldsuchtexten auf Reihenebene korrigieren:
   1. Suchen Sie im Inforegister **Zeilen** das entsprechende Feld und klicken Sie auf die drei Punkte auf der rechten Seite des Felds, um die Vorlagenfeldkarte zu öffnen.
   2. Wählen Sie unter **Zeilen Suchbegriff Art** > **Zeile** aus, um Feldsuchtexte auf Reihenebene zu identifizieren, und klicken Sie dann auf **Schließen**, um zur Dokumentenkarte zurückzukehren.
   3. Suchen Sie in der Dokumentenvorschau den entsprechenden Suchtext, dessen Wert Sie erfassen möchten, und klicken Sie dann mit der rechten Maustaste und halten Sie die Taste gedrückt, um ein orange-farbenes Kästchen um den Text zu zeichnen.
   4. Suchen Sie in der Dokumentenvorschau den entsprechenden Wert, den Sie erfassen möchten, und klicken Sie dann mit der linken Maustaste und halten Sie die Taste gedrückt, um ein blaues Kästchen um den Text zu zeichnen.
   5. Klicken Sie in der Aktionsleiste auf **Start** > **Felder erkennen**.

Document Capture merkt sich nun die Position Ihres blau umrahmten Werts im Verhältnis zum Suchtext mit dem orange-farbenen Rahmen und sucht dann für andere Zeilen nach entsprechenden Werten an den gleichen relativen Positionen. Die ermittelten Werte werden in der Dokumentenvorschau von blauen Kästchen umrahmt und für jede Zeile im Beleg automatisch in das entsprechende Feld im Inforegister **Zeilen** übertragen.

## So füllen Sie leere Felder basierend auf Formeln oder anderen Feldern

In manchen Geschäftsbelegen sind bestimmte Werte implizit und die entsprechenden Felder bleiben deshalb für einige Belegzeilen leer. Beispielsweise kann in einer Rechnung in der ersten Zeile auf eine zugehörige Bestellnummer verwiesen werden. In der zweiten Rechnungszeile wird dieser Bezug auf die gleiche Bestellnummer möglicherweise weggelassen, da dieser aus dem Verweis in der ersten Rechnungszeile erkennbar ist. Solche leeren Felder können jetzt automatisch auf Grundlage anderer Felder (in diesem Fall des entsprechenden Felds in der vorherigen Rechnungszeile) oder Formeln ausgefüllt werden.

So füllen Sie leere Felder basierend auf Feldern oder Formeln automatisch aus:

1. Folgen Sie der [Anleitung zur herkömmlichen Zeilenerkennung](@DC-147#so-erfassen-sie-zeilenfelder), um die Dokumentenkarte zu öffnen, orangefarbene Kästchen um die Überschriften zu zeichnen und die Zeilenerkennung durchzuführen.
2. Wenn ein Feld leer ist, sein Wert jedoch aus anderen Belegdaten abgeleitet werden könnte, gehen Sie zum Inforegister **Zeilen** und suchen Sie das leere Feld.
3. Klicken Sie auf die drei Punkte auf der rechten Seite des Felds, um die Vorlagenfeldkarte zu öffnen.
4. Gehen Sie im Inforegister **Allgemein** unter **Erweiterte Erkennungseinstellungen** zu **Wenn der Wert leer ist** und wählen Sie dann eine der folgenden Optionen aus:
   | Option                                 | Beschreibung                                                                                                   |
   | -------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
   | **Wert aus vorheriger Zeile kopieren** | Kopiert den Wert aus dem entsprechenden Feld in der vorherigen Belegzeile.                     |
   | **Wert aus Kopffeld kopieren**         | Kopiert den Wert aus einem Kopfzeilenfeld, das Sie im Feld **Wert aus Feld kopieren** angeben. |
   | **Wert aus Zeilenfeld kopieren**       | Kopiert den Wert aus einem Zeilenfeld, das Sie im Feld **Wert aus Feld kopieren** angeben.     |
   | **Formel verwenden**                   | Berechnet den Wert anhand einer Formel, die Sie im Feld **Formel** angeben.                    |
5. Wenn Sie oben in Schritt 4 **Wert aus Kopffeld kopieren** oder **Wert aus Zeilenfeld kopieren** ausgewählt haben, wird das Feld **Wert aus Feld kopieren** angezeigt. Wählen Sie in diesem Feld aus dem Dropdown-Menü das Feld aus, aus dem Sie den Wert kopieren möchten.
6. Wenn Sie oben in Schritt 4 **Formel verwenden** ausgewählt haben, wird das Feld **Formel** angezeigt. Klicken Sie auf die drei Punkte auf der rechten Seite dieses Felds, um die **Vorlagenfeldliste** zu öffnen, und wählen Sie dann die gewünschte Formel aus. Klicken Sie auf **OK**, um zur Vorlagenfeldkarte zurückzukehren.
7. Klicken Sie auf **Schließen**, um zur Dokumentenkarte zurückzukehren.
8. Klicken Sie in der Aktionsleiste auf **Start** > **Felder erkennen**.

Document Capture füllt nun das leere Feld für alle Zeilen entsprechend Ihrer Konfiguration aus.

## So erfassen Sie nur die Teile von Werten, die einer bestimmten Regel entsprechen

Wenn Sie einen bestimmten Wertetyp für ein Feld erfassen möchten, können Sie für dieses Feld eine Regel einrichten. Normalerweise könnte eine solche Regel dazu führen, dass Document Capture einige der erfassten Werte als ungültig erachtet, da sie Zeichen enthalten, die nicht der Regel entsprechen. Aber mit der zusätzlichen Funktion **Nur Übereinstimmung erfassen** können Sie solche unerwünschten Zeichen herausfiltern, indem Sie angeben, dass Document Capture nur den Teil des Werts erfassen soll, der der Regel entspricht.

Wenn Sie beispielsweise eine Regel zum Erfassen ausschließlich von Ziffern einrichten, werden alle erfassten Werte, die Ziffern enthalten, aber in Klammern eingeschlossen sind, als ungültig verworfen, wenn die Funktion **Nur Übereinstimmung erfassen** deaktiviert ist. Wenn Sie diese Funktion aktivieren, kann Document Capture die Klammern herausfiltern und sich nur auf die Ziffern konzentrieren, die der Regel entsprechen. Dies führt zur erfolgreichen Erfassung der gewünschten Werte.

So aktivieren Sie **Nur Übereinstimmung erfassen**:

1. Führen Sie die Schritte 1-5 der [Anleitung zur herkömmlichen Zeilenerkennung](@DC-147#so-erfassen-sie-zeilenfelder) aus, um die Dokumentenkarte zu öffnen.
2. Suchen Sie im Inforegister **Zeilen** das entsprechende Feld und klicken Sie auf die drei Punkte auf der rechten Seite des Felds, um die Vorlagenfeldkarte zu öffnen.
3. Gehen Sie im Inforegister **Allgemein** zu **Regel** und klicken Sie auf die drei Punkte auf der rechten Seite des Felds, um die Seite **Feldregeln** zu öffnen.
4. Richten Sie eine Regel ein oder verwenden Sie eine vorhandene.
5. Aktivieren Sie in der Spalte **Nur Übereinstimmung erfassen** das Kontrollkästchen, um die Funktion zu aktivieren.

Für das ausgewählte Feld erfasst Document Capture nur den Teil jedes Werts, der der von Ihnen eingerichteten Regel entspricht.

## Informationen zum Thema

[Mit Papier- und PDF-Belegen arbeiten](@DC-71)\
[Kopffelder in einem Beleg erfassen](@DC-110)