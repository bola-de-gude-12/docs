---
title: Einkaufsbelege in Document Capture konfigurieren
date: 25-09-2025
description: So konfigurieren Sie bestimmte Einstellungen für Einkaufsbelege, um sie besser an die Anforderungen Ihres Unternehmens anzupassen.
id: DC-139
lang: de
---

# Einkaufsbelege konfigurieren

Sie können bestimmte Einstellungen für Einkaufsbelege konfigurieren, um sie besser an die Anforderungen Ihres Unternehmens anzupassen. Informationen hierzu finden Sie in den folgenden Abschnitten.

In diesem Artikel werden zur Veranschaulichung Rechnungen verwendet; die Informationen gelten jedoch auch für Gutschriften.

## Automatische Betragsvalidierung

Wenn Sie eine Rechnung von einem Kreditor erhalten und diese in eine Einkaufsrechnung umwandeln, kann Document Capture automatisch prüfen, ob der Gesamtbetrag der Originalrechnung (oft als importierter Betrag bezeichnet) mit dem Betrag übereinstimmt, den Sie in die Einkaufsrechnung eingegeben haben. Wenn Sie diese Prüfung aktivieren und die beiden Beträge nicht übereinstimmen, können Sie die Einkaufsrechnung nicht buchen und Sie erhalten eine Fehlermeldung.

> [!NOTE]
> Es muss eine genaue Übereinstimmung zwischen den beiden Beträgen bestehen. Es ist jedoch möglich, Unterschiede bei der Rundungsgenauigkeit zu berücksichtigen, falls dies erforderlich ist. In Document Capture ist eine Abweichung von 0.01 Währungseinheiten erlaubt; diese kann jedoch in der **Finanzbuchhaltung Einrichtung** (für MW) oder auf der **Währungskarte** (keine MW) angepasst werden.
>
> Sie können entweder die Microsoft Dynamics 365 Business Central-Standardfelder **Rechnungsrundungspräzision (MW)** und **Rechnungsrundungsmethode (MW)** von oder die Document Capture-Felder **Maximal zulässige Differenz Inkl. MwSt** (nur App) und **Maximal zulässige Differenz exkl. MwSt** (nur App) verwenden.

Um Betragsvalidierung einzurichten, gehen Sie folgendermaßen vor:

1. Suchen Sie ({{search}}) nach **Document Capture Einrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Wählen Sie im Inforegister **Allgemein** unter **Betragsvalidierung beim Buchen** aus, welche Betragsarten übereinstimmen müssen: Beträge inklusive Mehrwertsteuer, Beträge ohne Mehrwertsteuer, Beträge inklusive und ohne Mehrwertsteuer oder keine (d. h. **Keine Übereinstimmung erforderlich**).

