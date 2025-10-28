---
title: Continia Sustainability mit Expense Management integrieren
date: 14-10-2024
description: null
id: EM-265
lang: de
---

# Continia Sustainability mit Expense Management integrieren

Wenn Continia Sustainability in Ihrem Unternehmen installiert ist, können Sie von der Integration mit Continia Expense Management profitieren. Durch eine solche Integration kann Continia Sustainability auf Grundlage der von Expense Management erfassten Daten CO2-Emissionsberechnungen durchführen und Ihnen so dabei helfen, Ihre Umweltauswirkungen zu verfolgen. Sobald Sie Continia Sustainability installiert haben, stehen Ihnen in Expense Management automatisch Funktionen für diese Lösung zur Verfügung. Diese werden unter [Nachhaltigkeitsspezifische Funktionalität in Expense Management](#nachhaltigkeitsspezifische-funktionalitat-in-expense-management) beschrieben.

Wenn Sie Continia Sustainability zunächst im Testmodus installiert haben, können Sie Ihre Testdaten an die Anforderungen Ihres Unternehmens anpassen und dann die angepassten Daten in Ihrer Produktionsumgebung einsetzen. Dies ist die empfohlene Vorgehensweise.

> [!TIP]
> Um die Einrichtungszeit zu minimieren, empfiehlt Continia dringend, dass Sie Ihre Testdaten an Ihre Geschäftsanforderungen anpassen und diese Daten dann mithilfe der Konfigurationsdatei in Ihre Produktionsumgebung exportieren. Andernfalls müssen Sie alle Einstellungen manuell einrichten, was sehr zeitaufwändig sein kann.

Möglicherweise gibt es Gründe dafür, dass Sie die obige Empfehlung nicht berücksichtigen. Wenn dies der Fall ist, müssen Sie Continia Sustainability von Grund auf mit Expense Management verknüpfen, indem Sie alle erforderlichen Felder, Feldabhängigkeiten und Buchungseinrichtungen manuell erstellen. Weitere Informationen hierzu finden Sie weiter unten unter [Continia Sustainability mit Expense Management ohne Verwendung von Testdaten verknüpfen](#continia-sustainability-mit-expense-management-ohne-verwendung-von-testdaten-verknupfen).

## Nachhaltigkeitsspezifische Funktionalität in Expense Management

Wenn Continia Sustainability installiert wurde, werden automatisch einige Änderungen an der Expense Management-App vorgenommen. Diese Änderungen betreffen die Seiten **Belegarten**, **Expense Buchungseinrichtung** und **Konfigurierte Felder**:

- Auf der Seite **Belegarten** wird die neue Spalte **Abhängigkeit Continia Sustainability** hinzugefügt.
- Auf der Seite **Expense Buchungseinrichtung** werden die zwei neuen Spalten **Umweltkontotyp** und **Umweltkonto-Nr.** hinzugefügt.
- Auf der Seite **Konfigurierte Felder** wird ein erweiterter Satz von Feldtypen hinzugefügt.

Diese Spalten und Feldtypen verknüpfen die Buchungsfunktion von Continia Sustainability mit Expense Management und liefern Continia Sustainability die notwendigen Daten zur Berechnung der CO2-Emissionen.

## Continia Sustainability mit Expense Management ohne Verwendung von Testdaten verknüpfen

Continia empfiehlt dringend, zunächst eine Testumgebung einzurichten und dann die Testdaten aus dieser Umgebung in die neue Produktionsumgebung zu exportieren, wie in der Einleitung oben erwähnt.

Für Testumgebungen hat Continia eine Einrichtung mit Daten für bestimmte Belegarten vorbereitet, die so konfiguriert sind, dass bei Auswahl der jeweiligen Belegart durch einen Expense-Benutzer zusätzliche Informationen angefordert werden. Die Testdaten hängen von der ausgewählten Lokalisierung ab, da Lokalisierungseinstellungen (wie Umweltkonten und Emissionsarten) meist auf den Emissionsfaktorsätzen basieren, die im jeweiligen Land verwendet oder von der jeweiligen nationalen Regierung bereitgestellt werden.

Wenn Sie in Ihrer Produktionsumgebung keine Testdaten verwenden möchten, müssen Sie Continia Sustainability von Grund auf manuell mit Expense Management verknüpfen. Hierfür gibt es zwei Möglichkeiten:

- [Mit der **Expense Buchungseinrichtung**](#so-verknupfen-sie-die-losungen-mithilfe-der-expense-buchungseinrichtung)
- [Mit der Funktion **Continia Sustainability Abhängigkeit**](#so-verknupfen-sie-die-losungen-mithilfe-von-continia-sustainability-abhangigkeit)

Nachfolgend finden Sie Informationen zu beiden Methoden.

### So verknüpfen Sie die Lösungen mithilfe der Expense Buchungseinrichtung

Mit der **Expense Buchungseinrichtung** können Sie Continia Sustainability manuell mit Expense Management verknüpfen. Diese Seite hat zwei neue Spalten, **Umweltkontotyp** und **Umweltkonto-Nr.**, die Sie ausfüllen müssen, um mit der Erfassung der CO2-Emissionen aus Mitarbeiterbelegen zu beginnen.

Um beispielsweise eine neue Belegart für Taxikosten zu erstellen, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Belegarten** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Aktionsleiste **Neu** aus, um eine neue Zeile in der Tabelle zu erstellen.
3. Geben Sie in der Spalte **Code** einen relevanten Code für die Belegart ein, beispielsweise **REISE-TAXI**.
4. Geben Sie in der Spalte **Beschreibung** eine relevante Beschreibung für die Belegart ein, beispielsweise **Reise (Taxi)**.
   > [!NOTE]
   > Weitere Informationen zum Einrichten neuer Belegarten finden Sie unter [Belegarten einrichten](@EM-41).
5. Wählen Sie in der Aktionsleiste **Einrichtung**, um die Seite **Expense Buchungseinrichtung** zu öffnen.
6. Wählen Sie in der Spalte **Buchungskontoart** die Option **Sachkonto** aus.
7. Wählen Sie in der Spalte **Buchungskonto Nr.** die Nummer des Kontos aus, das Sie für diese Belegart verwenden möchten.
8. Wählen Sie in der Spalte **Umweltkontotyp** den Kontotyp aus, den Sie verwenden möchten, beispielsweise **Geschäftsreisen**.
9. Wählen Sie in der Spalte **Umweltkonto-Nr.** die Nummer des Kontos aus, das verwenden möchten.

Sie haben jetzt die Buchung in Continia Sustainability für die Belegart **REISE-TAXI** eingerichtet. Das bedeutet, dass immer dann, wenn ein Expense-Benutzer einen Beleg mit der Belegart **REISE-TAXI** erstellt, dieser Beleg automatisch in Continia Sustainability gebucht wird.

### So verknüpfen Sie die Lösungen mithilfe von Continia Sustainability Abhängigkeit

Die Funktion **Continia Sustainability Abhängigkeit** ermöglicht es Ihnen, zusätzliche Felder zu konfigurieren, die angezeigt werden, wenn Expense-Benutzer Belege in der Expense App oder im Expense Portal erstellen.

Um beispielsweise eine neue Continia Sustainability-Abhängigkeit für Hotelkosten zu erstellen, bei denen die Emissionsfaktoren von Land zu Land unterschiedlich sind, gehen Sie wie folgt vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Belegarten** ein, und wählen Sie dann den zugehörigen Link.

2. Wählen Sie in der Aktionsleiste **Liste bearbeiten** aus.

3. Öffnen Sie in der Spalte **Abhängigkeit Continia Sustainability** das Dropdown-Menü für die Belegart aus, für die Sie die Abhängigkeit erstellen möchten – in diesem Fall **HOTEL** – und wählen Sie dann **HOTEL COUNTRY** aus.

4. Wählen Sie das Symbol {{search}}, geben Sie **Konfigurierte Felder** ein, und wählen Sie dann den zugehörigen Link.

5. Markieren Sie in der Tabelle unten eine leere Zeile und wählen Sie anschließend aus der sich öffnenden Liste **HOTEL COUNTRY** aus. Aktivieren Sie in der Spalte **Sichtbarkeit standardmäßig ausblenden** das Kontrollkästchen.

6. Markieren Sie in der Tabelle unten eine leere Zeile und wählen Sie anschließend aus der sich öffnenden Liste **NUMBER OF NIGHTS** aus. Aktivieren Sie in der Spalte **Sichtbarkeit standardmäßig ausblenden** das Kontrollkästchen.

7. Suchen Sie in der Tabelle in der Spalte **FELD CODE** nach **EXPENSE TYPE** und wählen Sie dann das Feld in der Spalte **Feldabhängigkeiten** aus, um die Seite **Feldtypabhängigkeiten** zu öffnen.

8. Wählen Sie in der Aktionsleiste **Neu** aus, um eine Abhängigkeit (Hotel Land) mit der Belegart **HOTEL** zu verknüpfen, und nehmen Sie dann die folgende Auswahl für die neue Zeile vor:

   <br>

   | Bedingung                 | Wert  | Referenzfeld Typ Code | Erwartung             |
   | ------------------------- | ----- | --------------------- | --------------------- |
   | Hat einen bestimmten Wert | HOTEL | HOTEL LAND            | Muss einen Wert haben |

   <br>

9. Wählen Sie in der Aktionsleiste **Neu** aus, um eine weitere Abhängigkeit (Anzahl der Nächte) mit der Belegart **HOTEL** zu verknüpfen, und nehmen Sie dann die folgende Auswahl für die neue Zeile vor:

   <br>

   | Bedingung                 | Wert  | Referenzfeld Typ Code | Erwartung             |
   | ------------------------- | ----- | --------------------- | --------------------- |
   | Hat einen bestimmten Wert | HOTEL | NUMBER OF NIGHTS      | Muss einen Wert haben |

Sie haben jetzt Feldabhängigkeiten für die Belegart **HOTEL** eingerichtet. Das bedeutet, dass Expense-Benutzer aufgefordert werden, zusätzliche Details für **HOTEL COUNTRY** und **NUMBER OF NIGHTS** hinzuzufügen, wenn sie Belege in der Expense App oder im Expense Portal erstellen.
