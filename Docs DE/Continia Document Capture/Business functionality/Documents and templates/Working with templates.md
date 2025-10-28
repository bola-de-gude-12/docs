---
title: Mit Vorlagen in Document Capture arbeiten
date: 04-07-2025
description: So richten Sie Vorlagen in Document Capture ein. Sie können sie kopieren, anzeigen und bearbeiten – einschließlich Mastervorlagen.
id: DC-18
lang: de
---

# Mit Vorlagen arbeiten

Damit Continia Document Capture die Felder importierter Belege erfassen kann, muss jedem Beleg eine Dokumentvorlage zugewiesen werden. Eine Dokumentvorlage ist im Prinzip eine Sammlung von Regeln und Konfigurationseinstellungen, die festlegen, wie Belege erfasst und verarbeitet werden sollen. In Document Capture gibt es drei Arten von Vorlagen, von denen zwei Dokumentvorlagen sind:

| Vorlagenart             | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                       |
| ----------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Identifikationsvorlagen | Identifikationsvorlagen sind Vorlagen, die die Herkunft importierter Belege identifizieren. Bei jedem Import eines Belegs sucht die Identifikationsvorlage der entsprechenden Belegkategorie nach einem passenden Datensatz in der Herkunftstabelle (z. B. Jeder Belegkategorie kann nur eine einzige Identifikationsvorlage zugewiesen werden. |
| Mastervorlagen          | Mastervorlagen sind die vorkonfigurierten Dokumentvorlagen, auf deren Basis Herkunftsvorlagen (z. B. Jeder Belegkategorie können mehrere Mastervorlagen zugewiesen werden. Wenn dies der Fall ist, werden Sie von Document Capture aufgefordert, die Vorlage auszuwählen, die Sie kopieren möchten, um sie als Herkunftsvorlage zu verwenden.   |
| Herkunftsvorlagen       | Herkunftsvorlagen sind Dokumentvorlagen, die jeweils an eine bestimmte Herkunft (z. B. einen Kreditor) gebunden sind. Document Capture verwendet Herkunftsvorlagen zum Erfassen, Überprüfen und Registrieren von Belegen.                                                                                                                       |

Dieser Artikel erläutert die Dokumentvorlagen Master- und Herkunftsvorlagen anhand von Kreditoren und der Belegkategorie **EINKAUF**. Weitere Informationen zu Identifikationsvorlagen finden Sie unter [Grundlegendes zu Identifikationsvorlagen](@DC-471).

## Vorlagen anpassen

Mastervorlagen sind nicht mit Kreditoren verknüpft, dienen aber als Grundlage für die Erstellung von Kreditorenvorlagen. Wenn ein Dokument von einem Kreditor ohne zugehörige Vorlage importiert wird (normalerweise, wenn Sie zum ersten Mal ein Dokument von einem Kreditor erhalten), erstellt Document Capture während der Felderkennung automatisch eine Vorlage für den Kreditor, indem eine der Kategorie **EINKAUF** zugewiesenen Mastervorlagen kopiert. To copy vendor templates:

Sie können die Vorlage jedoch anpassen, wenn einige der Standardfelder für Sie nicht zutreffend sind. Wenn Sie die Kreditorenvorlage anpassen möchten, indem Sie beispielsweise Felder hinzufügen oder entfernen, werden Ihre Änderungen nur auf diese bestimmte Vorlage und diesen bestimmten Kreditor angewendet. Weitere Informationen finden Sie unter [Vorlagenfelder verwalten](@DC-241) und [Neue Vorlagenfelder einrichten](@DC-19).

Möglicherweise möchten Sie auch die Mastervorlage bearbeiten. Wenn es beispielsweise Felder gibt, die in allen oder den meisten Ihrer Belege erfasst werden sollen, empfiehlt es sich, diese Felder der Mastervorlage hinzuzufügen, damit Sie sie nicht manuell jeder einzelnen Kreditorenvorlage hinzufügen müssen. Informationen zum Bearbeiten der Mastervorlage finden Sie unter [So konfigurieren Sie Mastervorlagen](#so-konfigurieren-Sie-Mastervorlagen) weiter unten.

## So konfigurieren Sie Mastervorlagen

So konfigurieren Sie Mastervorlagen:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und klicken Sie auf **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie im Inforegister **Vorlagen** in der Liste die Mastervorlage für PDF-Dateien (**EINKAUF-DE**), und klicken Sie auf **Bearbeiten**, um die Vorlagenkarte zu öffnen.
4. Im Inforegister **Allgemein** können Sie einige der grundlegenden Vorlageneinstellungen bearbeiten, z. B. welches Datumsformat beim Erfassen von Daten in Belegen verwendet werden soll, ob diese Vorlage die Standardkreditorenvorlage sein soll und ob Belegzeilen erfasst werden sollen.
5. Im Inforegister **Einkaufsbelege** können Sie eine Reihe von Einstellungen im Zusammenhang mit der Registrierung, Genehmigung und dem Abgleich von Belegen bearbeiten.
6. Im Inforegister **Felder** können Sie die einzelnen Vorlagenfelder und deren Verfügbarkeit anpassen:
   - Informationen zum Bearbeiten der Eigenschaften eines Felds oder zum Verschieben, Kopieren oder Löschen finden Sie unter [So passen Sie Mastervorlagenfelder an](@DC-19#so-passen-sie-mastervorlagenfelder-an).
   - Informationen zum Erstellen eines Vorlagenfelds finden Sie unter [So erstellen Sie manuell ein Mastervorlagenfeld](@DC-19#so-erstellen-sie-ein-neues-mastervorlagenfeld).
7. Im Inforegister **Codeunits** können Sie angeben, welche Codeunits in bestimmten Phasen des Prozesses verwendet werden sollen, um bestimmte Aktionen auszuführen.

Bei den meisten Änderungen, die Sie an der Mastervorlage vornehmen, werden Sie in einem Dialogfeld gefragt, ob Sie alle zugehörigen Vorlagen entsprechend aktualisieren möchten. Wenn Sie auf **Ja** klicken, werden die von Ihnen vorgenommenen Änderungen in allen Kreditorenvorlagen, die auf der Mastervorlage in der Kategorie **EINKAUF** basieren, übernommen.

> [!NOTE]
> Im Gegensatz zu Änderungen, die in anderen Abschnitten der Mastervorlage vorgenommen werden, werden alle Änderungen, die Sie an den Feldern der Mastervorlage im Abschnitt **Felder** vornehmen (Schritt 6 der Anleitung oben), nicht auf die Kreditorenvorlagen übertragen, die bereits auf Basis der Mastervorlage erstellt wurden. Nur Kreditorenvorlagen, die nach einer solchen Feldkonfiguration erstellt wurden, übernehmen die Änderungen.

## So kopieren und erstellen Sie Mastervorlagen

Anstatt eine vorhandene Mastervorlage zu bearbeiten, möchten Sie möglicherweise eine erstellen. Während der allgemeinen Einrichtung von Document Capture werden eine Reihe von Standardmastervorlagen für mehrere Belegkategorien erstellt – einschließlich der Kategorie **EINKAUF**. Sie können auch eine Mastervorlage erstellen, indem Sie eine der vorhandenen kopieren. So kopieren und erstellen Sie Mastervorlagen

1. Suchen Sie ({{search}}) nach **Belegkategorien** und wählen Sie den entsprechenden Eintrag aus.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und klicken Sie dann auf **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie im Inforegister **Vorlagen** in der Liste die Mastervorlage für PDF-Dateien (**EINKAUF-DE**), und klicken Sie dann auf **Kopieren...**, um die Karte **Vorlage kopieren** zu öffnen.
4. Bearbeiten Sie bei Bedarf die Standardeinstellungen und klicken Sie auf **OK** > **OK**, um eine Mastervorlagenkopie zu erstellen und sie der Liste der Vorlagen hinzuzufügen.
   > [!NOTE]
   > Für Mastervorlagen wird empfohlen, die **Automatische Nummerierung** zu deaktivieren und unter **Neue Vorlagennr.** einen passenden Namen für die neue Vorlage einzugeben. Die automatische Nummerierung benennt die neue Vorlage sonst mit einer Nummer, was die Identifizierung erschwert.
5. Um die kopierte Mastervorlage zu bearbeiten, wählen Sie sie in der Liste aus, klicken Sie auf **Bearbeiten** und folgen Sie dann [der Anleitung oben](#so-konfigurieren-sie-mastervorlagen).

## So kopieren Sie Kreditorenvorlagen

Das Kopieren von Kreditorenvorlagen funktioniert praktisch genauso wie das Kopieren von Mastervorlagen, mit Ausnahme der Benennung der neuen Vorlagen, die in der Benutzeroberfläche als Nummerierung bezeichnet wird. So kopieren Sie Kreditorenvorlagen:

1. Suchen Sie {{search}} nach **Belegkategorien** und wählen Sie dann den entsprechenden Link aus.
2. Um die Kategorie für Einkaufsbelege zu öffnen, wählen Sie die Zeile **EINKAUF** (nicht den Code **EINKAUF**), und klicken Sie dann auf **Bearbeiten** in der Aktionsleiste.
3. Wählen Sie im Inforegister **Vorlagen** die Vorlage in der Liste aus, die Sie kopieren möchten, und klicken Sie dann auf **Kopieren...**, um die Karte **Vorlage kopieren** zu öffnen.
4. Bearbeiten Sie bei Bedarf die Standardeinstellungen und klicken Sie auf **OK** > **OK**, um eine Vorlagenkopie zu erstellen und sie der Liste der Vorlagen hinzuzufügen.
5. Wenn Sie auf der Seite **Vorlage kopieren** die Option **Automatische Nummerierung** aktiviert haben, wird die neue Vorlage mit einer Nummer anstelle eines tatsächlichen Namens (der nächsten fortlaufenden Nummer in der Liste der Vorlagen) benannt. Sie können sie jedoch umbenennen, indem Sie sie in der Liste auswählen und in der Spalte **Nr.** einen neuen Namen eingeben.

> [!NOTE]
> Wenn Sie versuchen, eine Vorlage für einen Kreditor zu erstellen, der bereits in einem anderen Mandanten vorhanden ist, fragt Document Capture, ob Sie diese stattdessen kopieren möchten. Dies funktioniert nur, wenn die Kreditornamen exakt übereinstimmen. Die Groß- und Kleinschreibung kann jedoch unterschiedlich sein kann, beispielsweise „Cronus“ und „cronus“.

> [!TIP]
> Um die Liste der mit einem Kreditor verknüpften Vorlagen anzuzeigen, verwenden Sie die Aktion **Belegvorlagen** aus der Kreditorenliste oder der **Kreditorenkarte**. So zeigen Sie diese Aktion an, die standardmäßig ausgeblendet ist:
>
> 1. Suchen Sie ({{search}}) nach **Kreditoren** und wählen Sie den entsprechenden Eintrag aus.
> 2. Klicken Sie in der Liste der Kreditor oben rechts auf **Einstellungen** ({{settings}}) > **Personalisieren**.
> 3. Erweitern Sie in der Aktionsleiste die Aktionsgruppe **Zugehörig**.
> 4. Bewegen Sie den Cursor über **Kreditoren > Belegvorlagen** und klicken Sie dann auf **Anzeigen**, um die Aktion verfügbar zu machen.