---
title: Einkaufsgenehmigung in Document Capture aktivieren
date: 31-03-2025
description: So können Sie die Einkaufsgenehmigung aktivieren und die grundlegenden Einstellungen für die Beleggenehmigung bearbeiten.
id: DC-22
lang: de
---

# Einkaufsgenehmigung aktivieren

Die meisten grundlegenden Einstellungen für die Beleggenehmigung in Continia Document Capture, wie zum Beispiel Einstellungen für Genehmigungsworkflows, erzwungene Genehmigung, Vier-Augen-Genehmigung sowie Genehmigungsprüfungen und -validierungen, können auf der Seite **Document Capture Einrichtung** bearbeitet werden. In diesem Artikel wird beschrieben, wie Sie auf diese Einstellungen zugreifen und sie bearbeiten können und wie die Einkaufsgenehmigung aktiviert wird.

## So aktivieren Sie die Einkaufsgenehmigung mit dem unterstützten Setup

Mit dem unterstützten Setup ist das Aktivieren der Einkaufsgenehmigung in Document Capture ganz einfach. Gehen Sie dazu folgendermaßen vor:

1. Wählen Sie das Symbol {{search}}, geben Sie **Unterstütztes Setup** ein, und wählen Sie dann den zugehörigen Link, um die entsprechende Seite zu öffnen.
2. Wählen Sie unter **Continia Document Capture** die Option **Genehmigungsworkflow einrichten** aus, um das unterstützte Setup zu öffnen.
3. Wählen Sie **Weiter** und dann die Genehmigungsworkflows aus, die Sie einrichten möchten. Wählen Sie **Nächster** aus, um fortzufahren.
4. Wenn Sie Benutzer sofort als Genehmiger einrichten möchten, wählen Sie **Continia Benutzereinrichtung aufrufen**, um die Seite für die Benutzereinrichtung zu öffnen, und bearbeiten Sie dann die Benutzerliste nach Bedarf. Dies ist auch später möglich. Die Anleitung dazu finden Sie unter [Continia-Benutzereinrichtung für Genehmigungen](@DC-23).
5. Wenn Sie eine Reihe erweiterter Genehmigungseinstellungen sofort konfigurieren möchten, wählen Sie **Genehmigungseinrichtung** aus, um die Seite **Document Capture Einrichtung / Einkaufsgenehmigungen** zu öffnen, und nehmen Sie dann alle erforderlichen Änderungen vor. Sie können diese Einstellungen auch später mit der [Anleitung unten](#so-richten-sie-die-einkaufsgenehmigung-ein) vornehmen.
6. Wählen Sie **Weiter** > **Beenden**, um den Assistenten abzuschließen.

Sobald Sie das unterstützte Setup abgeschlossen haben, gehen Sie zur Seite **Continia Lösungsverwaltung** und aktivieren Sie das Modul **Document Approval**. Informationen hierzu finden Sie unter [Continia Lösungsverwaltung verwenden](@DC-107).

## So richten Sie die Einkaufsgenehmigung ein

> [!NOTE]
> Möglicherweise haben Sie bereits einige oder alle der in der folgenden Anleitung beschriebenen Einstellungen konfiguriert, wenn Sie die Einkaufsgenehmigung mithilfe des unterstützten Setups [wie oben beschrieben](#so-aktivieren-sie-die-einkaufsgenehmigung-mit-dem-unterstutzten-setup) aktiviert haben.

Um die Document Capture-Einkaufsgenehmigung einzurichten, gehen Sie folgendermaßen vor:

1. Suchen Sie {{search}} nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.

2. Wählen Sie in der Aktionsleiste **Start** > **Einkaufsgenehmigung**.

3. Unter **Allgemein** können Sie folgende Genehmigungsarten und Genehmigungseinstellungen aktivieren:

   - **Bestellgenehmigung aktivieren**

   - **Reklamationsgenehmigung aktivieren**

   - **Genehmigung von Rechnungen aktivieren**

   - **Genehmigungsworkflow für Einkaufsgutschriften aktivieren**

   > [!NOTE]
   > Durch Aktivieren einer der oben genannten Einstellungen wird automatisch eine [Genehmigungsgruppe](@DC-24) mit dem Code ALL erstellt – das heißt, mit allen Berechtigungen für alle Typen und Dimensionen, aber nur, wenn eine solche Gruppe noch nicht vorhanden ist.

   - **Genehmigung erzwingen zulassen** – Informationen zum Aktivieren der erzwungenen Genehmigung finden Sie unter [Genehmigung erzwingen](@DC-36).

   - **Benutze Konten und Dimensionseinschränkungen bei der Freigabe** – Informationen zum Konfigurieren von Konten- und Dimensionsberechtigungen für eine Gruppe oder einen Benutzer finden Sie unter [Genehmigungsgruppen](Approval user groups.md) und [Konten- und Dimensionsberechtigungen konfigurieren](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#konto--und-dimensionsberechtigungen-konfigurieren).

   - **Auf Abwarten lassen** – wenn Sie diese Einstellung aktivieren, wird den Genehmigern das Dialogfeld **Abwarten entfernen** nicht angezeigt, wenn sie Belege genehmigen, die auf Abwarten gesetzt wurden. Stattdessen wird der Abwartestatus während des gesamten Genehmigungsprozesses standardmäßig beibehalten.

   - **Kopiere Belegkommentar in Genehmigungskommentar** – wenn diese Einstellung aktiviert ist, werden vor der Registrierung hinzugefügte Belegkommentare als Genehmigungskommentare auf Einkaufsrechnungen, Gutschriften und Einkaufsaufträgen verfügbar gemacht, wenn der Beleg registriert wird.

   > [!TIP]
   > Wenn beispielsweise der Abwartestatus einer Rechnung entfernt wird, scheint die Rechnung bezahlt worden zu sein, obwohl dies in Wirklichkeit nicht der Fall ist. Durch die Aktivierung von **Auf Abwarten lassen** wird sichergestellt, dass Genehmiger den Abwartestatus nicht entfernen können, und es wird verhindert, dass sie solche unerwünschten Aktionen ausführen können.

4. Unter **E-Mail Einrichtung** können Sie die Benachrichtigungs-E-Mails anpassen, die an Genehmiger gesendet werden. Weitere Informationen finden Sie unter [So passen Sie Benachrichtigungs-E-Mails an](@DC-26#to-customize-notification-emails).

5. Um die [Vier-Augen-Genehmigung](@DC-35) zu aktivieren, gehen Sie zu **4-Augen-Freigabe** und wählen Sie entweder **Erforderlich** oder **Erforderlich - beide in voller Höhe**, je nachdem, was Sie bevorzugen. Die Vier-Augen-Genehmigung wird aktiviert, wodurch die folgenden zwei Felder bearbeitet werden können:

   1. **2ter. Genehmiger**: Hier können Sie festlegen, ob der zweite Genehmiger manuell oder automatisch ausgewählt werden soll. Weitere Informationen finden Sie unter [Manuelle oder automatische Identifizierung des Genehmigers](@DC-35#manual-or-automatic-approver-identification).

   2. **4-Augen Schwellenwert (MW)**: Wenn Sie in dieses Feld einen Betrag eingeben, wird die Vier-Augen-Genehmigung nur auf Rechnungen angewendet, die diesen Betrag in der Landeswährung überschreiten. Alle Rechnungen mit Werten, die darunter liegen, benötigen nur einen Genehmiger statt zwei.

   > [!NOTE]
   > Wenn die Beleggenehmigung durch einen [Genehmigungsablaufcode](@DC-33) initiiert wird, wird die Vier-Augen-Genehmigung nicht angewendet, selbst wenn sie hier aktiviert ist.

6. Wenn Sie möchten, dass Beträge und/oder Dimensionen während oder vor der Genehmigung überprüft werden (letzteres gilt nur für Dimensionen), gehen Sie zu **Prüfungen und Validierungen** und füllen Sie die Felder nach Bedarf aus.

7. Unter **Einkaufszuordnung** können Sie bei Bedarf die automatische oder manuelle Erstellung und Buchung von Einkaufszuordungsposten konfigurieren. Weitere Informationen finden Sie unter [Einkaufszuordnungen einrichten](@DC-41).

## Informationen zum Thema

[Genehmigungsgruppen](Approval user groups.md)\
[Continia Benutzereinrichtung für Genehmigungen](Continia user setup for approvals.md)\
[Vier-Augen-Genehmigung](@DC-35)