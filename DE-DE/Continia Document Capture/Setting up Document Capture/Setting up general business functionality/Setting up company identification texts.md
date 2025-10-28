---
title: Mandantensuchtexte einrichten
date: 21-03-2025
description:
id: DC-443
lang: de
---

# Mandantensuchtexte einrichten
Mandantensuchtexte werden verwendet, wenn Sie nur eine E-Mail-Adresse für den Empfang von Dokumenten haben und möchten, dass diese Dokumente nach dem Import automatisch in andere Mandanten übertragen werden. Die meisten Organisationen verwenden für jeden Mandanten eine separate E-Mail-Adresse, sodass sie Dokumente nicht automatisch mithilfe von Mandantensuchtexten verschieben müssen. Weitere Informationen finden Sie unter [Dokumente automatisch zu anderen Mandanten verschieben](/Continia Document Capture/Business functionality/Documents and templates/Moving a document to another company.md).

Wenn Sie Mandantensuchtexte verwenden, weisen Sie Continia Document Capture grundsätzlich an, automatisch jedes Dokument zu verschieben, das einen bestimmten, von Ihnen angegebenen Text enthält. Jedes Dokument, das den angegebenen Text enthält, wird zu einem Mandanten verschoben, dessen Namen Sie diesem bestimmten Text zugeordnet haben. Sie können mehrere Mandantensuchtexte einrichten, die alle auf dasselbe Dokument verweisen. Im Folgenden finden Sie ein Beispiel:

1. Sie haben in Microsoft Dynamics 365 Business Central einen Mandanten mit dem Namen **CRONUS Holding**. Für die CRONUS Holding sind aber auch die beiden alternativen Namen **CRONUS Capital** und **CRONUS Invest** eingetragen. Die Kreditoren verwenden unterschiedliche Namen, wenn sie Ihnen Rechnungen senden, aber alle Dokumente sollten zu **CRONUS Holding** verschoben werden.
1. Sie haben einen weiteren Mandanten in Business Central mit dem Namen **CRONUS Distribution**. CRONUS Distribution ist jedoch auch unter dem alternativen Namen **CRONUS Wholesale** registriert. Die Kreditoren verwenden unterschiedliche Namen, wenn sie Ihnen Rechnungen senden, aber alle Dokumente sollten zu **CRONUS Distribution** verschoben werden.

In einem solchen Szenario könnten Sie mit Mandantensuchtexten die Zuordnung zu den beiden Mandanten wie folgt einrichten:

| Mandantenname       | Mandantensuchtext     |
| ------------------- | --------------------- |
| CRONUS Holding      | *CRONUS Holding*      |
| CRONUS Holding      | *CRONUS Capital*      |
| CRONUS Holding      | *CRONUS Invest*       |
| CRONUS Distribution | *CRONUS Distribution* |
| CRONUS Distribution | *CRONUS Wholesale*    |

> [!NOTE] Vermeiden Sie Mandantensuchtexte, die nicht eindeutig für den Mandanten sind, zu dem Sie Dokumente verschieben möchten. Wie im obigen Beispiel deutlich wird, würde die Verwendung eines Mandantensuchtextes wie *CRONUS* nicht funktionieren, da Document Capture nicht ermitteln könnte, ob Dokumente mit diesem Text zu CRONUS Holding oder CRONUS Distribution verschoben werden sollen.

## So richten Sie Mandantensuchtexte ein
Um Mandantensuchtexte einrichten zu können, müssen Sie mindestens zwei Mandanten in Business Central haben und in allen muss Document Capture aktiviert und eingerichtet sein.

Um Mandantensuchtexte einzurichten, folgen Sie diesen Schritten:

1.  Wählen Sie das Symbol {{search}}, geben Sie **Mandantensuchtexte** ein und wählen Sie dann den zugehörigen Link.
1.  Wählen Sie in der Aktionsleiste **Neu** aus.
1.  Der Tabelle wird eine neue Zeile hinzugefügt. Wählen Sie in der Spalte **Mandantenname** den Mandanten aus, zu dem Sie eingehende Dokumente verschieben möchten.
1.  Geben Sie in der Spalte **Suchbegriff** einen Text ein, der den ausgewählten Mandanten in den eingehenden Dokumenten eindeutig identifiziert.
1.  Wiederholen Sie die Schritte 2–4 für jeden Mandantensuchtext, den Sie verwenden möchten.

Wenn Sie die benötigten Mandantensuchtexte eingegeben haben, müssen Sie die automatische Übertragung von Dokumenten für jede der Belegkategorien aktivieren, in die Dokumente beim Import automatisch verschoben werden sollen. Weitere Informationen hierzu finden Sie unter [Dokumente automatisch zu anderen Mandanten verschieben](/continia-document-capture/business-functionality/documents-and-templates/moving-a-document-to-another-company#moving-documents-to-other-companies-automatically).

## Informationen zum Thema
[Dokumente automatisch zu anderen Mandanten verschieben](/Continia Document Capture/Business functionality/Documents and templates/Moving a document to another company.md)  