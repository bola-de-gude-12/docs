---
title: Anmeldung mit Ihrem Microsoft 365-Konto
date: 09-12-2024
description: So verwenden Sie SSO, um sich bei der Expense-App und dem Portal anzumelden.
id: EM-160
lang: de
---

# Anmeldung mit Ihrem Microsoft 365-Konto

Single Sign-On (SSO) ist eine Authentifizierungsmethode, die es Benutzern ermöglicht, mit den gleichen Anmeldeinformationen auf mehrere Anwendungen zuzugreifen. Die Continia Expense App und das Portal unterstützen jetzt die Microsoft 365-Anmeldung, sodass sich Benutzer mit ihren Azure Active Directory (AD)-Anmeldeinformationen authentifizieren können. Bei der O365-Anmeldung profitieren Benutzer von einer zentralen Kontoverwaltung und SSO-Integration, während für die Anmeldung mit Benutzer-ID und Kennwort separate, anwendungsspezifische Anmeldeinformationen erforderlich sind. Dank dieser Funktion müssen Sie sich nicht mehrere Anmeldedaten merken und können mit einem vorhandenen Microsoft 365-Konto einfacher auf die Continia Expense-App und das Portal zugreifen.

Anforderungen:

- Die mit dem Expense-Benutzer verbundene E-Mail-Adresse muss ein gültiges Microsoft 365 Arbeits- oder Schulkonto sein

> [!NOTE]
> Diese Funktion wird mit Expense Management Version 7.0.0 veröffentlicht und ist mit allen vorherigen Versionen kompatibel, solange Sie über ein gültiges Microsoft 365-Konto verfügen.

So melden Sie sich mit Ihrem Microsoft 365-Konto bei der Expense App an:

1. Wählen Sie auf dem Anmeldebildschirm von Expense Management **Mit Microsoft 365 anmelden** aus.
2. Es wird eine Meldung angezeigt, in der Sie zur Bestätigung der Verwendung Ihres Microsoft-Kontos aufgefordert werden. Wählen Sie **Weiter** aus.
3. Geben Sie die E-Mail-Adresse und das Kennwort Ihres Microsoft 365-Kontos ein und wählen Sie **Anmelden**. Wenn die Zwei-Faktor-Authentifizierung für Ihr Microsoft 365-Konto aktiviert ist, müssen Sie die Anmeldung möglicherweise über die Microsoft Authenticator-App genehmigen.

> [!NOTE]
> Beachten Sie, dass der Administrator Ihres Unternehmens möglicherweise Genehmigungseinstellungen für Apps angewendet hat, die Zugriff auf die Anmeldung bei Microsoft 365 haben. Wenn Sie eine entsprechende Meldung erhalten, bitten Sie den Administrator Ihres Unternehmens, Continia Expense Management in Azure AD hinzuzufügen.

So melden Sie sich mit Ihrem Microsoft 365-Konto beim Expense Portal an:

- Wählen Sie auf dem Anmeldebildschirm von Expense Management **Mit Microsoft 365 anmelden** aus. Sie werden zum standardmäßigen Microsoft 365-Anmeldeverfahren weitergeleitet. Wenn Sie bereits mit Microsoft 365 bei einer anderen Website angemeldet sind, werden Sie automatisch mit denselben Anmeldeinformationen angemeldet.

> [!NOTE]
> Sobald Sie sich mit Ihrem Microsoft 365-Konto angemeldet haben, können Sie sich nicht mehr mit Ihren Continia-Anmeldeinformationen anmelden.
