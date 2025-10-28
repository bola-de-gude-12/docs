---
title: Grundlegende Konzepte in Document Capture
date: 24-12-2024
description: Eine Beschreibung der wesentlichen Konzepte in Document Capture.
id: DC-83
lang: de
---

# Grundlegende Konzepte in Document Capture

Die Arbeit mit Continia Document Capture ist im Allgemeinen recht einfach. Sie beinhaltet jedoch eine Reihe wesentlicher Konzepte, mit denen Sie sich unbedingt vertraut machen sollten. Dieser Artikel erläutert diese Konzepte.

## Was ist ein Beleg und wie wird er verarbeitet?

Ein Beleg ist ein gescanntes Papierdokument, eine PDF-Datei oder eine XML-Datei, die in Document Capture importiert wird. Dabei kann es sich um ein beliebiges Dokument handeln, beispielsweise eine Einkaufsrechnung, einen Verkaufsauftrag, einen Vertrag, ein Artikelzertifikat, einen Frachtbrief, eine Kundenabrechnung oder beliebige andere Dokumente.

Sobald ein Beleg in Document Capture importiert wurde, können Sie die darin enthaltenen Textinformationen erfassen und damit arbeiten. Die Informationen, die Sie erfassen müssen, hängen vom jeweiligen Belegtyp ab. Alle Belege werden, unabhängig vom Typ, am selben Ort verwaltet und verarbeitet – im Belegjournal.

Die Hauptfunktion des Belegjournals besteht darin, Ihnen die Arbeit mit importierten Belegen und die Erfassung der in diesen Belegen enthaltenen Textinformationen zu ermöglichen. Sobald die Informationen im Belegjournal erfasst wurden, müssen Sie den Beleg registrieren. Durch die Registrierung eines Belegs werden alle erfassten Informationen in eine echte Geschäftsentität in Microsoft Dynamics 365 Business Central umgewandelt. Wenn Sie beispielsweise eine Einkaufsrechnung von einem Kreditor registrieren, erstellen Sie eine Business Central-Einkaufsrechnung.

Der Prozess kann wie folgt beschrieben werden:

1. Der Beleg wird gescannt oder an Document Capture gesendet und mit OCR verarbeitet.
2. Der Beleg wird in das Belegjournal importiert.
3. Die Informationen werden erfasst.
4. Der Beleg wird registriert.
5. Eine Business Central-Einkaufsrechnung wird erstellt.

## Belege in Document Capture importieren

Bevor Sie mit Belegen in Document Capture arbeiten können, müssen die Belege in das System importiert werden. Hierfür gibt es verschiedene Möglichkeiten.

