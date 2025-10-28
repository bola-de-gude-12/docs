---
title: Expense Management Dokumentenspeicher einrichten
date: 16-11-2021
description: null
id: EM-144
lang: de
---

# Dokumentenspeicher einrichten

Wenn Sie Belege in Continia Expense Management importieren, werden die importierten Dateien standardmäßig direkt in der Microsoft Dynamics 365 Business Central-Datenbank gespeichert. Aufgrund von Speicherplatzbeschränkungen kann es jedoch erforderlich sein, diese Dateien stattdessen an anderen Orten zu speichern.

Um zu berechnen, wie viel Speicherplatz Sie zum Speichern Ihrer Dateien benötigen, verwenden Sie die folgenden Richtlinien:

- Eine durchschnittliche Datei benötigt etwa 500 KB Speicherplatz.
- Die überwiegende Mehrheit der Expense Management-Benutzer speichert durchschnittlich 10 Belege pro Monat.

Wenn Sie diese beiden Zahlen mit der Anzahl der voraussichtlich im System vorhandenen Benutzer multiplizieren, erhalten Sie eine ziemlich genaue Angabe darüber, wie viel Speicherplatz Sie benötigen.

In der folgenden Tabelle sind die verschiedenen Speicheroptionen aufgeführt, sodass Sie entscheiden können, welche für Sie die richtige ist:

| Speicherart                                          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                           |
| ---------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Datenbank**                                        | Dokumente werden in der Business Central-Datenbank gespeichert.                                                                                                                                                                                                                                                                                                        |
| **Azure Blob**                                       | Dokumente werden in einem Azure Blob-Container gespeichert, den Sie selbst hosten müssen. Weitere Informationen finden Sie unter [Azure Blob Storage einrichten](/Continia Expense Management/Development and Administration/Setting up Azure Blob storage.md). |
| **Dateisystem** (nur On-Premises) | Dokumente werden auf einem Dateiserver im selben LAN wie die Business Central-Dienstebene gespeichert.                                                                                                                                                                                                                                                                 |

## So ändern Sie die Einstellungen für den Dokumentenspeicher

Um den Dokumentenspeicher einzurichten, folgen Sie diesen Schritten:

1. Wählen Sie das Symbol {{search}}, geben Sie **Expense Management Einrichtung** ein und wählen Sie dann den zugehörigen Link.
2. Gehen Sie im Inforegister **Allgemein** zu **Dokumentenspeicherart** und wählen Sie im Feld Ihren bevorzugten Speichertyp aus.
3. Wenn Sie **Azure Blob-Speicher** auswählen, wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob Sie fortfahren möchten. Wählen Sie **Ja**.
4. Das Fenster **Speichereinstellungen aktualisieren** wird geöffnet. Geben Sie unter **Allgemein** die Informationen Ihres Azure Blob-Kontos ein. Wählen Sie **OK**, um das Fenster zu schließen und die Einstellungen zu aktualisieren.

## Benutzerdefinierter Speicher

Manche Kunden ziehen es vor, Dokumente in ihrem eigenen Dokumentenmanagementsystem (DMS) zu speichern. Dies ist etwas komplizierter und erfordert die Unterstützung eines Entwicklers. Wenn Sie dies jedoch benötigen, müssen Sie Ihre eigenen Speicherfunktionen implementieren.

## Informationen zum Thema

[Azure Blob Storage einrichten](/continia-expense-management/development-and-administration/setting-up-azure-blob-storage)\
[Speicher anpassen](/Continia Expense Management/Development and Administration/Development and customization/Customizing your storage.md)\
[Überlegungen bei der Migration in die Cloud](/continia-expense-management/development-and-administration/on-premises/upgrade/migrate-from-on-premises-to-cloud)
