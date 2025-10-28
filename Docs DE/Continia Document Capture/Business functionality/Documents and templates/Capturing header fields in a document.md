---
title: Erfassen von Kopffeldern in einem Dokument mit Document Capture
date: 30-09-2025
description: So erfassen Sie Kopffelder in einem Dokument mit Document Capture.
id: DC-110
lang: de
---

# Kopffelder in einem Beleg erfassen

> [!IMPORTANT]
> Zur Veranschaulichung konzentriert sich dieser Artikel auf Einkaufsbelege und Kreditoren. Die unten beschriebenen Vorgehensweisen gelten jedoch auch für andere Arten von Geschäftsbelegen und Belegherkünften.

In diesem Artikel wird beschrieben, wie Kopffelder erfasst werden. Informationen zur Zeilenerkennung finden Sie unter [Zeilenfelder in einem Beleg erfassen (Zeilenerkennung)](@DC-147).

Beim Erfassen von Feldern verwendet Continia Document Capture Suchtexte (auch Captions oder Suchbegriffe genannt) und Werte, um nach Textinformationen in importierten Belegen zu suchen und diese zu identifizieren. Sowohl Suchtexte als auch Werte sind identifizierbare Textzeichenfolgen, die als Textelemente in den importierten Dokumenten sichtbar sind, sich jedoch in ihrer Funktion unterscheiden.

Stellen Sie sich einen Feldsuchtext als eine Art Beschriftung vor, das Document Capture dabei hilft, den richtigen Wert für ein Vorlagenfeld zu identifizieren. Jedem Suchtext ist ein entsprechender Wert zugeordnet. Dies ist der eigentliche Text, der erfasst und beim Registrieren von Belegen verwendet werden soll. Ein Suchtext kann beispielsweise **Rechnungsnr.** sein und ein möglicher Wert die Nummer 1647. In der Dokumentenvorschau auf der rechten Seite des Belegjournals werden Suchtexte durch orangefarbene Kästchen hervorgehoben, während Feldwerte durch blaue Kästchen hervorgehoben werden.

Sobald ein Einkaufsbeleg in Business Central einem Kreditor zugewiesen wird, prüft Document Capture automatisch, ob diesem Kreditor eine Vorlage zugeordnet ist. Wenn ja, wird diese Vorlage auf den Beleg angewendet und alle Felder werden gemäß den Regeln und der Konfiguration dieser Vorlage erfasst. Alle Belegfelder müssen eingelesen werden und gültige Werte haben, damit Sie [den Beleg registrieren](@DC-67) können.

Wenn Sie einen Beleg von einem Kreditor zum ersten Mal erhalten, sind diesem Kreditor keine Vorlagen zugeordnet. Um dem Kreditor eine Vorlage zuzuweisen, aktivieren Sie im Belegjournal Felderkennung (siehe Schritt 5 unten). Dadurch wird automatisch eine Vorlage erstellt, mit dem Kreditor verknüpft und alle Felder für diesen Beleg erfasst.

> [!NOTE]
> Wenn ein Kreditor Ihnen zum ersten Mal einen Beleg sendet, aber bereits über eine zugehörige Vorlage in einem anderen Mandanten verfügt, kopiert Document Capture die Vorlage von diesem Mandanten in den aktuellen Mandanten. Sie müssen eine Konfiguration, die Sie bereits in einem anderen Mandanten für denselben Kreditor vorgenommen haben, dann nicht erneut durchführen.

