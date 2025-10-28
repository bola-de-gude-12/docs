---
title: Continia-Apps in Multi-Tenant-Umgebungen installieren oder aktualisieren
date: 09-01-2023
description: So funktioniert das PowerShell-Skript in Single-Tenant-Umgebungen und so installieren oder aktualisieren Sie Continia-Apps in Multi-Tenant-Umgebungen.
id: DC-116
lang: de
---

# Continia-Apps in Multi-Tenant-Umgebungen installieren oder aktualisieren

Wenn Sie eine oder mehrere Continia-Apps installieren oder aktualisieren müssen, hängt die zu verwendende Methode von der allgemeinen Softwarearchitektur Ihres Unternehmens ab – genauer gesagt davon, ob die Apps in einer Single-Tenant- oder einer Multi-Tenant-Umgebung verwendet werden sollen:

- **Single-Tenant-Umgebung:** [Verwenden Sie das vollautomatische PowerShell-Skript](#das-powershell-skript-in-einer-single-tenant-umgebung-verwenden), das von Continia entwickelt wurde.
- **Multi-Tenant-Umgebung:** Führen Sie die Skriptbefehle manuell aus, [wie unten beschrieben](#allowing-the-script-commands-manually-in-a-multitenant-environment).

## Das PowerShell-Skript in einer Single-Tenant-Umgebung verwenden

Continia hat ein PowerShell-Skript entwickelt, mit dem Sie Continia Document Capture und andere Continia-Apps in einer Single-Tenant-Umgebung problemlos installieren und aktualisieren können. Weitere Informationen finden Sie unter [Continia Document Capture On-Premises installieren](@DC-51) und [Continia Document Capture für App-Versionen von Business Central aktualisieren](@DC-6).

Wenn Sie das Skript ausführen, durchsucht es automatisch den Ordner, in dem es ausgeführt wird (einschließlich aller Unterordner), nach vorhandenen Instanzen von Document Capture und anderen Continia-Apps. Wenn eine frühere Version einer App erkannt wird, werden die App und alle Abhängigkeiten aktualisiert und alle alten Versionen deinstalliert. Wenn keine App erkannt wird, installiert das Skript die App automatisch zusammen mit allen anderen erforderlichen Apps.

Wie oben erwähnt funktioniert das Skript nicht in Multi-Tenant-Umgebungen. Wenn Ihr Unternehmen Document Capture auf einem Server ausführen muss, der mehrere Tenants (Instanzen) bedient, müssen Sie Document Capture selbst installieren und/oder aktualisieren, indem Sie die Skriptbefehle stattdessen manuell in jedem relevanten Tenant ausführen. Dieser Vorgang wird im folgenden Abschnitt genauer beschrieben.

## Manuelles Ausführen der Skriptbefehle in einer Multi-Tenant-Umgebung

Um Continia-Apps in einer Multi-Tenant-Umgebung zu installieren oder zu aktualisieren, müssen Sie die Befehle aus dem PowerShell-Skript manuell in allen relevanten Tenants ausführen. Einzelheiten hierzu finden Sie in den folgenden Installations- und Upgrade-Anleitungen. Beide Anleitungen basieren auf dem Beispiel von Continia Expense Management; Sie können sie jedoch auch problemlos zur Installation oder Aktualisierung von Document Capture verwenden. In diesem Fall überspringen Sie einfach alle für Expense Management relevanten Schritte.

> [!NOTE]
> Beachten Sie, dass die Document Capture OnPremise-App in beiden Anleitungen optional ist. Die App gewährt Ihnen Zugriff auf Funktionen, die nur in On-Premises-Installationen von Business Central verfügbar sind und ist erforderlich, wenn Sie den Dokumentspeichertyp **Dateisystem** oder den On-Premises OCR-Dienst verwenden möchten, der ebenfalls Zugriff auf das Dateisystem erfordert.
>
> Wenn Sie sich für die Installation von Document Capture OnPremise entscheiden, beachten Sie, dass Sie die Document Capture-Serverkomponenten (Service Tier-Bibliotheken) installieren müssen, bevor Sie die App veröffentlichen und installieren.

### So installieren Sie Apps

Um Expense Management zu installieren, müssen Sie für jede der aufgelisteten Apps dieselben drei Befehle in der folgenden Reihenfolge ausführen:

<br>

| Schritt | App-Name                                                 | Befehle                                                                                                                                                                                   |
| ------- | -------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1       | Continia Core                                            | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 2       | Continia Delivery Network                                | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 3       | Document Capture                                         | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 4       | Document Capture OnPremise (optional) | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |
| 5       | Expense Management                                       | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Install-NavApp** |

### So aktualisieren Sie Apps

Um Expense Management zu aktualisieren, müssen Sie die neuen Versionen der Apps mit denselben drei Befehlen für jede der aufgelisteten Apps in der unten beschriebenen Reihenfolge installieren.

> [!TIP]
> Beachten Sie, dass sich dieser Befehlssatz geringfügig von dem im oben beschriebenen Installationsprozess verwendeten unterscheidet.

<br>

| Schritt | App-Name                                                        | Befehle                                                                                                                                                                                            |
| ------- | --------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1       | Continia Core                                                   | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 2       | Continia Delivery Network                                       | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 3       | Document Capture                                                | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 4       | Document Capture OnPremise (falls verwendet) | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |
| 5       | Expense Management                                              | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **Publish-NavApp** > 2. **Sync-NavApp** > 3. **Start-NAVAppDataUpgrade** |

Dadurch werden die neuen Apps installiert und die Upgradeprozesse ausgeführt. Wenn Sie fertig sind, müssen Sie die alten Versionen der Apps deinstallieren, indem Sie die folgenden beiden Befehle für jede der aufgelisteten Apps in umgekehrter Reihenfolge ausführen:

<br>

| Schritt | App-Name                                                        | Befehle                                                                                                                                                  |
| ------- | --------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 1       | Expense Management                                              | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 2       | Document Capture OnPremise (falls verwendet) | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 3       | Document Capture                                                | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 4       | Continia Delivery Network                                       | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |
| 5       | Continia Core                                                   | Führen Sie die Befehle in dieser Reihenfolge aus: <br> 1. **UnInstall-NavApp** > 2. **UnPublish-NavApp** |

## Informationen zum Thema

[Continia Document Capture On-Premises installieren](@DC-51)\
[Continia Document Capture für App-Versionen von Business Central aktualisieren](@DC-6)

<style>
.content table tr td:nth-child(1) {
width: 80px;
}
.content table tr td:nth-child(2) {
width: 300px;
}
</style>