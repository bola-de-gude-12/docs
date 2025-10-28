---
title: Betragsverteilungscodes in Document Capture verwenden
date: 07-07-2025
description: So verwenden Sie Betragsverteilungscodes in Document Capture.
id: DC-118
lang: de
---

# Betragsverteilungscodes verwenden

Ein Betragsverteilungscode ist ein Code, der den Betrag eines Belegs automatisch auf mehrere Zeilen verteilt, wenn der Beleg in Microsoft Dynamics 365 Business Central Ihren Einstellungen entsprechend erstellt wird. Mit diesen Codes können Sie festlegen, wie der Betrag einer eingehenden Rechnung oder Gutschrift bei der Belegerstellung in Zeilen aufgeteilt werden soll und welche Konten, Beträge und Dimensionen auf jede neu erstellte Belegzeile angewendet werden sollen. Der Betrag jeder Belegzeile kann entweder ein fester Betrag oder ein Prozentsatz des erkannten Belegbetrags sein, je nachdem, wie Sie dies definiert haben.

> [!NOTE]
> Betragsverteilungscodes werden normalerweise auf den Gesamtbetrag des Belegs angewendet (wenn die Zeilenerkennung nicht aktiviert ist). Gegebenenfalls können Sie sie auch auf jedes andere Betragsfeld anwenden.

