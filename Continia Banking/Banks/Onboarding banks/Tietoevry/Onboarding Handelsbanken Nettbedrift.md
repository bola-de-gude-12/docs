---
title: Onboarding Handelsbanken Nettbedrift
date: 25-03-2025
description: Onboarding Handelsbanken Nettbedrift with direct communication
id: CB-228
lang: en
---

# Onboarding Handelsbanken Nettbedrift

As a customer of Handelsbanken Nettbedrift, you can send and retrieve bank files between Handelsbanken Nettbedrift and Microsoft Dynamics 365 Business Central using Continia Banking.

Handelsbanken Nettbedrift uses the digital service Tietoevry to establish the bank integration from Continia Banking to Handelsbanken Nettbedrift.  

{{include "cb- kyc-verification-note"}}



## To request a file transfer agreement

1. Contact Handelsbanken for the file transfer agreement file. 
2. Send the signed agreement to your Cash Management adviser at Handelsbanken Nettbedrift. 
3. When the bank has approved and signed the agreement, please forward it to Continia Software: bank-integration@continia.com.



## To order bank files

When the agreement with Handelsbanken Nettbedrift has been established, contact your cash management adviser to order the files you want to use. 



## To set up direct communication

Now, you can set up your bank account to use direct communication in Continia Banking.

1. In Business Central, select the {{search}} icon, enter **Bank Account Setup**, and select the related link.

1. Click **Next** to begin the assisted setup.

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

1. Now, select the **Establish connection with Tietoevry** link. This directs you to your online bank, where you can sign up for Handelsbanken Nettbedrift bank integration.

    > [!IMPORTANT]
    >
    > Make sure you use the same VAT Registration No. as the VAT number you specified on the previous page.

1. You have now set up the bank account to use direct communication. Select **Next,** and you'll see the bank account status has changed to Ready. <br>

> [!IMPORTANT]
>
> Due to the KYC verification process, it can take up to 72 hours from when Handelsbanken Nettbedrift receives the file transfer agreement. You complete the assisted Bank Account Setup until the connection is established at Continia Software.  

You can start using direct communication when you have received the ordered files and an email confirmation from Continia Software.



## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Continia Banking by following the recommended steps as specified in the [Quick guide to setting up Continia Banking](@CB-03). 

