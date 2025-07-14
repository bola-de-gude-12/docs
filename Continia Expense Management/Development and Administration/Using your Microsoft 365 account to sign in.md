---
title: Signing in with your Microsoft 365 account
date: 09-12-2024
description: How to use SSO to login to the Expense App and Portal.
id: EM-160 
lang: en
---

# Using your Microsoft 365 account to sign in

Single Sign-On (SSO) is an authentication method that allows users to access multiple applications with a single set of credentials. The Continia Expense App and Portal now support Microsoft 365 sign-in, enabling users to authenticate with their Azure Active Directory (AD) credentials. With O365 sign-on, users benefit from centralized account management and SSO integration, while the user ID/password sign-on requires separate, application-specific credentials. This feature reduces the need to remember multiple logins, making it easier to access the Continia Expense App and Portal using an existing Microsoft 365 account.

Requirement:

* The email address associated with the Expense User is a valid Microsoft 365 work or school account

> [!NOTE]
> This feature is released with Expense Management version 7.0.0 and is compatible with all previous versions as long as you have a valid Microsoft 365 account. 

To sign into the Expense App using your Microsoft 365 account:
1. On the Expense Management login screen, select **Sign in with Microsoft 365**.
1. A message displays asking you to confirm using your Microsoft account, select **Continue**.
1. Enter your Microsoft 365 account email and password, and select **Sign in**. If Two-factor authentication is enabled for your Microsoft 365 account, you may need to approve the sign-in through the Microsoft Authenticator App.

>[!NOTE]
>Please note that your organization's admin may have applied approval settings for apps that have access to sign in with Microsoft 365. If you encounter a message regarding this, please request your organization's admin to add Continia Expense Management in Azure AD.

To sign into the Expense Portal using your Microsoft 365 account::

* On the Expense Management login screen, select **Sign in with Microsoft 365**. You are redirected to the standard Microsoft 365 login procedure. If you are already logged in to another website using Microsoft 365, it will sign you in automatically using the same credentials.

>[!NOTE]
>Once signed in using your Microsoft 365 account, you can no longer sign in using your Continia credentials.