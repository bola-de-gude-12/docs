---
title: Document Capture-Berechtigungen
date: 15-09-2025
description: So funktionieren Berechtigungen in Document Capture.
id: DC-140
lang: de
---

# Document Capture-Berechtigungen

{{include "permissions" "Document Capture"}}

## Standardmäßige Continia-Berechtigungssätze

| Berechtigungssatz | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CSC BASIC         | Um sicherzustellen, dass alle Standardfunktionen wie vorgesehen funktionieren, ist der CSC BASIC-Berechtigungssatz für alle Business Central-Benutzer obligatorisch, auch für diejenigen, die Document Capture nicht direkt verwenden, da sie auch dann bestimmte Berechtigungen für den Zugriff auf und die Ausführung von Objekten benötigen, die den Standardcode von Business Central betreffen. Mit dem Berechtigungssatz können Sie außerdem den Aktivierungsstatus von Document Capture abrufen. Insgesamt ist er dem standardmäßigen BASIC-Berechtigungssatz von Dynamics NAV/Business Central ähnlich. |
| CSC APP SETUP     | Mit diesem Berechtigungssatz können Sie Continia-Produkte, einschließlich Continia Core, aktivieren. Es wird hauptsächlich für die Produktinstallation und – in Business Central Online – beim Vornehmen von Änderungen an Abonnementvereinbarungen verwendet, beispielsweise beim Auswählen und Abwählen abonnierter Module. Der Berechtigungssatz wird hauptsächlich bei Onlinebereitstellungen von Business Central benötigt, da Benutzer, die lokale Umgebungen einrichten, normalerweise stattdessen den CDC ADMIN-Berechtigungssatz verwenden.                                                            |

## Document Capture-spezifische Berechtigungssätze

| Berechtigungssatz | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ----------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CDC BASIC         | Um sicherzustellen, dass alle Standardfunktionen wie vorgesehen funktionieren, ist der CDC BASIC-Berechtigungssatz für alle Business Central-Benutzer obligatorisch, auch für diejenigen, die Document Capture nicht direkt verwenden, da sie auch dann bestimmte Berechtigungen für den Zugriff auf und die Ausführung von Objekten benötigen, die den Standardcode von Business Central betreffen. Der Berechtigungssatz ist dem standardmäßigen BASIC-Berechtigungssatz von Dynamics NAV/Business Central ähnlich. |
| CDC CAPTURE       | Mit diesem Berechtigungssatz können Sie Dateien importieren, Dokumentwerte erfassen und Dokumente mithilfe von Document Capture in Business Central registrieren. Beachten Sie, dass Ihnen je nach der von Ihnen verwendeten Business Central-Version auch bestimmte standardmäßige Business Central-Berechtigungssätze zugewiesen werden müssen, um Document Capture zum Erfassen und Verarbeiten von Dokumenten verwenden zu können.                                                                                |
| CDC APPROVE       | Mit diesem Berechtigungssatz können Sie alle grundlegenden Genehmigungsvorgänge ausführen, wenn Sie Dokumente in Business Central oder im Continia Web Approval Portal genehmigen: Genehmigen, Ablehnen, Auf Abwarten setzen, Weiterleiten und Bemerkung hinzufügen. Der Berechtigungssatz ist ab Business Central v14 anwendbar.                                                                                                                                                                     |
| CDC ADMIN         | Wenn Ihnen dieser Berechtigungssatz zugewiesen wird, erhalten Sie vollen Zugriff auf alle Document Capture-Tabellen. Dies ist normalerweise für Benutzer erforderlich, die Document Capture in Business Central einrichten.                                                                                                                                                                                                                                                                                           |
| CDC WEB           | Mit diesem Berechtigungssatz können Sie Dokumente im Web Approval Portal genehmigen. Der Berechtigungssatz gilt nur bis einschließlich Business Central v13. Ab Business Central v14 ist dieser Berechtigungssatz in CDC APPROVE enthalten.                                                                                                                                                                                                                                                           |
| CDC EDIT          | Mit diesem Berechtigungssatz können Sie Einkaufsrechnungszeilen beim Genehmigen von Dokumenten bearbeiten. Der Berechtigungssatz gilt nur bis einschließlich Business Central v13. Ab Business Central v14 ist dieser Berechtigungssatz in CDC APPROVE enthalten.                                                                                                                                                                                                                                     |
| CDC ALLOCAT       | Dieser Berechtigungssatz ist für Debitoren, die Zuweisungen verwenden, obligatorisch. Der Berechtigungssatz gilt nur bis einschließlich Business Central v13. Ab Business Central v14 ist dieser Berechtigungssatz in CDC BASIC enthalten.                                                                                                                                                                                                                                                            |
| CDC SENDEDOCS     | Mit diesem Berechtigungssatz können Sie Daten in eDocuments bearbeiten. Weitere Informationen finden Sie unter [Continia eDocuments](@DC-177).                                                                                                                                                                                                                                                                                                                                                                        |
| CDC PC ADMIN      | Mit diesem Berechtigungssatz können Sie die Einstellungen für [Einkaufsverträge](@DC-85) konfigurieren, Einkaufsverträge erstellen und die grundlegenden Details aller Verträge aktualisieren. Darüber hinaus können Sie die Überprüfungsfunktion des Einkaufsvertragsadministrators verwenden. Dazu gehört die Möglichkeit, Überprüfungen zu starten, Verträge an Prüfer zurückzugeben, Überprüfungen abzuschließen und abzubrechen.                                                                 |

