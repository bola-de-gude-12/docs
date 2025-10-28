---
title: Grundlegendes zu Identifikationsvorlagen in Document Capture
date: 27-06-2025
description: Eine Einführung in Identifikationsvorlagen und deren Anpassung.
id: DC-471
lang: de
---

# Grundlegendes zu Identifikationsvorlagen

Zur Veranschaulichung konzentriert sich die folgende Erläuterung der Identifikationsvorlagen auf Einkaufsbelege und Kreditoren, obwohl sich die unten beschriebenen Schritte auch auf andere Geschäftsbelege und Belegherkünfte beziehen können.

Identifikationsvorlagen werden verwendet, um die Herkunft eines importierten Belegs zu identifizieren, in diesem Fall den Kreditor. Wenn eine Identifikationsvorlage eine Umsatzsteuer-Identifikationsnummer für einen eingehenden Einkaufsbeleg identifiziert, durchsucht Continia Document Capture die Tabelle Kreditor nach einem Kreditor mit einer entsprechenden Umsatzsteuer-Identifikationsnummer und wendet bei Erfolg den identifizierten Kreditor und die zugehörige Standardvorlage auf den Beleg an. Eine ausführlichere Beschreibung der Funktionsweise sowie Informationen zum Anpassen bestimmter Teile der Identifikationsvorlage finden Sie in den folgenden Abschnitten.

> [!NOTE]
> Die Verwendung von Identifikationsvorlagen ist einer von drei Schritten bei der Identifizierung der Herkunft eines Belegs. Weitere Informationen finden Sie unter [Belegherkunft und -vorlage identifizieren](@DC-109).

## Die zugrunde liegende Logik

Jede Belegkategorie in Document Capture verfügt über eine Identifikationsvorlage. Wenn Sie einen Beleg in Document Capture importieren, versucht die Identifikationsvorlage, einen passenden Datensatz in der Herkunftstabelle mit diesem Beleg zu verknüpfen. Für die Belegkategorie **EINKAUF** wird dabei die Umsatzsteuer-Identifikationsnummer des Belegs erfasst und die Tabelle Kreditor nach einem Kreditor mit einer passenden Umsatzsteuer-Identifikationsnummer durchsucht.

