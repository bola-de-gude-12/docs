---
title: Benutzerspezifische Listen von Genehmigern für die Genehmigungsweiterleitung erstellen
date: 27-04-2023
description: Einrichten einer Liste verfügbarer Genehmiger für alle Benutzer, die zum Weiterleiten von Belegen zur Genehmigung ausgewählt werden können
id: DC-138
lang: de
---

# Benutzerspezifische Listen von Genehmigern für die Genehmigungsweiterleitung erstellen

Genehmiger erhalten in Ihrem Unternehmen möglicherweise gelegentlich Genehmigungsanforderungen, die für andere Genehmiger relevanter sind oder einfach versehentlich an sie gesendet wurden. In solchen Fällen müssen sie die Genehmigungsanforderungen an die richtigen Genehmiger weiterleiten. Sie können ihnen diesen Prozess erleichtern, indem Sie eine Liste der verfügbaren Genehmiger zur Auswahl einrichten. Sie müssen so nicht alle Genehmiger im gesamten Unternehmen durchgehen, um den richtigen Genehmiger zu finden, wenn sie Belege zur Genehmigung weiterleiten. Stattdessen wird ihnen eine begrenzte Liste mit den richtigen Genehmigern zur Auswahl angezeigt, die speziell für sie eingerichtet wurde.

## So richten Sie eine Liste von Genehmigern für die Genehmigungsweiterleitung ein

Um eine Liste einzurichten, die die Anzahl der verfügbaren Genehmiger pro Benutzer einschränkt, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Genehmigungsweiterleitung** ein, und wählen Sie dann den zugehörigen Link.
2. Geben Sie in der Spalte **Inhaber Benutzer-ID** der Tabelle die ID des Benutzers ein, dessen Berechtigungen für die Genehmigungsweiterleitung Sie bearbeiten möchten, oder wählen Sie sie aus.
3. Geben Sie in der Spalte **Weiterleiten an Benutzer-ID** die ID des Genehmigers ein, an den der ausgewählte Benutzer Genehmigungsanforderungen weiterleiten kann, oder wählen Sie sie aus.
   > [!NOTE]
   > Mit den Feldern **Inhaber Benutzer-ID** und **Weiterleiten an Benutzer-ID** kann jeweils nur ein Benutzer angegeben werden und nicht mehrere. Wenn Sie also möchten, dass der Benutzer Genehmigungsanforderungen an mehr als einen Genehmiger senden kann, müssen Sie der Tabelle für diesen Benutzer weitere Zeilen hinzufügen (wie in Schritt 4 unten beschrieben).
4. **Optional**: Wenn dem Benutzer für die Weiterleitung von Genehmigungsanforderungen weitere Genehmiger zur Verfügung stehen sollen, wiederholen Sie die Schritte 2–3 oben.

Der Benutzer unter **Inhaber Benutzer-ID** kann jetzt Genehmigungsanforderungen nur an die Genehmiger weiterleiten, die Sie unter **Weiterleiten an Benutzer-ID** angegeben haben. Dies kann sowohl in Microsoft Dynamics 365 Business Central als auch im Continia Web Approval Portal erfolgen.

## Informationen zum Thema

[Genehmigungsanforderungen bearbeiten](@DC-39)