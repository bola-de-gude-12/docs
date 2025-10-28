---
title: Genehmigungsgruppen in Document Capture
date: 31-03-2025
description: So richten Sie Genehmigungsgruppen mit bestimmten Konten- und Dimensionsberechtigungen in Document Capture ein.
id: DC-24
lang: de
---

# Genehmigungsgruppen

Sie können Genehmigungsgruppen mit bestimmten Konten- und Dimensionsberechtigungen einrichten, die für alle Mitglieder der Gruppe gelten. Dies ist nützlich, wenn Sie über eine relativ große Gruppe von Genehmigern verfügen, die alle über dieselben Zuweisungs- und Genehmigungsberechtigungen verfügen müssen, da Sie dann die Berechtigungen der Genehmiger nicht einzeln neu konfigurieren müssen.

> [!NOTE]
> Durch die Aktivierung der Genehmigung von Einkaufsrechnungen, Einkaufsgutschriften, Einkaufsbestellungen und/oder Reklamationen wird automatisch eine Genehmigungsbenutzergruppe mit dem Code ALL erstellt, das heißt mit allen Berechtigungen für alle Typen und Dimensionen. Dies ist aber nur der Fall, wenn eine solche Gruppe noch nicht vorhanden ist.

## So richten Sie Genehmigungsgruppen ein

So erstellen Sie eine Gruppe von Genehmigern und fügen ihr Mitglieder hinzu:

1. Wählen Sie das Symbol {{search}}, geben Sie **Genehmigungsgruppen** ein, und wählen Sie dann den zugehörigen Link.

2. Wählen Sie in der Aktionsleiste **Neu** aus, um eine Genehmigungsgruppe zu erstellen.

3. Geben Sie in der Spalte **Code** den Code ein, mit dem Sie die neue Gruppe identifizieren möchten.

4. Geben Sie in der Spalte **Name** den Namen der neuen Gruppe ein.

5. Um der Gruppe Mitglieder hinzuzufügen, wählen Sie die Gruppe in der Liste aus und wählen Sie dann **Mitglieder** in der Aktionsleiste aus, um die Mitgliederseite der Gruppe zu öffnen.