Die Identifikationsvorlage besteht aus einem einzigen Feld, **Ust.-IdNr.**, das mehrere verschiedene Suchtexte und Regeln verwendet, um die korrekte Umsatzsteuer-Identifikationsnummer jedes eingehenden Belegs zu identifizieren. Sowohl die Suchtexte als auch die Regeln können angepasst werden, wie unter [So bearbeiten Sie Suchtexte](#so-bearbeiten-sie-suchtexte) und [So bearbeiten Sie Suchregeln](#so-bearbeiten-sie-suchregeln) beschrieben, und gemeinsam bilden Sie die Grundlage des Identifikationsprozesses: Wenn die Identifikationsvorlage basierend auf Ihrer Auswahl von Suchtexten den Suchtext eines importierten Belegs erkennt, sucht sie nach einem entsprechenden Wert rechts vom Suchtext oder darunter. Wenn ein Wert gefunden wird, validiert sie diesen Wert anhand der ausgewählten Regeln, um sicherzustellen, dass das Format des Werts korrekt ist – mit anderen Worten, es wird bestätigt, dass es sich bei dem erfassten Wert tatsächlich um eine Umsatzsteuer-Identifikationsnummer handelt.

Sobald eine Umsatzsteuer-Identifikationsnummer erfasst wurde, führt Document Capture die Codeunit **CDC Purch Doc. - Identificat.** aus, um einen Kreditor mit einer entsprechenden Umsatzsteuer-Identifikationsnummer in der Tabelle Kreditor zu identifizieren. Sie können die Codeunit auf der Identifikationsvorlagenkarte im Inforegister **Codeunits** unter **Nach Capture** anzeigen.

> [!TIP]
> Um die Liste der mit einem Kreditor verknüpften Vorlagen anzuzeigen, verwenden Sie die Aktion **Belegvorlagen** aus der Kreditorenliste oder der **Kreditorenkarte**. So zeigen Sie diese Aktion an, die standardmäßig ausgeblendet ist:
>
> 1. Suchen Sie ({{search}}) nach **Kreditoren** und wählen Sie den entsprechenden Eintrag aus.
> 2. Klicken Sie in der Liste der Kreditor oben rechts auf **Einstellungen** ({{settings}}) > **Personalisieren**.
> 3. Erweitern Sie in der Aktionsleiste die Aktionsgruppe **Zugehörig**.
> 4. Bewegen Sie den Cursor über **Kreditoren > Belegvorlagen** und klicken Sie dann auf **Anzeigen**, um die Aktion verfügbar zu machen.

## So bearbeiten Sie Suchtexte

Sie können genau festlegen, nach welchen Suchtexten Document Capture suchen soll, um Umsatzsteuer-Identifikationsnummern in eingehenden Belegen zu identifizieren. Gehen Sie hierzu wie folgt vor:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Öffnen Sie die entsprechende Belegkategorie. Um beispielsweise die Kategorie für Einkaufsbelege zu öffnen, klicken Sie auf die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und klicken Sie dann auf **Bearbeiten** in der Aktionsleiste.
3. Suchen Sie im Inforegister **Vorlagen** in der Liste der Vorlagen die Vorlage **EINKAUF-ID**. Klicken Sie auf das Symbol {{vertical-dots}} und dann auf **Bearbeiten**, um die Vorlagenkarte zu öffnen.
4. Klicken Sie im Inforegister **Felder** in der Spalte **Feldname** auf die Option **UST ID Nummer**, um die Vorlagenfeldkarte zu öffnen.
5. Klicken Sie in der Aktionsleiste auf **Suchtexte**, um die Seite zum Bearbeiten zu öffnen.
6. Bearbeiten Sie die Liste der Suchtexte mit den Schaltflächen **Neu** und **Löschen** in der Aktionsleiste nach Bedarf.
7. Klicken Sie auf **Schließen**, wenn Sie fertig sind.

Document Capture durchsucht dann jeden einzelnen eingehenden Beleg nach den in dieser Liste enthaltenen Suchtexten, um die Umsatzsteuer-Identifikationsnummer jedes Belegs zu ermitteln, um die Herkunft des Belegs zu identifizieren.

## So bearbeiten Sie Suchregeln

Sie können auch die genauen Regeln festlegen, die Document Capture bei der Identifikation von Umsatzsteuer-Identifikationsnummern in eingehenden Belegen verwenden soll. Gehen Sie hierzu wie folgt vor:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Öffnen Sie die entsprechende Belegkategorie. Um beispielsweise die Kategorie für Einkaufsbelege zu öffnen, klicken Sie auf die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und klicken Sie dann auf **Bearbeiten** in der Aktionsleiste.
3. Suchen Sie im Inforegister **Vorlagen** in der Liste der Vorlagen die Vorlage **EINKAUF-ID**. Klicken Sie auf das Symbol {{vertical-dots}} und dann auf **Bearbeiten**, um die Vorlagenkarte zu öffnen.
4. Klicken Sie im Inforegister **Felder** in der Spalte **Feldname** auf die Option **UST ID Nummer**, um die Vorlagenfeldkarte zu öffnen.
5. Klicken Sie in der Aktionsleiste auf **Regeln**, um die Seite zum Bearbeiten zu öffnen.
6. Bearbeiten Sie die Liste der Regeln mit den Schaltflächen **Neu** und **Löschen** in der Aktionsleiste nach Bedarf.
7. Klicken Sie auf **Schließen**, wenn Sie fertig sind.

Document Capture durchsucht dann jeden einzelnen eingehenden Beleg anhand der in dieser Liste enthaltenen Regeln, um die Umsatzsteuer-Identifikationsnummer jedes Belegs zu ermitteln. Immer wenn mindestens eine Regel mit dem Format eines erfassten Werts übereinstimmt, wird dieser Wert als gültige Umsatzsteuer-Identifikationsnummer akzeptiert. Wie oben erwähnt, kann diese Umsatzsteuer-Identifikationsnummer dann von Document Capture verwendet werden, um die Herkunft des Belegs zu identifizieren.
