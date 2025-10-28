---
title: Einkäufercodeübersetzung
date: 28-02-2023
description:
id: DC-128
lang: de
---

# Einkäufercodeübersetzung

Einkäufercodes erfüllen in Microsoft Dynamics 365 Business Central einige wichtige Funktionen. Sie dienen beispielsweise dazu, Standardeinkaufsgenehmigungen zu starten und Sie bilden eine Grundlage für Statistiken. Wenn dies in Ihrem Unternehmen wichtig ist, müssen allen eingehenden Belegen die richtigen Einkäufercodes zugewiesen werden. Continia Document Capture verwendet zu diesem Zweck das Feld **Einkäufer/Verkäufer** im Abschnitt **Belegkopf** von eingehenden Belegen.

Wenn Document Capture [die Felder eines eingehenden Belegs erkennt](@DC-110), wird für **Einkäufer/Verkäufer** ein Wert erfasst, oder Sie können einen Wert manuell hinzufügen. Sofern der Wert in diesem Feld nicht dem genauen Einkäufercode des richtigen Einkäufers entspricht (was selten der Fall ist), muss der Wert in den richtigen Einkäufercode übersetzt werden, damit Sie den Beleg richtig registrieren können. Diese Übersetzung ist folgendermaßen möglich:

- Document Capture kann so eingerichtet werden, dass bei der Belegregistrierung [der erfasste Wert automatisch in einen bestimmten Einkäufercode übersetzt wird](#automatische-ubersetzung).
- Sie können bei jeder Registrierung eines Belegs den [entsprechenden Einkäufercode manuell auswählen](#manuelle-auswahl).

Diese beiden Methoden werden in den folgenden Abschnitten ausführlicher beschrieben und Sie finden Informationen, wie man [mehrere Übersetzungen für einen oder mehrere Kreditor(en) bearbeitet, löscht oder erstellt](#so-bearbeiten-loschen-oder-erstellen-sie-mehrere-ubersetzungen-fur-einen-oder-mehrere-kreditoren).

## Automatische Übersetzung

Um Document Capture so einzurichten, dass ein in **Einkäufer/Verkäufer** erfasster Wert automatisch in einen bestimmten Einkäufercode übersetzt wird, gehen Sie folgendermaßen vor:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Wählen Sie den Code **EINKAUF** aus, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, dessen Wert für **Einkäufer/Verkäufer** Sie übersetzen möchten.
4. Stellen Sie sicher, dass Belegfelder erkannt wurden. Falls dies nicht der Fall ist, wählen Sie in der Aktionsleiste **Start** > **Felder erkennen**.
5. Überprüfen Sie im Abschnitt **Belegkopf**, ob ein Wert für **Einkäufer/Verkäufer** erfasst wurde.
6. Klicken Sie in der Aktionsleiste auf **Start** > **Registrieren**. Dadurch wird die Seite **Einkäufer/Verkäufer Übersetzung** geöffnet, sofern der in Schritt 4 eingelesene Wert für **Einkäufer/Verkäufer** kein vorhandener Einkäufercode ist.
7. Wählen Sie unter **Einkäufer ziehen von...** je nach Präferenz eine der folgenden Optionen aus:
   - **Kreditor**: Wählen Sie diese Option, wenn Sie den Wert
     für **Einkäufer/Verkäufer** in den Einkäufercode übersetzen möchten, der auf der Kreditorenkarte eingerichtet wurde.
   - **Einkäufer aus Liste auswählen**: Wählen Sie diese Option, um die Seite **Verkäufer/Einkäufer** zu öffnen, auf der Sie dann den Einkäufercode auswählen können, in den Sie den Wert für **Einkäufer/Verkäufer** übersetzen möchten.
8. Unabhängig davon, welche der Optionen Sie in Schritt 7 oben auswählen, wird die Option **Ihre Auswahl in der Vorlage speichern** unter **Übersetzung einrichten** automatisch aktiviert. Um den ausgewählten Einkäufercode zur Standardübersetzung für die zugewiesene Vorlage zu machen, lassen Sie diese Option aktiviert und wählen Sie dann **OK** aus, um die Seite zu schließen und Ihre Einstellungen zu übernehmen.

Document Capture übersetzt jetzt automatisch jeden erfassten Wert für **Einkäufer/Verkäufer** in den ausgewählten Einkäufercode, wenn Sie einen Beleg registrieren, dem die betreffende Vorlage zugewiesen ist.

## Manuelle Auswahl

Um den Einkäufercode, in den ein erfasster Wert für **Einkäufer/Verkäufer** übersetzt werden soll, manuell auszuwählen, gehen Sie folgendermaßen vor:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Wählen Sie den Code **EINKAUF** aus, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, dessen Wert für **Einkäufer/Verkäufer** Sie übersetzen möchten.
4. Stellen Sie sicher, dass Belegfelder erkannt wurden. Falls dies nicht der Fall ist, wählen Sie in der Aktionsleiste **Start** > **Felder erkennen**.
5. Überprüfen Sie im Abschnitt **Belegkopf**, ob ein Wert für **Einkäufer/Verkäufer** erfasst wurde.
6. Klicken Sie in der Aktionsleiste auf **Start** > **Registrieren**. Dadurch wird die Seite **Einkäufer/Verkäufer Übersetzung** geöffnet, sofern der in Schritt 4 eingelesene Wert für **Einkäufer/Verkäufer** kein vorhandener Einkäufercode ist.
7. Wählen Sie unter **Einkäufer ziehen von...** je nach Präferenz eine der folgenden Optionen aus:
   - **Kreditor**: Wählen Sie diese Option, wenn Sie den Wert
     für **Einkäufer/Verkäufer** in den Einkäufercode übersetzen möchten, der auf der Kreditorenkarte eingerichtet wurde.
   - **Einkäufer aus Liste auswählen**: Wählen Sie diese Option, um die Seite **Verkäufer/Einkäufer** zu öffnen, auf der Sie dann den Einkäufercode auswählen können, in den Sie den Wert für **Einkäufer/Verkäufer** übersetzen möchten.
8. Unabhängig davon, welche der Optionen Sie in Schritt 7 oben auswählen, wird die Option **Ihre Auswahl in der Vorlage speichern** unter **Übersetzung einrichten** automatisch aktiviert. Deaktivieren Sie diese Option, und wählen Sie dann **OK**, um die Seite zu schließen und Ihre Einstellungen zu übernehmen.

Der erfasste Wert für **Einkäufer/Verkäufer** wird anschließend in den ausgewählten Einkäufercode für diesen bestimmten Beleg übersetzt, wenn Sie den Beleg registrieren.

## So bearbeiten, löschen oder erstellen Sie mehrere Übersetzungen für einen oder mehrere Kreditor(en)

Sie können die automatische Übersetzung auch mit der Seite **Einkäufer/Verkäufer Übersetzung** einrichten. Auf dieser Seite können Sie auch vorhandene Übersetzungen bearbeiten oder löschen, mehrere Übersetzungen auf einmal einrichten und Ihre Übersetzungseinstellungen global auf alle Kreditoren anwenden.

Um Übersetzungen über diese Seite zu verwalten, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie den Code **EINKAUF** aus, um das Belegjournal zu öffnen.
3. Wählen Sie einen Beleg in der Liste aus.
4. Stellen Sie sicher, dass Belegfelder erkannt wurden. Falls dies nicht der Fall ist, wählen Sie in der Aktionsleiste **Start** > **Felder erkennen**.
5. Klicken Sie in der Aktionsleiste auf **Übersetzungen** > **Verkäufer/Einkäufer**, um die Seite **Einkäufer/Verkäufer Übersetzung** zu öffnen.
6. Um eine neue Übersetzung hinzuzufügen oder eine vorhandene zu bearbeiten, geben Sie einen Wert in die Spalte **Einkäufer/Verkäufer** der Tabelle ein.
7. Wählen Sie in der Spalte **Verkäufer / Einkäufer Code** den Einkäufercode aus, in den der eingegebene Wert für **Einkäufer/Verkäufer** übersetzt werden soll.
8. Geben Sie in der Spalte **Aktiviert für** an, ob die Übersetzung für alle Kreditoren gelten soll oder nur für den, der dem in Schritt 3 oben ausgewählten Beleg zugewiesen ist.
   > [!NOTE]
   > Wenn Sie **Nur diesen Kreditor** auswählen, werden die Felder **Kreditorennr.** und **Kreditorenname** automatisch ausgefüllt. Sie können diese Werte nicht bearbeiten.
9. Wiederholen Sie die Schritte 6–8 für alle weiteren Übersetzungen, die Sie einrichten oder bearbeiten möchten.
10. **Optional**: Um eine Übersetzung zu löschen, wählen Sie die entsprechende Zeile in der Tabelle aus und wählen Sie dann **Löschen** in der Aktionsleiste. Wählen Sie im Dialogfeld, das geöffnet wird, zur Bestätigung **Ja** aus.
11. Wenn Sie fertig sind, schließen Sie die Seite **Einkäufer/Verkäufer Übersetzung**, um zum Belegjournal zurückzukehren.

Ihre Übersetzungseinstellungen werden jetzt entweder auf alle Kreditoren oder auf den aktuellen Kreditor angewendet (wie von Ihnen in Schritt 8 oben angegeben), und alle erfassten Werte für **Einkäufer/Verkäufer** in Belegen, die von den ausgewählten Kreditoren gesendet werden, werden Ihrer Einrichtung entsprechend automatisch übersetzt.

## Informationen zum Thema

[Felder in einem Beleg erfassen](@DC-110)\
[Belege registrieren](@DC-67)