Wie oben angegeben werden die Berechtigungssätze CDC WEB, CDC EDIT und CDC ALLOCAT ab Version 14 von Business Central nicht mehr unterstützt. Für Version 14 und alle nachfolgenden Versionen von Business Central wurden die einzelnen Berechtigungen dieser drei Berechtigungssätze stattdessen in die anderen oben genannten Berechtigungssätze aufgenommen.

> [!NOTE]
> Um die geteilte Genehmigung konfigurieren und Benutzer in das Web Approval Portal exportieren zu können, müssen Sie Zugriff auf alle Mandanten haben.

## Berechtigungssätze für Kreditorenbuchhalter und ähnliche Rollen

Wenn Ihre Rolle darin besteht, Rechnungen und andere Geschäftsdokumente zu bearbeiten (z. B. als Buchhalter oder Kreditorenbuchhalter), benötigen Sie mindestens die folgenden Berechtigungssätze für die für Sie relevanten Mandanten:

- CSC BASIC
- CDC BASIC
- CDC CAPTURE
- D365 BASIC<a href="#footnote-1.1"><sup>1
- D365 ACC. PAYABLE<a href="#footnote-1.1"><sup>1

<small style><div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.1">Der Name des Berechtigungssatzes hängt von Ihrer Version von NAV/Business Central ab.</li>
  </ol>
</div>
</small>

## Berechtigungssätze für Genehmiger

Wenn Sie Genehmiger sind (ob in Microsoft Dynamics NAV/Business Central oder im Web Approval Portal), benötigen Sie mindestens die folgenden Berechtigungssätze für die für Sie relevanten Mandanten:

- CSC BASIC
- CDC BASIC
- CDC APPROVE
- D365 BASIC<a href="#footnote-1.2"><sup>1
- D365 PURCH DOC, EDIT<a href="#footnote-1.2"><sup>1

<small style><div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.2">Der Name des Berechtigungssatzes hängt von Ihrer Version von NAV/Business Central ab.</li>
  </ol>
</div>
</small>

> [!NOTE]
> Im Web Approval Portal wird der Kontoname jeder Dokumentzeile in der Spalte **Kontoname** angezeigt. Damit dies sichtbar ist, müssen Sie direkten Zugriff auf die verschiedenen Arten von Konten haben, die hier angezeigt werden können (Sachkonten, Artikel, Ressourcen, Anlagen und Zu-/Abschläge). Der direkte Zugriff auf Sachkonten, Artikel, Ressourcen und Zu-/Abschläge ist in den oben genannten obligatorischen Berechtigungssätzen **D365 PURCH DOC, EDIT** und **D365 BASIC** enthalten. Wenn Sie Anlagen verwenden, muss Ihnen ein Standardberechtigungssatz zugewiesen werden, der Anlagen umfasst.

## Berechtigungssätze für Prüfer

Wenn Sie ein Prüfer von Einkaufsverträgen sind (ob in Microsoft Dynamics NAV/Business Central oder im Web Approval Portal), benötigen Sie mindestens die folgenden Berechtigungssätze für die für Sie relevanten Mandanten:

- CSC BASIC
- CDC BASIC
- CDC APPROVE
- D365 BASIC<a href="#footnote-1.3"><sup>1

