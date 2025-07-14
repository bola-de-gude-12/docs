---
title: Setting up bank accounts
description: Set up the company bank accounts with Payment Management.
date: 16-09-2022
id: PM-3
lang: en
---

# Setting up Bank Accounts

To use the many functionalities of Payment Management, your company bank accounts must be set up for Payment Management using the assisted bank account setup. 

You can set up your bank accounts to use:

- [Direct Communication](#to-set-up-bank-accounts-to-use-direct-communication) 
- [Manual Communication](#to-set-up-bank-accounts-to-use-manual-communication)

When a bank account is set up with Payment Management, a corresponding bank will automatically be created in Business Central together with a bank system. The bank system defines how bank data is validated and handled when exporting and importing bank data. If you need to manually import a bank setup file, see the section [To import a bank setup file](#To-import-a-bank-setup-file).

## To set up bank accounts to use direct communication

To set up your bank account to use direct communication:

1. From the [Bank Integration](@PM-98) article, navigate to article for the bank you are using.
2. In the article, select the link "Direct Communication" and follow the detailed steps for your specific bank or bank system. 



## To set up bank accounts to use manual communication

> [!IMPORTANT]
>
> To use manual communication between your bank and Payment Management, you must contact your bank and order the relevant bank files. To see which files you need to order, navigate to the detailed article for your bank from the article [Bank Integration](@PM-98).

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Account Setup**, and select the related link.

1. Select **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing bank account, or [create a new one](#to-create-a-new-bank-account) by selecting **New Bank Account**.

   > [!NOTE]
   >
   > Use the **Status** in the bank account overview, as an indicator to whether the bank account has already been set up for either manual or direct communication.  

1. In the **Communication** column, ensure that **Manual Communication** is selected for the bank account, and then select **Next**.

1. Fill in the fields in each step of the guide. Hover over a field to read a short description.

1. After you've set up the bank account, the status in the **Bank Accounts** overview will be set to **Ready** and the bank account is ready for use for manual communication. 



## To import a bank setup file



1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Systems**, then select the related link.
1. Create a bank system or open an existing bank system for which you want to import a new setup file.
1. On the bank system page, in the action bar select **Import Setup**.
1. Define how you want to import the file:
   - **Manually**: choose the file location from where the file must be imported
   - **Automatic import**: the file will be imported from Continia Online. The import requires that a **Bank System Code** has been defined on the bank card.



## To create a new bank account

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Account Setup**, then select the related link.
1. In the bank account setup guide, select **Next** to go to the bank account overview.
1. In the bank account overview, select **New Bank Account**. This will open a blank bank account card.
1. Fill in relevant bank account information, such as **Name**, **Bank Branch No.**, **Bank Account No.**, **Country/Region Code**, **SWIFT Code**, and **IBAN**.
1. Select **OK** to close the bank account card, and continue setting up the bank account with the assisted bank account setup. 

## Related information

[About Bank Communication](@PM-158)  
[Onboarding banks with Direct Communication](@PM-183)  
[Setting up Statement Intelligence](@PM-35)



