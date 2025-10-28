---
title: Emissionen in Document Capture verfolgen
date: 28-03-2025
description: So verfolgen Sie Treibhausgasemissionen in Document Capture.
id: DC-232
lang: de
---

# Emissionen in Document Capture mit Continia Sustainability verfolgen

Dieser Artikel beschreibt die Integration zwischen Continia Document Capture und Continia Sustainability, was es Ihnen ermöglicht, die Treibhausgasemissionen (THG) Ihres Unternehmens in Microsoft Dynamics 365 Business Central zu verfolgen.

In Document Capture erfasste emissionsbezogene Daten können in Ihre Umwelt-Buch.-Blätter in Continia Sustainability importiert werden, wo Sie auch das Herkunftsdokument eines bestimmten Datenpunkts überprüfen können. Weitere Informationen zu Umwelt-Buch.-Blättern finden Sie unter [Mit Umwelt-Buch.-Blättern arbeiten](@CS-34).

## Continia Sustainability-Vorlagenfelder

Sobald Continia Sustainability in einer Umgebung aktiviert ist, in der Document Capture bereits aktiv ist (oder umgekehrt), werden die folgenden Kopf- und Zeilenfelder in allen Mastervorlagen in der Einkaufskategorie verfügbar gemacht:

- **Umweltkontotyp** – wichtige Geschäftsbereiche und zugehörige Aktivitäten. Beispielsweise Anlage.

   > [!NOTE]
   > Wenn das Feld **Umweltkontotyp** in einem Sachkonto oder Artikel einen anderen Wert als leer hat, werden die folgenden Felder validiert. Wenn ein Wert in einem dieser Felder Aufmerksamkeit erfordert, wird im Abschnitt **Bemerkungen** im Belegjournal und auf der Dokumentenkarte ein konfigurierbarer Kommentar angezeigt.

- **Umweltkonto-Nr.** – die Nummer des Umweltkontos, das sich auf die Art der Emissionsaktivität bezieht. Beispiel: 10110 (Strom).

- **Emissionsart** – häufige Emissionsquellen im Zusammenhang mit den Aktivitäten eines Unternehmens. Beispielsweise Elektrizität oder Heizung.

- **Emissionscode** – der der jeweiligen Emissionsart zugewiesene Code. Beispielsweise EL-UK für den Typ „Elektrizität“.

- **Emissionseinheitenart** – die mit dem Emissionstyp verbundene Maßeinheit. Beispielsweise Energie oder Entfernung.

- **Emissionseinheitencode** – der Code der Maßeinheit, die dem Emissionstyp zugeordnet ist. Beispielsweise KWH (Kilowattstunde) oder KCAL (Kilokalorie).

- **Emissionsmenge** – die tatsächliche Menge in Bezug auf die Emission. Beispielsweise 100 (Meilen oder MI), 25 (Kilowattstunde oder KWH), etc.

- **Gesamte Emission Menge** – das Ergebnis des Werts im Feld **Emissionsmenge** multipliziert mit der Menge des zugehörigen Artikels. Wenn Sie beispielsweise 20 Packungen Kopierpapier gekauft haben, beträgt die gesamte Emissionsmenge 20 multipliziert mit der dem Artikel zugewiesenen Emissionsmenge, beispielsweise seinem Gewicht.

   > [!NOTE]
   > Wenn Sie einem Artikel bereits Umweltdaten hinzugefügt haben, beispielsweise ein Gewicht oder eine andere Kennzahl, lassen Sie das Feld **Gesamte Emission Menge** leer, wenn Sie die Continia Sustainability-Felder auf Zeilenebene ausfüllen.

Sie können diese Felder in einem Sachkonto, auf einer Artikelkarte oder direkt in einer Vorlage konfigurieren. Alle drei Methoden werden in diesem Artikel behandelt.

> [!NOTE]
> Unabhängig davon, wie Sie die Continia Sustainability-Felder konfigurieren, müssen Sie einen Wert für das Feld **Emissionsmenge** eingeben oder erfassen. Erst dann kann die Emission mit dem entsprechenden [Emissionsfaktor](@CS-22) berechnet werden.

### So konfigurieren Sie Continia Sustainability-Felder in einer Vorlage

Bevor Sie Continia Sustainability-Felder in einer Vorlage konfigurieren können, müssen Sie sie der Vorlage hinzufügen:

1. Wählen Sie das Symbol {{search}}, geben Sie **Belegkategorien** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Code **EINKAUF** aus, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, dessen Vorlage Sie die Continia Sustainability-Felder hinzufügen möchten.
4. Wählen Sie in der Aktionsleiste **Vorlage** > **Vorlagenfelder hinzufügen**.
5. Wählen Sie die Felder aus, die Sie der Vorlage hinzufügen möchten, und klicken Sie dann auf **OK**.

