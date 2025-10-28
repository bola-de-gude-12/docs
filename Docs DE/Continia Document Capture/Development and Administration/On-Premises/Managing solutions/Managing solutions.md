---
title: Continia Lösungsverwaltung verwenden (On-Premises)
date: 21-07-2025
description: So verwalten Sie Ihre Lösungen in On-Premises-Instanzen von Business Central.
id: DC-151
lang: de
---

# Continia Lösungsverwaltung verwenden (On-Premises)

Dieser Artikel befasst sich mit der allgemeinen Verwaltung von Continia-Lösungen in On-Premises-Bereitstellungen von Microsoft Dynamics 365 Business Central. Informationen zur Verwaltung von Continia-Lösungen in Online-Bereitstellungen von Business Central finden Sie unter [Continia Lösungsverwaltung vewenden](@DC-107).

Informationen zur Continia-Lizenzverwaltung, einschließlich Informationen zum Kaufen oder Kündigen von Lösungslizenzen, Verwalten von Modulen und Hinzufügen oder Entfernen von Mandanten, finden Sie unter [Lizenzen verwalten](@DC-488).

> [!IMPORTANT]
> Alle Anleitungen in diesem Artikel richten sich an Continia-Partner, da nur Partner die genannten Schritte durchführen können. Wenn eine der Anleitungen für Sie relevant ist, wenden Sie sich bitte an [Ihre/n Continia-Partner(in)](@DC-487) und bitten Sie ihn bzw. sie, die entsprechenden Anleitungen für Sie auszuführen.

## So aktivieren Sie eine Lösung

