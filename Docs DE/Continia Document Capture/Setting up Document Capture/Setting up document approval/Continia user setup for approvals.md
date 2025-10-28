---
title: Continia-Benutzereinrichtung für Genehmigungen in Document Capture
date: 15-01-2025
description: So konfigurieren Sie Benutzer als Genehmiger, und Sie erhalten einen Überblick über Berechtigungen für Genehmigungsadministratoren.
id: DC-23
lang: de
---

# Continia Benutzereinrichtung für Genehmigungen

Damit ein Benutzer Belege entweder in Continia Document Capture oder im Continia Web Approval Portal genehmigen kann, muss der Benutzer zuerst als Genehmiger konfiguriert werden. In diesem Artikel finden Sie die entsprechenden Informationen dazu.

> [!NOTE]
> Die Konfiguration von Benutzern als Genehmiger erfolgt in der **Continia Benutzereinrichtung**. Dies gilt auch für Continia Expense Management. Weitere Informationen finden Sie unter [Expense-Benutzer für Expense Management einrichten](@EM-36).

Die **Continia Benutzereinrichtung** ist eine Erweiterung der Standardtabelle zum Einrichten von Benutzern in Microsoft Dynamics 365 Business Central (BC). Viele der in der **Continia Benutzereinrichtung** angezeigten Felder stammen ursprünglich aus dieser Tabelle und werden auch in der **Genehmigungsbenutzereinrichtung** angezeigt. Wenn Sie Einstellungen in einer der beiden Einrichtungen ändern, werden sie auch automatisch in der anderen Einrichtung geändert.

Wenn Sie einen Datensatz in der **Continia Benutzereinrichtung** erstellen, wird automatisch auch ein Datensatz in der BC-Benutzereinrichtung erstellt. Wenn Sie einen Datensatz in der **Continia Benutzereinrichtung** löschen, wird der entsprechende Datensatz in der BC-Benutzereinrichtung möglicherweise ebenfalls zu Bereinigungszwecken automatisch gelöscht – jedoch nur unter bestimmten Umständen. Wenn Sie die **Continia Benutzereinrichtung** nach einer gewissen Zeit löschen, den Datensatz in der BC-Benutzereinrichtung jedoch zuvor mit Feldern gefüllt haben, die in der **Continia Benutzereinrichtung** nicht sichtbar sind, wird der Datensatz in der BC-Benutzereinrichtung nicht gelöscht.

## So richten Sie Benutzer als Genehmiger ein

So ermöglichen Sie einem Benutzer das Genehmigen von Dokumenten:

