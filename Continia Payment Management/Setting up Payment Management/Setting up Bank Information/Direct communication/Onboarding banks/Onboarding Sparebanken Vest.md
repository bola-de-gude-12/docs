---
title: Onboarding SpareBanken Vest
date: 08-08-2022
description: Onboarding SpareBanken Vest with direct communication
id: PM-219
lang: en
---

# Onboarding SpareBanken Vest to use Direct Communication

As a customer of Sparebanken Vest, you can send and retrieve bank files between Sparebanken Vest and Microsoft Dynamics 365 Business Central using the Payment Management Direct Communication module.

Payment Management uses the digital service Tietoevry to integrate with SpareBanken Vest, and this article covers the steps to set it up.  



## To request a file transfer agreement

Before you begin setting up direct communication in Payment Management, you must request a file transfer agreement with Sparebanken Vest.

1. Download and fill in the [transfer agreement](https://partnerzone.blob.core.windows.net/articles/pm/Continia%20Software%20AS%20Fullmaktsavtale.pdf) file.
1. Send the agreement to Sparebanken Vest (cm@spv.no). 
1. When the bank has approved and signed the agreement, please forward it to Continia (bank-integration@continia.com). 



## To set up direct communication

When the file transfer agreement has been approved, you can set up your bank accounts to use direct communication.

1. In Business Central, select the icon ![Search for page or report](/images/search_small.png), enter **Bank Account Setup**, and select the related link.

1. Select **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing Sparebanken Vest bank account, or create a new one by selecting **New Bank Account**.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

    > [!NOTE]
    >
    > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Specify notification email** page, fill in the fields with the relevant information. Continia uses this information in a Know Your Customer (KYC) verification process to verify the ownership of the bank account. 

    > [!IMPORTANT]
    >
    >The VAT Registration No. must be the same as the number you specified in the file transfer agreement. 
    >

1. On the **Establish secure connection** page, select **Establish connection with Tietoevry**. This opens your online bank from where you can set up direct communication with Continia Payment Management. 

    > [!NOTE]
    >
    > Please get in touch with your bank for detailed information about connecting with the online bank. 

1. Select **Next** to complete the bank account setup. When you return to the bank account overview, you'll see that the bank account status has been updated to Ready. <br>

> [!IMPORTANT]
>
> Due to the KYC verification process, it can take up to 72 hours for Sparebanken Vest to receive the file transfer agreement, and you complete the assisted Bank Account Setup guide until the connection is established at Continia.   


You can start using direct communication when you receive an email confirmation from Continia Software.  



## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Payment Management by following the recommended steps as specified in the [Quick guide to setting up Payment Management](@PM-226). 

## Related information

[Supported bank files](@PM-218)  

 

