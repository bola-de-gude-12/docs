---
title: Onboarding Nordea
description: Onboarding Nordea with direct communication
date: 11-06-2025
id: CB-83
lang: en
---

# Onboarding Nordea

As a customer of Nordea, you can use Nordea Corporate Access to send and receive bank files between Nordea and Microsoft Dynamics 365 Business Central using the Continia Banking Direct Communication service.

This article covers the steps to set up direct communication between Nordea Corporate Access and Continia Banking.  

## To request a Nordea Corporate Access agreement

Before you begin setting up direct communication in Continia Banking, contact your bank Cash Management adviser to request a Nordea Corporate Access agreement with the following services:

- Corporate Access File Transfer
- Corporate Access Payable
- Corporate Access Account Reporting
- Corporate Netbank/Corporate Netbank Administration

It is important to inform Nordea that you're implementing a Continia Banking solution. This way, Nordea can set up your accounts and agreements with the required files and settings.

> [!IMPORTANT]
>
> When migrating from Payment Management to Continia Banking, Nordea will automatically reuse the existing settings from the Payment Management setup. In Payment Management, it was necessary to request both CAMT.053 and CAMT.053e files, but in Continia Banking, only the required file should be enabled. Unless you explicitly request Nordea to update the settings to reflect only the provided files, the downloaded configuration may include unnecessary formats, which could cause issues. Make sure to coordinate with Nordea to adjust this before finalizing the setup.



## To set up direct communication

When you have the Nordea Corporate Access agreement in place, you can run the assisted Bank Account Setup guide to set up your bank account to use direct communication.

1. Search ({{search}}) for and select **Bank Account Setup**.

1. Click **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing Nordea bank account, or create a new one by selecting **New Bank Account**.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

    > [!NOTE]
    >
    > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Create certificate for direct communication** page, enter the information you received from the bank when you signed up for the Nordea Corporate Access service.

    | <span style="white-space: nowrap;">Field</span> | Description |
    | --- | --- |
    | User No. | The "Signer ID" in the Corporate Access File Transfer agreement. Refer to field #1 in the image below. <br />The User No. is always 10 or 11 digits. |
    | PIN Code | The "Activation Code for Nordea eID" sent to you in a text message by Nordea. |
    | Company ID | The "Sender ID-number" in the Corporate Access File Transfer agreement. Refer to field #2 in the image below.<br />The Company ID is always 10 or 11 digits. |
    | Certificate Holder | The "Name" in the Corporate Access File Transfer agreement. Refer to field #3 in the image below. |
    | Agreement No. | The "Agreement No." is available in the Corporate Access File Transfer agreement. Refer to field #4 in the image below. |

    <br>

    ![nordea-image](/images/nordea-image.png)

1. Click **Next** to continue the bank account setup. When you return to the bank account overview, you'll see that the bank account status has been updated to Ready, and you are ready to start using Continia Banking Direct Communication. 

> [!IMPORTANT]
>
> You must contact your bank Cash Management adviser for assistance in creating and using a different Signer ID from the one used when you first set up the Nordea Corporate Access agreement. 




## Additional information

The Signer ID (User No.) is automatically created with all the appropriate services and settings when you create a new Corporate Netbank Administration agreement. However, if you wish to use another Signer ID for Business Central, you can create a new one. If you do, please contact your cash management adviser for assistance or follow the guidelines below. 

- To create a new Signer ID, access your Nordea Corporate Online Bank and navigate to the **Corporate Access File Transfer** menu. If you choose to create a **Company Certificate** of the **ID type** *Other*, note that you can't use a slash or other special characters, such as *Cronus A/S*, in the **Last name** field. 
- Ensure that you subscribe to the correct files (status files, customer payment files, and bank account statement files) to continue sending bank data between Business Central and Nordea. Ask your Nordea Cash Management adviser for assistance. 
- Set up account rights for each payment type used in Corporate Access and connect them to the correct Signer ID. To manage the account rights, go to Corporate Netbank Administration, select **Corporate Access Payables**, choose **Signer ID,** and update accordingly. When setting up account rights, the field **Manual Confirmed** defines whether you want to send payments straight through Nordea (un-ticked) without additional approval in Corporate Netbank or if you're going to confirm payments in Corporate Netbank (ticked) manually. 
- In the Corporate Netbank Administration, navigate to the **Corporate Access File Transfer** menu and order a Signer/Nordea eID. You'll receive the PIN code via a text message from Nordea. 

Contact your usual contact person or cash management advisor at Nordea for further information and assistance.



