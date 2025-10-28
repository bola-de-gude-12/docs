---
title: Feldabhängigkeiten einrichten
date: 10-01-2025
description: null
id: EM-250
lang: de
---

# Feldabhängigkeiten einrichten

Um Benutzern die Einreichung von Belegen so einfach wie möglich zu machen, können Sie für die Continia Expense App und das Continia Expense Portal Einschränkungen zwischen verschiedenen Feldern einrichten. Diese Einschränkungen werden als Feldabhängigkeiten bezeichnet und definieren bestimmte Bedingungen.

Durch die Definition spezifischer Bedingungen werden entsprechende Erwartungen erzwungen. Wenn beispielsweise die Dimension ABTEILUNG auf die Bedingung VERKAUF eingestellt ist, wird der Benutzer aufgefordert, einen Wert für Erwartung einzugeben. Dies ist die Dimension PROJEKT.

> [!IMPORTANT]
>
> Feldabhängigkeiten gelten für alle Belegtypen: Abrechnungen, Belege, Fahrstrecken und Pauschalen.

Es gibt zwei verschiedene Feldabhängigkeiten:

- **Systemfeldabhängigkeiten** – Expense Management berechnet diese automatisch basierend auf Ihrer Einrichtung. Wenn Sie beispielsweise eine Dimension für eine bestimmte Belegart als obligatorisch festgelegt haben, generiert dies eine entsprechende Systemfeldabhängigkeit, die diese Dimension obligatorisch macht, wenn diese Belegart verwendet wird.
- **Benutzerdefinierte Feldabhängigkeiten** – Abhängigkeiten, die frei konfiguriert werden können, um Regeln und Erwartungen bei der Erstellung von Belegen durchzusetzen.

<iframe src="https://player.vimeo.com/video/969169181?h=d28a2efaa6&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="8 Manage daily admin_Field dependencies"></iframe>

## Eine Feldabhängigkeit hinzufügen

Sie können Feldtypen aus der folgenden Tabelle Feldtypen auswählen, um eine Systemfeldabhängigkeit oder eine benutzerdefinierte Feldabhängigkeit zu erstellen, die Sie selbst erstellen.

So fügen Sie Feldabhängigkeiten hinzu:

1. Wählen Sie das Symbol {{search}}, geben Sie **Feldtypabhängigkeiten** ein, und wählen Sie dann den entsprechenden Link.

2. Wählen Sie in der Aktionsleiste **Neu** aus.

3. Füllen Sie alle erforderlichen Felder aus:

   | Feld                  | Beschreibung                                                                                                                                                                                                                                                                                        |
   | --------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
   | Feld Typ Code         | Geben Sie den Belegtyp an. Sie können einen aus der Liste auswählen oder **Neu** auswählen, um [einen benutzerdefinierten Typ hinzuzufügen](@EM-80).                                                                                                                |
   | Bedingung             | Die Optionen lauten:<ul><li>Hat einen bestimmten Wert: Sie können diese Option nur für die Feldtypcodes des Datentyps _Option_ oder _Code_ verwenden.</li><li>Hat einen beliebigen Wert</li></ul>                                                   |
   | Wert                  | Geben Sie den Wert an, wenn die Bedingung auf _Hat einen bestimmten Wert_ gesetzt ist. Wenn beispielsweise der Feldtypcode auf _Belegart_ und die Bedingung auf _Hat einen bestimmten Wert_ festgelegt ist, können Sie in der Spalte **Wert** _Hardware_ auswählen. |
   | Referenzfeld Typ Code | Geben Sie den Feldtyp an, indem Sie ihn aus einer Liste auswählen.                                                                                                                                                                                                                  |
   | Erwartung             | Die Optionen lauten:<br /><ul><li>Muss einen Wert haben</li><li>Muss einen bestimmten Wert haben: Sie können diese Option nur für Feldtypcodes des Datentyps _Code_ oder _Text_ verwenden.</li><li>Darf keinen Wert haben</li></ul>                 |
   | Erwarteter Wert       | Gibt an, ob die Abhängigkeit ein mögliches Wertergebnis hat; dies wird hier angezeigt.                                                                                                                                                                                              |
   | System erstellt       | Dies ist ausgewählt, wenn die Abhängigkeit automatisch erstellt wurde.                                                                                                                                                                                                              |
   | Deaktiviert           | Gibt an, ob diese Abhängigkeit deaktiviert ist. Dies geschieht automatisch, wenn ein Konflikt erkannt wird.                                                                                                                                                         |
   | Erkannte Konflikte    | Wenn die Abhängigkeit deaktiviert ist, wird in diesem Feld der Grund dafür angegeben.                                                                                                                                                                                               |

