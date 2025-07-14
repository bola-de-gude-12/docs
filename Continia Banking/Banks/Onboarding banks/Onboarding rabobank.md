---
title: Onboarding Rabobank for Continia Banking
description: Information about Rabobank and how to set up direct communication.
date: 11-07-2025
id: CB-252
lang: en
---

# Onboarding Rabobank

To integrate with Rabobank, Continia Banking offers three different options: manual communication, direct communication through Bizcuit, and direct integration through their API. This article describes how to set up direct communication for Rabobank using direct integration.

To set up direct communication with Rabobank, you require:

* User account: Owner (*Eigenaar*) or AdministratorPlus (*BeheerderPlus*)
* Service: Rabo Business Banking or Rabo Business Banking Pro

You must authorize the user account to share account permissions with a third party. For more information, go to [rabobank.nl](https://www.rabobank.nl/bedrijven/service/online-bankieren/beheerderplus-autoriseren-rekeningen-delen-met-derden). For information about general preparation, refer to the next section of this article. 

For more information about connecting to Rabobank through Bizcuit, refer to the [Onboarding through Bizcuit](@CB-250) article.

## To prepare your Rabobank account

To use Continia Banking to communicate directly with Rabobank, you must make some preparations.

To set user permissions on the bank account:

1. Go to **Overzicht** (Overview) > **Gebruikersauthorisaties** (User authorizations) > **Overzicht Gebruikers** (Users overview) > **Gebruiker** (User) > **Per rekening** (Per account), and select a bank account.

2. Enable the following: 
   * **Saldo inzien** (View balance)
   * **Transacties inzien** (View transactions)
   * **Aanmaken en ondertekenen** (Create and sign)
   * **Inzien, aanmaken, wijzigen en verwijderen** (View, create, edit, and delete)

To set user permissions on Rabobank:

1. On Rabobank, go to **Overzicht** (Overview) >  **Gebruikersauthorisaties** (User authorizations) > **Overzicht Gebruikers** (Users overview) > **Gebruiker** (User) > **Algemeen** (General).

2. Navigate to **Betalen** (Payment), and enable **Importeren betaal en incassobestanden** (Import of payment and direct debit files).

3. Navigate to **Inzage**, and enable **Gegevens van passen en rekeningen inzien** (Access to cards and accounts).

   > [!IMPORTANT]
   >
   > Once set, it is important to keep the authorizations to prevent 404 errors from being displayed.


## To set up direct communication with Rabobank

To integrate with Rabobank directly, go through the steps of the assisted Assisted Setup guide **Set up Bank Account** in Continia Banking.  

1. Search ({{search}}) for and select **Bank Account Setup**.

1. Click **Next** to start the assisted setup.

1. On the **Bank System** field, select Rabobank,  and click **OK**.

1. Click **Next** to continue.

1. Click **Connect to Rabobank**. You are now directed to the login page of your bank. 

1. Log in to your bank, select one or multiple accounts, and select **Confirm**. A token is sent to Business Central. Continia uses this token to start the communication with your bank account.

1. Click **Next**. Now you can make payments and download account statements. To download account statements

The bank account reconciliation using Rabobank uses standard Continia Banking reconciliation functionality. 

