---
title: Document Capture von Business Central On-Premises zur Cloud migrieren
date: 08-07-2025
description: So migrieren Sie Document Capture von Business Central On-Premises zur Cloud.
id: DC-106
lang: de
---

# Document Capture von Business Central On-Premises zur Cloud migrieren

Wenn Ihr Unternehmen Continia Document Capture in Microsoft Dynamics NAV/Business Central On-Premises verwendet, aber in die Cloud wechseln möchte, können Sie mithilfe der Anleitung unten zu Business Central Online migrieren.

Die Migration von Document Capture zu Business Central Online basiert auf dem Standard-Cloudmigrationstool von Microsoft. Weitere Informationen finden Sie unter [Migrate on-premises data to Business Central Online](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data) (Microsoft-Artikel).

> [!NOTE]
> Ab 2025 Release Wave 1 (v26)wird das direkte Upgrade von Business Central 2019 (v14) auf die neueste Version nicht mehr unterstützt. Der unterstützte Upgradepfad erfolgt über 2024 Release Wave 2 (v25) und dann auf v26. Weitere Informationen finden Sie unter [Deprecated features in the platform - clients, server, and database](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-platform#changes-in-2025-release-wave-1-version-260) (Microsoft-Artikel).

## Überlegungen bei der Migration zur Cloud

Im Folgenden werden einige der wichtigsten Überlegungen und Aspekte genannt, die vor der Migration zu beachten sind:

- Der Speichertyp **Dateisystem**/**File Service** ist in Business Central Online nicht verfügbar. Daher müssen Sie vor der Migration einen anderen Speichertyp (zum Beispiel **Datenbank** oder **Azure Blob Storage**) auswählen.
- Wenn Sie **Datenbank** wählen, werden alle Dokumente in der Datenbank gespeichert, wodurch Datenbankspeicherplatz belegt wird und die Datenübertragung zu Business Central Online zeitaufwändiger wird. Falls Sie große Datenmengen übertragen müssen, sollten Sie stattdessen die Auswahl von **Azure Blob Storage** in Erwägung ziehen, da Ihnen sonst nur begrenzter Speicherplatz zur Verfügung steht (80 GB plus zusätzliche Speicherkapazität basierend auf Ihrer Anzahl an Business Central-Lizenzen) – es sei denn, Sie erwerben zusätzlichen Speicherplatz, was kostspielig sein kann. Weitere Informationen finden Sie im Abschnitt **Storage** in dem Artikel [Managing capacity](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-capacity#storage) (Microsoft-Artikel).
- Wenn Sie **Azure Blob Storage** auswählen, wird empfohlen, vor dem Starten der Migration zu diesem Speichertyp zu wechseln. Dadurch können Sie Ihre Datenbank viel schneller in Business Central Online übertragen, da in der Datenbank keine Dokumente gespeichert sind. Weitere Informationen finden Sie unter [Azure Blob Storage einrichen](https://docs.continia.com/de-de/continia-document-capture/development-and-administration/setting-up-azure-blob-storage).
- Sobald Sie zu Business Central Online migriert sind, können Sie On-Premises-OCR nicht mehr verwenden.

> [!NOTE]
> Es ist nicht mehr erforderlich, den Assistenten vor der Migration auszuführen, um TIFF- in PNG-Dateien zu konvertieren, da diese jetzt beim Zugriff auf Dokumente generiert werden.

Weitere Informationen zu Speichertypen und deren Einrichtung finden Sie unter [Dokumentenspeicher einrichten](@DC-3).

## So bereiten Sie Ihre On-Premises-Umgebung auf die Cloudmigration vor

Bevor Sie Daten zu Business Central Online migrieren, müssen Sie die folgenden Schritte in Ihrer On-Premises-Umgebung ausführen:

1. Führen Sie ein Upgrade auf Business Central April 2024 Release Wave 2 (BC v25) oder höher durch, sofern Sie dies nicht bereits zu einem früheren Zeitpunkt getan haben. Informationen hierzu finden Sie unter [Upgrade von NAV/Business Central mit einer Installation von Document Capture](Upgrading NAV or Business Central with Document Capture installed/Overview.md).

2. Führen Sie ein Upgrade auf Document Capture 2024 R2 (25.00) oder höher durch, sofern Sie dies nicht bereits getan haben.

> [!NOTE]
> Es gibt einen direkten Upgradepfad von Document Capture 4.50 oder höher auf Document Capture 2021 R2 (8.00), aber das Upgrade von einer Version vor Document Capture 4.50 erfordert mehrere manuelle Schritte.

## So migrieren Sie Daten in die Cloud

Nachdem Sie Ihre On-Premises-Umgebung wie [oben beschrieben](#so-bereiten-sie-ihre-on-premises-umgebung-auf-die-cloudmigration-vor) für die Migration vorbereitet haben, [installieren und konfigurieren Sie Document Capture](@DC-214) in Business Central Online. Wenn Sie diesen Prozess abgeschlossen haben, können Sie Ihre Daten zu Business Central
Online migrieren. Führen Sie dazu folgende Schritte in Ihrer neuen Online-Umgebung durch:

1. Führen Sie das Microsoft-Cloudmigrationstool aus: Wählen Sie das Symbol {{search}}, geben Sie **Einrichtung für die Cloud-Migration** ein und wählen Sie dann den entsprechenden Link, um den Einrichtungsassistenten **Einrichtung für die Cloud-Migration** zu öffnen. Weitere Informationen finden Sie unter [Run the assisted setup guide](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data#run-the-assisted-setup-guide) (Microsoft-Artikel).

2. Befolgen Sie die Anweisungen auf dem Bildschirm, um die Einrichtung abzuschließen.

   > [!IMPORTANT]Beachten Sie, dass Sie Ihre Demo-Anmeldeinformationen nicht in einer Produktionsumgebung verwenden können. Um eine Testmigration durchzuführen, verwenden Sie stattdessen eine Sandbox-Umgebung.
   >
   > Um eine Unterbrechung des Migrationsprozesses zu vermeiden, verwenden Sie Document Capture nicht, während das Cloudmigrationstool ausgeführt wird.

3. Sobald der Migrationsprozess abgeschlossen ist, gehen Sie die Schritte der **Post Migration Checklist** durch, um sicherzustellen, dass alle notwendigen Aktionen ausgeführt wurden.

4. Deaktivieren Sie die Cloudmigration und definieren Sie Benutzerzuordnungen zwischen On-Premises und Cloud. Weitere Informationen finden Sie unter „Disable Cloud Migration“ und „Define User Mappings“ in der Tabelle unter [Manage the migration](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/migrate-data#manage-the-migration) (Microsoft-Artikel).

5. Im Rollencenter wird jetzt die folgende Benachrichtigung angezeigt: „Continia Document Capture wurde von On-Premises in die Cloud migriert. Möchten Sie es aktivieren?". Wählen Sie **Ja**, um die Aktivierungsanleitung zu öffnen.

6. Folgen Sie der Anleitung, um Document Capture als Cloud-Lösung zu aktivieren. Überprüfen Sie während der Anleitung, ob Ihre Client-Anmeldeinformationen korrekt sind.

   > [!NOTE]Wenn das Continia Web Approval Portal in der alten On-Premises-Umgebung aktiviert war, müssen Sie es erneut einrichten. Weitere Informationen finden Sie unter [Web-Genehmigung einrichten](@DC-76).

Alle Document Capture-Daten wurden jetzt migriert und die App ist für die Verwendung in Business Central Online bereit.

> [!IMPORTANT]
> Wenn Sie wie oben beschrieben zu Business Central Online migrieren, werden die Client-Anmeldeinformationen (Client-ID und Kennwort) von Ihrer On-Premises-Umgebung in die Online-Umgebung kopiert unabhängig davon, von welcher Art von Umgebung (Produktion oder Test) und in welche (Produktion oder Sandbox) Sie migrieren.
>
> Wenn Sie jedoch die Cloudmigration deaktivieren (Schritt 4 oben), ist der Typ der Online-Umgebung wichtig:
>
> - **Wenn Sie in eine Sandbox-Umgebung migrieren**, werden Ihre ursprünglichen Client-Anmeldeinformationen automatisch gelöscht. Wenn Sie Document Capture anschließend als Cloud-Lösung aktivieren (Schritte 5–6 oben), werden neue Client-Anmeldeinformationen erstellt.
> - **Wenn Sie in eine Produktionsumgebung migrieren**, werden Ihre vorhandenen Client-Anmeldeinformationen für die Online-Umgebung wiederverwendet.

## Informieren Sie Continia über die Migration

Wenn Sie eine Continia-Lösung wie Document Capture von einer On-Premises-Umgebung zur Cloud migrieren, ist es wichtig, dass Sie die unten beschriebenen erforderlichen Schritte ausführen, um sicherzustellen, dass der Rechnungsstellungsprozess reibungslos und problemlos abläuft.

Als Partner oder Kunde liegt es in Ihrer Verantwortung, Ihren On-Premises-Vertrag mit Continia zu kündigen, sobald Sie die gesamte Lösung migriert haben und sie in der Cloud voll funktionsfähig ist. Die meisten Kunden migrieren ihre Lösungen schrittweise während einer Übergangsphase, die bis zu mehreren Monaten dauern kann. Der Prozess ist jedoch von Organisation zu Organisation unterschiedlich. Sobald der Migrationsprozess abgeschlossen ist, müssen Sie Continia in jedem Fall über die Kündigung informieren, indem Sie eine E-Mail an accounting@continia.com senden. Ihnen wird dann der Restbetrag Ihres On-Premises-Abrechnungszeitraums gutgeschrieben.

> [!IMPORTANT]
> Bitte informieren Sie Continia aus administrativen Gründen über die Kündigung, bevor Ihnen die Rechnung für die Verlängerung Ihres On-Premises-Vertrags um 12 Monate ausgestellt wird.

## Informationen zum Thema

[How to migrate DC and EM to Business Central 2021 release wave 1 (BC18) in BC cloud](https://continia.zendesk.com/hc/en-us/articles/360014053519-How-to-migrate-Document-Capture-and-Expense-Management-to-Microsoft-Dynamics-365-Business-Central-2020-release-wave-2-BC17-in-Microsoft-Business-Central-cloud?_ga=2.13216625.79067120.1621259529-972812024.1595933616)\
[Dokumentenspeicher einrichten](@DC-3)
