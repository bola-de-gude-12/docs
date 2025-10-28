---
title: Erweiterte Genehmigung einrichten
date: 17-07-2024
description: null
id: DC-31
lang: de
---

# Erweiterte Genehmigung einrichten

Mit der erweiterten Genehmigung können Sie Geschäftsdokumente basierend auf Belegbeträgen und benutzerdefinierten [Dimensionen](https://docs.microsoft.com/de-de/dynamics365/business-central/finance-dimensions) genehmigen. So richten Sie sie ein:

- [Deaktivieren Sie die Standardeinkaufsgenehmigung und aktivieren Sie die erweiterte Genehmigung.](#so-aktivieren-sie-die-erweiterte-genehmigung)
- [Richten Sie erweiterte Genehmigungsgruppen ein.](#so-richten-sie-erweiterte-genehmigungsgruppen-ein)
- [Fügen Sie den erweiterten Genehmigungsgruppen Genehmiger hinzu.](#so-fugen-sie-erweiterten-genehmigungsgruppen-genehmiger-hinzu)

In diesem Artikel werden zur Veranschaulichung Rechnungen verwendet; die Funktionalität kann jedoch auch für Gutschriften verwendet werden.

## So aktivieren Sie die erweiterte Genehmigung

Um die Standardeinkaufsgenehmigung zu deaktivieren und die erweiterte Genehmigung zu aktivieren, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Workflows** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie **Genehmigungsworkflow Einkaufsrechnung** aus, um die Seite **Workflow** zu öffnen.
3. Deaktivieren Sie den Workflow, indem Sie den Schalter **Aktiviert** umschalten, und verlassen Sie dann die Seite, um zur Liste zurückzukehren.
4. Wählen Sie in der Aktionsleiste **Neuer Workflow aus Vorlage** aus.
5. Wählen Sie **Erweiterter Genehmigungsworkflow Einkaufsrechnung** aus, um ihn der Liste der Workflows hinzuzufügen.
6. Aktivieren Sie auf der Seite **Workflow**, die geöffnet wird, den Workflow, indem Sie den Schalter **Aktiviert** umschalten. Verlassen Sie dann die Seite, um zur Liste zurückzukehren.

   > [!NOTE]
   > **Genehmigungsworkflow Einkaufsrechnung** und **Erweiterter Genehmigungsworkflow Einkaufsrechnung** können nicht gleichzeitig aktiviert werden.

## So richten Sie erweiterte Genehmigungsgruppen ein

Um erweiterte Genehmigungsgruppen mit Filtern und Dimensionen einzurichten, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Erw. Genehmigungsgruppe** ein, und wählen Sie dann den zugehörigen Link.

2. Wählen Sie in der Aktionsleiste **Neu** aus, um die Karte **Genehmigungsgruppe** zu öffnen.

3. Geben Sie im Inforegister **Allgemein** unter **Code** den Code ein, den diese Genehmigungsgruppe haben soll. Der Code kann beliebig sein und für Ihr Unternehmen entsprechend gewählt werden.

4. Optional: \*\*Geben Sie unter **Priorität** die Priorität der Genehmigungsgruppe ein. Der ersten erstellten Gruppe wird automatisch der Wert **1** zugewiesen. Wenn Sie mehrere Gruppen haben, wird die Gruppe mit der Priorität **1** zuerst mit den zur Genehmigung gesendeten Rechnungen verknüpft. Beim Erstellen mehrerer Genehmigungsgruppen müssen Filter verwendet werden (siehe Schritt 5).

5. **Optional**: Wenn Sie möchten, dass die Genehmigungsgruppe nur mit Rechnungen verknüpft wird, die bestimmte Filterbedingungen erfüllen, können Sie diese Bedingungen im Inforegister **Filter** angeben. Sie können drei Arten von Filtern hinzufügen, die sich auf verschiedene Teile der Rechnungen beziehen, die zur Genehmigung gesendet werden: Filter, die sich auf Felder im _Einkaufskopf_, auf das Feld _Einkäufer_ oder auf das Feld _Kreditor_ beziehen.

   > [!NOTE]
   > Wenn Sie unter **Einkaufskopf Filter** einen Feldfilter hinzufügen, z. B. **Fälligkeitsdatum=01.08.23**, wird die Genehmigungsgruppe nur mit übereinstimmenden Rechnungen verknüpft, die diesem Filter entsprechen,  also Rechnungen, die am 1. August 2023 fällig sind.

6. **Optional:** Füllen Sie die verbleibenden Felder im Inforegister **Allgemein** nach Bedarf aus:

   1. **Beschreibung:** Gibt die Beschreibung der Genehmigungsgruppe an.

   2. **Erster Posten angelegt durch**: Geben Sie an, wer der erste Genehmiger von Rechnungen sein soll, der mit der Genehmigungsgruppe verknüpft ist. **Einkäufer** bezieht sich auf den Einkäufer auf Rechnungen, die zur Genehmigung gesendet werden. Die **Genehmiger-ID** (die Standardoption) bezieht sich auf den ersten Genehmiger in der Gruppe, der die gleichen Dimensionen wie die erste Rechnungszeile besitzt und ein ausreichendes Genehmigungslimit hat.

   3. **Vier-Augen-Genehmigung**: Geben Sie an, dass mindestens zwei Genehmiger Rechnungen genehmigen müssen, damit sie als vollständig genehmigt gelten (**Rechnung**), oder ob mindestens zwei Genehmiger den Gesamtbetrag der Rechnungen für diese Rechnungen genehmigen müssen, um vollständig genehmigt zu werden (**Rechnungsgesamtbetrag und Dimensionen**).

   > [!NOTE]
   > Beim [Einrichten erweiterter Genehmigungsgruppen](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/setting-up-advanced-approval#so-richten-sie-erweiterte-genehmigungsgruppen-ein) können Sie unter **Erster Posten angelegt durch** > **Einkäufer** auswählen, damit immer der Einkäufer als erster Genehmiger zugewiesen wird. Wenn die **Vier-Augen-Genehmigung** jedoch auf **Rechnungsgesamtbetrag und Dimensionen** anstatt auf **Rechnung** eingestellt ist, zählt der Käufer nicht als einer der beiden erforderlichen Genehmiger.

7. Suchen Sie im Inforegister **Dimensionen** in der Liste der Dimensionen die Dimension(en), die Sie auf diese Genehmigungsgruppe anwenden möchten, und aktivieren Sie dann das bzw. die Kontrollkästchen unter **Aktiv**. Wenn Sie eine oder mehrere Dimensionen obligatorisch machen möchten, aktivieren Sie das/die entsprechende(n) Kontrollkästchen unter **Notwendig**. Beachten Sie, dass Ihnen hier nur die Dimensionen zur Verfügung stehen, die in der **Finanzbuchhaltung Einrichtung** konfiguriert sind.

   > [!IMPORTANT] Wenn Sie eine Dimension obligatorisch machen, muss ihr Wert während des Genehmigungsprozesses in allen Rechnungszeilen vorhanden sein. Andernfalls wird der Genehmigungsablauf angehalten und eine Fehlermeldung angezeigt. Die Funktion **Notwendig** wird hauptsächlich verwendet, wenn Sie mit mehreren Dimensionen arbeiten.

   > [!TIP]
   > Weitere Informationen zu Dimensionen, zum Beispiel zum Hinzufügen neuer Dimensionen, finden Sie im Microsoft-Artikel [Arbeiten mit Dimensionen](https://docs.microsoft.com/de-de/dynamics365/business-central/finance-dimensions).

## So fügen Sie erweiterten Genehmigungsgruppen Genehmiger hinzu

Sobald Sie eine erweiterte Genehmigungsgruppe [wie oben beschrieben](#so-richten-sie-erweiterte-genehmigungsgruppen-ein) erstellt haben, müssen Sie dieser Benutzer (das heißt Genehmiger) hinzufügen. Gehen Sie dazu folgendermaßen vor:

1. Öffnen Sie die Karte **Genehmigungsgruppen** der relevanten Gruppe (sofern sie nicht bereits geöffnet ist): Wählen Sie das Symbol {{search}}, geben Sie **Erw. Genehmigungsgruppe** ein, wählen Sie den entsprechenden Link, und wählen Sie dann die entsprechende Genehmigungsgruppe in der Liste aus.
2. Wählen Sie in der Aktionsleiste **Benutzer** aus, um die Seite **Erw. Genehmigungsbenutzer** zu öffnen.
3. Wählen Sie in der Liste unter **Name** die drei Punkte auf der rechten Seite aus, um die Liste **Continia Benutzer** zu öffnen, und wählen Sie dann den Benutzer aus, den Sie der Gruppe als Genehmiger hinzufügen möchten. Wählen Sie **OK**, um die Benutzerliste zu schließen.
4. Geben Sie unter **Genehmigungsgrenzwert** das Genehmigungslimit des Genehmigers ein.
5. Gehen Sie für jede der verbleibenden Listenspalten wie folgt vor:
   1. Wählen Sie das Feld aus, um die Seite zum Bearbeiten der **Dimensionsauswahl Genehmigungsbenutzer** zu öffnen.
      > [!NOTE]
      > Die Spalten der Liste stellen die Dimension(en) dar, die Sie beim Einrichten auf die Genehmigungsgruppe angewendet haben, und sie variieren entsprechend (siehe Schritt 7 in der Anleitung oben [So richten Sie erweiterte Genehmigungsgruppen ein](#so-richten-sie-erweiterte-genehmigungsgruppen-ein)). Wenn Sie beispielsweise beim Einrichten der Genehmigungsgruppe die Dimension **Abteilung Code** angewendet haben, wird diese als Spalte auf der Seite **Erw. Genehmigungsbenutzer** angezeigt.
   2. Wählen Sie in der Liste der Dimensionswerte den Wert aus, den Sie dem Genehmiger hinzufügen möchten, und aktivieren Sie dann das Kontrollkästchen unter **Genehmigungsberechtigung**, um diesen hinzuzufügen. Wählen Sie **Schließen**, um die Seite zu schließen und zur Seite **Erw. Genehmigungsbenutzer** zurückzukehren.
6. Wiederholen Sie Schritte 3–5 für alle weiteren Genehmiger, die Sie der Genehmigungsgruppe hinzufügen möchten.

Immer wenn eine Rechnung zur Genehmigung gesendet wird, erstellt Document Capture einen Genehmigungsposten. Diesem wird der Genehmiger aus der Genehmigungsgruppe zugewiesen, der über das niedrigste Genehmigungslimit verfügt (aber ausreichend, um als erster Genehmiger zu genehmigen) und die gleiche Kombination von Dimensionswerten wie mindestens eine der Rechnungszeilen besitzt. Wenn der erste Genehmiger alle relevanten Zeilen genehmigt hat, aber nicht über ein ausreichendes Genehmigungslimit verfügt, um _alle_ Rechnungszeilen zu genehmigen, weist Document Capture dann den nächsten Genehmiger in derselben Genehmigungsgruppe zu, der über ein höheres Genehmigungslimit verfügt, und es wird ein neuer Genehmigungsposten erstellt. Dieser Vorgang wird wiederholt, bis alle Rechnungszeilen genehmigt wurden.

## Informationen zum Thema

[Erweiterte Genehmigung](@DC-38)\
[Arbeiten mit Dimensionen](https://docs.microsoft.com/de-de/dynamics365/business-central/finance-dimensions) (Microsoft-Artikel)
