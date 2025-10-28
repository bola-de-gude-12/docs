---
title: Expense-Benutzer für Expense Management einrichten
date: 22-10-2024
description: Erfahren Sie, wie Sie Benutzer für Expense Management hinzufügen.
id: EM-36
lang: de
---

# Expense-Benutzer für Expense Management einrichten

Um Expense-Benutzer hinzuzufügen und Expense-Workflows in Expense Management zu initiieren, müssen Sie sie auf der Seite **Continia Benutzereinrichtung** konfigurieren. Auf dieser Seite können Sie für jeden Expense-Benutzer wichtige Einstellungen festlegen, beispielsweise seine Expense-Benutzergruppe und die Dokumentensichtbarkeit.

> [!NOTE]
> Die **Continia Benutzereinrichtung** ist auch relevant für Continia Document Capture. Weitere Informationen finden Sie unter [Continia Benutzereinrichtung für Genehmigungen](@DC-23).

So erstellen Sie einen Expense-Benutzer für Expense Management:

1. Wählen Sie das Symbol {{search}}, geben Sie **Continia Benutzereinrichtung** ein, und wählen Sie den zugehörigen Link.

2. Wählen Sie auf der **Continia Benutzereinrichtung Karte** in der Aktionsleiste **Neu** aus und füllen Sie im Inforegister **Allgemein** die folgenden Felder aus:

   | Feld                             | Beschreibung                                                                                                                                                                                                                           |
   | -------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | Continia Benutzer-ID             | Wählen Sie den Benutzer aus. Alle Genehmiger müssen Business Central-Benutzer sein, und Sie können diese mit der Lookup-Schaltfläche in diesem Feld anzeigen.                                          |
   | Name                             | Expense-Benutzer, die keine Genehmiger sind, benötigen keine Business Central-Lizenz. Wenn der Benutzer noch kein Business Central-Benutzer ist, werden Sie vom System aufgefordert, ihn hinzuzufügen. |
   | E-Mail                           | Geben Sie die E-Mail-Adresse des Expense-Benutzers ein, falls sie nicht automatisch ausgefüllt wird.                                                                                                                   |
   | Registrierung erzwingen zulassen | Legt fest, ob der Benutzer Fehler und Warnungen überschreiben kann, um die Registrierung eines Dokuments zu erzwingen.                                                                                                 |
   | Genehmigungsadministrator        | Legt fest, ob der Benutzer ein Genehmigungsadministrator ist, der für die Verwaltung von Genehmigungsprozessen verantwortlich ist.                                                                                     |

3. Geben Sie im Inforegister **Web Genehmigungen** den Genehmigungs-Client an. Hiermit geben Sie den Client an, den der Benutzer zum Genehmigen von Dokumenten verwendet. Diese Informationen werden beim Versenden einer E-Mail mit zu genehmigenden Dokumenten verwendet. Die E-Mail enthält einen Hyperlink für den Zugriff auf die zu genehmigenden Dokumente mit dem ausgewählten Client. Nur Benutzer, für die als Genehmigungs-Client Continia Web-Genehmigung ausgewählt ist, können auf das Web Approval Portal zugreifen.

4. Füllen Sie im Inforegister **Expense Management** die folgenden Felder aus:

   | Feld                                 | Beschreibung                                                                                                                                                                                                                                                                                                                                                              |
   | ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | Expense-Benutzer                     | Wenn dies aktiviert ist, können Benutzer Belege und andere in der Expense Management Einrichtung definierte Dokumente erstellen.                                                                                                                                                                                                                          |
   | Expense Management Anmeldetyp        | Legt fest, wie sich der Benutzer anmeldet. Die Optionen sind **Continia Online** oder **Microsoft 365**. Wenn **Microsoft 365** ausgewählt ist, müssen sich Benutzer mit ihren Microsoft 365-Anmeldeinformationen anmelden. Neue Benutzer erhalten eine Willkommens-E-Mail mit Anweisungen zur Anmeldung. |
   | Kann genehmigte Dokumente bearbeiten | Legt fest, ob der Benutzer Dokumente bearbeiten kann, deren Genehmigung aussteht oder die bereits freigegeben wurden.                                                                                                                                                                                                                                     |
   | Dokumentsichtbarkeit einschränken    | Wenn diese Option aktiviert ist, kann der Benutzer nur seine eigenen Dokumente anzeigen.                                                                                                                                                                                                                                                                  |
   | Kreditorennr.        | Hier richten Sie einen Kreditor für Expense-Benutzer ein. Sie können den Kreditor, den Sie für den Mitarbeiter erstellt haben, mithilfe der Lookup-Schaltfläche auswählen. Über die Kreditorennummer wird gebucht und bei der Rückerstattung an den Benutzer wird der Saldo bei diesem Kreditor angezeigt.                |
   | Mitarbeiternr.       | Die Mitarbeiternummer wird für die Buchung verwendet. Wenn sowohl **Mitarbeiternr.** als auch **Kreditorennr.** ausgefüllt wurden, wird **Mitarbeiternr.** verwendet.                                                                                                                     |
   | Spesen Benutzergruppe                | Legt die Gruppe fest, zu der der Expense-Benutzer gehört.                                                                                                                                                                                                                                                                                                 |
   | Spesen Erinnerung                    | Gibt den Code an, der zum Senden von Erinnerungen an Expense-Benutzer verwendet wird.                                                                                                                                                                                                                                                                     |
   | Genehmiger Name                      | Der Genehmiger für den Expense-Benutzer.                                                                                                                                                                                                                                                                                                                  |
   | Genehmigungslimit Unbegrenzt         | Gibt an, dass der Benutzer uneingeschränkte Genehmigungsrechte für Belege hat und kein Genehmigungslimit festgelegt ist.                                                                                                                                                                                                                                  |
   | Betrag                               | Legt den Höchstbetrag fest, den der Benutzer genehmigen kann.                                                                                                                                                                                                                                                                                             |

5. Wenn Sie mit der Eingabe der Benutzerdetails fertig sind, kehren Sie zur Seite **Continia Benutzereinrichtung** zurück und wählen Sie in der Aktionsleiste **Benutzer exportieren** aus. Dadurch werden Willkommens-E-Mails generiert und an neu erstellte Expense-Benutzer gesendet. Diese E-Mails enthalten einen Link zum Aktivieren ihrer Rolle und Erstellen eines Kennworts sowie Links zum Herunterladen der Expense App und des Expense Portals.