6. Wählen Sie in der Aktionsleiste **Neu** und dann ein Mitglied aus der Liste aus. Wiederholen Sie diesen Schritt für alle Mitglieder, die Sie hinzufügen möchten, und kehren Sie anschließend zur Seite **Genehmigungsgruppen** zurück.

   > [!NOTE]
   > Damit Sie einer Gruppe Mitglieder hinzufügen können, müssen diese zuerst als [Genehmiger konfiguriert](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#so-richten-sie-benutzer-als-genehmiger-ein) werden. Andernfalls sind sie in der Liste nicht verfügbar.

## So konfigurieren Sie Konten- und Dimensionsberechtigungen für eine Gruppe

> [!IMPORTANT]
> Als Voraussetzung für diese Anleitung muss die Funktion **Benutze Konten und Dimensionseinschränkungen bei der Freigabe** auf der Seite **Document Capture Einrichtung** aktiviert sein. Mehr Informationen dazu finden Sie unter [So richten Sie die Einkaufsgenehmigung ein](@DC-22#so-richten-sie-die-einkaufsgenehmigung-ein). Bevor Sie diese Funktion aktivieren, sollten Sie eine Genehmigungsgruppe erstellen, die alle nicht kritischen Dimensionen und Kontotypen enthält (z. B. Projekte, Ressourcen, Anlagen usw.). So werden Genehmigungen zugelassen, aber ohne Berechtigungen zuzuweisen. Fügen Sie dieser Gruppe dann alle relevanten Genehmiger hinzu. Dieser Ansatz ermöglicht es den Genehmigern, Dokumente zu genehmigen, die nicht kritische Dimensions- und Kontowerte enthalten.

Nachdem Sie eine Genehmigungsgruppe wie unter [So richten Sie Genehmigungsbenutzergruppen ein](#so-richten-sie-genehmigungsgruppen-ein) beschrieben eingerichtet haben, können Sie ihr Konto- und Dimensionsberechtigungen zuweisen. Sie können die folgenden zwei Arten von Berechtigungen konfigurieren:

- **Zuweisungsberechtigungen** – sie legen fest, welche Konten und Dimensionen die Gruppenmitglieder beim Zuweisen von Konten/Dimensionen zu Rechnungszeilen während der Genehmigung mit dem Continia Web Approval Portal auswählen können.
- **Genehmigungsberechtigungen** – sie legen fest, welche Rechnungszeilen die Gruppenmitglieder genehmigen können (nur Zeilen, denen Konten/Dimensionen zugewiesen wurden, für die die Mitglieder Berechtigungen haben).

Weitere Informationen zu diesen beiden Arten von Berechtigungen finden Sie unter [Weitere Informationen zu Zuweisungs- und Genehmigungsberechtigungen](#weitere-informationen-zu-zuweisungs--und-genehmigungsberechtigungen) weiter unten.

> [!IMPORTANT]
> Beachten Sie, dass Zuweisungsberechtigungen nur mit dem Web Approval Portal verwendet werden können.
>
> Damit Zuweisungsberechtigungen wirksam werden, muss außerdem die Funktion **Darf Buchungszeilen editieren** für alle Gruppenmitglieder aktiviert werden. Dies ist unter [So richten Sie Benutzer als Genehmiger ein](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#so-richten-sie-benutzer-als-genehmiger-ein) (Schritt 4) beschrieben. Andernfalls können die Mitglieder Belege zur Genehmigung nicht bearbeiten und diese nur genehmigen oder ablehnen.

So weisen Sie einer Genehmigungsgruppe Konten- und Dimensionsberechtigungen zu:

1. Wählen Sie das Symbol {{search}}, geben Sie **Genehmigungsgruppen** ein, und wählen Sie dann den zugehörigen Link.

2. Wählen Sie die Gruppe in der Liste aus und wählen Sie dann **Berechtigungen** in der Aktionsleiste aus.

3. Wählen Sie in der Spalte **Art** den Typ der Berechtigung aus. **Sachkonto**, **Artikel**, **Anlage**, **Zu/Abschlag** und **Projekt** sind alle Arten von Kontoberechtigungen, während **Dimension** die Dimensionsberechtigungen darstellt.

4. Wenn Sie in Schritt 3 oben **Dimension** ausgewählt haben, fügen Sie in der Spalte **Dimensionscode** einen Dimensionscode hinzu. Wenn Sie in Schritt 3 etwas anderes als **Dimension** ausgewählt haben, lassen Sie das Feld leer.

5. Geben Sie in der Spalte **Zuweisungsberechtigung** an, wie Sie die Zuweisungsberechtigungen einrichten möchten, die diese Gruppenmitglieder haben sollen.

   > [!TIP]
   > Die Optionen werden im Folgenden erläutert:
   >
   > - **Alle**: Die Gruppenmitglieder können den Rechnungszeilen bei der Genehmigung alle Konten/Dimensionen zuweisen, und es ist keine weitere Einrichtung erforderlich.
   > - **Markierte**: Die Mitglieder können die Konten/Dimensionen zuweisen, die Sie in der Spalte **Anzahl der Zuweisungsauswahl** auswählen (die Auswahl ist dann obligatorisch).
   > - **Nicht markierte**: Die Mitglieder können alle Konten/Dimensionen zuweisen mit Ausnahme der, die Sie in der Spalte **Anzahl der Zuweisungsauswahl** auswählen (die Auswahl ist dann obligatorisch).
   > - **Filter**: Die Mitglieder können die Konten/Dimensionen zuweisen, die Sie in der Spalte **Zuweisungsfilter für Auswahl** auswählen (die Auswahl ist dann obligatorisch).

6. Geben Sie in der Spalte **Genehmigungsberechtigung** an, wie Sie die Genehmigungsberechtigungen einrichten möchten, die diese Gruppenmitglieder haben sollen.

   > [!TIP]
   > Die Optionen werden im Folgenden erläutert:
   >
   > - **Alle**: Die Gruppenmitglieder können Rechnungszeilen mit beliebigen Konten/Dimensionen genehmigen, und es ist keine weitere Einrichtung erforderlich.
   > - **Markierte**: Die Mitglieder können Rechnungszeilen mit den Konten/Dimensionen genehmigen, die Sie in der Spalte **Anzahl der Genehmigungsauswahl** auswählen (die Auswahl ist dann obligatorisch).
   > - **Nicht markierte**: Die Mitglieder können Rechnungszeilen mit beliebigen Konten/Dimensionen genehmigen **mit Ausnahme** der, die Sie in der Spalte **Anzahl der Genehmigungsauswahl** auswählen (die Auswahl ist dann obligatorisch).
   > - **Filter**: Die Mitglieder können Rechnungszeilen mit den Konten/Dimensionen genehmigen, die Sie in der Spalte **Zuweisungsfilter für Genehmigung** auswählen (die Auswahl ist dann obligatorisch).
   > - **Gleich wie Zuweisung**: Die in Schritt 5 konfigurierten Einstellungen für die Zuweisungsberechtigungen werden kopiert und auch als Genehmigungsberechtigungen der Mitglieder verwendet.

7. Wenn Sie in Schritt 5 oben **Filter** ausgewählt haben: Wählen Sie in der Spalte **Zuweisungsfilter für Auswahl** die Konten/Dimensionen aus, denen die Gruppenmitglieder Rechnungszeilen während der Genehmigung zuweisen können.

8. Wenn Sie in Schritt 6 oben **Filter** ausgewählt haben: Wählen Sie in der Spalte **Zuweisungsfilter für Auswahl** die Konten/Dimensionen aus, für die Gruppenmitglieder Rechnungszeilen genehmigen können sollen.

   > [!NOTE]
   > Für beide Filteroptionen (Schritte 7 und 8) können Sie Bereiche oder mehrere Konten/Dimensionen mit der Standardfilternotation eingeben. Beispielsweise **10100..10500** und **10100|10500**.

9. Wenn Sie in Schritt 5 oben **Markierte** oder **Nicht markierte** ausgewählt haben: Wählen Sie in der Spalte **Anzahl der Zuweisungsauswahl** die Konten/Dimensionen aus, die die Gruppenmitglieder den Rechnungszeilen bei der Genehmigung zuweisen bzw. nicht zuweisen können.

10. Wenn Sie in Schritt 6 oben **Markierte** oder **Nicht markierte** ausgewählt haben: Wählen Sie in der Spalte **Anzahl der Genehmigungssauswahl** die Konten/Dimensionen aus, für die die Gruppenmitglieder Rechnungszeilen genehmigen bzw. nicht genehmigen können.

## Weitere Informationen zu Zuweisungs- und Genehmigungsberechtigungen

Beachten Sie insbesondere bei Zuweisungsberechtigungen Folgendes: Beim Verwenden von Lookup-Feldern im Web Approval Portal ist die Liste der verfügbaren Optionen im Lookup-Feld durch die Zuweisungsberechtigungen des jeweiligen Genehmigers eingeschränkt. Dies sind die Einschränkungen, die Sie mit den Optionen **Filter**, **Markierte** und/oder **Nicht markierte** wie [oben](#so-konfigurieren-sie-konto--und-dimensionsberechtigungen-fur-eine-gruppe) und [hier](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#so-konfigurieren-sie-die-individuellen-berechtigungen-von-genehmigern) beschrieben, angewendet haben.

Wenn beispielsweise nur 5–10 % aller Sachkonten für den Genehmiger normalerweise relevant sind, können Sie die Liste der verfügbaren Sachkonten für den Genehmiger beim Einrichten der Zuweisungsberechtigungen entsprechend einschränken. Im Web Approval Portal wird dann im entsprechenden Lookup-Feld nur die von Ihnen festgelegte Auswahl an Sachkonten angezeigt. Das gleiche Prinzip gilt für Artikel, Anlagen, Zu/Abschläge, Projekte und Dimensionen.

Sowohl für Zuweisungs- als auch Genehmigungsberechtigungen gilt Folgendes: Wenn ein Genehmiger Mitglied mehrerer Genehmigungsgruppen mit unterschiedlichen Berechtigungen ist oder ihm individuelle Berechtigungen und Berechtigungen als Mitglied einer oder mehrerer Genehmigungsgruppen zugewiesen wurden, erhält der Genehmiger die Summe aller Berechtigungen. Falls es einen Konflikt zwischen zugewiesenen Berechtigungen gibt, haben die ausgeschlossenen Berechtigungen Vorrang. Dies kann zum Beispiel der Fall sein, wenn Berechtigungen für denselben Datensatz in einer Gruppe enthalten sind, in einer anderen jedoch ausgeschlossen wurden.

Beispielsweise kann ein Genehmiger als Mitglied einer Genehmigungsgruppe Zugriff auf zehn Sachkonten haben. Wenn jedoch eines dieser Konten in den individuell zugewiesenen Berechtigungen des Genehmigers ausgeschlossen wird, hat der Genehmiger nur Zugriff auf die verbleibenden neun Konten, die über die Genehmigungsgruppe zugewiesen wurden. Auch hier gilt das gleiche Prinzip für Artikel, Anlagen, Zu/Abschläge, Projekte und Dimensionen.

Insbesondere für Genehmigungsberechtigungenist Folgendes zu beachten: Genehmiger werden mithilfe der Standardverfahren identifiziert (entweder über Genehmigungsabläufe oder über **Einkäufercode** für den ersten Genehmiger und Grenzbeträge für alle weiteren Genehmiger). Sie werden nicht anhand der Konto-/Dimensionsarten identifiziert. Wenn ein Beleg jedoch genehmigt wird und zur Freigabe bereit ist, prüft Document Capture, ob alle Zeilen von Genehmigern genehmigt wurden, die über die erforderlichen Berechtigungen für die verwendeten Konten-/Dimensionsarten verfügen.

> [!NOTE]
> Genehmigungsberechtigungen werden nur überprüft, wenn der letzte Genehmiger in der Kette das Dokument überprüft. Bei dieser Berechtigungsprüfung werden die Berechtigungen aller Genehmiger in der Kette berücksichtigt und zu einem einzigen Berechtigungssatz zusammengefasst. Gleichzeitig werden auch Änderungen der wichtigsten Werte in den Zeilen verglichen. Ändert einer der Genehmiger in der Kette einen Wert, etwa eine Dimension in einer Auftragszeile, verfällt die vorherige Genehmigung.

## Informationen zum Thema

[Einkaufsgenehmigung aktivieren](@DC-22)\
[Continia Benutzereinrichtung für Genehmigungen](Continia user setup for approvals.md)