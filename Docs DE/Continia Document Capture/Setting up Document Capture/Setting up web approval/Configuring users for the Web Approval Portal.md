---
title: Benutzer für das Web Approval Portal konfigurieren
date: 01-10-2024
description: null
id: DC-129
lang: de
---

# Benutzer für das Web Approval Portal konfigurieren

Die Vorgehensweise zum Konfigurieren von Benutzern für das Continia Web Approval Portal ist für Online- und On-Premises-Installationen von Microsoft Dynamics 365 Business Central gleich. Dies erfolgt in der Continia Benutzereinrichtung mithilfe verschiedener Felder, die für das Web Approval Portal relevant sind. So bearbeiten Sie diese Felder:

1. Wählen Sie das Symbol {{search}}, geben Sie **Continia Benutzereinrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Benutzer aus, dessen Eigenschaften Sie bearbeiten möchten.
3. Wählen Sie in der Aktionsleiste **Liste bearbeiten**, damit die Benutzereinträge in der Liste bearbeitet werden können.
4. Wählen Sie in der Spalte **Genehmigungs-Client** die Option **Continia Web Approval Portal** aus, um dem ausgewählten Benutzer Zugriff auf das Portal zu gewähren.
5. Wenn Sie möchten, dass der Benutzer Einkaufszeilen im Portal bearbeiten kann, aktivieren Sie das Kontrollkästchen unter **Darf Buchungszeilen editieren**.
6. Um festzulegen, nach welchen Belegen der Benutzer im Dokumentenarchiv des Portals suchen kann (entweder alle Belege oder nur die eigenen), nehmen Sie die entsprechende Auswahl in der Spalte **Beleg suchen** vor.
7. Wiederholen Sie Schritte 2–6 für alle weiteren Benutzer, deren Eigenschaften Sie bearbeiten möchten.
8. Wenn Sie fertig sind, wählen Sie in der Aktionsleiste **Benutzer exportieren** aus, um die Continia Benutzereinrichtung in das Web Approval Portal zu exportieren.

Anschließend prüft Document Capture, ob an den für den Benutzerexport relevanten Tabellen Änderungen vorgenommen wurden. Wenn dies der Fall ist, wird der Benutzerexport durchgeführt. Wenn keine derartigen Änderungen vorgenommen wurden, überspringt Document Capture den Benutzerexport, um unnötige Systemausfallzeiten durch einen Export zu vermeiden.

> [!IMPORTANT]
> Folgendes gilt für von Continia gehostete Versionen des Web Approval Portals (continiaonline.com): Wenn Ihr Unternehmen entweder den Business Central-Benutzeranmeldetyp **Windows** oder **Database** (NavUserPassword) verwendet, müssen die E-Mail-Domänen der konfigurierten Benutzer von Continia als gültig registriert werden, damit Sie Benutzer exportieren können. Dies gilt jedoch nicht für den Anmeldetyp **Office 365**.
>
> Beachten Sie, dass nur verifizierte Domänennamen – wie beispielsweise microsoft.com und ähnliche Unternehmensdomänen – als gültig registriert werden können. Die Domänen einiger bekannter E-Mail-Dienste von Drittanbietern wie gmail.com, yahoo.com und hotmail.com sind für diesen Zweck nicht zulässig, da die Zugehörigkeit dieser Domänen zu einem Unternehmen nicht überprüft werden kann.

## Mehrere Datenbanken verwenden

Ab der Version 1.16.0 ist es möglich, Benutzer in mehreren Datenbanken im Web Approval Portal einzurichten. Die eindeutige ID, die Benutzer gruppiert, ist ihre E-Mail-Adresse. Dies gilt auch für Partner, die mit mehreren Kunden zusammenarbeiten.

Wenn Sie Zugriff auf mehr als eine Datenbank haben, wird die Datenbankauswahl neben der Mandantensauswahl im Web Approval Portal angezeigt. Beachten Sie, dass die Mandantenauswahl nur innerhalb der aktuell ausgewählten Datenbank funktioniert und nur, wenn Sie auf der Seite **Einstellungen** des Web Approval Portals die klassische Ansicht ausgewählt haben. Wenn Sie beispielsweise in einer Datenbank auf fünf Mandanten zugreifen können und in einer anderen auf drei, werden Ihnen in der Mandantensauswahl nicht insgesamt acht Mandanten angezeigt.

## Verfügbare Anmeldetypen

Im Web Approval Portal sind alle drei Anmeldearten verfügbar, das heißt: **Datenbank**, **Microsoft 365** und **Windows**. Sie können sich mit anderen Anmeldearten an verschiedenen Datenbanken anmelden. So können Sie sich beispielsweise bei einer Datenbank über Microsoft 365 anmelden, bei einer anderen über Windows und bei einer weiteren mit NavUserPassword und auch zwischen diesen wechseln. Beachten Sie, dass Sie beim Wechseln zwischen Anmeldearten zur Eingabe Ihres Passworts aufgefordert werden.

## Informationen zum Thema

[Web-Genehmigung einrichten](@DC-76)
