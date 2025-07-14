---
title: Onboarding Eika Alliance in Continia Banking
date: 26-03-2025
description: Onboarding Eika Alliance with direct communication in Continia Banking.
id: CB-223
lang: en
---

# Onboarding Eika Alliance

Eika Alliance is an alliance of local banks across Norway collaborating on a common platform and brand. Customers of a bank in the Eika Alliance alliance can use Continia Banking to send and retrieve bank files between the Eika Alliance bank and Microsoft Dynamics 365 Business Central. 

Continia Banking uses the digital service Tietoevry to establish the bank integration with the Eika Alliance bank, and this article covers the steps to set it up.

{{include "cb- kyc-verification-note"}}

## To set up direct communication

When your request for Eika Alliance bank integration has been approved, you can set up your bank accounts to use direct communication.

1. In Business Central, select the {{search}} icon, enter **Bank Account Setup**, and select the related link.

1. Click **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing Eika Alliance bank account, or create a new one by selecting **New Bank Account**.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

    > [!NOTE]
    >
    > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Specify notification email** page, fill in the information needed for the KYC verification and select **Next**. 

1. Now, select the **Establish connection with Tietoevry** link. This directs you to your online bank, where you can sign up for Eika Alliance bank integration.

    > [!IMPORTANT]
    >
    > Make sure you use the same VAT Registration No. as the VAT number you specified on the previous page.

1. Click **Next** to complete the bank account setup. When you return to the bank account overview, you'll see that the bank account status has been updated to Ready. <br>

> [!IMPORTANT]
>
> It can take up to 72 hours after you subscribe to the bank integration and complete the assisted Bank Account Setup before Eika Alliance approves the signup and the connection is established at Continia. You can start using direct communication when you receive a confirmation email from Continia.



## To sign up for Eika Alliance bank integration

Before you begin setting up direct communication in Continia Banking, you must request access to the Eika Alliance bank integration.

1. In your online bank, select **Meny**.
1. Select **Betalingsprodukter** > **Produktoversikt**.
1. Select **Koble til Økonomisystem**.
1. Select **Continia Software**.
1. In the **Velg kontoer du får innbetalinger på** dropdown menu, select the accounts for the Camt 054C files. 

Eika Alliance now verifies the information, and if the request is approved, Eika Alliance sends an encrypted email to Continia Software to notify them about the bank integration. The email contains information about the contact person, company name, and VAT number. Continia Banking uses the VAT number for the KYC (Know Your Customer) verification when establishing the connection in Business Central.   



## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Continia Banking by following the recommended steps as specified in the [Quick guide to setting up Continia Banking](@CB-03). 





 

