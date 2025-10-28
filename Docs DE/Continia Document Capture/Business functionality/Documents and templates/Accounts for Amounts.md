---
title: Buchungseinrichtung
date: 08-07-2025
description:
id: DC-149
lang: de
---

# Buchungseinrichtung

Auf der Seite **Buchungseinrichtung** können Sie angeben, welche Konten als Buchungsvorschläge für die Kopfbetragsfelder verwendet werden sollen, die in Ihren eingehenden Belegen erfasst werden. Die auf der Seite aufgelisteten Kopfzeilenfelder werden von Continia Document Capture automatisch angezeigt. Nur Kopfzeilenfelder, die als Betragsfelder kategorisiert werden, werden hier angezeigt, d. h. keine Textfelder, Datumsfelder oder andere Feldtypen.

Wenn beispielsweise **Betrag ohne MwSt.** in der Tabelle der Betragsfelder angezeigt wird, können Sie festlegen, dass dieses Feld für die angegebene Dokumentvorlage in eine bestimmte Sachkontonummer (z. B. **34100**) übersetzt wird ( d. h. dieser zugeordnet wird). Wenn ein importierter Beleg dann dieser Vorlage zugeordnet wird und ein Betrag im Feld **Betrag ohne MwSt.** für diesen Beleg erfasst wird, wird die von Ihnen angegebene Sachkontonummer 34100 automatisch für jede Einkaufs- oder Verkaufszeile vorgeschlagen, die mit dem erfassten Betrag erstellt wird.

## So richten Sie die Buchungseinrichtung ein

Um festzulegen, welche Konten als Buchungskonten für die in Ihren Eingangsbelegen erfassten Beträge vorgeschlagen werden sollen, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie den Code der entsprechenden Belegkategorie, zum Beispiel **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, dessen Vorlage Sie bearbeiten möchten.
4. Klicken Sie in der auf Aktionsleiste **Vorlage** > **Buchungseinrichtung**, um die Seite **Buchungseinrichtung** zu öffnen.
5. Gehen Sie in der Tabelle in die Zeile des Betragsfeldes, dessen Kontozuordnung Sie bearbeiten möchten.
6. Füllen Sie für die ausgewählte Zeile die Tabellenfelder nach Bedarf aus. Das erste Tabellenfeld (in der Spalte **Feld**) stellt das Belegfeld dar, das den erfassten Betrag enthält, den Sie einem bestimmten Kontotyp, einer Kontonummer usw. zuordnen möchten, wenn für diesen Betrag Einkaufs- oder Verkaufszeilen erstellt werden. Geben Sie für die übrigen Tabellenfelder genau an, welchen Werten Sie den erfassten Betrag zuordnen möchten:
   - **Übersetze nach Art**: Wählen Sie den Kontotyp aus, dem Sie den erfassten Betrag zuordnen möchten.
   - **Übersetze nach Nr.**: Wählen Sie die Kontonummer aus, der Sie den erfassten Betrag zuordnen möchten.
   - **MwSt.-Produktbuchungsgruppe**: Wählen Sie die Mehrwertsteuer-Produktbuchungsgruppe aus, der Sie den erfassten Betrag zuordnen möchten. Dadurch können Sie die standardmäßige Mehrwertsteuer-Produktbuchungsgruppe überschreiben.
   - **Übersetze nach MwSt. Gesch. Buchung Gruppe**: Wählen Sie die Mehrwertsteuer-Geschäftsbuchungsgruppe aus, der Sie den erfassten Betrag zuordnen möchten. Dadurch können Sie die standardmäßige Mehrwertsteuer-Geschäftsbuchungsgruppe überschreiben.
   - **[Globale Dimensionen 1 und 2]**: Wählen Sie den bzw. die Dimensionswert(e) aus, den/die Sie dem erfassten Betrag zuweisen möchten. Dadurch können Sie die Standarddimensionswerte des Kontotyps und der Kontonummer überschreiben.
   > [!NOTE]
   > Standardmäßig werden nur die beiden vorkonfigurierten globalen Dimensionen als Spalten in der Tabelle angezeigt, und Sie können nur Werte für diese beiden Dimensionen direkt in der Tabelle hinzufügen und anzeigen. Sie können jedoch problemlos weitere Dimensionen und Werte mit den folgenden Schritten hinzufügen: Wählen Sie die entsprechende Zeile aus, wählen Sie **Zugehörig** > **Zeile** > **Dimensionen**, um die Seite **Zeilendimensionen** zu öffnen. Wählen Sie dann einen Dimensionscode und einen Dimensionswertcode in der Tabelle aus. Hinweis: Obwohl diese zusätzlichen Dimensionen und Werte hinzugefügt werden, werden sie standardmäßig nicht in der Tabelle **Buchungseinrichtung** angezeigt. Um sie in dieser Tabelle sichtbar zu machen, müssen Sie [die Tabelle anpassen](#so-passen-sie-die-tabelle-an).
   - **Abgrenzungscode**: Wählen Sie den Abgrenzungscode aus, dem Sie den erfassten Betrag zuordnen möchten.
7. Wiederholen Sie Schritte 5–6 für alle weiteren Betragsfelder, deren Kontozuordnungseigenschaften Sie bearbeiten möchten.

## So passen Sie die Tabelle an

Wie oben erwähnt, werden standardmäßig nur die beiden globalen Dimensionen als Spalten in der Tabelle der Betragsfelder auf der Seite **Buchungseinrichtung** angezeigt. Sie können die Tabelle jedoch problemlos anpassen, indem Sie ihr zusätzliche Dimensionsspalten hinzufügen. [Personalisieren Sie dazu die Seite](https://docs.microsoft.com/de-de/dynamics365/business-central/ui-personalization-user), indem Sie die folgenden Schritte ausführen:

1. Klicken Sie auf das Symbol **Einstellungen** {{settings}} > **Personalisieren**.
2. Klicken Sie in der oberen linken Ecke auf **+ Feld**, um den Bereich **Feld der Seite hinzufügen** zu öffnen.
3. Ziehen Sie das/die relevante(n) Dimensionsfeld(er) aus dem Bereich in den Tabellenkopf.
4. Klicken Sie auf **Fertig**, um das Banner **Personalisierung** zu schließen.

Die neuen Dimensionsspalten werden der Tabelle anschließend hinzugefügt. Möglicherweise müssen Sie die Seite aktualisieren, damit die Dimensionen sichtbar werden.

> [!TIP]
> Die Dimensionsfelder **Einheitencode** und **Variantencode** können in der Tabelle besonders relevant sein, da Betragsfelder manchmal bestimmten Artikelvarianten (z. B. Farben) oder bestimmten Mengeneinheiten (z. B. Packungen statt Paletten) zugeordnet werden müssen.

## Informationen zum Thema

[Betragsverteilungscodes verwenden](@DC-118)