Sie können diese Felder dann entweder manuell mit den entsprechenden Werten füllen oder diese Informationen manuell aus dem Beleg erfassen.

### So konfigurieren Sie Continia Sustainability-Felder in einem Sachkonto

So konfigurieren Sie Continia Sustainability-Felder in einem Sachkonto:

1. Wählen Sie das Symbol {{search}}, geben Sie **Kontenplan** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie das Konto aus, das Sie konfigurieren möchten.
3. Weisen Sie im Inforegister **Umweltbuchhaltung** den Feldern **Umweltkontotyp** und **Umweltkonto-Nr.** Werte zu. Beispielsweise Anlage und 10110.
4. Die Felder **Emissionstyp**, **Emissionscode**, **Emissionseinheitentyp** und **Emissionseinheitencode** werden automatisch ausgefüllt.

[Sobald die Continia Sustainability-Felder zu einer Vorlage hinzugefügt wurden](#so-konfigurieren-sie-continia-sustainability-felder-in-einer-vorlage), werden deren Werte automatisch basierend auf dem vorkonfigurierten Sachkonto ausgefüllt, wenn Sie die **Art** und die **Nr.** im Belegkopf auswählen. Dasselbe lässt sich durch die Eingabe eines Sachkontos in **Buchungseinrichtung** erreichen. Sie müssen allerdings nach der Eingabe der Werte derzeit **Start** > **Felder erkennen** auswählen.

Wenn Sie Zeilenerkennung verwenden, konfigurieren Sie die Felder **Übersetze nach Art** und **Übersetze nach Nr.**, um die Standardwerte aus Sachkonten oder Artikeln auf die zugehörigen Zeilenfelder der Vorlage anzuwenden. Alternativ geben Sie die erforderlichen Werte direkt in die Felder der Vorlagenzeile ein.

### So konfigurieren Sie Continia Sustainability-Felder auf einer Artikelkarte

So konfigurieren Sie Continia Sustainability-Felder auf einer Artikelkarte:

1. Wählen Sie das Symbol {{search}}, geben Sie **Artikel** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie die Nummer des Artikels aus, den Sie konfigurieren möchten. Beispielsweise 1920-S.
3. Weisen Sie im Inforegister **Umweltbuchhaltung** den Feldern **Umweltkontotyp** und **Umweltkonto-Nr.** Werte zu. Beispielsweise Waren und Dienstleistungen und 10003.
4. In diesem Fall werden nur die Felder **Emissionseinheitstyp** und **Emissionseinheitscode** automatisch ausgefüllt. Anschließend können Sie einen Wert für die **Emissionsmenge** eingeben, sofern dieser immer gleich ist. Andernfalls fügen Sie jedem Beleg die entsprechenden Werte hinzu.

[Sobald die Continia Sustainability-Felder zu einer Vorlage hinzugefügt wurden](#so-konfigurieren-sie-continia-sustainability-felder-in-einer-vorlage), werden deren Werte automatisch basierend auf der vorkonfigurierten Artikelkarte ausgefüllt, wenn Sie die **Art** und die **Nr.** im Belegkopf auswählen. Dasselbe lässt sich durch die Eingabe eines Artikels in **Buchungseinrichtung** erreichen. Sie müssen allerdings nach der Eingabe der Werte derzeit **Start** > **Felder erkennen** auswählen.

> [!NOTE]
> Derzeit werden Continia Sustainability-Felder aufgrund eines Fehlers in einigen Fällen nicht automatisch auf Zeilenebene ausgefüllt. Möglicherweise müssen Sie daher den Wert unter **Art** oder **Übersetze nach Nr.** im Belegjournal oder auf der Dokumentenkarte erneut eingeben, bevor die Continia Sustainability-Felder ausgefüllt werden.

Wenn Sie Zeilenerkennung verwenden, konfigurieren Sie die Felder **Übersetze nach Art** und **Übersetze nach Nr.**, um die Standardwerte aus Sachkonten oder Artikeln auf die zugehörigen Zeilenfelder der Vorlage anzuwenden. Alternativ geben Sie die erforderlichen Werte direkt in die Felder der Vorlagenzeile ein.

## So importieren Sie emissionsbezogene Daten in Continia Sustainability

Wenn Sie Belege mit Emissionsdaten buchen, stehen diese Daten Continia Sustainability zur Verfügung. Weitere Informationen finden Sie unter [Emissionsbezogene Zeilen aus Belegzeilen importieren](@CS-53).

## Informationen zum Thema

[Einen Emissionsfaktorsatz erstellen](@CS-74)\
[Grundlegende Konzepte in Continia Sustainability](@CS-58)\
[Continia Sustainability und Document Capture](@CS-78)\
[Der Konfigurations-Assistent für Continia Sustainability](@CS-80)\
[Einen vordefinierten Emissionsfaktorsatz von Continia hinzufügen](@CS-94)