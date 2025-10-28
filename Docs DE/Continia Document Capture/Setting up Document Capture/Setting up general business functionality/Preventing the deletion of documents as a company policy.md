---
title: Löschen von Dokumenten mit einer Unternehmensrichtlinie in Document Capture deaktivieren
date: 16-06-2025
description:
id: DC-477
lang: de
---

# Löschen von Dokumenten mit einer Unternehmensrichtlinie deaktivieren

Beim Importieren von Dokumenten in Continia Document Capture gelangen gelegentlich unerwünschte Dokumente in das System. Typische Beispiele hierfür sind:

- Belege, die nicht korrekt gescannt wurden und daher erneut gescannt werden müssen.
- Dokumente, die nicht in Document Capture gehören, beispielsweise wenn ein Kontoauszug (anstelle einer Einkaufsrechnung) an die E-Mail-Adresse gesendet wird, die zum Importieren von Einkaufsbelegen in Document Capture verwendet wird.

Solche unerwünschten Dokumente sollten von Zeit zu Zeit zu entfernt werden. Standardmäßig gibt es hierfür zwei Möglichkeiten:

- **Durch Löschen der Dokumente**: Im Belegjournal können Sie unerwünschte Dokumente löschen. Dadurch werden sie vollständig aus der Datenbank entfernt und können nicht mehr wiederhergestellt werden.
- **Durch Ablehnen der Dokumente**: Im Belegjournal haben Sie auch die Möglichkeit, die Dokumente abzulehnen. Dadurch bleiben die Dokumente in der Datenbank. Ihr Status wird jedoch auf **Abgelehnt** gesetzt, sodass Sie die Dokumente bei Bedarf weiterhin abrufen können.

Der Vorteil beim Löschen eines Dokuments besteht darin, dass es keinen Speicherplatz beansprucht, da es vollständig entfernt wird. Der offensichtliche Nachteil besteht darin, dass Sie es dann nicht mehr abrufen können. Abgelehnte Dokumente hingegen sind auch nach der Ablehnung noch aufrufbar, haben aber den Nachteil, dass sie Speicherplatz beanspruchen.

Das Löschen von Dokumenten ist in Document Capture standardmäßig zugelassen. Sie können jedoch konfigurieren, dass Dokumente nicht mehr gelöscht werden können, indem Sie eine Richtlinie zum Löschen von Dokumenten einrichten. Dies kann nützlich sein, wenn die allgemeine Richtlinie Ihres Unternehmens beispielsweise vorschreibt, alle Dokumente in der Datenbank aufzubewahren, unabhängig davon, wie sie in das System gelangt sind.

Um eine Richtlinie zum Löschen von Dokumenten einzurichten, folgen Sie diesen Schritten:

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Öffnen Sie die entsprechende Belegkategorie. Um beispielsweise die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**, da dadurch das Belegjournal geöffnet wird), und wählen Sie dann **Bearbeiten** in der Aktionsleiste.
3. Aktivieren oder deaktivieren Sie im Inforegister **Allgemein** die Option **Erlaube Löschen von Dokumenten**, je nachdem, wie Sie Ihre Richtlinie zum Löschen von Dokumenten einstellen möchten.

> [!NOTE]
> Belege, die bereits in Document Capture registriert wurden, können nicht gelöscht werden, unabhängig davon, ob Sie eine Richtlinie zum Löschen von Dokumenten eingerichtet haben oder nicht.

## Informationen zum Thema

[Dokumente ablehnen](@DC-478)