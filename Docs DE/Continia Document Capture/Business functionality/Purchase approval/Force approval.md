---
title: Genehmigung erzwingen
date: 06-08-2024
description: So erzwingen Sie die Genehmigung eines Belegs
id: DC-36
lang: de
---

# Genehmigung erzwingen

Mit der Funktion **Erzwinge Genehmigung** können Genehmigungsadministratoren die Genehmigung eines bestimmten Belegs erzwingen und so den üblichen Genehmigungsworkflow umgehen. In diesem Artikel werden Einkaufsrechnungen zur Veranschaulichung verwendet. Die Funktionalität gilt jedoch auch für Gutschriften.

Beachten Sie, dass die Funktion zuerst [in der **Document Capture Einrichtung** aktiviert](@DC-22) werden muss und dass sie nur von Genehmigungsadministratoren verwendet werden kann. Weitere Informationen zum Einrichten eines Benutzers als Genehmigungsadministrator finden Sie unter [So richten Sie Benutzer als Genehmiger ein](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#so-richten-sie-benutzer-als-genehmiger-ein).

> [!IMPORTANT]
> Wenn die Funktion nicht aktiviert wurde oder Sie nicht über die erforderlichen Genehmigungsadministrator-Berechtigungen verfügen, wird die Schaltfläche **Erzwinge Genehmigung** nicht auf der Seite **Einkaufsrechnung** angezeigt, wie [unten](#so-erzwingen-sie-die-genehmigung-einer-rechnung) beschrieben.

## So erzwingen Sie die Genehmigung einer Rechnung

Als Genehmigungsadministrator können Sie die Genehmigung einer Einkaufsrechnung erzwingen, indem Sie folgendermaßen vorgehen:

1. Öffnen Sie die Einkaufsrechnung, deren Genehmigung Sie erzwingen möchten.
2. Klicken Sie auf der Seite **Einkaufsrechnung** in der Aktionsleiste auf **Aktionen** > **Genehmigungsverwaltung** > **Erzwinge Genehmigung**.
3. In einem Dialogfeld werden Sie gefragt, ob Sie die Genehmigung der Rechnung erzwingen möchten. Wählen Sie **Ja**.

Die Rechnung wird jetzt sofort genehmigt und in die Kachel **Freigegebene Rechnungen** im Rollencenter verschoben.

> [!NOTE]
> Die erzwungene Genehmigung aller Rechnungen wird in der Tabelle **Genehmigungsposten** protokolliert. Außerdem wird auf der Seite **Einkaufsrechnung** der entsprechenden Rechnung im Inforegister **Allgemein** im Feld **Genehmigungsbemerkungen** der Text **Genehmigung forciert durch [Benutzer-ID]** angezeigt.

## Was Sie beachten müssen

Obwohl **Erzwinge Genehmigung** eine nützliche Funktion ist, wenn eine Ausnahme gemacht werden muss, muss sie sorgfältig und verantwortungsbewusst eingesetzt werden. Dies beeinträchtigt nicht nur die Integrität des etablierten Genehmigungsablaufs, sondern hat auch folgende Auswirkungen:

- Die Betragsprüfung bei der Genehmigung, die überprüft, ob der erkannte Betrag dem konfigurierten Betrag entspricht, wird übersprungen.
- Die [Überprüfung der Genehmigungsberechtigung](@DC-24), wird übersprungen, falls diese aktiviert ist.
- Das Betrugsrisiko ist erhöht.
- Dies kann zu Compliance-Problemen und/oder verstärkter Kontrolle bei Audits führen.
- Dies kann zu Fehlern führen, die andernfalls nicht auftreten würden, einschließlich falscher oder doppelter Zahlungen.

Um diese Auswirkungen zu mindern, müssen Sie unbedingt Folgendes beachten:

- Aktivieren Sie [Betragsvalidierung beim Buchen](@DC-139).
- Beschränken Sie die Verwendung der Funktion **Erzwinge Genehmigung** auf eine kleine Anzahl vertrauenswürdiger Personen.
- Legen Sie klare Richtlinien und Grenzen fest, wenn Sie Personen schulen, die Zugriff auf die Funktion haben.
- Stellen Sie die Einhaltung sicher, indem Sie die Nutzung der Funktion überwachen und regelmäßige Audits durchführen.

## Informationen zum Thema

[Document Capture Einrichtung](@DC-22)\
[Continia Benutzereinrichtung für Genehmigungen](@DC-23)