Sie können importierte Beträge mithilfe [der Anleitung unten](#importierte-betrage-anpassen) ändern.

## Importierte Beträge anpassen

Wenn ein Kreditor Ihnen eine Rechnung schickt, registriert Document Capture den Gesamtbetrag dieser Rechnung automatisch und kopiert ihn in die entsprechende Einkaufsrechnung, die erstellt wird. Dieser Gesamtbetrag der ursprünglichen Rechnung, d. h. der importierte Betrag, kann jedoch [von bestimmten Benutzern](#benutzer-die-importierte-betrage-anpassen-konnen) geändert werden. Das Ändern importierter Beträge kann erforderlich sein, wenn Abweichungen durch Folgendes entstehen:

- Bei Mehrwertsteuerdifferenzen (wenn Sie Rechnungen mit einem anderen Mehrwertsteuersatz als Ihr Kreditor buchen)
- Wenn Mehrwertsteuer von verschiedenen Systemen unterschiedlich berechnet wird
- Rundungsprobleme (wenn Sie andere Rundungsregeln als Ihr Kreditor verwenden)

> [!NOTE]
> Die Methode zum Ändern importierter Beträge, hängt davon ab, wie die Belege registriert wurden – [als Standardbelege](@DC-67#to-register-a-document) (die Standardmethode) oder [als Buch.-Blattzeilen](@DC-67#registering-documents-as-general-journal-lines). Weitere Informationen finden Sie unter [Standardmäßig registrierte Belege](#standardmassig-registrierte-belege) und [Als Buch.-Blattzeilen registrierte Belege](#als-buch-blattzeilen-registrierte-belege).

### Standardmäßig registrierte Belege

Um die importierten Beträge von Belegen zu ändern, die als Standardbelege registriert wurden (hier am Beispiel von Einkaufsrechnungen), gehen Sie folgendermaßen vor:

1. Wählen Sie im Rollencenter im Abschnitt **Continia Document Capture Aktivitäten** die Option **Offene Rechnungen** aus.
2. Wählen Sie in der Liste der Einkaufsrechnungen die Rechnung aus, in der Sie importierte Beträge ändern möchten. Wählen Sie hierzu die entsprechende Nummer in der Spalte **Nr.** aus.
3. Die ausgewählte Einkaufsrechnung wird geöffnet. Klicken Sie in der Aktionsleiste auf **Rechnung** und dann auf **Importierte Beträge ändern**.
4. Geben Sie unter **Neuer Betrag ohne MwSt.** und/oder **Neuer Betrag inkl. MwSt.** den/die Beträg(e) ein, den/die Sie auf diese Rechnung anwenden möchten.
5. Wählen Sie **OK**, um die Seite **Belegsumme ändern** zu schließen.

Die neuen Beträge werden auf die Einkaufsrechnung angewendet und im Inforegister **Allgemein** unter **Betrag ohne MwSt. (importiert)** und/oder **Betrag inkl. MwSt. (importiert)** angezeigt.

### Als Buch.-Blattzeilen registrierte Belege

Um die importierten Beträge von Belegen zu ändern, die als Buch.-Blattzeilen registriert wurden, gehen Sie folgendermaßen vor:

1. Suchen Sie ({{search}}) nach **Fibu Buch.-Blätter** oder **Einkaufs Buch.-Blätter** (je nachdem, wo diese Belege als Zeilen registriert wurden), und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Liste die Buch.-Blattzeilen aus, in denen Sie importierte Beträge ändern möchten.
3. Klicken Sie in der Aktionsleiste auf **Zeile** > **Importierte Beträge ändern**.
4. Geben Sie unter **Neuer Betrag ohne MwSt.** und/oder **Neuer Betrag inkl. MwSt.** den/die Beträg(e) ein, den/die Sie auf die ausgewählte Buch.-Blattzeile anwenden möchten.
5. Klicken Sie auf **OK**, um die Seite **Belegsumme ändern** zu schließen.

Die neuen Beträge werden jetzt auf den Beleg angewendet, der durch die ausgewählte Buch.-Blattzeile dargestellt wird, obwohl sie nicht sofort im eigentlichen Buch.-Blatt sichtbar sind.

## Benutzer, die importierte Beträge anpassen können

Um [importierte Beträge ändern zu können](#importierte-betrage-anpassen), müssen Sie eines der folgenden Kriterien erfüllen, je nachdem, ob Rechnungsgenehmigung für den aktuellen Mandanten eingerichtet wurde oder nicht:

### Rechnungsgenehmigung nicht aktiviert

Wenn Rechnungsgenehmigung _deaktiviert_ ist, müssen Sie berechtigt sein, die Tabelle **CDC Document** zu bearbeiten. Die folgenden [Berechtigungssätze](/Continia Document Capture/Development and Administration/Document Capture permissions.md) geben Ihnen diesen Zugriff: CDC CAPTURE und CDC ADMIN. Ein Administrator muss Sie einem dieser beiden Berechtigungssätze hinzufügen.

### Rechnungsgenehmigung aktiviert

Wenn Rechnungsgenehmigung _aktiviert_ ist, müssen Sie Genehmigungsadministrator sein. Dies kann nur ein Administrator konfigurieren, und die folgenden Schritte sind erforderlich:

1. Suchen Sie ({{search}}) nach **Continia Benutzereinrichtung** und wählen Sie dann den entsprechenden Link aus.
2. Klicken Sie in der Aktionsleiste auf **Bearbeiten**, um die **Continia Benutzereinrichtung Karte** zu öffnen.
3. Aktivieren Sie im Inforegister **Allgemein** > **Genehmigungsadministrator**, indem Sie den Schalter umschalten.

## Informationen zum Thema

[Einkaufsbelege einrichten](@DC-476)\
[Registrierung von Belegen als Fibu. Buch.-Blattzeilen einrichten](@DC-112)