4. Wählen Sie in der Aktionsleiste **Konsistenzprüfung** aus, um diese Regel zu aktivieren.

5. Wählen Sie in der Aktionsleiste **Erzwinge Synchronisation mit Continia Online** und die Regel wird an die zugehörigen Mobilgeräte gesendet.

> [!NOTE]
> Die Feldabhängigkeit ist nur aktiv, wenn die Feldtyp- und Referenzfeldtypcodes **Konfigurierte Felder** sind.

## Systemabhängigkeiten aktualisieren

Systemfeldabhängigkeiten werden ermittelt, wenn Sie **Systemabhängigkeiten aktualisieren** auswählen. Alle resultierenden Regeln werden der Seite „Feldtypabhängigkeiten“ hinzugefügt. Wenn in einem Feld Konflikte erkannt werden, wird eine Meldung angezeigt und die widersprüchlichen Regeln werden deaktiviert. Wenn Sie **Systemabhängigkeiten aktualisieren** auswählen, wird automatisch eine Konsistenzprüfung durchgeführt, die die Bedingungen neu bewertet.

Die Liste der Systemfeldabhängigkeiten wird regelmäßig berechnet und aktualisiert, kann aber auch manuell aktualisiert werden, um die neuesten Änderungen der Einrichtung in Ihrem Mandanten widerzuspiegeln. Wenn Sie Systemfeldabhängigkeiten aktualisieren, werden diese automatisch auf der Seite Feldtypabhängigkeiten erstellt. Sie müssen sie jedoch immer manuell aktivieren, sodass Sie die vollständige Kontrolle haben.

So berechnen und aktualisieren Sie Systemfeldabhängigkeiten:

1. Wählen Sie das Symbol {{search}}, geben Sie **Feldabhängigkeiten** ein, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Aktionsleiste **Systemabhängigkeiten aktualisieren** aus.

Expense Management ermittelt die Systemfeldabhängigkeiten auf Grundlage der folgenden Aspekte:

- Belegart mit Teilnehmern erforderlich
- Standarddimensionen

> [!NOTE]
> Wenn Sie ein Upgrade von Versionen vor Expense Management 7.0 durchführen und es gewohnt sind, dass Expense Management Feldabhängigkeiten automatisch berechnet, beachten Sie, dass dies nicht mehr erfolgt, da Konflikte auftreten können. Alle Konflikte müssen gelöst werden.

## Eine Konsistenzprüfung durchführen

Wenn Sie eine neue Feldabhängigkeit hinzufügen, werden Sie feststellen, dass die Abhängigkeit deaktiviert ist und die Meldung „Führen Sie die Aktion „Konsistenzprüfung“ aus, um diese Abhängigkeit zu aktivieren“ angezeigt wird.

Mithilfe der Konsistenzprüfung können Sie Abhängigkeiten richtig konfigurieren. Sie können ermitteln, ob Regeln sinnvoll sind oder miteinander in Konflikt stehen, die Regelkonsistenz und mögliche Konflikte prüfen und Vorschläge zur Lösung etwaiger Probleme erhalten.

So führen Sie eine Konsistenzprüfung durch:

- Wählen Sie in der Aktionsleiste **Konsistenzprüfung** und **Systemabhängigkeiten aktualisieren** aus, um die Konsistenzprüfung automatisch zu starten.