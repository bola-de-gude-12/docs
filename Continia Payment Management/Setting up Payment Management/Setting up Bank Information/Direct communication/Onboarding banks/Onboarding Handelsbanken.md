---
title: Onboarding Handelsbanken GlobalOnLine
date: 18-06-2025
description: Onboarding Handelsbanken GlobalOnLine with direct communication.
id: PM-181
lang: en
---

# Onboarding Handelsbanken GlobalOn-Line with Direct Communication

As a customer of Handelsbanken, using Handelsbanken GlobalOn-Line with Global Gateway SFTP communication, you can send and retrieve bank files between Handelsbanken and Microsoft Dynamics 365 Business Central using the Payment Management Direct Communication service.

> [!IMPORTANT]
>
> Payment Management does not support accounts set up with the Corporate Signing agreement. This agreement requires a PGP key for functionality, which is not supported by Payment Management.

This article explains how to establish direct communication between Handelsbanken GlobalOn-Line and Payment Management. It consists of the following phases:

1. [Sign up at Handelsbanken GlobalOnLine](#to-sign-up-for-a-handelsbanken-globalon-line-agreement)
2. [Setup SMTP Email account (if not created earlier)](#to-set-up-an-smtp-email-account)
3. [Set up direct communication](#to-set-up-direct-communication)
4. [Finalize the setup](#to-finalize-the-setup)

> [!IMPORTANT]
>
> If you use Handelsbanken Netbank Erhverv as your online banking solution, refer to the article [Onboarding Bank Connect banks](Onboarding Bank Connect banks.md).



## To sign up for a Handelsbanken GlobalOn-Line agreement 

To establish direct communication between Payment Management and Handelsbanken, you must contact your Cash Management adviser at your bank and request access to the bank's online banking solution, and subscribe to the following services: 

- Handelsbanken Global On-Line
- Handelsbanken Global Gateway SFTP communication

Once the agreement is approved, you will receive an email that contains the following details:
- Agreement number
- User number, which will be used to authenticate the connection from Business Central.
- Paths for importing and exporting files that need to be entered on the bank card.



## To set up an SMTP email account

Before you can set up direct communication, the SFTP communication agreement must be established in Business Central for authentication and authorization. 

> [!IMPORTANT]
>
> You can only set up direct communication in a production environment and not in a sandbox environment.

To set up an SMTP email account:

1. In Business Central, search ({{search}}) for and select **Set up Email**.
2. Click **Next** to start setting up the email account.
3. In the overview of email account types, select "SMTP", and click **Next**. 
4. Enter the required account information, and click **Next**.
5. Select **Finish** to save the setup and close the assisted guide.

> [!NOTE] 
>
> For more detailed information about SMTP email accounts, refer to the [Microsoft documentation](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-how-setup-email).



## To set up direct communication

Once you have received the agreement from Handelsbanken GlobalOn-Line, you can proceed with setting up direct communication in Payment Management.

1. In Business Central, search ({{search}}) for and select **Bank Account Setup**.

1. Click **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing bank account, or create a new one by selecting **New Bank Account**.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

   > [!NOTE]
   >
   > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Choose bank system** page, select **HBISO20022**.

1. On the **Create certificate** page, fill in the fields as requested. Payment Management will auto-fill in most of the fields with existing information from Business Central. Type in the information that you received in the email from the bank. 
   | <span style="white-space: nowrap;">Field</span> | Description |
   | --- | --- |
   | Agreement No. | Companies based in Sweden must use their Swedish organization number. If your company is based in a different country, you must use The Global On-Line agreement number that you received in the email from Handelsbanken. The number is also called the *Handelsbanken SHB-number*, and it always starts with "33". |
   | User No. | The User No./User ID that you received in an email from Handelsbanken when you signed the Global On-Line agreement. |
   | PIN Code | Your password to Handelsbanken Global Gateway SFTP. Create one yourself using a combination of numbers, letters, and capital letters. Don't use language-specific characters. |
   | SFTP Certificate Email | Add your email address and when the email is generated, forward it to your contact at Handelsbanken for them to handle the last step of the setup. |
   
1. Click **Next** to complete the bank account setup. An email will be sent from the SMTP mail server to the designated contact email address, usually the Cash Management Adviser. It is important that this adviser forwards the email promptly to the respective customer contact at Handelsbanken. The email will contain comprehensive details and an essential SSH key, which is crucial for Handelsbanken to successfully complete the setup process.

## To finalize the setup

To complete the setup on the bank card:

1. Select the {{search}} icon, enter **Banks**, and then select the related link.

2. Open the relevant Handelsbanken bank card.

3. On the bank card, navigate to the **Communication Agreement** FastTab and fill in the following fields:
   * **File Path/Folder for Import** - enter the import folder name. Use: *out* (no backslashes).
   * **File Path/Folder for export** - enter the import folder name. Use: *in* (no backslashes).

> [!IMPORTANT] 
>
> If the connection cannot be established, please check the file archive for the error code and contact Continia to resolve the issue.

## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Payment Management by following the recommended steps as specified in the [Quick guide to setting up Payment Management](@PM-226). 



## Related information

[Supported bank files](@PM-137)  
