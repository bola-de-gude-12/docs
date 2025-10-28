---
title: Continia eDocuments in Document Capture aktivieren
date: 15-10-2025
description: So aktivieren Sie Continia eDocuments in Document Capture.
id: DC-178
lang: de
---

# Continia eDocuments aktivieren

In diesem Artikel wird beschrieben, wie Sie Continia eDocuments aktivieren. Die Aktivierung ist der erste Teil des gesamten Einrichtungsprozesses:

- Aktivieren von Continia eDocuments (dieser Artikel)
- [Einrichten von Continia eDocuments](@DC-179), einschließlich Import von XML-Strukturen und Stylesheets, falls erforderlich
- [Einrichten des Continia Delivery Networks](@DC-75), falls dies noch nicht erfolgt ist
- [Einrichten von Debitoren und Kreditoren](@DC-180)

> [!NOTE]
> Wenn Sie Continia Document Capture bereits verwenden, müssen Sie Continia eDocuments wie unten beschrieben aktivieren. Wenn Sie ein neuer Benutzer sind, wird Continia eDocuments automatisch für Sie aktiviert und eingerichtet.

## So aktivieren Sie Continia eDocuments

So aktivieren Sie Continia eDocuments und konvertieren vorhandene XML-Vorlagen:

> [!NOTE]
> Die Schritte 1–3 sind nur erforderlich, wenn Sie Document Capture 24.0 oder älter verwenden.

1. Suchen Sie ({{search}}) nach **Continia Funktionsverwaltung** und wählen Sie dann den entsprechenden Link aus.
2. Suchen Sie in der Liste der Funktionen nach **Continia eDokumente**. Aktivieren Sie in der Spalte **Aktiviert** auf der rechten Seite der Tabelle das Kontrollkästchen, um Continia eDocuments zu aktivieren.
3. Es wird ein Dialogfeld angezeigt, in dem Sie gefragt werden, ob Sie die Funktion aktivieren möchten. Klicken Sie zur Bestätigung auf **Ja**.
4. Der **Continia eDokumente Einrichtungsassistent** wird geöffnet. Klicken Sie auf **Nächster**, um den Assistenten zu starten.
5. Wählen Sie im Dropdown-Menü **Importieren von** die Methode aus, die Sie zum Importieren Ihrer eDocuments-Konfigurationseinstellungen verwenden möchten. Klicken Sie auf **Nächster**, um fortzufahren.
6. Die Seite **Continia eDokumente Einrichtungsassistent** wird geöffnet. Dies ermöglicht es Ihnen, Ihre vorhandenen Debitoren- und Kreditorenvorlagen zu kopieren und in Vorlagen zu konvertieren, die mit Continia eDocuments verwendet werden können. Sie haben die folgenden Optionen:
   - Um Ihre vorhandenen Vorlagen zu kopieren und zu konvertieren, klicken Sie unten rechts auf der Seite auf **Nächster**.
     > [!IMPORTANT]
     > Es werden keine vorhandenen Vorlagen gelöscht oder ersetzt; sie werden nur kopiert und dann konvertiert. Daher gehen keine der Vorlagen verloren.
   - Wenn Sie neu beginnen möchten, aktivieren Sie den Schalter **XML-Vorlagen nicht kopieren und konvertieren** und klicken Sie dann in der unteren rechten Ecke der Seite auf **Weiter**. Sollten Sie Ihre Meinung ändern, können Sie die Vorlagen auch später kopieren und konvertieren.
7. Klicken Sie unten rechts auf der Seite auf **Beenden**, um den Einrichtungsassistenten abzuschließen.

Continia eDocuments ist jetzt aktiviert. Um die Funktionalität zum Senden und Empfangen von Geschäftsdokumenten nutzen können, müssen Sie sie auch einrichten. Dies wird unter [Continia eDocuments einrichten](@DC-179) beschrieben.

> [!IMPORTANT]
> Wenn Sie in Schritt 6 oben das Kopieren und Konvertieren vorhandener Vorlagen auswählen, werden keine XML-Mastervorlagen kopiert und konvertiert, sondern nur unterstützte XML-Vorlagen (Kreditorenvorlagen). Dies liegt daran, dass die Mastervorlageneinrichtung für Continia eDocuments anders ist. In Continia eDocuments ist für jede Belegart nur eine Mastervorlage erforderlich (einschließlich aller elektronischen Formate, wie z. B. **PEPPOLBIS3** und **OIOUBL**), während es bisher eine Mastervorlage für jedes elektronische Format für jede Belegart gab.
>
> Dies bedeutet auch, dass alle Konfigurationen, die Sie zuvor für vorhandene XML-Mastervorlagen durchgeführt haben (beispielsweise für den automatischen Abgleich oder die Genehmigung), nach der Migration zu Continia eDocuments erneut durchgeführt werden müssen. Dies ist jedoch nur einmal erforderlich.