1. Wählen Sie das Symbol {{search}}, geben Sie **Continia Benutzereinrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Benutzer aus, den Sie als Genehmiger einrichten möchten.
3. Wählen Sie in der Aktionsleiste **Bearbeiten**, um die **Continia Benutzereinrichtung Karte** des ausgewählten Benutzers zu öffnen.
4. Füllen Sie im Inforegister **Allgemein** die Felder nach Bedarf aus. Die folgenden Felder sind Pflichtfelder:
   - Geben Sie unter **Verkäufer/Einkäufer** den Namen des ausgewählten Benutzers ein, wie er in Business Central registriert ist. Dieser Name wird mit dem angegebenen Benutzer synchronisiert.
   - Geben Sie unter **Benutzer ID - nächster Genehmiger (Manager)** die ID des Managers des ausgewählten Benutzers ein. Sie können hier auch einen anderen Genehmiger der nächsten Ebene eingeben, der Belege genehmigen kann, wenn die Limits des Benutzers nicht ausreichen).
   - Unter **Einkaufsrechnung- und Gutschriftsgenehmigung** müssen Sie entweder unter **Genehmigungslimit** einen maximalen Genehmigungsbetrag für den ausgewählten Benutzer eingeben oder, falls zutreffend, **Unbegrenzte Genehmigung** auswählen.
   > [!NOTE]
   > Wenn Sie Zuweisungsberechtigungen für den Benutzer oder für eine Gruppe, der der Benutzer angehört, konfigurieren möchten, müssen Sie außerdem **Darf Buchungszeilen editieren** aktivieren. Weitere Informationen finden Sie unter [So konfigurieren Sie die individuellen Berechtigungen von Genehmigern](#so-konfigurieren-sie-die-individuellen-berechtigungen-von-genehmigern) und [So konfigurieren Sie Konten- und Dimensionsberechtigungen für eine Gruppe](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/approval-user-groups#so-konfigurieren-sie-konto--und-dimensionsberechtigungen-fur-eine-gruppe).
   >
   > Wenn der Benutzer ein Genehmigungsadministrator sein soll, schalten Sie den Schalter **Genehmigungsadministrator** um. Beachten Sie, dass dadurch auch automatisch die entsprechende Einstellung in der **Genehmigungsbenutzereinrichtung** aktiviert wird. Außerdem wird dem Benutzer hierdurch zusätzlich zu den Continia-spezifischen Berechtigungen eine Reihe standardmäßiger Genehmigungsadministratorberechtigungen gewährt , die unter [Berechtigungen für Genehmigungsadministratoren](#berechtigungen-fur-genehmigungsadministratoren) weiter unten erwähnt werden.
5. Wählen Sie im Inforegister **Web Genehmigungen** den Genehmigungs-Client aus, den der ausgewählte Benutzer zum Genehmigen von Belegen verwenden kann. Der ausgewählte Genehmigungs-Client wird immer dann geöffnet, wenn der Benutzer einen Link in einer [Benachrichtigungs-E-Mail](Email notifications.md) öffnet. Beachten Sie, dass in der Weiterleitungsliste nur Benutzer mit einem Wert unter **Genehmigungs-Client** in der **Continia Benutzereinrichtung** angezeigt werden. Weitere Informationen finden Sie unter [Benutzerspezifische Listen von Genehmigern für die Genehmigungsweiterleitung erstellen](@DC-138).

> [!IMPORTANT]
> Sobald Sie einen Benutzer als Genehmiger eingerichtet haben, müssen Sie diesem Benutzer eine entsprechende Business Central-Lizenz zuweisen, damit sich der Benutzer anmelden und Genehmigungen vornehmen kann. Hierfür sollte eine Team Members-Lizenz ausreichend sein, vorbehaltlich der Microsoft-Lizenzbedingungen. Diese sind im Microsoft Dynamics 365 Business Central Licensing Guide, der auf der [Business Central](https://dynamics.microsoft.com/business-central/overview/)-Website zum Download zur Verfügung steht, festgelegt. Informationen zum Zuweisen von Lizenzen zu Benutzern finden Sie im Microsoft-Artikel [Benutzer gemäß Lizenzen erstellen](https://learn.microsoft.com/de-de/dynamics365/business-central/ui-how-users-permissions).

## Berechtigungen für Genehmigungsadministratoren

Genehmigungsadministratoren verfügen über mehr Berechtigungen als normale Genehmiger. Benutzer, die als Genehmigungsadministrator eingerichtet wurden, können die folgenden Aktionen ausführen:

- Weiterleiten von Genehmigungsanforderungen im Auftrag anderer Benutzer. Normale Genehmiger erhalten eine Fehlermeldung, wenn sie dies versuchen.
- Verwenden der [Funktion **Genehmigung erzwingen**](@DC-36).
- [Löschen oder Bearbeiten von Genehmigungsanforderungen](@DC-39), einschließlich Hinzufügen und Ändern von Benutzern.
- Genehmigen von Belegen, bei denen importierte und zugewiesene Beträge nicht übereinstimmen. Normale Genehmiger erhalten in solchen Fällen eine Fehlermeldung, während Genehmigungsadministratoren die Möglichkeit haben, fortzufahren.
- Aktivieren der automatischen Genehmigung und automatischen Buchung in **Rechnung Reg. Schritt 2** auf Vorlagenebene. Administratoren ohne Genehmigungsberechtigungen, die versuchen, **Rechnung Reg. Schritt 2** auf **Freigeben** oder **Buchen** zu setzen, erhalten eine Fehlermeldung, die auf die Einschränkungen hinweist.
- Ändern [importierter Beträge](/continia-document-capture/setting-up-document-capture/setting-up-purchase-documents/configuring-purchase-documents#importierte-betrage-anpassen).

## Konten- und Dimensionsberechtigungen konfigurieren

Wenn Sie einen Benutzer [wie oben beschrieben](#so-richten-sie-benutzer-als-genehmiger-ein) als Genehmiger eingerichtet haben, können Sie die Konten- und Dimensionsberechtigungen für diesen Benutzer konfigurieren. Verwenden Sie hierfür die folgenden zwei Aktionen in der Aktionsleiste auf der Seite **Continia Benutzereinrichtung** (diese sind auch auf der **Continia Benutzereinrichtung Karte** verfügbar):

- **Genehmigungsgruppen** – hiermit können Sie [einem Benutzer eine oder mehrere Gruppenberechtigung(en) hinzufügen](#so-weisen-sie-einem-genehmiger-gruppenberechtigungen-zu).
- **Genehmigungsberechtigungen** – hiermit können Sie die [individuellen Berechtigungen für den Benutzer konfigurieren](#so-konfigurieren-sie-die-berechtigungen-einzelner-genehmiger).

> [!IMPORTANT]
> Damit beide Aktionen verwendet werden können, muss zuerst die Funktion **Benutze Konten und Dimensionseinschränkungen bei der Freigabe** auf der Seite **Document Capture Einrichtung** aktiviert werden. Eine Anleitung hierfür finden Sie unter [So richten Sie die Einkaufsgenehmigung ein](@DC-22#so-richten-sie-die-einkaufsgenehmigung-ein). Um einem einzelnen Benutzer Gruppenberechtigungen zuweisen können, muss mindestens eine [Genehmigungsgruppe eingerichtet werden](Approval user groups.md).

## So weisen Sie einem Genehmiger Gruppenberechtigungen zu

Um einem Benutzer, der als Genehmiger konfiguriert wurde, eine oder mehrere Gruppenberechtigung(en) zuzuweisen, gehen Sie folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Continia Benutzereinrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Benutzer aus, dessen Berechtigungen Sie konfigurieren möchten.
3. Wählen Sie in der Aktionsleiste **Document Capture** > **Genehmigungsgruppen** aus.
4. Fügen Sie auf der Seite, die sich öffnet, die Gruppe(n) hinzu, deren Berechtigungen Sie dem Benutzer zuweisen möchten.
   > [!NOTE]
   > Wenn Sie einem Benutzer Gruppenberechtigungen zuweisen, werden diese auf die individuellen Berechtigungen des Benutzers übertragen, was zu gewissen Einschränkungen der Benutzerberechtigungen führt. Sie müssen daher mit möglichen Beschränkungen rechnen, wenn Sie außerdem die [individuellen Berechtigungen von Genehmigern konfigurieren](#so-konfigurieren-sie-die-individuellen-berechtigungen-von-genehmigern) möchten. Beides sollte jedoch gleichzeitig möglich sein, und das System weist Sie darauf hin, wenn es Konflikte zwischen den individuellen Berechtigungen eines Benutzers und den zugewiesenen Gruppenberechtigungen gibt.

## So konfigurieren Sie die individuellen Berechtigungen von Genehmigern

Beim Einrichten der Berechtigungen eines Genehmigers können Sie die folgenden zwei Arten von Berechtigungen konfigurieren:

- **Zuweisungsberechtigungen** – sie legen fest, welche Konten und Dimensionen der Benutzer beim Zuweisen von Konten/Dimensionen zu Rechnungszeilen während der Genehmigung auswählen kann
- **Genehmigungsberechtigungen** – sie legen fest, welche Rechnungszeilen der Benutzer genehmigen kann (nur Zeilen, denen Konten/Dimensionen zugewiesen wurden, für die der Benutzer Berechtigungen hat)

> [!IMPORTANT]
> Beachten Sie, dass Zuweisungsberechtigungen nur mit dem Web Approval Portal verwendet werden können.
>
> Damit Zuweisungsberechtigungen wirksam werden, muss außerdem die Funktion **Darf Buchungszeilen editieren** aktiviert sein, wie unter [So richten Sie Benutzer als Genehmiger ein](#so-richten-sie-benutzer-als-genehmiger-ein) (Schritt 4) beschrieben. Andernfalls kann der Benutzer die Belege zur Genehmigung nicht bearbeiten und diese nur genehmigen oder ablehnen.

So konfigurieren Sie die individuellen Berechtigungen eines Benutzers, der als Genehmiger eingerichtet wurde:

1. Wählen Sie das Symbol {{search}}, geben Sie **Continia Benutzereinrichtung** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie den Benutzer aus, dessen Berechtigungen Sie konfigurieren möchten.
3. Wählen Sie in der Aktionsleiste **Document Capture** > **Benutzerrechte** aus.
4. Wählen Sie auf der Seite, die geöffnet wird, in der Spalte **Art** den Berechtigungstyp aus. **Sachkonto**, **Artikel**, **Anlage**, **Zu/Abschlag** und **Projekt** sind alle Arten von Kontoberechtigungen, während **Dimension** die Dimensionsberechtigungen darstellt.
5. Wenn Sie in Schritt 4 oben **Dimension** ausgewählt haben, fügen Sie in der Spalte **Dimensionscode** einen Dimensionscode hinzu. Wenn Sie in Schritt 4 etwas anderes als **Dimension** ausgewählt haben, lassen Sie das Feld leer.
6. Geben Sie in der Spalte **Zuweisungsberechtigung** an, wie Sie die Zuweisungsberechtigungen einrichten möchten, die dieser Benutzer haben soll.
   > [!TIP]
   > Die Optionen werden im Folgenden erläutert:
   >
   > - **Alle**: Der Benutzer kann den Rechnungszeilen bei der Genehmigung alle Konten/Dimensionen zuweisen, und es ist keine weitere Einrichtung erforderlich.
   > - **Markierte**: Der Benutzer kann die Konten/Dimensionen zuweisen, die Sie in der Spalte **Anzahl der Zuweisungsauswahl** auswählen (die Auswahl ist dann obligatorisch).
   > - **Nicht Markierte**: Der Benutzer kann alle Konten/Dimensionen zuweisen, **mit Ausnahme** derer, die Sie in der Spalte **Anzahl der Zuweisungsauswahl** auswählen (die Auswahl ist dann obligatorisch).
   > - **Filter**: Der Benutzer kann die Konten/Dimensionen zuweisen, die Sie in der Spalte **Zuweisungsfilter für Auswahl** auswählen (die Auswahl ist dann obligatorisch).
7. Geben Sie in der Spalte **Genehmigungsberechtigung** an, wie Sie die Genehmigungsberechtigungen einrichten möchten, die dieser Benutzer haben soll.
   > [!TIP]
   > Die Optionen werden im Folgenden erläutert:
   >
   > - **Alle**: Der Benutzer kann Rechnungszeilen mit beliebigen Konten/Dimensionen genehmigen, und es ist keine weitere Einrichtung erforderlich.
   > - **Markierte**: Der Benutzer kann Rechnungszeilen mit den Konten/Dimensionen zuweisen, die Sie in der Spalte **Anzahl der Genehmigungsauswahl** auswählen (die Auswahl ist dann obligatorisch).
   > - **Nicht markierte**: Der Benutzer kann Rechnungszeilen mit allen Konten/Dimensionen zuweisen, **mit Ausnahme** derer, die Sie in der Spalte **Anzahl der Genehmigungsauswahl** auswählen (die Auswahl ist dann obligatorisch).
   > - **Filter**: Der Benutzer kann Rechnungszeilen mit den Konten/Dimensionen genehmigen, die Sie in der Spalte **Zuweisungsfilter für Genehmigung** auswählen (die Auswahl ist dann obligatorisch).
   > - **Gleich wie Zuweisung**: Die in Schritt 6 konfigurierten Einstellungen für Zuweisungsberechtigungen werden kopiert und auch als Genehmigungsberechtigungen des Benutzers verwendet.
8. Wenn Sie in Schritt 6 oben **Filter** ausgewählt haben: Wählen Sie in der Spalte **Zuweisungsfilter für Auswahl** die Konten/Dimensionen aus, die der Benutzer Rechnungszeilen während der Genehmigung zuweisen können soll.
9. Wenn Sie in Schritt 7 oben **Filter** ausgewählt haben: Wählen Sie in der Spalte **Zuweisungsfilter für Genehmigung** die Konten/Dimensionen aus, für die der Benutzer Rechnungszeilen genehmigen können soll.
   > [!NOTE]
   > Für beide Filteroptionen (Schritte 8 und 9) können Sie Bereiche oder mehrere Konten/Dimensionen mit der Standardfilternotation eingeben – zum Beispiel **10100..10500** und **10100|10500**.
10. Wenn Sie in Schritt 6 oben **Markierte** oder **Nicht markierte** ausgewählt haben: Wählen Sie in der Spalte **Anzahl der Zuweisungsauswahl** die Konten/Dimensionen aus, die der Benutzer Rechnungszeilen während der Genehmigung zuweisen/nicht zuweisen können soll.
11. Wenn Sie in Schritt 7 oben **Markierte** oder **Nicht markierte** ausgewählt haben: Wählen Sie in der Spalte **Anzahl der Genehmigungsauswahl** die Konten/Dimensionen aus, für die der Benutzer Rechnungszeilen genehmigen/nicht genehmigen können soll.

## Informationen zum Thema

[Benutzerspezifische Listen von Genehmigern für die Genehmigungsweiterleitung erstellen](@DC-138)\
[Einkaufsgenehmigung aktivieren](@DC-22)\
[Genehmigungsgruppen](Approval user groups.md)\
[E-Mail-Benachrichtigungen](Email notifications.md)
