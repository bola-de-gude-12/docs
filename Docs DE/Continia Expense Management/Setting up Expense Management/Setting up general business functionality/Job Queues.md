---
title: Verfügbare Aufgabenwarteschlangen in Expense Management
date: 23-10-2024
description: Die verfügbaren Aufgabenwarteschlange in Expense Management.
id: EM-278
lang: de
---

# Verfügbare Aufgabenwarteschlangen

In Expense Management können mehrere wiederkehrende Aktivitäten mit Hilfe von Aufgabenwarteschlangen automatisiert werden, z. B. die Synchronisierung mit Continia Online, das Versenden von Genehmigungs- und Erinnerungs-E-Mails, das Versenden von Statusberichten und das Aktualisieren von Feldabhängigkeiten. Der Einrichtungsvorgang ist für alle diese Aufgaben gleich und unterscheidet sich lediglich in der verwendeten Codeunit oder dem verwendeten Bericht.

Um eine Übersicht über alle vorhandenen Aufgaben zu erhalten, gehen Sie auf die Seite **Expense Management Einrichtung** und wählen Sie **Einrichtung** > **Einrichtung Aufgabenwarteschlangenposten**. Alternativ können Sie das Suchsymbol auswählen und nach Aufgabenwarteschlangenposten suchen. Weitere Informationen zu Aufgabenwarteschlangen finden Sie im Artikel [Aufgabenwarteschlangen einrichten](@EM-65).

Expense Management verfügt über die folgenden Standardcodeunits:

| Codeunit | Name                                                   | Beschreibung                                                                                                                                                                                                                                                                            |
| -------- | ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 6086305  | CEM Online Synch. Mgt. | Automatisiert die Synchronisierung mit Continia Online, um die Einstellungen von Business Central zu aktualisieren und von Expense-Benutzern übermittelte Dokumente herunterzuladen.                                                                                    |
| 6086313  | CEM Expense Approval Email                             | Sendet regelmäßig E-Mails an Genehmiger über zur Genehmigung ausstehende Dokumente. Dies kann so eingestellt werden, dass die Aufgabe täglich ausgeführt wird, und zwar nur dann, wenn neue Dokumente zur Genehmigung vorliegen.                        |
| 6086314  | CEM Reminder Email                                     | Sendet Erinnerungs-E-Mails bezüglich ausstehender Dokumente an Expense-Benutzer. Mit der Erinnerungsfunktion können Sie konfigurieren, wie viele Tage bis zum Versand einer E-Mail vergehen sollen.                                                     |
| 6086353  | CEM Send Status Report                                 | Sendet einen detaillierten Statusbericht aller von einem Benutzer eingereichten Dokumente (gebucht oder offen). Sie können die Berichtsdetails im Inforegister **E-Mail** auf der Seite **Expense Management Einrichtung** anpassen. |
| 6086569  | CEM Update Field Dependencies                          | Validiert Feldabhängigkeiten, um Konflikte zu vermeiden, indem eine Konsistenzprüfung durchgeführt wird.                                                                                                                                                                |
| 6225300  | CEM PCD Analyze Expenses                               | Identifiziert wiederkehrende Ausgaben und benachrichtigt den Administrator, wenn diese für die automatische Verwaltung mit einem Einkaufsvertrag geeignet sind.                                                                                                         |
