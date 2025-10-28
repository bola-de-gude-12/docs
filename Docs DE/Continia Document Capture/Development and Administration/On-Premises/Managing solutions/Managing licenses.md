---
title: Lizenzen verwalten
date: 15-09-2025
description: So verwalten Sie Continia-Lizenzen für On-Premises Business Central.
id: DC-488
lang: de
---

# Lizenzen verwalten

Dieser Artikel enthält Informationen zur Verwaltung von Continia-Lizenzen für Microsoft Dynamics 365 Business Central On-Premises. Weitere Informationen zur On-Premises-Lösungsverwaltung finden Sie unter [Continia Lösungsverwaltung verwenden (On-Premises)](@DC-151). Informationen zur Lösungsverwaltung für Business Central Online finden Sie unter [Continia Lösungsverwaltung verwenden (Online)](@DC-107).

Mithilfe der folgenden Anleitungen können Sie Lösungslizenzen kaufen oder kündigen, Module (manchmal auch als Granules bezeichnet) verwalten und Mandanten hinzufügen oder entfernen.

> [!IMPORTANT]
> Alle Anleitungen in diesem Artikel richten sich an Continia-Partner, da nur Partner die genannten Schritte durchführen können. Wenn eine der Anleitungen für Sie relevant ist, wenden Sie sich bitte an [Ihre/n Continia-Partner(in)](@DC-487) und bitten Sie ihn bzw. sie, die entsprechenden Anleitungen für Sie auszuführen.

## So kaufen Sie eine Lizenz

Wenn Sie als Partner eine Lizenz für eine oder mehrere Continia-Lösungen für einen Kunden erwerben möchten, gehen Sie folgendermaßen vor:

