---
title: Onboarding Handelsbanken Nettbedrift
date: 06-01-2025
description: Onboarding Handelsbanken Nettbedrift with direct communication
id: PM-221
lang: en
---

# Onboarding Handelsbanken Nettbedrift to use Direct Communication

As a customer of Handelsbanken Nettbedrift, you can send and retrieve bank files between Handelsbanken Nettbedrift and Microsoft Dynamics 365 Business Central using the Payment Management Direct Communication service.

Handelsbanken Nettbedrift uses the digital service Tietoevry to establish the bank integration from Payment Management to Handelsbanken Nettbedrift.  

{{include "pm- kyc-verification-note"}}



## To request a file transfer agreement

1. Contact Handelsbanken for the file transfer agreement file. 
2. Send the signed agreement to your Cash Management adviser at Handelsbanken Nettbedrift. 
3. When the bank has approved and signed the agreement, please forward it to Continia Software: bank-integration@continia.com.



## To order bank files

When the agreement with Handelsbanken Nettbedrift has been established, contact your cash management adviser to order the files you want to use. To see which files you must order, see the article [Handelsbanken Nettbedrift](@PM-220).



## To set up direct communication

Now, you can set up your bank account to use direct communication in Payment Management.

1. In Business Central, select the {{search}} icon, enter **Bank Account Setup**, and select the related link.

1. Select **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing bank account, or create a new one by selecting **New Bank Account**.

1. On the **Bank Account Card** page, on the **General** FastTab, the following details must be included:

    * **Bank Branch No.**: 9049
    * **Bank Account No.**: 0721538

    This ensures that the Tietoevry Bank reference is properly associated with the bank card.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

    > [!NOTE]
    >
    > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Specify notification email** page, fill in the fields with the relevant information. Continia uses this information in a Know Your Customer (KYC) verification process to verify the ownership of the bank account. Select **Next**.

    > [!IMPORTANT]
    >
    >The VAT Registration No. must be the same as the VAT number that you specified in the file transfer agreement. 
    >

1. You have now set up the bank account to use direct communication. Select **Next,** and you'll see the bank account status has changed to Ready. <br>

> [!IMPORTANT]
>
> Due to the KYC verification process, it can take up to 72 hours from when Handelsbanken Nettbedrift receives the file transfer agreement. You complete the assisted Bank Account Setup until the connection is established at Continia Software.  

You can start using direct communication when you have received the ordered files and an email confirmation from Continia Software.



## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Payment Management by following the recommended steps as specified in the [Quick guide to setting up Payment Management](@PM-226). 

