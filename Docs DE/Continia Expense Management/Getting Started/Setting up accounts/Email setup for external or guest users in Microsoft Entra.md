---
title: E-Mail-Einrichtung für externe Benutzer oder Gastbenutzer in Microsoft Entra
date: 27-05-2025
description: Erfahren Sie, wie Sie E-Mail für externe Benutzer und Gastbenutzer in Entra einrichten
id: EM-317
lang: de
---

# E-Mail-Einrichtung für externe Benutzer oder Gastbenutzer in Microsoft Entra

Ein externer Benutzer oder Gastbenutzer in Microsoft Entra hat entweder den Zusatz #EXT# in seiner E-Mail-Adresse oder eine entsprechende Bezeichnung (z. B. „Externer Techniker“). Ein Standardbenutzername wird dagegen normalerweise im folgenden Format angegeben:

Benutzer_xxxxyyyyyzzzzzzz

Wenn Sie ein Continia-Benutzerkonto für einen Gast oder externen Business Central-Benutzer erstellen, wird die zu Continia Online exportierte E-Mail in den Informationen auf der **Benutzerkarte** angezeigt. Sie finden sie unter **Microsoft 365** im Feld **Authentifizierungs-E-Mail**. Sie enthält normalerweise das Wort „Techniker“ oder die E-Mail-Adresse enthält den Zusatz EXT. Dies hat zur Folge, dass die Anmeldung beim Expense Mobile Portal und Web Portal fehlschlägt.

So richten Sie die E-Mail für externe oder Gastbenutzer richtig ein:

1. Suchen Sie {{search}} nach **Continia Benutzer**.
2. Wählen Sie oben rechts **Einstellungen** > **Personalisieren**.
3. Wählen Sie in der Aktionsleiste **Personalisieren** > **+Feld** aus, um eine Spalte hinzuzufügen.
4. Ziehen Sie die Spaltenüberschrift aus der Liste **Feld der Seite hinzufügen** an die Stelle in der Tabelle, an der sie platziert werden soll.
5. Klicken Sie auf den Text des Felds und geben Sie Folgendes ein: Office 365-Authentifizierung E-Mail.
6. Klicken Sie auf **Fertig**.
7. Fügen Sie der neuen Spalte die richtige E-Mail-Adresse hinzu (sie muss mit der Adresse in der Spalte **E-Mail** übereinstimmen).
8. Klicken Sie in der Aktionsleiste auf **Benutzer exportieren** > **OK**.

## Informationen zum Thema

[Beibehalten der Expense-Historie beim Ändern von Benutzer-E-Mails](@EM-325)