Wenn Sie [eine Lizenz für eine Lösung gekauft haben](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-licenses#so-kaufen-sie-eine-lizenz), können Sie die Lösung mit den folgenden Schritten aktivieren:

1. Suchen Sie ({{search}}) nach **Continia Lösungsverwaltung** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie in der Liste der installierten Continia-Lösungen die Lösung aus, die Sie aktivieren möchten.
3. Klicken Sie in der Aktionsleiste auf **Lösung aktivieren**.
4. Befolgen Sie die Anweisungen auf dem Bildschirm im unterstützten Setup, um die Aktivierung abzuschließen.

Wenn Sie diese Lösung zum ersten Mal aktivieren, wird gleichzeitig auch der Mandant des Kunden aktiviert. In diesem Fall müssen Sie beim Ausführen des unterstützten Setups die Anmeldeinformationen des Kunden eingeben und den Mandantentyp (Test oder Produktion) auswählen.

## So deaktivieren Sie eine Lösung

So deaktivieren Sie eine Continia-Lösung:

1. Suchen Sie ({{search}}) nach **Continia Lösungsverwaltung** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie in der Liste der installierten Continia-Lösungen die Lösung aus,die Sie deaktivieren möchten.
3. Klicken Sie in der Aktionsleiste auf **Lösung deaktivieren**.

> [!NOTE]
> Wenn eine Lösung deaktiviert wurde, funktionieren bestimmte Kernfunktionen dieser Lösung nicht mehr. Die Lösung ist jedoch weiterhin in der Benutzeroberfläche sichtbar und Sie können weiterhin auf Daten darin zugreifen.

Beachten Sie, dass beim Deaktivieren aller Lösungen auch der Mandant deaktiviert wird, bei dem Sie aktuell angemeldet sind.

## So ändern Sie Client Credentials

> [!WARNING]
> Seien Sie vorsichtig, wenn Sie Client Credentials ändern. Sie sollten Client Credentials nur ändern, wenn Sie von einer Produktionsumgebung zu einer Demoumgebung wechseln. Andernfalls besteht die Gefahr, dass wichtige Daten in Continia Online verloren gehen.

> [!NOTE]
> Wenn Sie die Anmeldeinformationen eines Kunden ändern, werden alle Mandanten des Kunden und ihre jeweiligen Lösungen automatisch deaktiviert. Nach der Änderung müssen Sie alle Lösungen für jeden Mandanten manuell neu aktivieren.

So ändern Sie Client Credentials:

1. Suchen Sie ({{search}}) nach **Continia Lösungsverwaltung** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie in der Aktionsleiste auf **Client Credentials**, um die Seite **Continia Client Credentials** zu öffnen.
3. Geben Sie die neue Kunden-ID und das entsprechende Kundenkennwort ein und wählen Sie **Speichern**, um die Änderungen zu speichern und die Seite zu schließen.
4. Reaktivieren Sie alle Lösungen manuell mit [dem üblichen Verfahren](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#so-aktivieren-sie-eine-losung).
5. Wiederholen Sie alle oben genannten Schritte für alle weiteren Mandanten.

## Mandanten aktivieren

Sobald ein [Mandant hinzugefügt wurde](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-licenses#so-fugen-sie-mandanten-hinzu), muss dieser aktiviert werden. Aktivieren Sie hierzu alle relevanten Lösungen (Sie müssen mindestens eine Lösung pro Mandant aktivieren, um den Mandanten zu aktivieren), was Sie mit [dem üblichen Verfahren](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#so-aktivieren-sie-eine-losung) durchführen können.

## Mandanten deaktivieren

Sie können einen Mandanten direkt in der Benutzeroberfläche deaktivieren, indem Sie für den Mandanten, bei dem Sie aktuell angemeldet sind, [alle aktiven Lösungen deaktivieren](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#so-deaktivieren-sie-eine-losung). Wenn alle aktiven Lösungen deaktiviert wurden, wird auch der Mandant deaktiviert.

> [!NOTE]
> Wenn ein Mandant deaktiviert wurde, funktionieren bestimmte Kernfunktionen dieses Mandanten nicht mehr. Der Mandant ist jedoch weiterhin in der Benutzeroberfläche sichtbar und Sie können weiterhin auf Daten darin zugreifen.

## Einen Mandanten als Testmandanten registrieren

Mandanten können grundsätzlich entweder als Test- oder Produktionsmandanten registriert werden und eine Änderung des Mandantentyps ist nach der ersten Aktivierung einer Lösung grundsätzlich möglich. Ihre Optionen hängen jedoch davon ab, ob Sie Demo- oder Produktion-Credentials verwenden, wie unten beschrieben:

**Produktions-Credentials verwenden**  
Wenn Sie für den Mandanten eines Kunden [die erste Lösung aktivieren](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#so-aktivieren-sie-eine-losung), müssen Sie diesen entweder als Testumandanten oder als Produktionsmandanten definieren. Wenn Produktions-Credentials verwendet werden, gibt es keinen technischen Unterschied zwischen diesen beiden Mandantentypen, da beide auf Produktionsumgebungen verweisen. Der einzige Unterschied besteht darin, dass Sie für ein Testmandanten keine Lizenz erwerben müssen.

Sie können den Mandantentyp bei Bedarf auch später noch ändern. Gehen Sie hierzu wie folgt vor:

1. Suchen Sie ({{search}}) nach **Continia Lösungsverwaltung** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie unter **Company Status** den Mandantentyp (Test oder Produktion) aus.

**Demo-Credentials verwenden**\
Wenn Sie die erste Lösung für ein Kundenmandanten aktivieren, wird der Mandant immer als Testmandant registriert und dies kann nicht geändert werden.

## So aktivieren Sie einen Mandanten nach Datenbankänderungen

Manchmal müssen Sie möglicherweise Änderungen an Ihrer Datenbank vornehmen, beispielsweise wenn Sie sie auf einen neuen Server verschieben müssen oder Ihr System sichern möchten, um neue Funktionen zu testen. In diesem Fall müssen Sie nach der Änderung sämtliche Mandanten erneut aktivieren.

Um einen versehentlichen Import von Produktionsdaten in eine Testumgebung zu vermeiden, erkennt das System automatisch, ob die Datenbank wiederhergestellt oder auf einen anderen Server verschoben wurde. Wenn das System Änderungen an den Datenbankinformationen erkennt, werden alle Mandanten und ihre jeweiligen Lösungen deaktiviert und auf der Continia Continia Lösungsverwaltungs-Seite wird eine Warnung angezeigt. So aktivieren Sie die deaktivierten Mandanten und Lösungen wieder:

1. Suchen Sie ({{search}}) nach **Continia Lösungsverwaltung** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie auf die angezeigte Warnung (wie oben erwähnt), um die Seite **Continia Client Credentials** zu öffnen.
3. Führen Sie je nach Situation einen der folgenden Schritte aus:
   - Wenn es sich bei der Datenbank um eine Kopie einer anderen Datenbank handelt (egal ob es sich um eine Produktions- oder Testdatenbank handelt), ändern Sie die Client Credentials und klicken Sie auf **Speichern**. Aktivieren Sie alle Lösungen manuell mit [dem üblichen Verfahren](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#so-aktivieren-sie-eine-losung).
   - Wenn die Datenbank verschoben oder wiederhergestellt wurde, klicken Sie auf **Update Database Info**, um mit Ihren vorhandenen Anmeldeinformationen fortzufahren. Dadurch werden alle Lösungen automatisch reaktiviert.
4. Wiederholen Sie alle oben genannten Schritte für alle weiteren Mandanten, die mit der geänderten Datenbank verknüpft sind.

## So reaktivieren Sie einen umbenannte Mandanten

Wenn ein Mandant umbenannt wurde, müssen Sie ihn erneut aktivieren. Sie können dies entweder vom Rollencenter oder von der Seite **Continia Lösungsverwaltung** aus tun. Beide Methoden werden nachfolgend beschrieben.

Reaktivierung über das Rollencenter:

1. Im Rollencenter erhalten Sie die Meldung, dass die Lösung installiert wurde. Sie werden gefragt, ob Sie sie jetzt aktivieren möchten. Klicken Sie auf diese Meldung, um das unterstützte Setup für die **Lösungsaktivierung** zu starten.
2. Schließen Sie die Anleitung ab, indem Sie den Anweisungen auf dem Bildschirm folgen, um die Lösung erneut zu aktivieren.

Reaktivierung über **Continia Lösungsverwaltung**:

1. Suchen Sie ({{search}}) nach **Continia Lösungsverwaltung** und wählen Sie dann den entsprechenden Link aus.
2. Auf der Seite **Continia Lösungsverwaltung** wird eine Meldung in Rot angezeigt, die darauf hinweist, dass der Mandant nicht richtig aktiviert wurde. Klicken Sie auf diese Meldung, um den Mandanten inklusive aller zuvor aktivierten Lösungen erneut zu aktivieren. Die rote Meldung wird nach der Aktivierung nicht mehr angezeigt.

## So kopieren Sie einen Mandanten zur Verwendung als Testmandant

> [!NOTE]
> In jeder Datenbank wird nur ein Satz Client Credentials gespeichert. Beispielsweise werden in einer Produktionsdatenbank die Produktionsanmeldeinformationen des Kunden gespeichert und von dort verweisen sie auf die Produktionsumgebungen von Continia Online, das Continia Web Approval Portal und die Continia Cloud OCR-Dienste. Wenn Sie eine vollständige Trennung Ihrer Test- und Produktionsumgebungen wünschen, müssen Sie eine Datenbank erstellen und hierfür Demo-Credentials verwenden.

So erstellen Sie einen Testmandanten in einer Produktionsdatenbank, indem Sie einen Produktionsmandanten in derselben Datenbank kopieren:

1. Kopieren Sie den Mandanten und geben Sie ihm einen neuen Namen. Ausführliche Informationen hierzu finden Sie in [diesem Microsoft-Artikel](https://docs.microsoft.com/en-us/dynamics-nav/how-to--create-companies).
2. Öffnen Sie den Mandanten, den Sie soeben als Kopie erstellt haben.
3. Suchen Sie ({{search}}) nach **Continia Mandant Einrichtung** und wählen Sie dann den entsprechenden Link aus.
4. Geben Sie unter **Allgemein** einen neuen Mandantencode ein und klicken Sie auf **OK**, wenn Sie fertig sind.
5. Aktivieren Sie den Mandanten, indem Sie alle relevanten Lösungen mit [üblichen Verfahren aktivieren](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#so-aktivieren-sie-eine-losung). Wählen Sie beim Ausführen des unterstützten Setups **Testmandant** als Mandanttyp aus.
6. Um den neuen Mandantencode an Continia Online zu senden, suchen Sie ({{search}}) nach **OCR Konfigurationsdateien exportieren** und wählen Sie den entsprechenden Link aus. Ein Dialogfeld bestätigt, dass eine Reihe von Konfigurationsdateien exportiert wurde. Klicken Sie auf **OK**, um es zu schließen.

## So kopieren Sie einen Mandanten zur Verwendung als aktiver Mandant

So erstellen Sie einen aktiven Mandanten in einer Produktionsdatenbank, indem Sie einen Produktionsmandanten in derselben Datenbank kopieren:

1. Kopieren Sie den Mandanten und geben Sie ihm einen neuen Namen. Informationen hierzu finden Sie unter [Creating companies in Dynamics NAV](https://docs.microsoft.com/en-us/dynamics-nav/how-to--create-companies) (Microsoft-Artikel).
2. Deaktivieren Sie den ursprünglichen Mandanten:
   1. Öffnen Sie den ursprünglichen Mandanten (sofern Sie dort nicht bereits angemeldet sind).
   2. Verwenden Sie die Continia Lösungsverwaltung, um den ursprünglichen Mandanten [durch Deaktivieren aller aktiven Lösungen](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#so-deaktivieren-sie-eine-losung) zu deaktivieren. Wenn alle aktiven Lösungen deaktiviert wurden, wird auch der Mandant deaktiviert.
3. Aktivieren Sie den neuen Mandanten:
   1. Öffnen Sie den neuen Mandanten.
   2. Aktivieren Sie mithilfe der Continia Lösungsverwaltung den neuen Mandanten, indem Sie mindestens eine Lösung aktivieren. Verwenden Sie hierfür [das übliche Verfahren](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#so-aktivieren-sie-eine-losung).

## So kopieren Sie eine Produktionsdatenbank zur Verwendung als Testdatenbank

Wenn Sie eine Produktionsdatenbank kopieren, um sie als Testdatenbank zu verwenden, müssen Sie die Testdatenbank von den Produktionsdetails in Continia Online trennen (d. h. Details zum Aktivierungsstatus, dem Continia Web Approval Portal und den Continia Cloud OCR-Diensten). Hierzu müssen Sie einen neuen Satz an Demo-Client-Anmeldeinformationen angeben und anschließend alle relevanten Lösungen aktivieren.

> [!IMPORTANT]
> **Sie können dieselben Client Credentials nicht gleichzeitig in mehreren Datenbanken verwenden.**
>
> Der Aktivierungsstatus eines Mandanten wird in Continia Online gespeichert. Wenn das System prüft, ob ein Mandant aktiviert ist, erfolgt dies auf Grundlage der Client Credentials, des Mandantennamens und der Mandanten-GUID, die für den Mandanten in der Datenbank gespeichert sind. Wenn Sie die Client Credentials nicht ändern, wird die neue Testdatenbank als Produktionsdatenbank aktiviert und übernimmt dabei den Aktivierungsstatus der vorhandenen Produktionsdatenbank. Außerdem wird die Testdatenbank mit Produktionsdetails in Continia Online verknüpft (in Bezug auf das Continia Web Approval Portal und die Continia Cloud OCR-Dienste).

So kopieren Sie eine Produktionsdatenbank zur Verwendung als Testdatenbank:

1. Stellen Sie die neue Datenbank wieder her.
2. Verwenden Sie Continia Lösungsverwaltung, [um die Client Credentials](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-change-client-credentials) in Client-Demoanmeldeinformationen zu ändern.
3. Suchen Sie ({{search}}) nach **Continia Mandant Einrichtung** und wählen Sie dann den entsprechenden Link aus.
4. Geben Sie unter **Allgemein** einen neuen Mandantencode ein und klicken Sie auf **OK**, wenn Sie fertig sind.
5. Aktivieren Sie den Mandanten, indem Sie alle relevanten Lösungen mit [üblichen Verfahren aktivieren](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#so-aktivieren-sie-eine-losung). Da Sie Demo-Client Credentials verwenden, wird der Mandant standardmäßig als Testmandant registriert.
6. Wenn Sie On-Premises OCR verwenden und in Ihren Belegkategorien E-Mail-Adressen angegeben haben, entfernen Sie diese E-Mail-Adressen oder weisen Sie andere zu. Suchen Sie ({{search}}) dazu nach **Belegkategorien** und wählen Sie den entsprechenden Link aus. Wählen Sie eine Kategorie (nicht deren Code) aus und klicken Sie in der Aktionsleiste auf **Bearbeiten**. Ändern Sie auf dem Inforegister **Allgemein** den Wert des Felds **E-Mail**.
7. Um den neuen Mandantencode an Continia Online zu senden, suchen Sie ({{search}}) nach **OCR Konfigurationsdateien exportieren** und wählen Sie den entsprechenden Link aus. Ein Dialogfeld bestätigt, dass eine Reihe von Konfigurationsdateien exportiert wurde. Klicken Sie auf **OK**, um es zu schließen.

## Eine Produktionsdatenbank auf einen neuen Server kopieren

Wenn Sie eine Produktionsdatenbank auf einen neuen Server kopieren, müssen Sie die [Client Credentials](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#so-andern-sie-die-client-credentials) in einer der Datenbanken aktualisieren oder die Client Credentials aus einer der Datenbanken löschen. Um die Client Credentials zu löschen, führen Sie die Tabelle aus und löschen Sie den entsprechenden Datensatz in der Tabelle.

## Daten mithilfe von Importtools in einen Mandanten kopieren

Beim Importieren von Daten von einem Mandanten in einen anderen mithilfe von Importtools wie Rapid Start müssen Sie sicherstellen, dass Continia Core-Tabellen übersprungen werden, da diese die Aktivierungsdaten des aktuellen Mandanten speichern. Wenn die Continia Core-Tabellen nicht übersprungen werden, könnten Sie die Daten beschädigen und den Aktivierungsstatus des Mandanten ungültig machen.

Daher müssen Sie den Import von Daten überspringen, die in Objekten im folgenden Bereich gespeichert sind: 6192810 bis 6192868.
