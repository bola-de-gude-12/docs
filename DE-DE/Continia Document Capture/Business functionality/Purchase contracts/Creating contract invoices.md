---
title: Vertragsrechnungen in Document Capture erstellen
date: 23-07-2025
description: So erstellen Sie Rechnungen, die mit Einkaufsverträgen in Document Capture verknüpft sind.
id: DC-88
lang: de
---

# Vertragsrechnungen erstellen

Eine Vertragsrechnung ist eine Rechnung, die mit einem Einkaufsvertrag verknüpft wurde. Beim Registrieren der Rechnung werden die Zeilen des Einkaufsvertrags automatisch in die Rechnung eingefügt.

Im ersten Schritt muss [eine eingehende Rechnung mit einem Vertrag verknüpft werden](#so-verknupfen-sie-einen-einkaufsvertrag-mit-einer-rechnung), und im zweiten Schritt [muss die Rechnung als Vertragsrechnung registriert werden](#so-registrieren-sie-eine-rechnung-als-vertragsrechnung). Bei der Registrierung wird die Vertragsrechnung als echte Geschäftseinheit in Microsoft Dynamics 365 Business Central erstellt. Mit der Buchungseinrichtung können Sie Continia Document Capture auch so einrichten, dass die Verknüpfung zwischen der Rechnung und dem Vertrag bei der Registrierung automatisch erstellt wird.

In diesem Artikel werden zur Veranschaulichung ausschließlich Rechnungen verwendet, da dies das mit Abstand häufigste Szenario ist. Die gleiche Funktionalität gilt jedoch auch für Vertragsgutschriften.

> [!IMPORTANT]
> Damit die Zeilen des Vertrags automatisch in die Rechnung eingefügt werden, muss die Zeilenerkennung in der entsprechenden Vorlage deaktiviert werden.

## So verknüpfen Sie einen Einkaufsvertrag mit einer Rechnung

Wenn eine Rechnung von einem Beleg erstellt wird, kann ein Einkaufsvertrag mit der eingehenden Rechnung entweder manuell oder automatisch von Document Capture verknüpft werden. Beide Methoden werden nachfolgend beschrieben:

### Automatische Verknüpfung

Um den Vertrag automatisch mit der Rechnung zu verknüpfen, müssen Sie den Vertrag auf Grundlage einer Einkaufsrechnung erstellen, wie unter [So erstellen Sie einen Einkaufsvertrag auf der Grundlage eines Belegs](@DC-86#so-erstellen-sie-einen-einkaufsvertrag-auf-der-grundlage-eines-belegs) beschrieben. Dadurch wird der Vertrag automatisch mit der Rechnung verknüpft und im Belegjournal werden dem Abschnitt **Belegkopf** der ausgewählten Rechnung die folgenden beiden Werte hinzugefügt:

- Im Feld **Art** wird der Wert **Einkaufsvertrag** hinzugefügt.
- Im Feld **Nr.** wird die Vertragsnummer hinzugefügt.

### Manuelle Verknüpfung

Um den Vertrag manuell mit der Rechnung zu verknüpfen, müssen Sie diese beiden Werte hinzufügen, indem Sie die folgenden Schritte ausführen:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Liste der Belege die Rechnung aus, die Sie mit dem Vertrag verknüpfen möchten.
4. Klicken Sie in der Aktionsleiste auf **Einkaufsvertrag** > **Einkaufsvertrag auswählen**.
5. Wählen Sie auf der Seite **Einkaufsvertragsauswahl** einen Vertrag aus. Auf der Registerkarte **Abgleich Übersicht** helfen Ihnen die Felder **Abzugleichender Betrag**, **Abgeglichener Betrag** und **Differenz** dabei, den richtigen Vertrag auszuwählen, unabhängig davon, ob die Belegzeilen erkannt werden oder nicht.

Dadurch wird der Vertrag mit der Rechnung verknüpft, und diese kann anschließend als Vertragsrechnung registriert werden.

## So registrieren Sie eine Rechnung als Vertragsrechnung

Nachdem Sie wie oben beschrieben einen Vertrag mit einer Rechnung verknüpft haben, können Sie die Rechnung als Vertragsrechnung in Business Central registrieren. Dazu müssen Sie die Rechnung wie andere [Rechnungen registrieren](@DC-67). Dadurch werden die Zeilen des Vertrags automatisch in die Rechnung eingefügt. Die Zeilen werden auf der Seite **Einkaufsrechnung** im Inforegister **Zeilen** unter einer übergeordneten Zeile angezeigt, die die Nummer des Einkaufsvertrags angibt, aus dem die Zeilen stammen.

> [!NOTE]
> Die in die Rechnung eingefügten Zeilen sind exakte Kopien der Zeilen im verknüpften Vertrag, wobei die Beträge basierend auf dem Status der Einstellung **Belegbetrag verteilen** auf der Seite **Einkaufsvertragseinrichtung** berechnet werden. Weichen die Beträge von Rechnung und Vertrag ab, werden Sie mit einem Dialogfeld darauf hingewiesen. Sie müssen dann manuelle Schritte zur Bestätigung ausführen.

## So erstellen Sie eine Vertragsrechnung mit der Buchungseinrichtung

Sie können den Verknüpfungsprozess über die Buchungseinrichtung automatisieren. So können Sie festlegen, wie die Beträge eingehender Rechnungen bei der Registrierung verbucht werden. Sie können festlegen, dass die Beträge von einem bestimmten Einkaufsvertrag für alle Rechnungen mit der ausgewählten Vorlage übertragen werden. Damit richten Sie Document Capture so ein, dass automatisch eine Verknüpfung zwischen den Rechnungen und dem angegebenen Vertrag bei der Rechnungsregistrierung erstellt wird. Gehen Sie hierzu wie folgt vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf den Code **EINKAUF**, um das Belegjournal zu öffnen.
3. Wählen Sie in der Liste der Belege die Rechnung aus, die Sie als Vertragsrechnung registrieren möchten.
4. Klicken Sie in der Aktionsleiste auf **Vorlage** > **Buchungseinrichtung**.
5. Wählen Sie in der Feldzeile **Betrag ohne MwSt.** unter **Art** die Option **Einkaufsvertrag** aus.
6. Wählen Sie unter **Nr.** den Vertrag aus, den Sie mit der ausgewählten Rechnung und mit allen anderen Rechnungen mit derselben Vorlage verknüpfen möchten.
7. Schließen Sie die Seite **Buchungseinrichtung**, um zum Belegjournal zurückzukehren.
8. Klicken Sie in der Aktionsleiste auf **Start** > **Registrieren**, um die Rechnung zu registrieren.

Dadurch wird die Rechnung automatisch mit dem ausgewählten Vertrag verknüpft und die Zeilen des Vertrags in die Rechnung eingefügt. Die Zeilen werden auf der Seite **Einkaufsrechnung** im Inforegister **Zeilen** unter einer übergeordneten Zeile angezeigt, die die Nummer des Einkaufsvertrags angibt, aus dem die Zeilen stammen.

> [!NOTE]
> Die in die Rechnung eingefügten Zeilen sind exakte Kopien der Zeilen im verknüpften Vertrag, wobei die Beträge basierend auf dem Status der Einstellung **Belegbetrag verteilen** auf der Seite **Einkaufsvertragseinrichtung** berechnet werden. Weichen die Beträge von Rechnung und Vertrag ab, werden Sie mit einem Dialogfeld darauf hingewiesen. Sie müssen dann manuelle Schritte zur Bestätigung ausführen.

## Informationen zum Thema

[Einkaufsverträge erstellen](@DC-86)  
[Einkaufsverträge genehmigen](@DC-87)  
[Vertragsrechnungen genehmigen](@DC-89)  
[Das Einkaufsvertragsarchiv anzeigen](@DC-90)