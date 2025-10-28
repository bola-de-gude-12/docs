---
title: Dokumentenspeicher einrichten
date: 09-07-2024
description: null
id: DC-3
lang: de
---

# Dokumentenspeicher einrichten

Wenn Sie Belege in Continia Document Capture importieren, werden die importierten Dateien standardmäßig direkt in der Microsoft Dynamics 365 Business Central-Datenbank gespeichert. Aufgrund von Speicherplatzbeschränkungen kann es jedoch erforderlich sein, diese Dateien stattdessen an anderen Orten zu speichern.

Um zu berechnen, wie viel Speicherplatz Sie zum Speichern Ihrer Dateien benötigen, verwenden Sie die folgenden Richtlinien:

- Eine durchschnittliche PDF-Datei benötigt etwa 100 KB Speicherplatz pro Seite.
- Bei der überwiegenden Mehrheit der Document Capture-Kunden hat eine Rechnung im Durchschnitt zwei Seiten.

Wenn Sie diese beiden Werte mit der Gesamtzahl Ihrer PDF-Dateien multiplizieren, können Sie den benötigten Speicherplatz gut abschätzen.

In der folgenden Tabelle sind die verschiedenen Speicheroptionen aufgeführt, sodass Sie entscheiden können, welche für Sie die richtige ist:

| Speicherart                                                    | Beschreibung                                                                                                                                                                                                                                                                                                                                                                         |
| -------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Dateisystem** (nur On-Premises)           | Dokumente werden auf einem Dateiserver im selben LAN wie die Business Central-Dienstebene gespeichert.                                                                                                                                                                                                                                                               |
| **Datenbank**                                                  | Dokumente werden in der Business Central-Datenbank gespeichert.                                                                                                                                                                                                                                                                                                      |
| **Azure Blob Storage**                                         | Dokumente werden in einem Azure Blob-Container gespeichert, den Sie selbst hosten müssen. Weitere Informationen finden Sie unter [Azure Blob Storage einrichten](/Continia Document Capture/Development and Administration/Setting up Azure Blob storage.md). |
| **Continia File Service** (nur On-Premises) | Dokumente werden in Cloud-kompatiblen, vordefinierten Repositories gespeichert, die auf einen bestimmten Ordner verweisen. Dieser Ordner kann lokal oder freigegeben sein. Informationen zum Einrichten finden Sie unter [Continia File Service installieren](@DC-124).                                                              |

## So ändern Sie die Einstellungen für den Dokumentenspeicher

Um den Dokumentenspeicher einzurichten, folgen Sie diesen Schritten:

1. Wählen Sie das Symbol {{search}}, geben Sie **Speichermigrationsassistent** ein, und wählen Sie dann den zugehörigen Link.
2. Folgen Sie den Anweisungen auf dem Bildschirm.
3. Wenn Sie fertig sind, wählen Sie **Beenden**, um den Assistenten zu schließen und die Einstellungen zu übernehmen.

So können Sie eine Speichermigration überprüfen, pausieren und fortsetzen:

- Wählen Sie das Symbol {{search}}, geben Sie **Speichermigrationsassistent** ein, und wählen Sie dann den zugehörigen Link.

Um erweiterte Speicherkonfigurationen vorzunehmen (z. B. das Ändern von Speichereinstellungen ohne Datenmigration), folgen Sie diesen Schritten:

1. Wählen Sie das Symbol {{search}}, geben Sie **Document Capture Einrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Gehen Sie im Inforegister **Allgemein** zu **Dokumentenspeicherart** und wählen Sie im Feld Ihren bevorzugten Speichertyp aus.
3. Wenn Sie **Azure Blob-Speicher** auswählen, wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob Sie fortfahren möchten. Wählen Sie **Ja**.
4. Das Fenster **Speichereinstellungen aktualisieren** wird geöffnet. Geben Sie unter **Allgemein** die Informationen Ihres Azure Blob-Kontos ein. Klicken Sie auf **OK**, um das Fenster zu schließen und die Einstellungen zu aktualisieren.

## Benutzerdefinierter Speicher

Manche Kunden ziehen es vor, Dokumente in ihrem eigenen Dokumentenmanagementsystem (DMS) zu speichern. Dies ist etwas komplizierter und erfordert die Unterstützung eines Entwicklers. Wenn Sie dies jedoch benötigen, müssen Sie Ihre eigenen Speicherfunktionen implementieren. Weitere Informationen hierzu finden Sie unter [Benutzerdefinierten Speicher einrichten](/Continia Document Capture/Development and Administration/Development and customization/Customizing your storage.md).

## Informationen zum Thema

[Azure Blob Storage einrichten](/Continia Document Capture/Development and Administration/Setting up Azure Blob storage.md)\
[Benutzerdefinierten Speicher einrichten](/Continia Document Capture/Development and Administration/Development and customization/Customizing your storage.md)\
[Überlegungen bei der Migration in die Cloud](@DC-106#considerations-when-migrating-to-the-cloud)

<style>
  .content table tr td:nth-child(1) {
    width: 130px;
  }
  .content table tr td:nth-child(2) {
    width: 700px;
  }  
</style>
