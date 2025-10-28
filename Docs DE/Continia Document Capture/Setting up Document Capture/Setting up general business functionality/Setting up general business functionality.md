---
title: Überblick über die Einrichtung von Geschäftsfunktionen in Document Capture
date: 16-06-2025
description:
id: DC-77
lang: de
---

# Überblick über die Einrichtung allgemeiner Geschäftsfunktionen

Mit der Standardkonfiguration von Continia Document Capture können Sie sofort mit der Verarbeitung von Dokumenten beginnen. Document Capture bietet jedoch auch zahlreiche weitere Konfigurationsmöglichkeiten, mit denen Sie die App genau an die Bedürfnisse Ihres Unternehmens anpassen können.

Die folgende Tabelle listet die wichtigsten davon auf:

| Thema                                                                                                                          | Siehe                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------- |
| Registrierung beim Continia Delivery Network, um Peppol- und NemHandel-Rechnungen und -Gutschriften empfangen zu können        | [Das Continia Delivery Network einrichten](@DC-75)                              |
| Festlegen, wo Dokumente gespeichert werden sollen, wenn Sie andere Speicherorte als Ihre Business Central-Datenbank bevorzugen | [Dokumentenspeicher einrichten](@DC-3)                                          |
| Ändern der Unternehmensrichtlinie, um festzulegen, ob Dokumente in Ihrem Unternehmen gelöscht werden können oder nicht         | [Löschen von Dokumenten mit einer Unternehmensrichtlinie deaktivieren](@DC-477) |
| Definieren von Dokumentenstatuscodes, die im Belegjournal verwendet werden                                                     | [Dokumentenstatuscodes definieren](@DC-79)                                      |
| Einrichten von Aufgabenwarteschlangen, um Dokumente in vordefinierten Intervallen und nicht manuell zu importieren             | [Aufgabenwarteschlangen einrichten](@DC-16)                                     |
| Einrichten von Mandantensuchtexten                                                                                             | [So richten Sie Mandantensuchtexte ein](@DC-443)                                |
| Einrichten und Aktivieren von Secure Archive, einschließlich der Protokollierung von Belegaktivitäten                          | [Secure Archive einrichten](@DC-155)                                            |
| Einrichten von Aufbewahrungsfristen für die Datenpflege und Durchführen von Datenpflegeaktionen                                | [Datenpflege einrichten](@DC-187)                                               |

<br>
Wenn Sie Document Capture On-Premises oder in einer privaten Cloud-Umgebung ausführen, müssen außerdem die folgenden zusätzlichen Konfigurationsschritte durchgeführt werden:
<br>

| Thema                                                                | Siehe                                           |
| -------------------------------------------------------------------- | ----------------------------------------------- |
| Konfigurieren, ob Sie Cloud oder On-Premises OCR verwenden möchten   | [Cloud und On-Premises OCR einrichten](@DC-142) |
| Einrichten von Document Capture zum Scannen mit einem Desktopscanner | [Einen Desktopscanner anschließen](@DC-119)     |

> [!IMPORTANT]
> Document Capture verknüpft Dokumente mit Transaktionen in Microsoft Dynamics 365 Business Central unter Verwendung der Transaktionsnummer. Daher ist es wichtig, dass die Nummernserien in Business Central getrennt werden und Überschneidungen vermieden werden.

<style>
  .content table tr td:nth-child(1) {
    width: 550px;
  }
  .content table tr td:nth-child(2) {
    width: 280px;
  }  
</style>