1. Gehen Sie zur [Continia PartnerZone](https://partnerzone.continia.com/partnerzone/dashboard/).
2. Klicken Sie im Menü oben auf **License Manager**. Beachten Sie, dass Sie Administratorrechte haben müssen, um darauf zugreifen zu können.
3. Sie haben die folgenden Optionen:
   - Suchen Sie in der Kundenliste den Kunden, für den Sie eine Lizenz kaufen möchten, und klicken Sie rechts auf **Manage**, um die Seite **Solutions manager** zu öffnen.
   - Wenn der Kunde noch nicht auf der Liste ist, legen Sie einen neuen Kunden an: Klicken Sie oben rechts auf **Create new customer** und fügen Sie alle relevanten Details hinzu. Diese finden Sie im [Microsoft PartnerSource Business Center](https://businesscenter.mbs.microsoft.com/). Beachten Sie, dass **MS Voice ID** die Microsoft-Lizenznummer des Kunden ist. Klicken Sie auf **Next**, um die Seite **Solutions manager** zu öffnen.
4. Wählen Sie auf der Seite **Solutions manager** die Lösung aus, für die Sie eine Lizenz erwerben möchten.
5. Wählen Sie den gewünschten Lizenztyp und die Anzahl der Benutzer aus. Die angezeigten Optionen richten sich nach der Benutzeranzahl, die Sie beim Einrichten des Kunden eingegeben haben. Daher sind einige Optionen möglicherweise abgeblendet.
   > [!NOTE]
   > Wenn Sie oben in Schritt 4 **Document Capture** auswählen, müssen Sie nach Auswahl des Lizenztyps und der Benutzeranzahl auch die gewünschte OCR-Technologie auswählen.
6. Geben Sie unter **Companies** den Namen des Unternehmens des Kunden ein und klicken Sie auf **Add company**, um weitere Mandanten hinzuzufügen. Beachten Sie, dass für zusätzliche Unternehmen zusätzliche Kosten anfallen, da diese nicht in der Basislizenz enthalten sind.
7. Klicken Sie auf **Add license**, wenn Sie fertig sind.
8. Wiederholen Sie die Schritte 4 bis 7 für alle weiteren Lösungen, für die Sie eine Lizenz erwerben möchten.
9. Klicken Sie im blauen Feld rechts auf **Complete order**, um die Bestellbestätigungsseite zu öffnen. Geben Sie in die angezeigten Felder ggf. weitere Informationen ein (alle optional) und wählen Sie **Submit order**, wenn Sie fertig sind.

Die aufgegebene Bestellung wird nun an Continia übermittelt und Sie als Partner erhalten eine Bestellbestätigung per E-Mail. Sobald die Bestellung bearbeitet wurde, wird Ihnen eine weitere E-Mail mit den Anmeldeinformationen zugesandt, die Sie zum [Aktivieren der lizenzierten Lösungen](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#so-aktivieren-sie-eine-losung) verwenden müssen. Beachten Sie, dass die Bearbeitung Ihrer Bestellung bis zu zwei Tage dauern kann, da alle Bestellungen manuell vom Continia-Personal bearbeitet werden. Abschließend wird Ihnen zu einem späteren Zeitpunkt noch eine dritte E-Mail mit einer Rechnung zugesandt.

## Eine Lizenz kündigen

Wenn Sie aus irgendeinem Grund eine Lizenz kündigen möchten, senden Sie eine Kündigungs-E-Mail mit dem Namen und der Lizenznummer des Kunden an <accounting@continia.com>. Beachten Sie, dass diese E-Mail spätestens 30 Tage vor dem Datum der Lizenzverlängerung bei Continia eingehen muss.

Alle Lizenzen verlängern sich am Ende der Lizenzlaufzeit automatisch, das heißt Sie müssen jede Lizenz, die Sie nicht mehr nutzen möchten, aktiv kündigen, damit sie beendet wird.

## So fügen Sie Module hinzu

> [!NOTE]
> Sie können Module erst hinzufügen, wenn eine aktive Lizenz für diese vorliegt. Denken Sie daher unbedingt daran, [eine Lizenz zu kaufen](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-licenses#so-kaufen-sie-eine-lizenz), bevor Sie die folgenden Schritte ausführen.

Als Partner können Sie einer Kundenlizenz Module hinzufügen, indem Sie die folgenden Schritte ausführen:

1. Melden Sie sich beim [Microsoft PartnerSource Business Center](https://businesscenter.mbs.microsoft.com/) an.
2. Suchen Sie den entsprechenden Kunden anhand der Microsoft-Kontonummer des Kunden.
3. Klicken Sie auf **Registered ISV Modules**.
4. Klicken Sie auf **Add ISV Module**.
5. Wählen Sie in der Liste der ISV-Anbieter **Continia** aus.
6. Wählen Sie das/die Modul(e) aus, das/die Sie der Lizenz hinzufügen möchten. Eine Liste aller Continia-Module finden Sie unter [ISV modules to add to NAV/Business Central license](https://partnerzone.continia.com/partnerzone/my-continia/isv-modules/).
7. Klicken Sie auf **Register**, um der Lizenz die ausgewählten Module hinzuzufügen.
8. Laden Sie eine aktualisierte Lizenz für den Kunden herunter.
9. Laden Sie die aktualisierte Lizenz in die Business Central-Umgebung Ihres Kunden hoch und bitten Sie den Kunden, Business Central neu zu starten.

## So entfernen Sie Module

Als Partner können Sie von einer Kundenlizenz Module entfernen, indem Sie die folgenden Schritte ausführen:

1. Senden Sie eine E-Mail an <accounting@continia.com> mit Informationen darüber, welche Module entfernt werden sollen.
2. Melden Sie sich beim [Microsoft PartnerSource Business Center](https://businesscenter.mbs.microsoft.com/) an.
3. Suchen Sie den entsprechenden Kunden anhand der Microsoft-Kontonummer des Kunden.
4. Klicken Sie auf **Registered ISV Modules**.
5. Heben Sie die Auswahl aller Module auf, die Sie entfernen möchten, um sie zu deaktivieren.
6. Klicken Sie auf **Register**, um die ausgewählten Module von der Lizenz zu entfernen.
7. Laden Sie eine aktualisierte Lizenz für den Kunden herunter.
8. Laden Sie die aktualisierte Lizenz in die Business Central-Umgebung Ihres Kunden hoch und bitten Sie den Kunden, Business Central neu zu starten.

## So fügen Sie Mandanten hinzu

Um der Continia-Lösung eines Kunden einen oder mehrere Mandanten hinzuzufügen, gehen Sie folgendermaßen vor:

1. Gehen Sie zur [Continia PartnerZone](https://partnerzone.continia.com/partnerzone/dashboard/).
2. Klicken Sie im Menü oben auf **License Manager**. Beachten Sie, dass Sie Administratorrechte haben müssen, um darauf zugreifen zu können.
3. Suchen Sie in der Kundenliste den Kunden, für den Sie eine Lizenz kaufen möchten, und klicken Sie rechts auf **Manage**, um die Seite **Solutions manager** zu öffnen.
4. Wählen Sie auf der Seite **Solutions manager** die Lösung aus, der Sie einen Mandanten hinzufügen möchten.
5. Klicken Sie unter **Additional companies** auf **Add additional company** und geben Sie den Namen des Mandanten ein, den Sie hinzufügen. Beachten Sie, dass für zusätzliche Unternehmen zusätzliche Kosten anfallen, da diese nicht in der Basislizenz enthalten sind.
6. Klicken Sie auf **Add license**, wenn Sie fertig sind.
7. Wiederholen Sie die Schritte 4 bis 6 für alle weiteren Lösungen, denen Sie Mandanten hinzufügen möchten.
8. Klicken Sie im blauen Feld rechts auf **Complete order**, um die Bestellbestätigungsseite zu öffnen. Geben Sie in die angezeigten Felder ggf. weitere Informationen ein (alle optional) und klicken Sie auf **Submit order**, wenn Sie fertig sind.

## Mandanten entfernen

Als Partner können Sie ein oder mehrere Mandanten aus der Lizenz Ihres Kunden entfernen, indem Sie eine E-Mail mit Informationen darüber, welche Mandanten entfernt werden sollen, an <accounting@continia.com> senden. Diese E-Mail sollte auch den Namen und/oder die Voice-ID des Kunden enthalten.

## Informationen zum Thema

[Lösungen verwalten](@DC-151)  
[Continia Document Capture Partner](@DC-487)  
[Continia PartnerZone](https://partnerzone.continia.com/partnerzone/dashboard/)  
[Microsoft PartnerSource Business Center](https://businesscenter.mbs.microsoft.com/)