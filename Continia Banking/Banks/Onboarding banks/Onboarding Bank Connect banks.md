---
title: Onboarding Bank Connect banks with Continia Banking
date: 27-05-2025
description: Onboarding Bank Connect banks with direct communication
id: CB-147
lang: en
---

# Onboarding Bank Connect banks with direct communication

Bank Connect is a collaboration between the Regional Bankers' Association, local banks, and the three data centers; SDC, BEC, and Bankdata. As a customer of one of the banks in this collaboration, you can send and retrieve bank files between Bank Connect and Microsoft Dynamics 365 Business Central using the Continia Banking Direct Communication service. 

This article covers the steps to set up direct communication between your bank and Continia Banking using Bank Connect.

## To sign up for the Bank Connect Web Service

Before you begin setting up direct communication in Continia Banking, please get in touch with your Cash Management adviser in your bank and request the following:

- Access to the Bank Connect Web Service 
- A technical EDI Web service user and PIN code

> [!NOTE]
>
> When your agreement has been approved, a web service user is automatically created by Bank Connect, and you'll receive a letter with the required PIN code.  



## To order bank files from your bank

When the agreement with Bank Connect has been established, sign in to your bank and order the files you want to use. To see which files you need to order, navigate to your bank from the [Bank Integration overview](@CB-79).

> [!NOTE]
>
> It can take up to a day before receiving the files, as the files are generated during the night or early morning and not by request.



## To set up direct communication

Even before you receive the ordered files, you can set up your bank accounts to use direct communication in Continia Banking. 

1. Search ({{search}}) for and select **Bank Account Setup**.

1. Click **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing bank account, or create a new one by selecting **New Bank Account**.

1. Ensure that Direct Communication is selected for the bank account in the Communication column, and then select **Next**.

   > [!NOTE]
   >
   > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Create certificate for direct communication** page, enter the information you received in the letter from your bank.

   | <span style="white-space: nowrap;">Field</span> | Description |
   | --- | --- |
   | User No. | This is equivalent to the Function ID consisting of a minimum of 11 characters (the 5-digit customer number can't be used). |
   | PIN Code | The activation code. |
   | Main Bank Branch Code | Your bank's main branch number, which you can find [here](https://www.bankconnect.dk/da/faq/pengeinstitutter) (the number is mentioned in parenthesis after the bank name). |

1. Click **Next** to complete the bank account setup. When you return to the **Bank Account Overview** page, you'll see the status for the bank account has changed to *Ready*. 

You can start using direct communication when you receive the files you ordered from the bank. 

## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Continia Banking by following the recommended steps as specified in the [Quick guide to setting up Continia Banking](@CB-03). 