> [!TIP]
> Document Capture unterstützt die Nachhaltigkeitsfunktion von Business Central und erleichtert Ihnen die Berechnung und Verfolgung der Treibhausgasemissionen (THG) Ihres Unternehmens. Die folgenden Kopffelder können zu Ihren Vorlagen hinzugefügt werden:
>
> - **Nachhaltigkeitskonto Nr.**
> - **Kraftstoff/Strom**\*
> - **Entfernung**\*
> - **Eigener Betrag**\*
> - **Installations-Multiplikator**\*
> - **Zeitfaktor**\*
> - **CO2-Emission**
> - **CH4-Emission**
> - **N2O-Emission**
>
> Die oben mit einem Sternchen markierten Felder, die als Aktivitätsfelder bezeichnet werden, werden nicht aus den Document Capture-Vorlagen in Standard-Einkaufsrechnungen übernommen. Stattdessen berechnet Document Capture automatisch die Emissionsfaktorfelder (z. B. CO₂, CH₄, N₂O) in der Dokumentenkarte. Weitere Informationen finden Sie unter [Nachhaltigkeitsmanagement – Überblick](https://learn.microsoft.com/de-de/dynamics365/business-central/finance-manage-sustainability) (Microsoft-Artikel).

## So erfassen Sie Felder

So erfassen Sie die Felder eines Dokuments:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, in diesem Fall **EINKAUF**, um das Belegjournal zu öffnen.
3. Wenn Document Capture für den Beleg, dessen Felder Sie erfassen möchten, automatisch einen Kreditor identifiziert hat, wird die Nummer des identifizierten Kreditors im Feld **Kreditor** in der Belegliste angezeigt. Wenn kein Kreditor identifiziert wurde, weisen Sie einen Kreditor manuell zu, wie unter [Den mit einem Beleg verknüpften Kreditor ändern](@DC-71#den-mit-einem-beleg-verknupften-kreditor-andern) beschrieben.

Wenn Sie zuvor Belege vom zugewiesenen Kreditor erhalten und importiert haben, wird die mit diesem Kreditor verknüpfte Vorlage automatisch zum Erfassen von Feldsuchtexten und -werten verwendet. Andernfalls ist keine Vorlage zugeordnet; Document Capture erstellt und weist jedoch automatisch eine zu. Anschließend werden Suchtexte und Werte für die Felder eingelesen und mit orangefarbenen und blauen Kästchen in der Dokumentenvorschau auf der rechten Seite hervorgehoben.

Sie können die identifizierten Feldwerte und Suchtexte jederzeit ändern. Weitere Informationen finden Sie unter [Document Capture zum Erkennen von Werten trainieren](#document-capture-zum-erkennen-von-werten-trainieren) weiter unten.

> [!TIP]
> PDFs sind komplexe Dokumente mit mehreren Ebenen. Wenn Sie beim Verarbeiten einer PDF-Datei in Document Capture auf ungültige Werte feststellen, öffnen Sie die PDF-Datei mit einem modernen Browser, MS Paint oder einem ähnlichen Programm. Sie können sie dann entweder als PDF drucken oder noch einmal als PDF speichern, sodass Document Capture sie korrekt verarbeiten kann. Beachten Sie, dass dies nur für On-Premises-Einrichtungen gilt, da die Cloud-OCR präziser ist.

## Grundlegendes zu Feldsuchtexten und -werten

Wie oben erwähnt, sucht und identifiziert Document Capture Textinformationen in importierten Belegen anhand von Feldsuchtexten und entsprechenden Werten. Im Folgenden finden Sie Textbeispiele, die in Rechnungen zu finden sein könnten:

| Textbeispiel                                                               | Erläuterung                                                                                                         |
| -------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| Rechnungsnummer: 12345678                                  | Der Suchtext lautet **Rechnungsnummer** und der entsprechende Wert **12345678**.                    |
| Rechnungsdatum: 01.01.2021 | Der Suchtext lautet **Rechnungsdatum** und der Wert **01.01.2021**. |

Die Beispiele oben zeigen, dass Suchtexte und Werte immer paarweise funktionieren. Normalerweise ändern sich die Suchtexte nicht von Beleg zu Beleg, wenn die Belege vom selben Kreditor gesendet wurden, es sei denn, der Kreditor ändert das Rechnungslayout. Werte hingegen sind von Beleg zu Beleg unterschiedlich. Beispielsweise erhöht sich die Rechnungsnummer normalerweise schrittweise mit jeder Rechnung, was auch für das Rechnungsdatum zutrifft.

Suchtexte werden für jedes Vorlagenfeld definiert, und die Werte werden im Beleg erfasst und gespeichert. Wichtig: Damit Suchtexte und Werte richtig erfasst werden können, muss der Abstand zwischen ihnen in allen Belegen desselben Kreditors gleich sein. Beispielsweise steht in den obigen Beispielen der Suchtext in einem bestimmten Abstand direkt vor dem entsprechenden Wert. Wenn die beiden Elemente in allen nachfolgenden Belegen dieselbe Position und denselben Abstand zueinander haben, werden sie alle korrekt verarbeitet.

Zum Beispiel kann ein Suchtext **Rechnungsnummer** in einer Zeile stehen und der entsprechende Wert dann direkt darunter in der nächsten Zeile (ein gängiges Rechnungsformat). Dies funktioniert ohne Probleme, solange der Abstand zwischen dem Suchtext und dem Wert bei allen Belegen desselben Kreditors gleich ist. Auch Suchtexte, die weit entfernt von den zugehörigen Werten stehen, sind akzeptabel, sofern der Abstand zwischen beiden in allen Belegen gleichbleibt.

Bei der Identifizierung von Feldern in einem Beleg sucht Document Capture nach Suchtexten, die für jedes Vorlagenfeld definiert sind, und versucht dann, die zugehörigen Werte einzulesen. Wenn Document Capture beispielsweise nach der Textzeichenfolge **Rechnungsnummer** in einer Rechnung sucht und diese findet, kann anschließend die entsprechende Rechnungsnummer ermittelt werden, je nach Vorlagenkonfiguration.

> [!NOTE]
> Obwohl Sie auf der Seite **Feld Suchtexte** mehrere Suchbegriffe für ein bestimmtes Vorlagenfeld definieren können, wie z. B. „Rechnungsdatum“ und „Gutschriftsdatum“ für das Feld **Rechnungsdatum**, wird bei der Felderkennung nur der erste von Document Capture gefundene Suchbegriff beibehalten. Hierdurch wird eine präzise und zuverlässige Erkennung aller Ebenen im Dokument sichergestellt.

### Standardfeldwerte

Wenn Kopffelder nicht erkannt werden, werden bei der Registrierung der Rechnung häufig Standardwerte angewendet. Diese Werte werden automatisch vom Kreditor oder der Vorlage übernommen und sind standardmäßig nicht sichtbar. Wenn die Kopffelder einen Wert enthalten, der entweder aus dem Beleg erkannt oder manuell ausgewählt wurde, wird der Wert vom Kreditor/aus der Vorlagenkarte nicht verwendet.

Wenn auf der Belegkategoriekarte die Einstellung **Zeige Standardwert des Feldes** aktiviert ist, werden in der Kopffeldliste – sowohl im Belegjournal als auch auf der Dokumentenkarte – die Standardwerte für die unten aufgeführten Felder in Klammern neben den Feldnamen angezeigt.

- Einkaufskategorie:
  - Genehmigungsablaufcode
  - Zuständigkeitseinheit
  - Kreditor Bankkontonr.
  - Kreditor-MwSt.-Nr.
  - Kreditor Telefonnr.
  - Dimensionen 1-8\*

- Verkaufskategorie:
  - Zuständigkeitseinheit
  - Dimensionen 1-8\*
  \* Die angezeigten Dimensionswerte basieren auf der Reihenfolge, die auf der Seite **Standarddimension Prioritäten** festgelegt wurde.

So aktivieren Sie die Einstellung **Zeige Standardwert des Feldes**:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Um die Einkaufsbelegkategorie zu öffnen, markieren Sie die Zeile der entsprechenden Belegkategorie, beispielsweise **EINKAUF**, und klicken Sie anschließend in der Aktionsleiste auf **Bearbeiten**.
3. Aktivieren Sie im Inforegister **Allgemein** die Einstellung **Zeige Standardwert des Feldes**.

> [!NOTE]
> Die erwarteten Werte können beim Erstellen der eigentlichen Rechnung geändert oder überschrieben werden. Dies ist abhängig von den endgültigen Dokumentdaten, Ihren eigenen Überschreibungen und Aktualisierungen der zugehörigen Felder während der Verarbeitung.

## Document Capture zum Erkennen von Werten trainieren

Manchmal kann Document Capture den Feldwert in einem Beleg nicht erfassen, oder es wird ein falsches Element als Feldwert identifiziert. In diesem Fall können Sie Document Capture ganz einfach trainieren, indem Sie den Suchtext ändern und/oder anzeigen, wo genau der richtige Wert im Beleg zu finden ist. Gehen Sie hierzu wie folgt vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code der entsprechenden Belegkategorie, in diesem Fall **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie im Bereich mit den Belegfeldern (unter **Belegkopf**) das Vorlagenfeld aus, das Sie korrigieren möchten, zum Beispiel **Buchungsbeschreibung**.
4. Wählen Sie mit der Maus genau aus, welcher Text im Beleg für das ausgewählte Vorlagenfeld erfasst werden soll. Um den Suchtext festzulegen, klicken Sie mit der rechten Maustaste und halten Sie die Taste gedrückt, um in der Dokumentenvorschau einen orangefarbenen Rahmen um den entsprechenden Text zu zeichnen.
5. Um den entsprechenden Wert für das ausgewählte Vorlagenfeld festzulegen, klicken Sie mit der linken Maustaste und halten Sie die Schaltfläche gedrückt, um in der Dokumentenvorschau ein blaues Kästchen um den entsprechenden Text zu zeichnen.
6. Der ausgewählte Text wird dem Vorlagenfeld im Abschnitt mit den Belegfeldern hinzugefügt. Stellen Sie sicher, dass er korrekt erfasst wurde.
7. Um zu bestätigen, dass der Text stets korrekt erfasst wird, klicken Sie in der Aktionsleiste auf **Start** > **Felder erkennen**. Wenn der Text auch beim zweiten Mal nicht richtig erfasst wird, führen Sie die Schritte 4 bis 7 erneut aus, bis Sie das gewünschte Ergebnis erhalten.

> [!TIP]
> Wenn das Feld, für das Sie einen Wert erfassen möchten, in den Abschnitten **Belegkopf** oder **Zeilen** nicht verfügbar ist, können Sie es hinzufügen, indem Sie den gewünschten Wert in der Dokumentenvorschau auswählen.
>
> 1. Wählen Sie ein Kopf- oder Zeilenfeld aus. Kopffelder können aus der Dokumentenkarte oder dem Belegjournal ausgewählt werden, während Zeilenfelder nur aus der Dokumentenkarte ausgewählt werden können.
> 2. Drücken Sie **Strg** und wählen Sie den gewünschten Wert in der Dokumentenvorschau aus, um den **Vorlagenfeld-Einrichtungsassistenten** zu öffnen. Beachten Sie, dass Werte mit **Strg** und der linken Maustaste und Suchtexte mit **Strg** und der rechten Maustaste erkannt werden müssen.
> 3. Klicken Sie auf **Weiter > Vorlagenfeld**, um die **Vorlagenfeldliste** zu öffnen und ein vorhandenes Feld aus der Mastervorlage auszuwählen, oder auf **Weiter > Neu erstellen**, um ein benutzerdefiniertes Feld zu erstellen.
> 4. Wenn Sie fertig sind, klicken Sie auf **Beenden**, um zur Dokumentenkarte zurückzukehren.

## Informationen zum Thema

[Mit Papier- und PDF-Belegen arbeiten](@DC-71)\
[Vorlagenfelder verwalten](@DC-241)