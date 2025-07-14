---
title: Onboarding SpareBank 1
date: 08-08-2022
description: Onboarding SpareBank 1 with direct communication
id: PM-213
lang: en
---

# Onboarding SpareBank 1 with Direct Communication

SpareBank 1 is an alliance of 15 independent banks across Norway collaborating on a common platform and brand. Customers of a bank in the SpareBank 1 alliance can use the Payment Management Direct Communication service to send and retrieve bank files between SpareBank 1 and Microsoft Dynamics 365 Business Central. 

Payment Management uses the digital service Tietoevry to establish the bank integration with SpareBank 1, and this article covers the steps to set it up.

{{include "pm- kyc-verification-note"}}

## To set up direct communication

When your request for SpareBank 1 bank integration has been approved, you can set up your bank accounts to use direct communication.

1. In Business Central, select the icon ![Search for page or report](/images/search_small.png), enter **Bank Account Setup**, and select the related link.

1. Select **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing SpareBank1 bank account, or create a new one by selecting **New Bank Account**.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

    > [!NOTE]
    >
    > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Specify notification email** page, fill in the information needed for the KYC verification and select **Next**. 

1. Now, select the **Establish connection with Tietoevry** link. This directs you to your online bank, where you can sign up for SpareBank 1 bank integration. For details, see the section [Sign up for SpareBank 1 bank integration](#to-sign-up-for-sparebank-1-bank-integration). 

    > [!IMPORTANT]
    >
    > Make sure you use the same VAT Registration No. as the VAT number you specified on the previous page.

1. Select **Next** to complete the bank account setup. When you return to the bank account overview, you'll see that the bank account status has been updated to Ready. 

    > [!IMPORTANT]
    > It can take up to 72 hours after you subscribe to the bank integration and complete the assisted Bank Account Setup before SpareBank 1 approves the signup and the connection is established at Continia. You can start using direct communication when you receive a confirmation email from Continia.



## To sign up for SpareBank 1 bank integration

Before you begin setting up direct communication in Payment Management, you must request access to the SpareBank 1 bank integration.

1. In your online bank, select **Meny**    
1. Select **Betalingsprodukter** > **Produktoversikt**
1. Select **Koble til Økonomisystem** 
1. Select **Continia Software** 
1. In the **Velg kontoer du får innbetalinger på** dropdown menu, select the accounts for the Camt 054C files. 

SpareBank 1 now verifies the information, and if the request is approved, Sparebank 1 sends an encrypted email to Continia Software to notify them about the bank integration. The email contains information about the contact person, company name, and VAT number. Payment Management uses the VAT number for the KYC (Know Your Customer) verification when establishing the connection in Business Central.   



## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Payment Management by following the recommended steps as specified in the [Quick guide to setting up Payment Management](@PM-226). 



## Related information

[SpareBank 1 overview](@PM-143)  

 

