---
title: Genehmigungsweiterleitung in Document Capture
date: 27-06-2025
description: So leiten Sie Genehmigungsanforderungen in Document Capture an einen anderen Benutzer weiter.
id: DC-404
lang: de
---

# Genehmigung weiterleiten

Dieser Artikel beschreibt die Funktion zur Weiterleitung der Genehmigung in Continia Document Capture, mit der Sie die Genehmigung eines Belegs an einen anderen Benutzer delegieren können. Vorausgesetzt, die Genehmigungsbenutzer sind entsprechend konfiguriert, ist diese Funktionalität sowohl in Microsoft Dynamics 365 Business Central als auch im [Continia Web Approval Portal](@DC-165) verfügbar.

> [!NOTE]
> Wenn der erste Genehmiger in einem Workflow eine Weiterleitung ohne Genehmigung vornimmt, wird die Genehmigungshierarchie neu erstellt. Dies basiert auf der Annahme, dass die Genehmigungsanfrage an die falsche Person gesendet wurde, sodass ein anderer Workflow erforderlich ist, wenn die Anfrage bei der richtigen Person eingeht.

## Voraussetzungen für die Genehmigungsweiterleitung

Bevor Sie die Funktion zur Weiterleitung von Genehmigungen nutzen können, müssen Sie die folgenden Schritte ausführen:

- Aktivieren Sie das Modul Genehmigungen. Informationen hierzu finden Sie unter [Continia Lösungsverwaltung verwenden](@DC-107#to-enable-or-disable-modules).
- Konfigurieren Sie Genehmigungsbenutzer in Document Capture. Weitere Informationen finden Sie unter [Continia Benutzereinrichtung für Genehmigungen](@DC-23).
- **Optional:** Fügen Sie diese Benutzer zur Liste **Genehmigungsweiterleitung** hinzu. Informationen hierzu finden Sie unter [Benutzerspezifische Listen von Genehmigern für die Genehmigungsweiterleitung erstellen](@DC-138).

## So leiten Sie eine Genehmigung in Business Central weiter

Um eine Genehmigung an einen anderen Benutzer zu delegieren, führen Sie die folgenden Schritte in Business Central aus:

1. Wählen Sie im Rollencenter unter **Continia Document Capture Aktivitäten** den Stapel **Rechnungen zur Genehmigung** aus.
2. Klicken Sie auf der Seite **Einkaufsrechnungen** auf die Einkaufsrechnung, deren Genehmigung Sie weiterleiten möchten.
3. Klicken Sie auf der Seite **Einkaufsrechnung** in der Aktionsleiste auf **Genehmigen** > **Weiterleiten**.
4. Abhängig von Ihrer Konfiguration gibt es bis zu drei Weiterleitungsoptionen:
   - **Genehmigen und weiterleiten** – wählen Sie diese Option aus, um das Dokument zu genehmigen und es zur weiteren Genehmigung an einen anderen Benutzer weiterzuleiten.
   - **Ohne Genehmigung weiterleiten** – wählen Sie diese Option aus, um das Dokument zur Genehmigung an einen anderen Benutzer weiterzuleiten, ohne es selbst zu genehmigen.
   - **Weiterleiten und Beleg nach Genehmigung an mich zurücksenden** – wählen Sie diese Option aus, um das Dokument zur Genehmigung an einen anderen Benutzer weiterzuleiten und es dann automatisch zur weiteren Genehmigung an Sie zurücksenden zu lassen.
5. Wählen Sie den Benutzer aus, an den Sie die Genehmigung weiterleiten möchten, und wählen Sie dann **OK**.

## So leiten Sie eine Genehmigung im Web Approval Portal weiter

Um eine Genehmigung an einen anderen Benutzer zu delegieren, führen Sie die folgenden Schritte im Web Approval Portal aus:

1. Melden Sie sich am Web Approval Portal an. Wenn Sie nicht das [mandantenübergreifende Dashboard](@DC-165#the-available-views) verwenden, wechseln Sie zu dem Mandanten, für den Sie eine Genehmigung weiterleiten möchten.

2. Wählen Sie den Beleg aus, der Ihre Genehmigung erfordert, indem Sie ihn in der Spalte {{checkmark}} auswählen und dann im Aktionsmenü auf **Weiterleiten** klicken. Alternativ können Sie den Beleg öffnen, indem Sie auf **Typ**, **Name**, **Beschreibung** oder andere Felder klicken.

   > [!TIP]
   > Wenn Sie Dokumente über die Spalte {{checkmark}} auswählen, können Sie mehrere Dokumente gleichzeitig bearbeiten.

3. Wählen Sie den Benutzer aus, an den Sie die Genehmigung weiterleiten möchten.

4. Abhängig von Ihrer Konfiguration gibt es bis zu drei Weiterleitungsoptionen:
   - **Genehmigen und weiterleiten** – wählen Sie diese Option aus, um das Dokument zu genehmigen und es zur weiteren Genehmigung an einen anderen Benutzer weiterzuleiten.
   - **Ohne Genehmigung weiterleiten** – wählen Sie diese Option aus, um das Dokument zur Genehmigung an einen anderen Benutzer weiterzuleiten, ohne es selbst zu genehmigen.
   - **Weiterleiten und Beleg nach Genehmigung an mich zurücksenden** – wählen Sie diese Option aus, um das Dokument zur Genehmigung an einen anderen Benutzer weiterzuleiten und es dann automatisch zur weiteren Genehmigung an Sie zurücksenden zu lassen.

5. Geben Sie bei Bedarf einen Kommentar ein. Wählen Sie dann **Weiter**.