<small style><div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1.3">Der Name des Berechtigungssatzes hängt von Ihrer Version von NAV/Business Central ab.</li>
  </ol>
</div>
</small>

## Legacy-Berechtigungssätze (für ältere Versionen)

Die folgenden Berechtigungssätze gelten nur für frühere Versionen von Document Capture (vor 27.0) und werden hier zu Referenzzwecken beibehalten.

| Berechtigungssatz | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| CDC-ALL           | Um sicherzustellen, dass alle Standardfunktionen wie vorgesehen funktionieren, ist der CDC-ALL-Berechtigungssatz für alle Business Central-Benutzer obligatorisch, auch für diejenigen, die Document Capture nicht direkt verwenden, da sie auch dann bestimmte Berechtigungen für den Zugriff auf und die Ausführung von Objekten benötigen, die den Standardcode von Business Central betreffen. Der Berechtigungssatz ist dem standardmäßigen BASIC-Berechtigungssatz von Dynamics NAV/Business Central ähnlich. |
| CDC-CAPTURE       | Mit diesem Berechtigungssatz können Sie Dateien importieren, Dokumentwerte erfassen und Dokumente mithilfe von Document Capture in Business Central registrieren. Beachten Sie, dass Ihnen je nach der von Ihnen verwendeten Business Central-Version auch bestimmte standardmäßige Business Central-Berechtigungssätze zugewiesen werden müssen, um Document Capture zum Erfassen und Verarbeiten von Dokumenten verwenden zu können.                                                                              |
| CDC-APPROVE       | Mit diesem Berechtigungssatz können Sie alle grundlegenden Genehmigungsvorgänge ausführen, wenn Sie Dokumente in Business Central oder im Continia Web Approval Portal genehmigen: _Genehmigen_, _Ablehnen_, _Auf Abwarten setzen_, _Weiterleiten_ und _Bemerkung hinzufügen_. Der Berechtigungssatz ist ab Business Central v14 anwendbar.                                                                                                                                                         |
| CDC-SUPER         | Wenn Ihnen dieser Berechtigungssatz zugewiesen wird, erhalten Sie vollen Zugriff auf alle Document Capture-Tabellen. Dies ist normalerweise für Benutzer erforderlich, die Document Capture in Business Central einrichten.                                                                                                                                                                                                                                                                                         |
| CDC-WEB           | Mit diesem Berechtigungssatz können Sie Dokumente im Web Approval Portal genehmigen. Der Berechtigungssatz gilt nur bis einschließlich Business Central v13. Ab Business Central v14 ist dieser Berechtigungssatz in CDC-APPROVE enthalten.                                                                                                                                                                                                                                                         |
| CDC-EDIT          | Mit diesem Berechtigungssatz können Sie Einkaufsrechnungszeilen beim Genehmigen von Dokumenten bearbeiten. Der Berechtigungssatz gilt nur bis einschließlich Business Central v13. Ab Business Central v14 ist dieser Berechtigungssatz in CDC-APPROVE enthalten.                                                                                                                                                                                                                                   |
| CDC-ALLOCAT       | Dieser Berechtigungssatz ist für Debitoren, die Zuweisungen verwenden, obligatorisch. Der Berechtigungssatz gilt nur bis einschließlich Business Central v13. Ab Business Central v14 ist dieser Berechtigungssatz in CDC-ALL enthalten.                                                                                                                                                                                                                                                            |
| CDC-SENDEDOCS     | Mit diesem Berechtigungssatz können Sie Daten in eDocuments bearbeiten. Weitere Informationen finden Sie unter [Continia eDocuments](@DC-177).                                                                                                                                                                                                                                                                                                                                                                      |
| CDC-PC-ADMIN      | Mit diesem Berechtigungssatz können Sie die Einstellungen für [Einkaufsverträge](@DC-85) konfigurieren, Einkaufsverträge erstellen und die grundlegenden Details aller Verträge aktualisieren. Darüber hinaus können Sie die Überprüfungsfunktion des Einkaufsvertragsadministrators verwenden. Dazu gehört die Möglichkeit, Überprüfungen zu starten, Verträge an Prüfer zurückzugeben, Überprüfungen abzuschließen und abzubrechen.                                                               |

<style>
  .content table tr td:nth-child(1) {
    width: 120px;
  }
  .content table tr td:nth-child(2) {
    width: 610px;
  }  
</style>