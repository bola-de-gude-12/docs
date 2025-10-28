---
title: Signing in to the Continia Expense Portal and app
date: 17-09-2025
description: How to sign in with your Continia account or MS 365 with SSO
id: EM-328
lang: en
---

# Signing in to the Continia Expense Portal and Mobile App
You can sign in to the Expense Portal online or via the Expense Mobile App, using either your Continia account email, or with your Microsoft 365 (O365) account email.

## Sign in with Continia

Use the email that is associated with your Continia account.
1.  Enter your email address and password.
1.  Click **Sign in**.

## Sign in with Microsoft 365
Single Sign-On (SSO) is an authentication method that allows users to access multiple applications with a single set of credentials. The Continia Expense Portal and online Mobile App both support O365 sign-in, which means users can instead authenticate with their Azure Active Directory (AD) credentials. With the O365 sign-in, users benefit from centralized account management and an SSO integration, while the user ID/password sign-in requires separate, application-specific credentials.

This feature reduces the need to remember multiple logins, making it easier to access the Continia Expense Portal and Mobile App using an existing Microsoft 365 account.

> [!WARNING]
> After you've signed in to the Continia Expense Portal with Microsoft 365, you won't be able to sign in to the portal thereafter with your Continia credentials. 

### Pre-requisites

Before you can sign in to the Continia Expense Portal with O365, you must have an email address tied to a valid O365 work or school account (not a personal account). This also applies to signing in to the portal in the Expense Mobile App.

> [!NOTE]
> This feature is compatible with all previous versions of Expense Management. As long as you are a valid Microsoft 365 user.

### Sign in to the online Expense Portal
Simplify your sign in process and sign in to the online Expense Portal using your O365 account.
To sign in to the portal:

1. In the Continia Expense Portal, click **Sign in with Microsoft 365** at the bottom-right of the page.
2. You are redirected to a Microsoft login sequence. If you've already logged on to another website with O365 then the system will automatically try to sign you in using the same credentials.

### Sign in to the Expense Mobile App

To sign in to the Expense Mobile App using your O365 account:

1. On the Expense Management login screen, tap **Sign in with Microsoft 365**.
2. A message displays asking you to confirm using your Microsoft account, tap **Continue**.
3. Enter your O365 account email and password.
4. Tap **Sign in**. If Two-factor authentication is enabled for your O365 account, you may need to approve the sign-in via the Microsoft Authenticator App.

> [!NOTE]
> If an admin in your organization has applied approval settings for apps that have access to sign in with O365, you may encounter a message regarding this. In such a scenario, you must ask the admin to add Continia Expense Management in Azure AD.

## Error message: Need admin approval

If you receive an error message that you need admin approval to log in, then you must contact the admin of your organization to add Continia Expense Management in Azure AD.


## Related information

For more information about the Expense Mobile App and portal, see:

[Using expense reports from your browser](@EM-294)

[Overview of the Continia Expense Mobile App](@EM-212)

[Continia Expense App FAQs](@EM-245)