**Per E-Mail:** Sie können Belege in Document Capture importieren, indem Sie sie als PDF- oder XML-Dateien an eine E-Mail anhängen und diese E-Mail dann an eine spezielle E-Mail-Adresse senden, die von Document Capture überwacht wird. Für jede Belegkategorie in Document Capture gibt es eine eigene E-Mail-Adresse. Stellen Sie daher sicher, dass Sie Ihre Belege an die richtige Adresse senden. Sie können die Belege, die Sie erhalten, entweder selbst an die jeweilige E-Mail-Adresse weiterleiten oder die ursprünglichen Absender (meist Ihre Kreditoren) bitten, sie direkt an diese E-Mail-Adresse zu senden. Weitere Informationen hierzu finden Sie unter [Belege importieren](/continia-document-capture/business-functionality/documents-and-templates/importing-documents#per-e-mail).

**Mit einem Netzwerkscanner:** Eine andere Möglichkeit zum Importieren Ihrer Belege besteht darin, sie mit einem Netzwerkscanner zu scannen. Die meisten Netzwerkscanner können so eingerichtet werden, dass sie Belege scannen und als PDF-Dateien an eine festgelegte E-Mail-Adresse senden. Dazu richten Sie Ihren Scanner einfach so ein, dass alle gescannten Dateien im PDF-Format an die E-Mail-Adresse gesendet werden, die von Document Capture überwacht wird, wie oben beschrieben. Es ist keine zusätzliche Konfiguration erforderlich, da Document Capture alle eingehenden E-Mails und deren Anhänge automatisch einliest, wie im obigen Abschnitt beschrieben.

**Mit einem Desktopscanner:** Document Capture unterstützt das Scannen von Belegen mithilfe eines Desktopscanners, der direkt an den PC eines Endbenutzers angeschlossen ist. Document Capture kann mit dem Scanner kommunizieren und den Scanvorgang direkt von Business Central aus starten. Weitere Informationen zum Anschließen eines Desktopscanners finden Sie unter [Einen Desktopscanner anschließen](/Continia Document Capture/Setting up Document Capture/Setting up general business functionality/Connecting a desktop scanner.md). Weitere Informationen zur Verwendung von Desktopscannern finden Sie unter [Einen Desktopscanner verwenden](/continia-document-capture/business-functionality/documents-and-templates/importing-documents#einen-desktopscanner-verwenden).

**Über das Continia Delivery Network:** Das Continia Delivery Network verbindet Sie mit dem globalen Peppol eDelivery Network und dem dänischen NemHandel-Netzwerk, wodurch Sie eDokumente direkt in Business Central importieren können. Weitere Informationen zum Continia Delivery Network finden Sie unter [Grundlegendes zum Continia Delivery Network](@DC-53).

## Mit Belegen arbeiten

Sobald Ihre Belege in Document Capture importiert wurden, können Sie damit arbeiten. Alle Belege sind in Belegkategorien eingeteilt und die meisten von ihnen verwenden Belegvorlagen. Diese beiden Konzepte sind von grundlegender Bedeutung. Deshalb werden sie in den folgenden Abschnitten zusammen mit einigen anderen wichtigen Konzepten erläutert.

**Belegkategorien:** Alle Belege gehören einer bestimmten Belegkategorie an, in denen alle Belege eines bestimmten Typs enthalten sind. Beispielsweise gehören alle Einkaufsrechnungen und Gutschriften zur Belegkategorie **EINKAUF**, während alle Verkaufsaufträge zur Kategorie **VERKAUF** gehören. Jede Belegkategorie enthält eine Reihe von Regeln und Konfigurationen, die definieren, wie Belege innerhalb dieser Kategorie verarbeitet werden. Wenn Sie beispielsweise nur mit Einkaufsbelegen arbeiten, sind andere Belegarten und Belegkategorien für Sie möglicherweise nicht so wichtig. Denken Sie aber daran, dass es verschiedene Arten von Belegen und Belegkategorien gibt. Weitere Informationen zu Belegkategorien finden Sie unter [Mit Belegkategorien arbeiten](/Continia Document Capture/Setting up Document Capture/Setting up document categories and templates/Working with document categories.md).

**Vorlagen:** Eine Vorlage ist eine Sammlung von Regeln und Konfigurationseinstellungen, die festlegen, wie Belege erfasst und verarbeitet werden sollen. Alle Vorlagen sind einer Belegkategorie zugeordnet, und jede Vorlage ist mit einem bestimmten Kreditor verknüpft. Vorlagen können auch mit anderen Entitäten als Kreditoren verknüpft werden, aber dieser Artikel konzentriert sich zur Veranschaulichung ausschließlich auf Kreditoren. In der Vorlage legen Sie fest, welche Informationen und welche Felder erfasst werden sollen, wenn Sie einen Beleg von einem bestimmten Kreditor erhalten. Da jeder Kreditor über eine eigene Vorlage verfügt, können Sie Vorlagen verwenden, um für jeden Kreditor unterschiedliche Informationen zu erfassen oder unterschiedliche Regeln und Konfigurationen anzuwenden. Weitere Informationen zu Vorlagen finden Sie unter [Überblick über Belege und Vorlagen](/Continia Document Capture/Business functionality/Documents and templates/Documents and templates overview.md).

**Belege:** Belege sind die eigentlichen Entitäten, die in Document Capture verarbeitet und gespeichert werden, wie z. B. Einkaufsrechnungen und Gutschriften. Wenn Sie einen Beleg importieren, identifiziert Document Capture die Herkunft dieses Belegs (z. B. den Kreditor, der diesen gesendet hat) und verknüpft ihn mit der jeweiligen Vorlage, die dieser Herkunft zugeordnet ist. Sobald eine Herkunft identifiziert bzw. manuell zugewiesen wurde und die zugehörige Vorlage angewendet wurde, werden alle relevanten Informationen im Beleg automatisch erfasst, und der Beleg wird gemäß den Regeln und der Konfiguration der angewendeten Vorlage verarbeitet. Weitere Informationen über Belege finden Sie [oben](@DC-83#was-ist-ein-beleg-und-wie-wird-er-verarbeitet) und unter [Überblick über Belege und Vorlagen](/Continia Document Capture/Business functionality/Documents and templates/Documents and templates overview.md).

**Belegjournal:** Im Belegjournal werden importierte Belege verarbeitet und die darin enthaltenen Textinformationen erfasst. Welche Informationen erfasst werden sollen, hängt von der Art des Belegs ab, mit dem Sie arbeiten, und Sie können die genauen Regeln in Vorlagen definieren. Durch die Erfassung können alle Belege registriert werden und so in Geschäftsentitäten in Business Central umgewandelt werden. Weitere Informationen zum Arbeiten mit Belegen finden Sie unter [Mit Papier- und PDF-Belegen arbeiten](/Continia Document Capture/Business functionality/Documents and templates/Working with paper and PDF documents.md).

**Dokumentenkarte:** Hier können Sie ebenfalls mit Belegen arbeiten. Der Unterschied zwischen dem Belegjournal und der Dokumentenkarte besteht darin, dass Sie mit der Dokumentenkarte auch Belegzeilen erfassen können, was im Belegjournal nicht möglich ist. Weitere Informationen zum Arbeiten mit Belegen finden Sie unter [Mit Papier- und PDF-Belegen arbeiten](/Continia Document Capture/Business functionality/Documents and templates/Working with paper and PDF documents.md).

## Einkaufsbelege abgleichen

Sie nutzen möglicherweise die Funktionalität von Business Central für Bestellungen und Reklamationen, je nach Ihren Anforderungen. Dann ist es wichtig, dass Einkaufsrechnungen und Gutschriften bei der Verarbeitung diesen Belegtypen zugeordnet werden. Document Capture wurde speziell dafür entwickelt, genau dies so effizient wie möglich auszuführen. Weitere Informationen finden Sie unter [Überblick über Bestell- und Lieferabgleich](/Continia Document Capture/Business functionality/Order and receipt matching/Overview of order and receipt matching.md).

## Einkaufsbelege genehmigen

Die meisten Unternehmen bevorzugen es, ihre Einkaufsrechnungen und Gutschriften genehmigen zu lassen, bevor sie sie buchen und ihre Kreditoren bezahlen. Document Capture bietet einen optimierten Workflow, der den Anforderungen der meisten Unternehmen entspricht, und mehr als 2.000 Unternehmen nutzen ihn bereits. Weitere Informationen zum Genehmigen von Einkaufsbelegen finden Sie unter [Überblick über die Einkaufsgenehmigung](/Continia Document Capture/Business functionality/Purchase approval/Overview of purchase approval.md).

## Belegarchiv

Wenn ein Beleg importiert und verarbeitet wurde, wird dieser automatisch im Belegarchiv gespeichert. Hier können Sie beliebig lange auf alle verarbeiteten Belege zugreifen. Weitere Informationen zum Belegarchiv finden Sie unter [Auf das Belegarchiv zugreifen](/Continia Document Capture/Business functionality/Documents and templates/Accessing the document archive.md).

## Informationen zum Thema

[Belege importieren](/Continia Document Capture/Business functionality/Documents and templates/Importing documents.md)\
[Einen Desktopscanner anschließen](/Continia Document Capture/Setting up Document Capture/Setting up general business functionality/Connecting a desktop scanner.md)\
[Grundlegendes zum Continia Delivery Network](@DC-53)\
[Mit Belegkategorien arbeiten](/Continia Document Capture/Setting up Document Capture/Setting up document categories and templates/Working with document categories.md)\
[Überblick über Belege und Vorlagen](/Continia Document Capture/Business functionality/Documents and templates/Documents and templates overview.md)\
[Mit Papier- und PDF-Belegen arbeiten](/Continia Document Capture/Business functionality/Documents and templates/Working with paper and PDF documents.md)\
[Überblick über Bestell- und Lieferabgleich](/Continia Document Capture/Business functionality/Order and receipt matching/Overview of order and receipt matching.md)\
[Überblick über die Einkaufsgenehmigung](/Continia Document Capture/Business functionality/Purchase approval/Overview of purchase approval.md)\
[Auf das Belegarchiv zugreifen](/Continia Document Capture/Business functionality/Documents and templates/Accessing the document archive.md)