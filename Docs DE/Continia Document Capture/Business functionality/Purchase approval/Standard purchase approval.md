---
title: Standardeinkaufsgenehmigung
date: 13-01-2022
description: Eine Beschreibung der Standardeinkaufsgenehmigung und wie sie für Rechnungen verwendet werden kann
id: DC-32
lang: de
---

# Standardeinkaufsgenehmigung

Bei der Standardeinkaufsgenehmigung wird der Genehmigungsworkflow zu genehmigender Belege vom Gesamtbetrag des Belegs und dem zugewiesenen Einkäufercode bestimmt.

Der Beleg wird zunächst an den Genehmiger weitergeleitet, der dem eingegebenen Einkäufercode zugeordnet ist. Wenn der Belegbetrag innerhalb des Genehmigungslimits des Genehmigers liegt, kann der Genehmiger den Beleg genehmigen und den Genehmigungsprozess abschließen. Wenn der Belegbetrag jedoch das Genehmigungslimit des Genehmigers überschreitet, wird der Beleg stattdessen an den Manager des Genehmigers weitergeleitet. Falls auch der Manager nicht über ein ausreichendes Genehmigungslimit verfügt, wird der Beleg an den nächsten Manager weitergeleitet und so weiter, bis ein Genehmiger mit einem ausreichenden Genehmigungslimit gefunden wurde.

In diesem Artikel werden Einkaufsrechnungen zur Veranschaulichung der Standardeinkaufsgenehmigung verwendet. Die Funktionalität gilt jedoch auch für Gutschriften.

> [!IMPORTANT]
> Als Voraussetzung muss [Einkaufsgenehmigung in der **Document Capture Einrichtung** aktiviert sein](@DC-22).
>
> Die Standardkonfiguration vom Continia Document Capture **Genehmigungsworkflow Einkaufsrechnung** muss unverändert bleiben. Für das Ereignis **Die Genehmigung für einen Einkaufsbeleg wird angefordert** müssen in der Workflowreaktion unter **Erstellen Sie eine Genehmigungsanforderung für den Datensatz mithilfe des Typ des Genehmigers %1 und %2 (DC)** folgende Einstellungen vorgenommen werden:
>
> - **Genehmigertyp** muss **Verkäufer/Einkäufer** sein.
> - **Einschränkungsart Genehmiger** muss **Genehmigerkette** sein.
>
> Außerdem müssen alle Benutzer in der Genehmigungskette [als Genehmiger eingerichtet sein](@DC-23). Andernfalls wird beim Einreichen des Belegs zur Genehmigung ein Fehler zurückgegeben.

## So starten Sie die Standardeinkaufsgenehmigung für eine Rechnung

Sie können eine Standardeinkaufsgenehmigung für eine Rechnung starten, indem Sie einfach einen Einkäufercode zuweisen. Dies erfolgt normalerweise bei der Erfassung der Felder nach dem Scannen und Importieren von Belegen.

Um einer Rechnung einen Einkäufercode zuzuweisen, gehen Sie wie folgt vor:

1. Erfassen Sie zuerst die Felder mit dem gewohnten Prozess:
   1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
   2. Wählen Sie den Code **EINKAUF** aus, um das Belegjournal für Einkaufsbelege zu öffnen.
   3. Wählen Sie in der Belegliste im Belegjournal die Rechnung aus, deren [Felder Sie erfassen](/continia-document-capture/business-functionality/documents-and-templates/working-with-paper-and-pdf-documents#capturing-fields) möchten.
2. Um einen Einkäufercode anzuwenden, gehen Sie im Abschnitt **Belegkopf** zum Feld **Einkäufer/Verkäufer** in der Tabelle.
3. Wählen Sie für das Feld **Einkäufer/Verkäufer** unter **Wert** die drei Punkte auf der rechten Seite aus, um die Seite **Verkäufer/Einkäufer** zu öffnen.
4. Wählen Sie in der Liste der Einkäufercodes den Code aus, den Sie auf die Rechnung anwenden möchten, und klicken Sie dann auf **OK**, um die Seite zu schließen.

Der gewählte Einkäufercode wird anschließend dem Feld **Einkäufer/Verkäufer** hinzugefügt und bei der Registrierung in die Rechnung kopiert, wodurch die Standardeinkaufsgenehmigung gestartet wird. Wenn Sie die Rechnung zur Genehmigung einreichen, wird sie an den Genehmiger gesendet, der dem gewählten Einkäufercode zugeordnet ist, und im Falle eines unzureichenden Genehmigungslimits an den Manager des Genehmigers weitergeleitet.

## Informationen zum Thema

[Document Capture Einrichtung](@DC-22)  
[Continia Benutzereinrichtung für Genehmigungen](@DC-23)  
[Felder erfassen](/continia-document-capture/business-functionality/documents-and-templates/working-with-paper-and-pdf-documents#capturing-fields)