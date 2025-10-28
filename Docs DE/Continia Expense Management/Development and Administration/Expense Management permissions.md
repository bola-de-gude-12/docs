---
title: Expense Management-Berechtigungen
date: 22-08-2025
description:
id: EM-62
lang: de
---

# Expense Management-Berechtigungen

{{include "permissions" "Expense Management"}}

## Standardmäßige Continia-Berechtigungssätze

| Berechtigungssatz | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| ----------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CSC BASIC         | Dieser Berechtigungssatz gewährt Zugriff auf alle Continia Core-Funktionen und ermöglicht Ihnen, den Aktivierungsstatus von Expense Management abzurufen. Allen Benutzern von Expense Management muss der Berechtigungssatz CSC BASIC zugewiesen werden, um sicherzustellen, dass alle Standardfunktionen wie vorgesehen funktionieren.                                                                                                                                                                                                                              |
| CSC APP SETUP     | Mit diesem Berechtigungssatz können Sie Continia-Produkte, einschließlich Continia Core, aktivieren. Es wird hauptsächlich für die Produktinstallation und – in Business Central Online – beim Vornehmen von Änderungen an Abonnementvereinbarungen verwendet, beispielsweise beim Auswählen und Abwählen abonnierter Module. Der Berechtigungssatz wird hauptsächlich bei Onlinebereitstellungen von Business Central benötigt, da Benutzer, die lokale Umgebungen einrichten, normalerweise stattdessen den CEM-SUPER-Berechtigungssatz verwenden. |

## Expense Management-spezifische Berechtigungssätze

| Berechtigungssatz | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CEM-ALL           | Mit diesem Berechtigungssatz können Sie alle grundlegenden Expense Management-Vorgänge in Business Central durchführen. Allen Expense Management-Benutzern von Version 26 und vorherigen Versionen muss der Berechtigungssatz CSC BASIC zugewiesen werden, um sicherzustellen, dass alle Standardfunktionen wie vorgesehen funktionieren. <br>Der Berechtigungssatz CEM-ALL ist für Benutzer erforderlich, die Expense Management nicht auf einem System verwenden, auf dem Expense Management installiert und aktiv ist. Diese Benutzer vermeiden dann, dass bei der Interaktion mit der Standardfunktionalität von Business Central Expense Management-Berechtigungsfehler auftreten. Expense Management verfolgt standardmäßige Business Central-Tabellen zum Aktualisieren von Lookup-Werten für Feldtypen. Dieser Berechtigungssatz bietet Zugriff zum Aktualisieren dieser Lookup-Werte sowie Lesezugriff auf die Expense Management Einrichtung-Tabelle. |
| CEM-APPROVE       | Mit diesem Berechtigungssatz können Sie alle grundlegenden Genehmigungsvorgänge ausführen, wenn Sie Dokumente in Business Central oder im Continia Web Approval Portal genehmigen: _Genehmigen_, _Ablehnen_, _Auf Abwarten setzen_, _Weiterleiten_ und _Bemerkung hinzufügen_. Der Berechtigungssatz allein reicht nicht aus, sondern sollte zusammen mit [CDC-APPROVE](/continia-document-capture/development-and-administration/document-capture-permissions#document-capture-specific-permission-sets) verwendet werden, da Expense Management das allgemeine Document Capture-Framework zur Genehmigung verwendet.                                                                                                                                                                                                                                                                                                                                                                                          |
| CEM-SUPER         | Wenn Ihnen dieser Berechtigungssatz zugewiesen wird, erhalten Sie vollen Zugriff auf alle Expense Management-Tabellen. Dies gilt in der Regel für Benutzer, die Expense Management einrichten.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| CEM-NAVUSER       | Expense-Benutzer, die Business Central zur Registrierung von Ausgaben verwenden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

> [!NOTE]
> Um die geteilte Genehmigung konfigurieren und Benutzer in das Web Approval Portal exportieren zu können, müssen Sie Zugriff auf alle Mandanten haben.

## Berechtigungssätze für Kreditorenbuchhalter und ähnliche Rollen

Wenn Ihre Rolle darin besteht, Rechnungen und andere Geschäftsdokumente zu bearbeiten (z. B. als Administrator oder Kreditorenbuchhalter), müssen Ihnen mindestens die folgenden Berechtigungssätze für die für Sie relevanten Mandanten zugewiesen sein:

- CSC BASIC
- CEM-SUPER
- D365 BASIC<a href="#footnote-1.1"><sup>1
- Ein Kreditorenberechtigungssatz Ihrer Wahl aus Standard Business Central

<small style><div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.1">Der Name des Berechtigungssatzes hängt von Ihrer Version von NAV/Business Central ab.</li>
  </ol>
</div>
</small>

## Berechtigungssätze für Genehmiger

Wenn Sie Genehmiger sind (ob in Microsoft Dynamics NAV/Business Central oder im Web Approval Portal), müssen Ihnen mindestens die folgenden Berechtigungssätze für die für Sie relevanten Mandanten zugewiesen sein:

- CSC BASIC
- CDC-ALL
- CEM-APPROVE
- CDC-APPROVE
- D365 BASIC<a href="#footnote-1.2"><sup>1

<small style><div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.2">Der Name des Berechtigungssatzes hängt von Ihrer Version von NAV/Business Central ab.</li>
  </ol>
</div>
</small>

## Berechtigungssätze für Prüfer

Wenn Sie ein Einkaufsvertragsprüfer sind (ob in Microsoft Dynamics NAV/Business Central oder im Web Approval Portal), müssen Ihnen mindestens die folgenden Berechtigungssätze für die für Sie relevanten Mandanten zugewiesen sein:

- CSC BASIC
- CDC-ALL
- CDC-APPROVE
- D365 BASIC<a href="#footnote-1.3"><sup>1

<small style><div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.3">Der Name des Berechtigungssatzes hängt von Ihrer Version von NAV/Business Central ab.</li>
  </ol>
</div>
</small>

## Berechtigungen beim Implementieren von Service Packs aktualisieren

Wenn Sie Expense Management aktualisieren oder ein Service Pack in Business Central Online oder Apps anwenden, werden die Berechtigungen immer automatisch aktualisiert.

Wenn Sie jedoch ein Service Pack in FOB-basierten Versionen von NAV/Business Central anwenden, müssen Sie die folgende Codeunit manuell ausführen, wenn Berechtigungen geändert wurden:

- 6086320 (**CEM Create EM Roles**) – zum Aktualisieren der Expense Management-spezifischen Berechtigungssätze

Durch das Ausführen dieser Codeunit werden lediglich Berechtigungen hinzugefügt oder geändert; es werden keine Berechtigungen gelöscht.

<style>
  .content table tr td:nth-child(1) {
    width: 90px;
  }
  .content table tr td:nth-child(2) {
    width: 640px;
  }  
</style>