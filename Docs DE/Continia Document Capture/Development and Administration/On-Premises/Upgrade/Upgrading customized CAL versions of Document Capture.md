---
title: Upgrade angepasster C/AL-Versionen von Document Capture
date: 02-04-2025
description: So aktualisieren Sie Continia Document Capture und Continia Expense Management von C/AL-Codeanpassungen auf AL-Erweiterungen.
id: DC-113
lang: de
---

# Upgrade angepasster C/AL-Versionen von Document Capture

Das Upgrade von Continia Document Capture und Continia Expense Management von C/AL-Codeanpassungen auf AL-Erweiterungen basiert auf dem standardmäßigen Upgradeprozess von Microsoft, wie unter [Upgrading Customized C/AL Application to Microsoft Base Application version 25](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-to-microsoft-base-app-v25) (Microsoft-Artikel) beschrieben. Die Informationen unten können als Ergänzung zu dieser Anleitung betrachtet werden und enthalten alle [zusätzlichen Voraussetzungen](#voraussetzungen) und [erforderlichen Continia-spezifischen Schritte](#upgradeprozess) für alle Aufgaben in der Microsoft-Anleitung.

> [!NOTE]
> Ab 2025 Release Wave 1 (v26)wird das direkte Upgrade von Business Central 2019 (v14) auf die neueste Version nicht mehr unterstützt. Der unterstützte Upgradepfad erfolgt über Release Wave 2 (v25) 2024 und dann auf v26. Weitere Informationen finden Sie unter [Deprecated features in the platform - clients, server, and database](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/deprecated-features-platform#changes-in-2025-release-wave-1-version-260) (Microsoft-Artikel).

Beachten Sie, dass Sie sowohl Document Capture als auch Expense Management gleichzeitig aktualisieren müssen. Um Ihre C/AL-Versionen dieser Apps auf AL-Erweiterungen zu aktualisieren, müssen Sie gemäß der oben genannten Microsoft-Anleitung auf Business Central 2024 Release Wave 2 (BC v25) aktualisieren.

## Voraussetzungen

- Sie müssen zuerst ein Upgrade auf Microsoft Dynamics 365 Business Central April 2019 (BC v14) durchführen. Eine Übersicht darüber, welche BC v14-Versionen mit BC v25 kompatibel sind, finden Sie in der [Dynamics 365 Business Central Upgrade-Kompatibilitätsmatrix](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-v14-v15-compatibility) (Microsoft-Artikel).
- Document Capture muss auf die neuste veröffentlichte Version (einschließlich des neusten Service Packs) aktualisiert werden.

## Upgradeprozess

> [!IMPORTANT]
> Um eine konsistente Migration auf BC v25 zu gewährleisten, muss Expense Management installiert werden, auch wenn es nicht in der Datenbank verwendet wird. Wenn die Migration abgeschlossen ist, können Sie Expense Management bei Bedarf wieder deinstallieren.

Die unten aufgeführten nummerierten Schritte beziehen sich alle auf die Microsoft-Anleitung [Upgrading Customized C/AL Application to Microsoft Base Application version 25](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-to-microsoft-base-app-v25) (Microsoft-Artikel). Bei allen Aufgaben geht es um Erweiterungen von Drittanbietern, in diesem Fall um die fünf Continia-Apps Document Capture, Expense Management, Continia Core, Continia Delivery Network und Continia Business Foundation. Für jede der Aufgaben müssen Sie die beschriebenen Aktionen ausführen:

### Aufgabe 4: Leere System-, Base-, Business Foundation- und Anpassungserweiterungen erstellen

Für diese Aufgabe benötigen Sie leere Versionen der fünf Continia-Apps. Diese finden Sie unter folgendem Link:

- [Continia-Apps](https://continiadocsstorageprod.blob.core.windows.net/docsfiles/ContiniaApps.zip)

### Aufgabe 5: Tabellenmigrationserweiterung erstellen

In dieser Aufgabe müssen Sie zwei Versionen einer Erweiterung erstellen, die nur aus den Nicht-Systemtabellenobjekten Ihrer benutzerdefinierten Basisanwendung besteht. Die zweite Version ist eine leere Erweiterung, die eine migration.json-Datei enthält, wie in der Microsoft-Anleitung unter „Create the second version - empty“ beschrieben. Hängen Sie dieser migration.json-Datei die folgenden IDs an:

- 4b915d7e-c02a-435f-85ab-649086c1e002
- bbb72c8a-3abf-478f-9239-a34dbc252d07
- 0745e76d-0b72-4641-87c2-ee45db5d2c32
- 6da8dd2f-e698-461f-9147-8e404244dd85
- 8d4eab29-8c7f-4b6c-be9a-b7fdfb9da196

### Aufgabe 10: DestinationAppsForMigrations-Erweiterungen veröffentlichen

Veröffentlichen Sie in Schritt 2 dieser Aufgabe die folgenden fünf Erweiterungen in der angegebenen Reihenfolge:

1. Continia Core
2. Continia Business Foundation
3. Continia Delivery Network
4. Continia Document Capture
5. Continia Expense Management

Führen Sie dazu die folgenden Befehle aus, wobei „\<path to extension\>“ der Pfad zum Speicherort ist, an dem die in [Aufgabe 4 oben](#aufgabe-4-leere-system--base--business-foundation--und-anpassungserweiterungen-erstellen) heruntergeladenen leeren Erweiterungen gespeichert wurden:

<br>

```
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Core"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Business Foundation"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Delivery Network"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Document Capture"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Expense Management"
```

### Aufgabe 11: Tenant synchronisieren

Führen Sie in Schritt 4 dieser Aufgabe die folgenden Befehle aus:

<br>

```
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Core”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Business Foundation”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Delivery Network"
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Document Capture”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Expense Management”
```

### Aufgabe 12: DestinationAppsForMigration installieren und Tabellen verschieben

Installieren Sie in Schritt 3 dieser Aufgabe die Continia-Apps in Ihrem System und verschieben Sie Daten aus den alten Tabellen in die neuen Tabellen, die der Tabellenmigrationserweiterung gehören.

<br>

```
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Core”
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Business Foundation”
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Delivery Network”
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Document Capture”
Install-NAVApp -ServerInstance <server instance name> -Name “Continia Expense Management”
```

### Aufgabe 13: Endgültige Erweiterungen veröffentlichen

Führen Sie in Schritt 5 dieser Aufgabe die folgenden Befehle aus, wobei „\<path to extension\>“ der Pfad zum Speicherort ist, an dem Sie die Erweiterungen gespeichert haben, die Sie in Aufgabe 3 der [Microsoft-Anleitung](https://learn.microsoft.com/en-us/dynamics365/business-central/dev-itpro/upgrade/upgrade-to-microsoft-base-app-v25) erstellt haben:

<br>

```
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Core"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Business Foundation"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Delivery Network"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Document Capture"
Publish-NAVApp -ServerInstance <server instance name> -Path "<path to extension>\Continia Expense Management"
```

### Aufgabe 14: Endgültige Erweiterungen synchronisieren

Führen Sie in dieser Aufgabe die folgenden Befehle aus:

<br>

```
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Core”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Business Foundation”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Delivery Network"
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Document Capture”
Sync-NAVApp -ServerInstance <server instance name> -Name “Continia Expense Management”
```

### Aufgabe 17: Upgrade und Installation der letzten Erweiterungen

Führen Sie in dieser Aufgabe die folgenden Befehle aus:

<br>

```
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Core”
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Business Foundation”
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Delivery Network”
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Document Capture”
Start-NAVAppDataUpgrade -ServerInstance <server instance name> -Name “Continia Expense Management”
```

## Informationen zum Thema

[Document Capture von Business Central On-Premises zur Cloud migrieren](@DC-106)