---
title: Genehmigungsabläufe verwenden
date: 01-10-2024
description: So weisen Sie einem Einkaufsbeleg einen Genehmigungsablauf zu, einschließlich der Zuweisung mithilfe von Vorlagen
id: DC-33
lang: de
---

# Genehmigungsabläufe verwenden

Ein Genehmigungsablauf ist eine benutzerdefinierte Liste von Genehmigern, die für die Genehmigung der jeweiligen Einkaufsbelege erforderlich sind. In diesem Artikel wird die Verwendung von Genehmigungsabläufen anhand von Einkaufsrechnungen veranschaulicht. Die Funktionalität gilt jedoch auch für Gutschriften.

Nachdem Sie [einen Genehmigungsablauf eingerichtet](@DC-30) haben, können Sie ihn einem Beleg zuweisen, um genau festzulegen, wer den Beleg genehmigen soll und in welcher Reihenfolge. Wenn Sie einem Beleg einen Genehmigungsablauf zuweisen, überschreibt dieser den standardmäßigen Prozess für die Einkaufsgenehmigung, der auf Einkäufercodes basiert.

Alle Genehmiger im Genehmigungsablauf müssen den Beleg genehmigen, bevor er gebucht werden kann, und dies muss in der Reihenfolge vorgenommen werden, die Sie während der Einrichtung festgelegt haben.

> [!IMPORTANT]
> Das Feld **Genehmigungsablaufcode**, das erforderlich ist, wenn Sie Belegen Genehmigungsabläufe zuweisen, ist nur sichtbar, wenn in der **Document Capture Einrichtung** [Einkaufsgenehmigung aktiviert wurde](@DC-22).

## So weisen Sie einer Rechnung einen Genehmigungsablauf zu

1. Gehen Sie im Rollencenter unter **Continia Document Capture Aktivitäten** zu **Einkaufsgenehmigung - Rechnungen** und wählen Sie **Offene Rechnungen** aus, um die Liste der offenen Einkaufsrechnungen zu öffnen.
2. Öffnen Sie in der Liste die Rechnung, der Sie einen Genehmigungsablauf zuweisen möchten.
3. Gehen Sie im Inforegister **Allgemein** zu **Genehmigungsablaufcode** und wählen Sie die drei Punkte rechts aus, um die Seite **Genehmigungsabläufe** zu öffnen.
4. Wählen Sie den Genehmigungsablaufcode aus, den Sie auf die Einkaufsrechnung anwenden möchten, und klicken Sie dann auf **OK**, um die Seite zu schließen.

Der Code wird anschließend unter **Genehmigungsablaufcode** hinzugefügt und der ausgewählte Genehmigungsablauf wird der Rechnung zugewiesen. Wenn Sie die Rechnung zur Genehmigung einreichen, wird sie in der angegebenen Reihenfolge an die Genehmiger im Genehmigungsablauf gesendet.

> [!NOTE]
> Genehmigungsablaufcodes können auch mit erweiterten Genehmigungen verwendet werden, vorausgesetzt, dass der Beleg zur Einkaufskategorie gehört und es sich zum Beispiel um eine Gutschrift, Bestellung, Einkaufsrechnung oder Reklamation handelt.

## So weisen Sie Genehmigungsabläufe mit Vorlagen zu

Wenn Sie zur Bestimmung der Beleggenehmiger und dessen Reihenfolge immer Genehmigungsabläufe verwenden möchten, können Sie den entsprechenden Genehmigungsablaufcode in einer Belegvorlage angeben, die den Code automatisch allen Belegen zuweist, die diese Vorlage verwenden.

Um einen Genehmigungsablaufcode auf eine Vorlage anzuwenden, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie den Code **EINKAUF** aus, um das Belegjournal zu öffnen.
3. Wählen Sie in der Belegliste den Beleg aus, dessen Vorlage Sie bearbeiten möchten.
4. Klicken Sie in der Aktionsleiste auf **Vorlage** > **Vorlagenkarte**.
5. Wählen Sie im Inforegister **Einkaufsbelege** unter **Genehmigung** das Feld **Genehmigungsablaufcode** und anschließend den Code aus, den Sie auf die Vorlage anwenden möchten.

Der ausgewählte Genehmigungsablaufcode wird jetzt der Vorlage hinzugefügt und somit allen Belegen zugewiesen, die diese Vorlage verwenden.

## Informationen zum Thema

[Genehmigungsabläufe erstellen](@DC-30)\
[Document Capture Einrichtung](@DC-22)