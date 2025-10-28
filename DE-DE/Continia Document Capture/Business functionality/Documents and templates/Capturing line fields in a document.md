---
title: Zeilenfelder in einem Beleg erfassen (Zeilenerkennung) in Document Capture
date: 19-03-2025
description: null
id: DC-147
lang: de
---

# Zeilenfelder in einem Beleg erfassen (Zeilenerkennung)

> [!IMPORTANT]
> Zur Veranschaulichung konzentriert sich dieser Artikel auf Einkaufsbelege und Kreditoren. Die unten beschriebenen Vorgehensweisen gelten jedoch auch für andere Arten von Geschäftsbelegen und Belegherkünften.

Die Vorgehensweise zum Erfassen von Zeilenfeldern in einem importierten Beleg ist der zum [Erfassen von Kopffeldern](@DC-110) sehr ähnlich. Der Hauptunterschied besteht darin, dass bei der Erkennung von Kopffeldern die Zeilen des Belegs unberücksichtigt bleiben und nur der Belegkopf zum Erfassen von [Feldsuchtexten und -werten](@DC-110#understanding-field-captions-and-values) berücksichtigt wird. Bei der Zeilenerkennung werden außer den erfassten Kopffeldern auch Feldsuchtexte und -werte in den Belegzeilen eingelesen. Dadurch können in Belegen mehr Details erfasst werden, was in manchen Kontexten sehr nützlich sein kann. Dies hängt davon ab, welche Daten in Ihrer Organisation benötigt werden.

Die Zeilenerkennung wird im Folgenden genau beschrieben. Wenn Sie einen Beleg von einem Kreditor zum ersten Mal erhalten, sind diesem Kreditor keine Vorlagen zugeordnet. Um dem Kreditor eine Vorlage zuzuweisen, müssen Sie im Belegjournal die Felderkennung aktivieren (siehe [Schritt 4 unten](#so-erfassen-sie-zeilenfelder)). Dadurch wird automatisch eine Vorlage erstellt, mit dem Kreditor verknüpft und alle Felder für diesen Beleg erfasst.

> [!NOTE]
> Wenn ein Kreditor Ihnen zum ersten Mal einen Beleg sendet, aber bereits über eine zugehörige Vorlage in einem anderen Mandanten verfügt, kopiert Continia Document Capture die Vorlage von diesem Mandanten in den aktuellen Mandanten. Sie müssen eine Konfiguration, die Sie bereits in einem anderen Mandanten für denselben Kreditor vorgenommen haben, dann nicht erneut durchführen.

## So erfassen Sie Zeilenfelder

So erfassen Sie die Felder eines Belegs, einschließlich Zeilenfelder:

1. Wählen Sie das Symbol {{search}}, geben Sie **Belegkategorien** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Code der entsprechenden Belegkategorie, in diesem Fall **EINKAUF**, um das Belegjournal zu öffnen.
3. Wenn Document Capture für den Beleg, dessen Felder Sie erfassen möchten, automatisch einen Kreditor identifiziert hat, wird die Nummer des identifizierten Kreditors im Feld **Kreditor** in der Belegliste angezeigt. Wenn kein Kreditor identifiziert wurde, weisen Sie einen Kreditor manuell zu, wie unter [Den mit einem Beleg verknüpften Kreditor ändern](@DC-71#den-mit-einem-beleg-verknupften-kreditor-andern) beschrieben.
4. Wenn es sich um den ersten Beleg handelt, den Sie vom zugewiesenen Kreditor erhalten und importieren, gibt es keine zugehörige Vorlage. Sie müssen daher eine Vorlage zuweisen, indem Sie Felderkennung aktivieren. Wählen Sie in der Aktionsleiste **Start** > **Felder erkennen**. Anschließend werden Suchtexte und Werte für die Felder eingelesen und mit orangefarbenen und blauen Kästchen in der Dokumentenvorschau auf der rechten Seite hervorgehoben.
   > [!NOTE]
   > Wenn Sie zuvor Belege vom zugewiesenen Kreditor erhalten und importiert haben, wird die mit diesem Kreditor verknüpfte Vorlage automatisch zum Erfassen von Feldsuchtexten und -werten verwendet.
5. Wählen Sie in der Aktionsleiste **Dokument** > **Dokumentenkarte** aus, um die Dokumentenkarte zu öffnen.
6. Wählen Sie im Inforegister **Zeilen** für die erste Zeile in der Tabelle das Feld in der Spalte **Nr.** aus. Gehen Sie in der Dokumentenvorschau zu der Zeilenspaltenüberschrift, die dem ausgewählten Feld **Nr.** entspricht (z. B. **Artikel**, **Nummer** oder ähnlich), klicken Sie mit der rechten Maustaste und halten Sie die Taste gedrückt, um ein organgefarbenes Kästchen um die entsprechende Überschrift in der Dokumentenvorschau zu ziehen.
   > [!NOTE]
   >
   > > Wenn das importierte Dokument keine Zeilenspaltenüberschrift enthält, die **Nr.** entspricht, fahren Sie mit dem ersten Feld fort, das eine solche enthält (normalerweise **Beschreibung**). Klicken Sie dann mit der rechten Maustaste, um in der Dokumentenvorschau ein orangefarbenes Kästchen um die Kopfzeile zu zeichnen.
   >
   > Beachten Sie jedoch, dass das Feld **Nr.** normalerweise obligatorisch ist (wie es in der Standardvorlage der Fall ist). Der Beleg kann nicht registriert werden, wenn dieses Feld keinen Wert enthält. In diesem Fall müssen Sie einen Wert in das Feld manuell eingeben. Das Gleiche gilt für alle anderen Felder, die auf der Vorlagenkarte auf **Erforderlich** gesetzt wurden.
7. Wiederholen Sie Schritt 6 für alle Felder, die im Beleg eine passende Spaltenüberschrift haben. Alle Spaltenüberschriften im Zeilenbereich des Belegs sollten nun in der Dokumentenvorschau von orangefarbenen Kästchen umrahmt sein.
8. Wählen Sie in der Aktionsleiste **Start** > **Felder erkennen**. Die Werte unter den umrahmten Spaltenüberschriften werden jetzt automatisch für jede Zeile im Beleg in die entsprechenden Felder im Inforegister **Zeilen** übertragen.
9. Wählen Sie für jede Zeile die relevanten Werte in **Übersetze nach Art** und **Übersetze nach Nr.** aus, damit Document Capture die Kontoreferenzen des Kreditors in intern verwendbare Kontotypen und -nummern übersetzen kann.

   > [!IMPORTANT]
   > Um die Reihenfolge zu ändern, in der die Spalten im Abschnitt **Zeilen** angezeigt werden, wählen Sie in der Aktionsleiste **Vorlage** > **Vorlagenkarte** und verwenden Sie im Abschnitt **Felder** die Aktionen **Nach oben** oder **Nach unten**, um die Position des ausgewählten Felds zu verschieben. Versuchen Sie nicht, die Reihenfolge durch Verschieben von Zeilenspalten mit den Optionen **Einstellungen** > **Personalisieren** auf der **Dokumentenkarte** zu ändern, da hierdurch die Verknüpfung zwischen der ausgewählten Spalte und dem zugehörigen, in der Dokumentenvorschau hervorgehobenen Wert unterbrochen wird. Auch das Personalisieren von Feldspalten, die keine Vorlagen sind, wie beispielsweise **Übersetzen nach Nr.**, unterbricht diese Verknüpfung.

Alle Belegzeilen sind jetzt erfasst und die Zeilenerkennung wurde automatisch für die zugeordnete Vorlage aktiviert.

> [!TIP]
> Sie können die identifizierten Feldwerte und Suchtexte ändern. Weitere Informationen finden Sie unter [Document Capture zum Erkennen von Werten trainieren](@DC-110#document-capture-zum-erkennen-von-werten-trainieren).

## So konfigurieren Sie die Zeilenerkennung

Wenn Sie die Zeilenerkennung für eine Dokumentvorlage wie oben beschrieben aktiviert haben, können Sie diese beliebig konfigurieren. Gehen Sie dazu folgendermaßen vor:

1. Wählen Sie im Belegjournal den Beleg aus, in dessen Vorlage Sie die Zeilenerkennung konfigurieren möchten.
2. Wählen Sie in der Aktionsleiste **Vorlage** > **Vorlagenkarte** aus, um die Vorlagenkarte zu öffnen.
3. Auf dem Inforegister **Allgemein** ist **Zeilen erkennen** automatisch aktiviert, wenn Sie [Zeilenfelder mit der Anleitung oben erfasst](#so-erfassen-sie-zeilenfelder) haben. Wenn Sie noch keine Zeilenfelder erfasst haben, aktivieren Sie **Zeilen erkennen**, um die Zeilenerkennung zu aktivieren. Dadurch werden die folgenden Konfigurationsfelder angezeigt:

   - **Kreditor/Debitor verwendet gleiche Artikelnummern** – aktivieren Sie diese Option, wenn Sie dieselben Artikelnummern wie der Kreditor verwenden.
   - **Erste Tabellenzeile enthält Suchbegriffe** – aktivieren Sie diese Option, wenn die oberste Zeile in der Belegzeilentabelle als Überschrift mit Suchtexten für jede Spalte verwendet werden soll (was normalerweise der Fall ist. Dies ist standardmäßig aktiviert, sobald Sie [Zeilenfelder manuell erfassen](#so-erfassen-sie-zeilenfelder).
   - **Artikelpreise überprüfen** – Wenn diese Option aktiviert ist, vergleicht Document Capture automatisch die Artikelpreise aller erkannten Belegzeilen mit den berechneten Artikelpreisen des Kreditors.

   > [!NOTE]
   > Wenn ein erkannter Preis vom Artikelpreis des Kreditors abweicht, wird im Bemerkungsbereich des Belegjournals eine Warnung angezeigt. Die Preise werden nur überprüft, wenn keine zugehörigen Bestellungen vorliegen. Die Funktion berücksichtigt, ob für die geprüften Artikelnummern spezielle Kreditoreneinkaufspreise oder -rabatte gelten.

   > [!TIP]
   > PDFs sind komplexe Dokumente mit mehreren Ebenen. Wenn Sie beim Verarbeiten einer PDF-Datei in Document Capture auf ungültige Werte feststellen, öffnen Sie die PDF-Datei mit einem modernen Browser, MS Paint oder einem ähnlichen Programm. Sie können sie dann entweder als PDF drucken oder noch einmal als PDF speichern, sodass Document Capture sie korrekt verarbeiten kann. Beachten Sie, dass dies nur für On-Premises-Einrichtungen gilt, da die Cloud-OCR präziser ist.

## Informationen zum Thema

[Mit Papier- und PDF-Belegen arbeiten](@DC-71)\
[Kopffelder in einem Beleg erfassen](@DC-110)