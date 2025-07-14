---
title: Onboarding Barclays
date: 09-02-2024
description: Onboarding Barclays with direct communication
id: PM-306
lang: en
---

# Onboarding Barclays with Direct Communication

As a customer of Barclays, using Barclays with SFTP communication, you can send and retrieve bank files between Barclays and Microsoft Dynamics 365 Business Central using the Payment Management Direct Communication service.

This article covers how to set up direct communication between Barclays and Payment Management.

> [!IMPORTANT]
>
> Before setting up the connection with Barclays Bank, please contact Continia.

## To sign up for Barclays  

To establish direct communication between Payment Management and Barclays, you must contact your Cash Management adviser at your bank and request access to the bank's online banking solution, and subscribe to the following services: 



> [!NOTE]
>
> When the agreement has been approved, you'll receive a letter with an SHB number (agreement no.) and the user number you must use to authenticate the connection from Business Central.



## Order bank files from your bank

When the agreement with Barclays has been established, log in to your bank and order the files you want to use. To see which files you must order, see [Barclays](@PM-222).



## To set up an SMTP email account

Before you can set up direct communication, the SFTP communication agreement must be established in Business Central for authentication and authorization. 

1. In Business Central, select the icon ![Search for page or report](/images/search_small.png), enter **Set up Email**, and select the related link.
2. Click **Next** to start setting up the email account.
3. In the overview of email account types, select "SMTP", and then **Next**. 
4. Enter the required account information, and select **Next**.
5. Select **Finish** to save the setup and close the assisted guide.

> [!NOTE] 
>
> For more detailed information about SMTP email accounts, refer to the [Microsoft documentation](https://docs.microsoft.com/en-us/dynamics365/business-central/admin-how-setup-email).



## To set up direct communication

When you've received the agreement from Barclays, you can begin the setup of direct communication in Payment Management.

1. In Business Central, select the icon ![Search for page or report](/images/search_small.png), enter **Bank Account Setup**, and select the related link.

1. Select **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing bank account, or create a new one by selecting **New Bank Account**.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

   > [!NOTE]
   >
   > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Choose bank system** page, select **Barclays**.

1. On the **Create certificate** page, fill in the fields as requested. Payment Management will auto-fill in most of the fields with existing information from Business Central. Type in the information that you received in the letter from the bank. 
   | <span style="white-space: nowrap;">Field</span> | Description |
   | --- | --- |
   | Agreement No. | The Global On-Line agreement number you received from Barclays. The number is also referred to as the *x*, and it always starts with x. |
   | User No. | The User No./User ID you received from Barclays |
   | PIN Code | Your password to Barclays SFTP. You should use a combination of numbers, letters, and capital letters. Don't use language-specific characters. |

1. Select **Next** to complete the bank account setup.  

When you return to the bank account overview, you'll see the bank account status has changed to Ready. However, you'll not be able to use direct communication before you've received an email from Barclays confirming that the access has been approved.

## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Payment Management by following the recommended steps as specified in the [Quick guide to setting up Payment Management](@PM-226). 

## Related information

[Supported bank files](@PM-137)  
