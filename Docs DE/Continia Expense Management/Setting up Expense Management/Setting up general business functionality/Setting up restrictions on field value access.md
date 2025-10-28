---
title: Einschränkungen auf Feldwertzugriff einrichten
date: 06-01-2025
description: Geben Sie an, welche Feldwerte für verschiedene Benutzertypen in der Expense App und im Expense Portal sichtbar sind
id: EM-296
lang: de
---

# Einschränkungen auf Feldwertzugriff einrichten

Sie können den Expense-Benutzern helfen, sich beim Einreichen von Belegen auf das für sie Relevante zu konzentrieren, indem Sie genau festlegen, welche Feldwerte für bestimmte Benutzertypen in der Expense App und im Expense Portal sichtbar sind.  Indem Sie festlegen, welche Felder sichtbar sind, lassen sich Fehler minimieren und Buchhalter müssen weniger Zeit damit verbringen, zu überprüfen, ob die Ausgaben richtig verbucht wurden.

Mit dieser Funktion können Sie den Zugriff auf bestimmte Feldwerte für einzelne Expense-Benutzer oder für eine Gruppe von Expense-Benutzern einrichten.

> [!NOTE]
> Standardmäßig sind alle Feldwerte verfügbar. Mit der Einschränkung des Zugriffs auf Feldwerte legen Sie fest, welche Feldwerte für einen Benutzer verfügbar sind. Wenn Sie beispielsweise festlegen, welche Feldwerte für eine Benutzergruppe verfügbar sind, sieht diese Gruppe nur diese Feldwerte. Eine Gruppe mit der Standardkonfiguration sieht dagegen alle Feldwerte.

Die Beschränkung des Zugriffs auf bestimmte Feldwerte ist insbesondere bei großen Konfigurationen sinnvoll, bei denen möglicherweise Hunderte verschiedener Projekte zur Auswahl stehen und viele verschiedene Feldtypen vorhanden sind, darunter Feldtypen, die Dimensionen wie Projekt, Aufgabe, Abteilung oder Kostengruppe darstellen. Feldwerte wie Belegart hängen von den Anforderungen Ihrer Organisationen ab.

## So schränken Sie den Benutzerzugriff auf Feldwerte ein

So richten Sie eine eingeschränkte Ansicht der Feldwerte für einen oder mehrere Expense-Benutzer ein:

1. Suchen Sie {{search}} nach Konfigurierte Felder, und wählen Sie dann den zugehörigen Link.
2. Wählen Sie in der Tabelle **Kopffelder** > Spalte **Feldbeschreibung** den Link zum Datensatz des Felds aus, auf das Sie Zugriff gewähren möchten.
3. Wählen Sie in der Aktionsleiste der Feldtypkarte **Feldtypen** > **Lookup Wert Zugriff** aus.
4. Füllen Sie auf der Seite **Lookup Wert Zugriff** die Felder in der obersten Zeile der Tabelle nach Bedarf aus:
   - **Wert Code**: Wählen Sie im Dropdown-Menü den Wert aus, auf den Sie für das in Schritt zwei ausgewählte Feld Zugriff gewähren möchten.
   - **Art**: Wählen Sie im Dropdownmenü **Benutzer** oder **Gruppe** aus, um Einstellungen auf einen einzelnen Expense-Benutzer oder eine Gruppe von Expense-Benutzern anzuwenden.
   - **Code**: Wählen Sie im Dropdown-Menü einen Benutzer oder eine Benutzergruppe aus.
   - **Beschreibung**: Wählen Sie das Feld aus und es wird automatisch eine Beschreibung basierend auf den von Ihnen ausgewählten Werten eingetragen. Wenn Sie das Feld auswählen, wird auch automatisch die Seite **Lookup Werte** geöffnet. Verwenden Sie den Rückwärtspfeil, um zur Seite **Lookup Wert Zugriff** zurückzukehren.
5. Wiederholen Sie Schritt vier, um der eingeschränkten Ansicht, die Sie einrichten, weitere Feldwerte hinzuzufügen.

   > [!NOTE]
   > Sie müssen für jeden Feldwert, auf den Sie dem Benutzer oder der Gruppe Zugriff gewähren möchten, einen Tabelleneintrag erstellen. Wenn die Tabelle auf der Seite **Lookup Wert Zugriff** nur eine Zeile enthält, hat der Benutzer oder die Gruppe, die Sie unter **Art** definiert haben, nur Zugriff auf diesen Wert.

Sie haben jetzt die Feldwerte eingerichtet, auf die für die angegebenen Felder und Benutzer bzw. Benutzergruppen zugegriffen werden kann.