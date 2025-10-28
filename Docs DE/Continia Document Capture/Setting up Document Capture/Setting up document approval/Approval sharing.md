---
title: Geteilte Genehmigung in Document Capture einrichten
date: 23-07-2025
description: Einrichten der automatischen geteilten Genehmigung, zum Beispiel bei Abwesenheit der Genehmiger.
id: DC-25
lang: de
---

# Geteilte Genehmigung einrichten

Die geteilte Genehmigung ermöglicht es Ihnen, Ihre Genehmigungsaufgaben für einen bestimmten Zeitraum automatisch an einen anderen Genehmiger weiterzuleiten, falls Sie in diesem Zeitraum keine Belege genehmigen können. Der andere Genehmiger ist dann Ihr Vertreter, bis Sie wieder verfügbar sind.

Administratoren können geteilte Genehmigung stellvertretend für andere Benutzer einrichten (für alle Benutzer und Zwecke)

## So richten Sie die geteilte Genehmigung ein

So richten Sie die geteilte Genehmigung ein:

1. Suchen Sie {{search}} nach **Geteilte Genehmigung** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie in der Aktionsleiste auf **Liste bearbeiten**, damit die Liste bearbeitet werden kann.
3. Geben Sie in den Spalten **Inhaber Benutzer-ID** und **Geteilt mit Benutzer-ID** die Benutzer-ID der Person ein, die Genehmigungsaufgaben teilt (im Folgenden als ursprünglicher Genehmiger bezeichnet) und die des Ersatzgenehmigers.
4. Wählen Sie in der Spalte **Teilungsart** die Option **Normal** aus, es sei denn, Sie müssen die Abwesenheitseinstellungen des ursprünglichen Genehmigers ändern (eine eher seltene Ausnahme).
   > [!NOTE]
   > Einzelne Benutzer können die geteilte Genehmigung bei Abwesenheit normalerweise selbst mit [der Anleitung unten](#geteilte-genehmigung-fur-einzelne-benutzer-bei-abwesenheit) einrichten. Gelegentlich muss ein Administrator dies im Auftrag eines Benutzers vornehmen. In solchen Fällen muss der Administrator **Abwesend** anstelle von **Normal** auswählen, und der Benutzer kann den Eintrag dann bei Bedarf später bearbeiten. Wenn der Administrator **Normal** auswählt (was meistens der Fall ist), kann der Benutzer den Eintrag zu einem späteren Zeitpunkt _nicht_ bearbeiten.
5. Geben Sie in den Spalten **Gültig von** und **Gültig bis** das Start- und Enddatum des Zeitraums ein, in dem Genehmigungsaufgaben geteilt werden sollen, oder wählen Sie die Daten aus.
6. Wenn der Ersatzgenehmiger die Grenzwerte und Berechtigungen des ursprünglichen Genehmigers übernehmen soll, aktivieren Sie das Kontrollkästchen **Inhaber Grenzwerte und Berechtigungen verwenden**.
7. Geben Sie in der Spalte **E-Mail senden** an, ob Genehmigungs-E-Mails an den Ersatzgenehmiger, den ursprünglichen Genehmiger oder beide gesendet werden sollen.
8. Wenn Sie möchten, dass Genehmigungsaufgaben für alle Mandanten geteilt werden, in denen beide Benutzer vorhanden sind, aktivieren Sie das Kontrollkästchen **Kopiere in alle Mandanten**. Wenn Sie dieses Kontrollkästchen nicht aktivieren, gilt diese geteilte Genehmigung nur für den Mandanten, in dem Sie sich gerade befinden.

## So richten Sie eine Genehmigungsgruppe ein

Wenn Sie Genehmigungen für mehrere Personen verwalten, können Sie einen Benutzer erstellen und ihn als Genehmigungsgruppe verwenden. Diese Lösung bietet sich auch an, wenn eine Unternehmensrichtlinie vorschreibt, dass Genehmiger auf höchster Ebene ihre eigenen Genehmigungsanfragen von jemand anderem als sich selbst genehmigen lassen müssen.

So erstellen Sie einen Benutzer, der wie eine Gruppe funktioniert:

1. Suchen Sie {{search}} nach **Continia Benutzereinrichtung** und wählen Sie dann den entsprechenden Link aus.

2. Klicken Sie in der Aktionsleiste auf **Neu**.

3. Klicken Sie auf dem Inforegister **Allgemein** auf die drei Punkte neben dem Feld **Continia Benutzer-ID**.

4. Wählen Sie im sich öffnenden Dialogfeld entweder eine vorhandene Benutzer-ID aus oder klicken Sie in der Aktionsleiste auf **Neu**, um einen Benutzer zu erstellen.

5. Wechseln Sie zurück zur Seite **Continia Benutzereinrichtung Karte** und füllen Sie das Feld **Name** aus.

6. Klicken Sie auf die drei Punkte neben dem Feld **Benutzer ID - nächster Genehmiger (Manager)**. Wählen Sie im sich öffnenden Dialogfeld eine vorhandene Genehmiger-ID aus. Wenn die geteilte Genehmigung der Gruppe auf die Beschränkungen des Gruppeninhabers eingerichtet ist und über kein unbegrenztes Genehmigungslimit verfügt, wird das Dokument an den hier angegebenen Manager gesendet.

   > [!IMPORTANT]
   > Die Continia Benutzer-ID, die Sie für diese Genehmigungsgruppe erstellt oder aus der Liste **Continia Benutzer** ausgewählt haben, kann nur für diesen Zweck verwendet werden.

7. Geben Sie im Abschnitt **Einkaufsrechnung- und Gutschriftsgenehmigung** im Feld **Genehmigungslimit** den gewünschten Wert ein. Alternativ können Sie für diese Genehmigungsgruppe die Einstellung **Unbegrenzte Genehmigung** aktivieren.

Jetzt haben Sie einen Genehmigungsbenutzer, der als Genehmigungsgruppe funktioniert.

### So fügen Sie einer Genehmigungsgruppe Benutzer hinzu

1. Suchen Sie {{search}} nach **Geteilte Genehmigung - Document Capture** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie in der Aktionsleiste auf **Neu**.
3. Wählen Sie unter der Spalte **Inhaber Benutzer-ID** den Benutzer aus, den Sie im vorherigen Schritt erstellt haben.
4. Wählen Sie unter der Spalte **Geteilt mit Benutzer-ID** einen Benutzer aus, den Sie in die Gruppe für die geteilte Genehmigung aufnehmen möchten.
5. Wählen Sie unter der Spalte **Teilungsart** die Option **Normal** aus.
6. Aktivieren Sie in der Spalte **Inhaber Grenzwerte und Berechtigungen verwenden** das Kontrollkästchen, um die für die Genehmigungsgruppe konfigurierten Berechtigungen zu aktivieren. Wenn das Kontrollkästchen deaktiviert ist, haben die den einzelnen Mitgliedern der Genehmigungsgruppe zugewiesenen Berechtigungen Vorrang.
7. Wählen Sie in der Spalte **E-Mail senden** die entsprechende Option:<br><ul><li>**Nur Inhaber Benutzer**</li><li>**Nur Geteilt-mit Benutzer**</li></ul>
8. Wiederholen Sie diese Schritte für jeden Benutzer, den Sie in die Gruppe aufnehmen möchten.

Um die Anzahl der der Gruppe hinzugefügten Benutzer anzuzeigen, gehen Sie zur Seite **Continia Benutzereinrichtung** und überprüfen Sie die Werte in den Spalten **Geteilte Genehmigung mit diesem Benutzer** und **Geteilte Genehmigung mit anderen Benutzern**.

## So richten Sie geteilte Genehmigung für einzelne Benutzer bei Abwesenheit ein

Das Einrichten der geteilten Genehmigung bei Abwesenheit mit [der Anleitung oben](#geteilte-genehmigung) ist besonders hilfreich, wenn Administratroren mehrere Benutzer gleichzeitig einrichten. Für einzelne Benutzer gibt es jedoch eine benutzerfreundlichere Möglichkeit, mit der Sie diese selbst einrichten können:

1. Suchen Sie {{search}} nach **Genehmigungsposten** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie in der Aktionsleiste auf **Abwesenheitseinrichtung**.
3. Geben Sie in den Spalten **Weiterleiten von Datum** und **Weiterleiten bis Datum** das Start- und Enddatum des Zeitraums ein, in dem Genehmigungsaufgaben geteilt werden sollen. Sie können die Daten auch auswählen.
4. Geben Sie unter **Weiterleiten an** die Benutzer-ID des Ersatzgenehmigers ein, an den Ihre Genehmigungsaufgaben weitergeleitet werden sollen.
5. Wenn Sie möchten, dass Ihre Genehmigungsaufgaben für alle Mandanten geteilt werden, in denen Sie und der Ersatzbenutzer vorhanden sind, aktivieren Sie das Kontrollkästchen **Kopiere in alle Mandanten**. Wenn Sie dieses Kontrollkästchen nicht aktivieren, gilt die von Ihnen eingerichtete geteilte Genehmigung bei Abwesenheit nur für den Mandanten, in dem Sie sich gerade befinden.

> [!NOTE]
> Im Vergleich zu [der Seite **Geteilte Genehmigung**, die für Administratoren gedacht ist](#geteilte-genehmigung), ist die Seite **Abwesenheit einrichten** etwas einfacher, und die folgenden zwei Felder werden in der Benutzeroberfläche nicht angezeigt:
>
>  - **Inhaber Grenzwerte und Berechtigungen verwenden**
>  - **E-Mail senden**
>
> Obwohl diese beiden Felder auf der Seite **Abwesenheit einrichten** für Benutzer verborgen sind, existieren sie im Hintergrund und sind standardmäßig aktiviert, wenn Sie die geteilte Genehmigung über diese Seite einrichten. Mit der Standardeinstellung **E-Mail senden an** werden Genehmigungs-E-Mails nur an den Ersatzgenehmiger gesendet. Wenn Sie eine dieser Standardeinstellungen ändern möchten, muss dies auf der Seite **Geteilte Genehmigung** vorgenommen werden, normalerweise von einem Administrator.