Informationen zum Einrichten von Betragsverteilungscodes finden sie unter [So erstellen Sie Betragsverteilungscodes](#so-erstellen-sie-betragsverteilungscodes) weiter unten.

Sobald Sie einen oder mehrere Betragsverteilungscodes eingerichtet haben, können diese auf Belege angewendet werden. Betragsverteilungscodes können mit den folgenden Methoden angewendet werden:

 - [Automatische Anwendung mit einer Dokumentvorlage](#so-wenden-sie-betragsverteilungscodes-mit-einer-vorlage-an)
 - [Manuelle Anwendung im Belegjournal](#so-wenden-sie-betragsverteilungscodes-manuell-bei-der-registrierung-an) bei der Belegregistrierung
 - [Aktivierung im jeweiligen Beleg nach der Registrierung](#betragsverteilungscodes-in-registrierten-belegen-aktivieren), entweder direkt in Business Central oder über das Continia Web Approval Portal

## So erstellen Sie Betragsverteilungscodes

1. Suchen Sie {{search}} nach **Standard Betragsverteilungscodes** und wählen Sie den entsprechenden Link aus.

2. Klicken Sie in der Aktionsleiste auf **Liste bearbeiten**.

3. Wählen Sie in der Tabelle eine leere Zeile aus und geben Sie dann in der Spalte **Code** den Namen des Codes ein, den Sie erstellen möchten.

4. **Optional**: Geben Sie in der Spalte **Beschreibung** eine Beschreibung des Codes ein, den Sie erstellen.

5. Wählen Sie in der Spalte **Aktiviert für Einkauf** eine der folgenden Optionen aus:
    - **Ja für alle Kreditoren**, wenn der Code auf alle eingehenden Belege angewendet werden soll.
    - **Ja für ausgewählte Kreditoren**, wenn der Code nur auf Belege bestimmter Kreditoren angewendet werden soll.

6. Wenn Sie oben in Schritt 5 **Ja für ausgewählte Kreditoren** ausgewählt haben, klicken Sie in der Aktionsleiste auf **Kreditoren**. Wählen Sie auf der Seite, die geöffnet wird, in der Tabellenspalte **Kreditorennr.** einen Kreditor aus, auf dessen Belege der Code angewendet werden soll. Gehen Sie zu einer neuen Zeile und wiederholen Sie den Vorgang für alle weiteren Kreditoren. Schließen Sie dann die Seite, um zur Seite **Standard Betragsverteilungscodes** zurückzukehren.

7. Klicken Sie in der Aktionsleiste auf **Bearbeiten**, um die **Standard Betragsverteilungscode Karte** zu öffnen.

8. **Optional**: Aktivieren Sie im Inforegister **Allgemein** die Option **Nach Dimensionen verteilen**, wenn Belegbeträge entsprechend den Dimensionen in mehrere Zeilen aufgeteilt werden sollen und die vorhandene Kontonummer für alle erstellten Zeilen beibehalten wird.

   > [!IMPORTANT]
   > **Diese Funktion ist ab Document Capture 2023 R1 (11.00) verfügbar.**
   >
   > Wenn der Belegbetrag in mehrere Zeilen aufgeteilt wird, wird den Zeilen automatisch die Kontonummer zugewiesen, die ursprünglich dem Beleg zugewiesen wurde. Aus diesem Grund können Sie die Felder **Art** und **Nr.** bei Aktivierung von **Nach Dimensionen verteilen** nicht bearbeiten. Sie können **Nach Dimensionen verteilen** nur anwenden, wenn Sie [Betragsverteilungscodes im jeweiligen Beleg nach der Registrierung aktivieren](#betragsverteilungscodes-in-registrierten-belegen-aktivieren) – die anderen beiden Methoden, d. h. die automatische Anwendung mit einer Dokumentvorlage und die manuelle Anwendung im Belegjournal schlagen beide fehl.

9. Wählen Sie im Inforegister **Zeilen** eine Zeile in der Tabelle aus, und füllen Sie dann die Tabellenfelder nach Bedarf aus.
    - **Art**: Wählen Sie den Kontotyp aus, auf den der Betrag dieser Zeile gebucht werden soll.

    - **Nr.**: Wählen Sie die Nummer des Kontos aus, auf das der Betrag dieser Zeile gebucht werden soll.

    - **Beschreibung**: Geben Sie eine beliebige Beschreibung der Zeile ein.

    - **Verteilung %**: Geben Sie den Prozentsatz des erkannten Belegbetrags an, der auf diese Zeile angewendet werden soll.

    - **Einstandspreis**: Geben Sie den festen Betrag ein, den Sie dieser Zeile zuweisen möchten.

    - **[Globale Dimensionen 1 und 2]**: Geben Sie den bzw. die Dimensionswert(e) ein, den/die Sie dieser Zeile zuweisen möchten.
   > [!NOTE]
   > Es werden nur die beiden vorkonfigurierten globalen Dimensionen als Spalten in der Tabelle angezeigt, und Sie können nur Werte für diese beiden Dimensionen direkt in der Tabelle hinzufügen und anzeigen. Sie können jedoch weitere Dimensionen und Werte mit den folgenden Schritten hinzufügen: Wählen Sie die entsprechende Zeile aus, klicken Sie auf **Zeile** > **Dimensionen**, um die Seite **Standard Betragsverteilung Dimensionen** zu öffnen, und wählen Sie dann einen Dimensionscode und einen Dimensionswertcode in der Tabelle aus. Sie können der Tabelle auf der Seite **Bearbeiten** beliebig viele Zeilen für Dimensionen hinzufügen. Klicken Sie dann auf **Schließen**, um zur **Standard Betragsverteilungscode Karte** zurückzukehren. Ihre Dimensionscodes und -werte werden anschließend der ausgewählten Zeile zugewiesen, auch wenn sie in der Tabelle nicht sichtbar sind.

10. Um eine weitere Belegzeile hinzuzufügen, wählen Sie eine neue Zeile in der Tabelle aus und füllen Sie die Felder nach Bedarf aus. Wiederholen Sie diesen Vorgang, bis Sie alle Zeilen eingerichtet haben, die beim Erstellen des Belegs in Business Central automatisch erstellt werden sollen.

    > [!TIP]
    > In jeder Zeile können Sie entweder **Verteilung %** oder **Einstandspreis** angeben, jedoch nicht beides gleichzeitig. Wenn Sie **Verteilung %** verwenden, müssen die Werte, die Sie für alle Zeilen eingeben, insgesamt 100 % ergeben. Wenn sich die Werte auf weniger (oder mehr) als 100 % summieren, werden diese Prozentsätze auf den jeweiligen Beleg angewendet und der ursprüngliche Belegbetrag wird überschrieben. Weitere Informationen finden Sie unter [Vom Belegbetrag abweichende Betragsverteilungscodewerte](#abweichungen-zwischen-werten-von-betragsverteilungscodes-und-belegbetragen).

Sie haben jetzt einen Betragsverteilungscode mit der Beschreibung eingerichtet, die Sie in Schritt 3 angegeben haben. Sobald dieser Code auf einen importierten Beleg angewendet und dieser Beleg in Business Central erstellt wird, wird der Betrag des Belegs in die Anzahl der Zeilen aufgeteilt, die Sie in den Schritten 9–10 auf der **Standard Betragsverteilungscode Karte** angegeben haben. Außerdem werden die von Ihnen angegebenen Konten und Dimensionswerte automatisch bei der Belegerstellung angewendet.

Beispiele, wie verschiedene Codes bei der Anwendung implementiert werden, finden Sie unter [Beispiele für die Anwendung von Betragsverteilungscodes](#beispiele-fur-die-anwendung-von-betragsverteilungscodes) weiter unten.

## So wenden Sie Betragsverteilungscodes mit einer Vorlage an

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**) aus und klicken Sie dann auf **Bearbeiten** in der Aktionsleiste, um die Karte **Belegkategorie** zu öffnen.
3. Wählen Sie im Inforegister **Vorlagen** in der Liste der Vorlagen die Vorlage aus, die Sie konfigurieren möchten, und klicken Sie dann auf **Bearbeiten**, um die Vorlagenkarte zu öffnen.
4. **Optional**: Klicken Sie im Inforegister **Felder** auf **Neues Vorlagenfeld erstellen**, um den **Vorlagenfeld Einrichtungsassistenten** zu starten. Wählen Sie dann das gewünschte Betragsfeld aus, auf das ein Betragsverteilungscode angewendet werden soll.
5. Klicken Sie in der Aktionsleiste auf **Zugehörig** > **Vorlage** > **Übersetzungen** > **Buchungseinrichtung**, um die Seite **Buchungseinrichtung** zu öffnen.
6. Wählen Sie in der Liste das Feld aus, auf das Sie einen Betragsverteilungscode anwenden möchten (zum Beispiel **Betrag ohne MwSt.** oder ein ähnliches Feld).
7. Wählen Sie in der Spalte **Art** die Option **Betragsverteilungscode** aus.
8. Wählen Sie in der Spalte **Nr.** den Betragsverteilungscode aus, den Sie anwenden möchten.

Der ausgewählte Betragsverteilungscode wird auf alle Belege angewendet, die diese Vorlage verwenden.

## So wenden Sie Betragsverteilungscodes manuell bei der Registrierung an

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, zum Beispiel **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Liste den Beleg aus, auf den Sie einen Betragsverteilungscode anwenden möchten.
4. Klicken Sie unter **Belegkopf** auf die drei Punkte rechts neben dem Feld **Art**, um die Seite **Kontoarten** zu öffnen.
5. Wählen Sie in der Liste der Kontotypen **Betragsverteilungscode** aus und klicken Sie dann auf **Schließen**, um zum Belegjournal zurückzukehren.
6. Klicken Sie unter **Belegkopf** auf die drei Punkte rechts neben dem Feld **Nr.**, um die Seite **Standard Betragsverteilungscodes** zu öffnen.
7. Wählen Sie in der Liste den Code aus, den Sie anwenden möchten, und klicken Sie dann auf **OK**, um zum Belegjournal zurückzukehren.
8. Ein Dialogfeld wird angezeigt, in dem Sie gefragt werden, ob Sie den Code als Standardkonto für das primäre Betragsfeld konfigurieren möchten. Klicken Sie je nach Präferenz auf **Ja** oder **Nein**, um das Dialogfeld zu schließen.

Der ausgewählte Betragsverteilungscode wird jetzt auf den Beleg angewendet, sobald Sie den Beleg in Business Central registrieren.

## Betragsverteilungscodes in registrierten Belegen aktivieren

Sie können einen Betragsverteilungscode für einen Beleg aktivieren, auch nachdem der Beleg registriert wurde. Dies kann entweder in Business Central oder im Web Approval Portal vorgenommen werden. Im Folgenden werden beide Methoden am Beispiel von Rechnungen beschrieben.

> [!NOTE]
> Sie müssen eine dieser beiden Methoden verwenden, wenn Sie die Einstellung **Nach Dimensionen verteilen** (verfügbar ab Document Capture 2023 R1) [beim Einrichten](#so-erstellen-sie-betragsverteilungscodes) aktiviert haben.

### So aktivieren Sie Codes in Business Central

1. Klicken Sie im Rollencenter im Navigationsmenü oben auf **Einkauf** > **Einkaufsrechnungen**.
2. Wählen Sie in der Liste die offene Rechnung aus, für die Sie einen Betragsverteilungscode aktivieren möchten. Die Seite **Einkaufsrechnung** wird geöffnet.
3. Klicken Sie in der Aktionsleiste auf **Aktionen** > **Funktion** > **Hole Std. Betragsverteilungscodes...**.
4. Wählen Sie auf der Seite, die sich öffnet, unter **Verteilungscode** den Code aus, den Sie anwenden möchten.
5. Geben Sie unter **Zeilen** an, ob Sie die vorhandenen Rechnungszeilen durch die Zeilen ersetzen möchten, die durch den Betragsverteilungscode hinzugefügt werden, oder ob Sie die vorhandenen Rechnungszeilen beibehalten und die Zeilen des Betragsverteilungscodes zusätzlich hinzufügen möchten.
6. Das Feld **Betrag für Verteilung** wird basierend auf den Daten der ausgewählten Rechnung automatisch ausgefüllt. Sie können den angezeigten Betrag jedoch bei Bedarf bearbeiten.
7. Klicken Sie auf **OK**, wenn Sie fertig sind

Die Rechnung wird dann mit den Änderungen des angewendeten Betragsverteilungscodes aktualisiert.

### So aktivieren Sie Codes im Web Approval Portal

1. Wählen Sie in der Liste den Beleg aus, für den Sie einen Betragsverteilungscode aktivieren möchten. Die Seite für den Beleg wird geöffnet.
2. Klicken Sie in der Aktionsleiste auf **Vorlage verwenden**, um die Seite **Vorlage verwenden** zu öffnen.
3. Wählen Sie im Dropdown-Menü oben den Code aus, den Sie anwenden möchten.
4. Geben Sie unter dem Dropdown-Menü an, ob Sie die vorhandenen Rechnungszeilen durch die Zeilen ersetzen möchten, die durch den Betragsverteilungscode hinzugefügt wurden, oder ob Sie die vorhandenen Rechnungszeilen beibehalten und die Zeilen Betragsverteilungscodes zusätzlich hinzufügen möchten.
5. Das Feld **Betrag für Verteilung** wird basierend auf den Daten des ausgewählten Belegs automatisch ausgefüllt. Sie können den angezeigten Betrag jedoch bei Bedarf bearbeiten.
6. Klicken Sie auf **Weiter**, wenn Sie fertig sind.

Die Rechnung wird dann mit den Änderungen des angewendeten Betragsverteilungscodes aktualisiert.

## Beispiele für die Anwendung von Betragsverteilungscodes

Sobald ein Betragsverteilungscode auf einen Beleg angewendet wird, wird der Belegbetrag unabhängig von der verwendeten Methode in Zeilen aufgeteilt, wie von Ihnen festgelegt. Im Folgenden finden Sie einige Beispiele.

> [!NOTE]
> Wenn Sie im Inforegister **Einkaufsbelege** unter **Genehmigung** die Option **Betragsvalidierung** auf der jeweiligen Vorlagenkarte aktiviert haben, wird bei Abweichungen zwischen importierten und zugewiesenen Beträgen ein Dialogfeld angezeigt, das Sie über die Abweichung informiert. In diesen Fällen müssen Sie das Problem manuell beheben, indem Sie beispielsweise Zeilen hinzufügen und/oder anpassen, damit die importierten und zugewiesenen Beträge übereinstimmen.

### Standardeinrichtung

Im Folgenden sehen Sie ein Beispiel, bei dem die **Standard Betragsverteilungscode Karte** für einen Betragsverteilungscode mit der Bezeichnung **Büro** eingerichtet ist:

<br>

| Art       | Nr. | Beschreibung           | Verteilung % | Einstandspreis | Abteilung Code |
| --------- | ------------------- | ---------------------- | :----------: | :------------: | :------------: |
| Sachkonto | 31400               | Bürokosten, Verwaltung |      50      |        -       |      VERW      |
| Sachkonto | 31400               | Bürokosten, Verkauf    |      30      |        -       |     VERKAUF    |
| Sachkonto | 40800               | Bürokosten, Produktion |      20      |        -       |      PROD      |

Wenn dieser Betragsverteilungscode auf eine Rechnung mit einem importierten Betrag von 200 EUR ohne Mehrwertsteuer angewendet wird, werden der Rechnung automatisch die folgenden drei Zeilen hinzugefügt:

<br>

| Art       | Nr. | Beschreibung           | EK-Preis ohne MwSt. | Abteilung Code |
| --------- | ------------------- | ---------------------- | :---------------------------------: | :------------: |
| Sachkonto | 31400               | Bürokosten, Verwaltung |                100,00               |      VERW      |
| Sachkonto | 31400               | Bürokosten, Verkauf    |                60,00                |     VERKAUF    |
| Sachkonto | 40800               | Bürokosten, Produktion |                40,00                |      PROD      |

Der Rechnungsbetrag wurde hier gemäß den angegebenen Prozentsätzen auf die Zeilen verteilt und die richtigen Konten und Dimensionswerte (in diesem Fall unterschiedliche Abteilungscodes) wurden auf die Zeilen angewendet, wie beim Einrichten angegeben.

### Abweichungen zwischen Werten von Betragsverteilungscodes und Belegbeträgen

Im Abschnitt [So erstellen Sie Betragsverteilungscodes](#so-erstellen-sie-betragsverteilungscodes) wird darauf hingewiesen, dass die Werte für **Verteilung %** insgesamt 100 % ergeben müssen. Dies ist auch im obigen Beispiel veranschaulicht. Wenn sich die Werte jedoch auf weniger (oder mehr) als 100 % summieren, werden diese Prozentsätze auf den jeweiligen Beleg angewendet und der ursprüngliche Belegbetrag wird überschrieben. Hier ist ein Beispiel:

<br>

| Art       | Nr. | Beschreibung           | Verteilung % | Einstandspreis | Abteilung Code |
| --------- | ------------------- | ---------------------- | :----------: | :------------: | :------------: |
| Sachkonto | 31400               | Bürokosten, Verwaltung |      30      |        -       |      VERW      |
| Sachkonto | 31400               | Bürokosten, Verkauf    |      30      |        -       |     VERKAUF    |
| Sachkonto | 40800               | Bürokosten, Produktion |      30      |        -       |      PROD      |

Wenn dieser Betragsverteilungscode auf eine Rechnung mit einem importierten Betrag von 200,00 EUR ohne Mehrwertsteuer angewendet wird, werden der Rechnung die folgenden drei Zeilen hinzugefügt:

<br>

| Art       | Nr. | Beschreibung           | EK-Preis ohne MwSt. | Abteilung Code |
| --------- | ------------------- | ---------------------- | :---------------------------------: | :------------: |
| Sachkonto | 31400               | Bürokosten, Verwaltung |                60,00                |      VERW      |
| Sachkonto | 31400               | Bürokosten, Verkauf    |                60,00                |     VERKAUF    |
| Sachkonto | 40800               | Bürokosten, Produktion |                60,00                |      PROD      |

Der Gesamtbetrag beträgt jetzt 180,00 EUR ohne Mehrwertsteuer (genau 90 % des importierten Betrags von 200,00 EUR), der dann in drei Zeilen mit jeweils 30 % des Gesamtbetrags aufgeteilt wurde.

> [!NOTE]
> Ähnlich verhält es sich, wenn die Summe der Werte für **Einstandspreis** kleiner (oder größer) als der importierte Rechnungsbetrag ist. Die Gesamtsumme für **Einstandspreis** wird auf die Rechnung angewendet und der ursprüngliche Rechnungsbetrag überschrieben. In beiden Fällen werden Sie darüber informiert, dass eine Diskrepanz zwischen den importierten und den zugewiesenen Beträgen besteht, und Sie müssen dieses Problem manuell beheben.

### Gemischte Betragsverteilungscodewerte

Im Abschnitt [So erstellen Sie Betragsverteilungscodes](#so-erstellen-sie-betragsverteilungscodes) wird darauf hingewiesen, dass Sie nicht gleichzeitig **Verteilung %** und **Einstandspreis** beim Erstellen von Betragsverteilungscodes verwenden können. Wenn Sie jedoch für einen Code mehrere Zeilen einrichten, können Sie beide Optionen über mehrere Zeilen verteilt verwenden. Dies wird im folgenden Beispiel veranschaulicht:

<br>

| Art       | Nr. | Beschreibung           | Verteilung % | Einstandspreis | Abteilung Code |
| --------- | ------------------- | ---------------------- | :----------: | :------------: | :------------: |
| Sachkonto | 31400               | Bürokosten, Verwaltung |      25      |        -       |      VERW      |
| Sachkonto | 31400               | Bürokosten, Verkauf    |       -      |       50       |     VERKAUF    |
| Sachkonto | 40800               | Bürokosten, Produktion |       -      |       50       |      PROD      |

Wenn dieser Betragsverteilungscode auf eine Rechnung mit einem importierten Betrag von 200,00 EUR ohne Mehrwertsteuer angewendet wird, werden der Rechnung die folgenden drei Zeilen hinzugefügt:

<br>

| Art       | Nr. | Beschreibung           | EK-Preis ohne MwSt. | Abteilung Code |
| --------- | ------------------- | ---------------------- | :---------------------------------: | :------------: |
| Sachkonto | 31400               | Bürokosten, Verwaltung |                25,00                |      VERW      |
| Sachkonto | 31400               | Bürokosten, Verkauf    |                50,00                |     VERKAUF    |
| Sachkonto | 40800               | Bürokosten, Produktion |                50,00                |      PROD      |

Der Prozentsatz in **Verteilung %** wird erst angewendet, wenn die beiden **Einstandspreis**-Beträge vom importierten Betrag abgezogen wurden: (200 – 50 – 50) × 0,25 = 25.