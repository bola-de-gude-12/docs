---
title: Feldübersetzungen in Document Capture verwenden
date: 14-05-2025
description: So verwenden Sie die Feldübersetzungsfunktion in Document Capture.
id: DC-460
lang: de
---

# Feldübersetzungen verwenden

Feldübersetzungen bieten Unterstützung bei Werten, die entweder schwer zu erfassen wären oder manuelle Arbeit erfordern. Dies ist eine der einfachsten und dennoch flexibelsten Funktionen in Continia Document Capture. Wenn Sie diese beherrschen, können Sie sich viel Zeit und Mühe sparen.

Die Funktion zur Feldübersetzung konvertiert erfasste Werte für das Feld, in dem sie konfiguriert ist, in andere Werte – oder in gar keine Werte, wobei der erfasste Wert entweder ganz oder teilweise entfernt wird. Das Entfernen von Teilen erfasster Werte ist ein so häufiges Szenario, dass Felder wie **Betrag inkl. MwSt.** standardmäßig so konfiguriert sind, dass bestimmte Währungssymbole und Sonderzeichen entfernt werden.

<a href="/images/DC/DocumentsAndTemplates/Field translations A.png" target="_blank">
</images/DC/DocumentsAndTemplates/Field translations A.png" alt="Field translations">
</a>

## So verwenden Sie Feldübersetzungen

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie den Code der entsprechenden Belegkategorie, zum Beispiel **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Liste der Dokumente das Dokument aus, mit dem Sie arbeiten möchten.
4. Wählen Sie auf dem Inforegister **Belegkopf** oder **Zeilen** die drei Punkte neben dem Feld aus, auf das Sie Feldübersetzungen anwenden möchten.
5. Geben Sie im Inforegister **Feldübersetzungen** in der Spalte **Übersetze von** den Wert ein, den Sie übersetzen möchten.
6. Geben Sie in der Spalte **Übersetze nach** den gewünschten Ergebniswert ein. Wenn Sie dieses Feld leer lassen, wird der unter **Übersetzen von** eingegebene Wert entfernt.
7. Wenn die Feldübersetzung nur erfolgen soll, wenn die Groß-/Kleinschreibung der erfassten Werte mit der unter **Übersetze von** eingegebenen Groß-/Kleinschreibung übereinstimmt, aktivieren Sie das Kontrollkästchen **Groß-/Kleinschreibung beachten**. Zum Beispiel: Hazel, aber nicht HAZEL.

## So verwenden Sie einen Platzhalter in Feldübersetzungen

Ähnlich wie bei der [Verwendung von Regeln](@DC-245) ist es möglich, das Sternchen ( \* ) als Platzhalter in Feldübersetzungen zu verwenden. Dadurch können Sie die Daten vor und/oder nach einer bestimmten Zahl, einem Begriff oder einem Sonderzeichen übersetzen – auch wenn diese Daten variieren oder Ihnen unbekannt sind.

Wenn beispielsweise nur die ersten sechs Ziffern der Rechnungsnummer 555002-20250723 für Sie relevant sind, verwenden Sie das Platzhalterzeichen mit einem vorangestellten Bindestrich (z. B.: -\*), um die unerwünschten Daten in einen leeren Wert zu übersetzen. In diesem Beispiel wäre das Ergebnis der Übersetzung 555002.

<a href="/images/DC/DocumentsAndTemplates/Field translations B.png" target="_blank">
</images/DC/DocumentsAndTemplates/Field translations B.png" alt="Wildcards in field translations">
</a>
