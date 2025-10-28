---
title: Signing in with your Microsoft 365 account
date: 05-08-2025
description: How to use SSO to log in to the Expense App and Portal
id: EM-160 
lang: en
---

# Using your Microsoft 365 account to sign in

Single Sign-On (SSO) is an authentication method that allows users to access multiple applications with a single set of credentials. The Continia Expense Mobile App and online Portal  support Microsoft 365 (O365) sign-in, which means users can instead authenticate with their Azure Active Directory (AD) credentials. With the O365 sign-on, users benefit from centralized account management and an SSO integration, while the user ID/password sign-on requires separate, application-specific credentials.

This feature reduces the need to remember multiple logins, making it easier to access the Continia Expense Mobile App and Portal using an existing Microsoft 365 account.

>[!WARNING]
>After you've signed in using your Microsoft 365 account, you can no longer sign in using your Continia credentials.

## Pre-requisites

* The email address associated with the Expense User is a valid Microsoft 365 work or school account.

> [!NOTE]
> This feature is released with Expense Management version 7.0.0 and is compatible with all previous versions as long as you have a valid Microsoft 365 account. 

## Sign in to the Expense Mobile App

To sign into the Expense Mobile App using your Microsoft 365 account:

1. On the Expense Management login screen, tap **Sign in with Microsoft 365**.
1. A message displays asking you to confirm using your Microsoft account, tap **Continue**.
1. Enter your Microsoft 365 account email and password.
1. Tap **Sign in**. If Two-factor authentication is enabled for your Microsoft 365 account, you may need to approve the sign-in via the Microsoft Authenticator App.

>[!NOTE]
>If an admin in your organization has applied approval settings for apps that have access to sign in with Microsoft 365, you may encounter a message regarding this. In such a scenario, you must ask the admin to add Continia Expense Management in Azure AD.

## Sign in to the online Expense Portal

To sign in to the online Expense Portal using your Microsoft 365 account:

* On the Expense Management login screen, click **Sign in with Microsoft 365**. 

You are redirected to the standard Microsoft 365 login procedure. If you are already logged in to another website using Microsoft 365, it will sign you in automatically using the same credentials.
