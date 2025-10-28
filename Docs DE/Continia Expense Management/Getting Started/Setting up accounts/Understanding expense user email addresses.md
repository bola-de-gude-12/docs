---
title: Grundlegendes zu Expense-Benutzer-E-Mail-Adressen
date: 27-05-2025
description: Erfahren Sie mehr über die verschiedenen E-Mail-Adressfelder und ihre Bedeutung
id: EM-322
lang: de
---

# Grundlegendes zu Expense-Benutzer-E-Mail-Adressen

Ein Expense-Benutzer wird normalerweise durch seine E-Mail-Adresse identifiziert, die in der Continia Benutzereinrichtung in Microsoft NAV/Business Central angegeben ist. Manchmal werden jedoch stattdessen andere E-Mail-Felder in Continia exportiert. Dazu gehört die in den folgenden Feldern angegebene E-Mail-Adresse: Authentifizierungs-E-Mail (in Benutzern) oder Office 365-Authentifizierungs-E-Mail (in der Continia-Benutzerliste). In den folgenden Abschnitten erfahren Sie mehr über die einzelnen Felder.

## Continia Benutzereinrichtung

Hier wird normalerweise die E-Mail-Adresse für den Benutzernamen/Anmeldenamen des Expense-Benutzers angegeben.

Dies ist die Adresse, an die die Willkommens-E-Mail von Expense Management gesendet wird. Es handelt sich dabei um dieselbe Adresse für die Anmeldung bei der Expense Mobile App oder dem Expense Web Portal. Die einzige Ausnahme besteht, wenn sie Office365 für die Anmeldung verwenden. Weitere Informationen finden Sie unter [Office 365 on the Expense Web Portal and Expense Mobile App](https://continia.zendesk.com/hc/da/articles/360019865699).

## Authentifizierungs-E-Mail

Wenn ein Continia-Benutzer auch ein Microsoft NAV/Business Central-Benutzer ist, finden Sie die Authentifizierungs-E-Mail in der Benutzerliste. Dies ist die E-Mail-Adresse, die in Continia als E-Mail-Adresse des Expense-Benutzers exportiert wird (unabhängig von den Angaben in der Continia Benutzereinrichtung).

## Office 365-Authentifizierungs-E-Mail

Die dritte für Expense Management relevante E-Mail-Angabe ist das Feld Office365-Authentifizierung E-Mail. Sie können dies in der Continia-Benutzerliste sehen, wenn Sie diese Spalte bereits manuell hinzugefügt haben.

Diese E-Mail-Adresse hat Vorrang vor der Authentifizierungs-E-Mail des Benutzers. Sie ist nützlich für externe Benutzer, Alias-Benutzer (z. B. Partnertechniker) oder um die Verwendung der langen Microsoft-E-Mail-Adresse zu vermeiden.

Wenn eine Office365-Authentifizierungs-E-Mail verwendet wird, stellen Sie sicher, dass die E-Mail-Adresse für die Continia-Benutzereinrichtung und die E-Mail-Adresse in diesem Feld übereinstimmen. Andernfalls findet das System beim Senden von Erinnerungen und Updates möglicherweise nicht die richtige Benutzer-ID.

## Informationen zum Thema

[Beibehalten der Expense-Historie beim Ändern von Benutzer-E-Mails](@EM-325)  
[E-Mail-Einrichtung für externe Benutzer oder Gastbenutzer in Microsoft Entra](@EM-317)