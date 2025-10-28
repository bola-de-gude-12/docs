---
title: Expense Management von Business Central On-Premises zur Cloud migrieren
date: 09-07-2025
description:
id: EM-112
lang: de
---

# Expense Management von Business Central On-Premises zur Cloud migrieren

Wenn Ihr Unternehmen Expense Management in Microsoft Dynamics NAV/Business Central On-Premises verwendet, aber in die Cloud wechseln möchte, können Sie mithilfe dieser Anleitung zu Business Central Online migrieren.

Die Migration von Expense Management zu Business Central Online basiert auf dem Standard-Cloudmigrationstool von Microsoft. Weitere Informationen finden Sie in der Microsoft-Dokumentation unter [Migrate On-Premises Data to Business Central Online](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data).

## Überlegungen zur Dokumentenspeicherart bei der Migration in die Cloud

_Vor_ der Migration müssen Sie Ihre **Dokumentenspeicherart** festlegen. Wir empfehlen, diese auf Datenbank einzustellen, basierend auf den folgenden Überlegungen:

- Der Speichertyp **Dateisystem**/**File Service** ist in Business Central Online nicht verfügbar. Daher müssen Sie vor der Migration einen anderen Speichertyp (zum Beispiel **Datenbank** oder **Azure Blob Storage**) auswählen.
- Wenn Sie viele Dokumente haben, speichert der Speichertyp **Datenbank** alle Dokumente für die Migration in der Datenbank und stellt sicher, dass keine Dateien verloren gehen. Denken Sie daran, dass Dokumente Datenbankspeicherplatz beanspruchen und die Datenübertragung zu Business Central Online zeitaufwändiger machen können. Sofern Sie keinen zusätzlichen Speicherplatz erwerben, was kostspielig sein kann, steht Ihnen nur begrenzter Speicherplatz zur Verfügung (80 GB plus zusätzliche Speicherkapazität, abhängig von der Anzahl Ihrer Business Central-Lizenzen). Weitere Informationen finden Sie in diesem [Microsoft-Artikel](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-capacity#storage).
- Wenn Sie viele Daten, aber keine Dokumente übertragen müssen, können Sie Ihre Datenbank viel schneller in Business Central Online übertragen, da darin keine Dokumente gespeichert sind. Wenn Sie **Azure Blob Storage** bevorzugen, können Sie _nach_ der Migration darauf umsteigen.

Weitere Informationen zu Speichertypen und deren Einrichtung finden Sie unter [Dokumentenspeicher einrichten](@EM-144).

## Voraussetzungen

Bevor Sie Daten zu Business Central Online migrieren, müssen Sie die folgenden Schritte in Ihrer On-Premises-Umgebung ausführen, um sie für die Cloudmigration vorzubereiten.

1. Führen Sie ein Upgrade auf Business Central April 2019 (BC v14) oder höher durch, sofern Sie dies nicht bereits zu einem früheren Zeitpunkt getan haben. Informationen hierzu finden Sie unter [Upgrade von NAV/Business Central mit einer Installation von Expense Management](@EM-107).
2. Führen Sie ein Upgrade auf Expense Management 2021 R2 (8.00) oder höher durch, sofern Sie dies nicht bereits getan haben.
3. Wie im vorherigen Abschnitt erwähnt, müssen Sie zum Zeitpunkt der Migration die **Dokumentenspeicherart** auf **Datenbank** einstellen; andernfalls werden keine Dateien migriert. Bei Bedarf können Sie den Speichertyp später ändern (z. B. **Azure Blob Storage**). Der Speichertyp **Dateisystem** ist in Business Central Online jedoch nicht verfügbar.

> [!NOTE]
> Bisher mussten Sie auf die neuesten verfügbaren Versionen von Business Central und Expense Management aktualisieren, um zur Cloud migrieren zu können. Dies ist nicht mehr erforderlich, wenn Sie Version 24.1.0 oder höher von Expense Management in Ihrer Business Central-Onlineumgebung (Ziel) verwenden.

## Daten in die Cloud migrieren

Nachdem Sie Ihre On-Premises-Umgebung für die Migration vorbereitet haben, können Sie Ihre Daten zu Business Central Online migrieren. Führen Sie dazu folgende Schritte in Ihrer neuen Online-Umgebung durch:

1. Führen Sie das Microsoft-Cloudmigrationstool aus: Wählen Sie das Symbol {{search}}, geben Sie **Einrichtung für die Cloud-Migration** ein und wählen Sie dann den entsprechenden Link, um den Einrichtungsassistenten **Einrichtung für die Cloud-Migration** zu öffnen. Weitere Informationen finden Sie unter [Run the assisted setup guide](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data#run-the-assisted-setup-guide) (Microsoft-Artikel).

2. Befolgen Sie die Anweisungen auf dem Bildschirm, um die Einrichtung abzuschließen.

   > [!IMPORTANT]
   > Sie können Expense Management nicht verwenden, wenn das Cloudmigrationstool ausgeführt wird, da dies den Migrationsprozess unterbrechen würde.

3. Nachdem der Migrationsprozess abgeschlossen ist, folgen Sie den Schritten in der **Post Migration Checklist**, um sicherzustellen, dass alle notwendigen Aktionen ausgeführt wurden.

   > [!IMPORTANT]
   >
   > Bevor Sie die Cloudmigration deaktivieren, müssen Sie die Art der Onlineumgebung berücksichtigen, zu der Sie migriert sind:
   >
   > - **Bei der Migration in eine Sandbox-Umgebung**: Ihre ursprünglichen Client-Anmeldeinformationen werden automatisch gelöscht. Wenn Sie Expense Management anschließend als Cloud-Lösung aktivieren (Schritte 5–6), werden neue Client-Anmeldeinformationen erstellt.
   > - **Bei der Migration in eine Produktionsumgebung**: Ihre vorhandenen Client-Anmeldeinformationen für die Online-Umgebung werden wiederverwendet.

4. Deaktivieren Sie die Cloudmigration und definieren Sie Benutzerzuordnungen zwischen On-Premises und Cloud. Weitere Informationen finden Sie unter „Disable Cloud Migration“ und „Define User Mappings“ in der Tabelle unter [Manage the migration](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data#manage-the-migration) (Microsoft-Artikel).

5. Im **Rollencenter** wird die folgende Benachrichtigung angezeigt: „Continia Expense Management wurde von On-Premises in die Cloud migriert. Möchten Sie es aktivieren?" Wählen Sie **Ja**, um die Aktivierungsanleitung zu öffnen.

6. Folgen Sie der Anleitung, um Expense Management als Cloud-Lösung zu aktivieren.

   > [!NOTE]
   > Wenn das Continia Web Approval Portal in der alten On-Premises-Umgebung aktiviert war, müssen Sie es erneut einrichten. Weitere Informationen finden Sie unter [Web-Genehmigung einrichten](@EM-82).

Sie haben jetzt alle Expense Management-Daten migriert und die App ist für die Verwendung in Business Central Online bereit. Wenn Sie wie oben beschrieben zu Business Central Online migrieren, werden die Client-Anmeldeinformationen (Client-ID und Kennwort) von Ihrer On-Premises-Umgebung in die Online-Umgebung kopiert unabhängig davon, von welcher Art von Umgebung (Produktion oder Test) und in welche Umgebung (Produktion oder Sandbox) Sie migrieren.

## Informieren Sie Continia über die Migration

Um sicherzustellen, dass Ihr Rechnungsstellungsprozess reibungslos und problemlos abläuft, wenn Sie eine Continia-Lösung wie Expense Management von einer On-Premises-Umgebung in die Cloud migrieren, empfehlen wir Ihnen, die folgenden Punkte zu berücksichtigen:

- Als Partner oder Kunde liegt es in Ihrer Verantwortung, Ihren On-Premises-Vertrag mit Continia zu kündigen, nachdem Sie die gesamte Lösung migriert haben und sie in der Cloud voll funktionsfähig ist.
- Die meisten Kunden migrieren ihre Lösungen schrittweise während einer Übergangsphase, die bis zu mehreren Monaten dauern kann. Der Prozess ist jedoch von Organisation zu Organisation unterschiedlich.
- Wenn der Migrationsprozess abgeschlossen ist, müssen Sie Continia über die Kündigung informieren, indem Sie eine E-Mail an accounting@continia.com senden. Dort wird Ihnen dann der Restbetrag Ihres On-Premises-Abrechnungszeitraums gutgeschrieben.

> [!IMPORTANT]
> Bitte informieren Sie uns aus administrativen Gründen über die Kündigung, bevor Ihnen die Rechnung für die Verlängerung Ihres On-Premises-Vertrags um 12 Monate ausgestellt wird.

## Informationen zum Thema

[How to migrate Document Capture and Expense Management to Business Central 2021 release wave 1 (BC18) in BC cloud](https://continia.zendesk.com/hc/en-us/articles/360014053519-How-to-migrate-Document-Capture-and-Expense-Management-to-Microsoft-Dynamics-365-Business-Central-2020-release-wave-2-BC17-in-Microsoft-Business-Central-cloud?_ga=2.13216625.79067120.1621259529-972812024.1595933616)