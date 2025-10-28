---
title: Automatische Genehmigung aktivieren
date: 25-04-2025
description: So aktivieren Sie die Funktion zur automatischen Genehmigung in Document Capture.
id: DC-461
lang: de
---

# Automatische Genehmigung aktivieren

Sie können Zeit und zusätzliche Arbeit sparen, indem Sie alle Belege, die mit zugehörigen Belegen (innerhalb einer zulässigen Abweichung) übereinstimmen, automatisch genehmigen lassen. Dies ist sowohl für manuell als auch automatisch abgeglichene Belege möglich.

Wie beim Abgleich wird die automatische Genehmigung pro Vorlage konfiguriert. Wenn Sie diese Funktion in einer bestimmten Vorlage aktivieren, wird sie auf alle Dokumente angewendet, die die diese Vorlage verwenden.

So richten Sie die automatische Genehmigung ein:

1. Wählen Sie das Symbol {{search}}, geben Sie **Belegkategorien** ein, und wählen Sie dann den zugehörigen Link.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie auf der Seite **Belegkategorie** im Inforegister **Vorlagen** die Vorlage aus, die Sie konfigurieren möchten.
4. Wählen Sie in der Titelleiste des Inforegisters **Bearbeiten** aus, um die Vorlagenkarte zu öffnen.
5. Aktivieren Sie im Inforegister **Einkaufsbelege** unter **Genehmigung** die Einstellung **Autom. bestätigen innerhalb der Abweichung**.

> [!NOTE]
> Der Wert des Felds **Rechnung Reg. Schritt 2** (zu finden im Inforegister **Einkaufsbelege** unter **Registrierung**) wirkt sich auch auf den automatischen Genehmigungsprozess aus. Darüber hinaus muss die Bestellung im Rahmen eines Genehmigungsablaufs für die Genehmigung vorab genehmigt worden sein. Wenn jedoch **Autom. bestätigen innerhalb der Abweichung** auf der Vorlagenkarte aktiviert ist und alle Beträge übereinstimmen, werden registrierte Rechnungen automatisch genehmigt, wenn sie später zur Genehmigung gesendet werden – auch wenn **Rechnung Reg. Schritt 2** leer gelassen wird.

Alle Belege, die die konfigurierte Vorlage verwenden, werden jetzt automatisch genehmigt, wenn sie mit den entsprechenden Belegen innerhalb der definierten Abweichung übereinstimmen. Alle Belege, die auf diese Weise genehmigt und anschließend registriert werden, werden als offene Einkaufsrechnungen oder Gutschriften mit dem Status **Freigegeben** erstellt. Im Abschnitt **Genehmigungsbemerkungen** wird außerdem darauf hingewiesen, dass der jeweilige Beleg automatisch genehmigt wurde.

## Informationen zum Thema

[Genehmigung von Belegen einrichten](@DC-21)