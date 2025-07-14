---
title: Authentication with Bizcuit
description: Information about the service provider Bizcuit and how to create a Bizcuit account.
date: 20-02-2025
id: PM-165
lang: en
---

# Onboarding Bizcuit with Direct Communication

To integrate with your bank, Payment Management uses Bizcuit: a leading [PSD2](#psd2)-licensed service provider in the Netherlands. Payment Management integrates seamlessly with Bizcuit, so you can download your bank account statements and initiate payments directly from Microsoft Dynamics 365 Business Central.

> [!NOTE]
>
> The direct communication services supported by Bizcuit depend on your bank. Navigate to your bank from the [Bank Integration overview](@PM-98) to see which services are supported.

This article covers the steps to set up direct communication between your bank and Payment Management using Bizcuit.

> [!IMPORTANT]
>
> To avoid issues with subscription charges, customers must create their user accounts through our onboarding link in the assisted setup process. This step is required since Bizcuit now offers subscription plans.

## To set up direct communication with Bizcuit

To use the services of Bizcuit, you must create an account at Bizcuit. The signup to Bizcuit is handled through the assisted **Bank Account Setup** guide in Payment Management.  

1. In Business Central, select the icon ![Search for page or report](/images/search_small.png), enter **Bank Account Setup**, and select the related link.

1. Select **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing bank account, or create a new one by selecting **New Bank Account**.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

1. If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Create Bizcuit Account** page, select the link to start the signup process with Bizcuit. This will open a new tab in your browser, from where you can:

   - Link your account:
     - Confirm your identity with [iDIN](#idin) by using the login details of your personal bank account. 
     - Add your business account.
     - Specify the ultimate beneficial owners (UBOs) of the organization.
   - Create your administration with company information such as the name, the Chamber of Commerce number, and an incoming and outgoing email address.
   - Link your bank accounts.

   >[!NOTE]
   >
   >For detailed information from Bizcuit about creating and linking accounts, please refer to the links in the [See also](#see-also) section. 

1. When you have created and set up your account with Bizcuit, you'll be directed back to the Payment Management Bank Account Setup to finish the setup.

   > [!IMPORTANT]
   > On the **Bank Account Overview** page, the bank account statuses indicate if the accounts are ready for use. It can take up to 2 days before your bank account is fully up and running with Bizcuit.  

## To prepare to connect to Bizcuit

Before you can set up direct communication with Bizcuit, you must connect and verify your bank account.

To connect the bank account:

1. Go to Bizcuit, and on the main screen, navigate to **Aanbevelingen** (recommendations). If you recently created your Bizcuit account, you are prompted to connect the bank account.

2. To connect the account you used when creating your Bizcuit account, select **Bankrekening koppelen** (Connect the bank account). If you want to connect a different bank account, navigate to **Instellingen** (Settings) and select **Bankrekening toevoegen** (Add bank account). You can now add the permissions.

3. To make sure verify the registration is correct, you must confirm your IBAN number and the bank account name using the **Deze tenaamstelling is correct** (The naam on this bank account is correct) checkbox. Select **Bevestigen** (Confirm) to confirm. 

   If the bank account name is different from the name registered as the director at the *Kamer van Koophandel* (Chamber of Commerce), you will be prompted to verify your authority. On the **Bevoegdheid** (Authority) dialog, select the **Ik bevestig dat ik gemachtigd ben om transacties in te zien in de naam van ...** (I confirm that I am authorized to view transactions in name of xxx) checkbox and select **Bevestig bevoegdheid** (Confirm authority).

   > [!NOTE]
   >
   > Confirming your authority requires you to have the required permissions in the bank environment. For example, for ABN AMRO and Rabobank you must be the owner or have these permissions assigned to you by the owner. For ING you must be the owner. 

## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Payment Management by following the recommended steps as specified in the [Quick guide to setting up Payment Management](@PM-226). 



## Additional information

### PSD2

The European revised Payment Services Directive (PSD2) has been in force since 2019 and states that customers are in charge of their bank data and payment solutions. The new legislation provides the legal framework within which all payment service providers must operate.

Following the introduction of the new legislation, Bizcuit has developed an innovative solution that offers to proceed with all administrative and financial transactions within the Bizcuit app. Bizcuit has been granted a PSD2 license, allowing the app to operate with fully automatic links to all banks. For more information about how Bizcuit complies with the PSD2 regulations in the article, refer to this article: [What is PSD2](https://www.bizcuit.nl/wat-is-psd2/).

### iDIN

iDIN is a collaboration between all major Dutch banks, allowing customers to use their personal bank login to authenticate identification on various online websites and organizations, such as Bizcuit.

When customers are using their personal bank account to link a business account to Bizcuit, it'll only be used to confirm their identity. Bizcuit will not have access to any personal bank account data.

## Related information

[Setting up bank accounts](@PM-3)  
[Bizcuit - Getting started](https://support.bizcuit.nl/)  
[Bizcuit - Link account](https://support.bizcuit.nl/bankrekeningen)  
