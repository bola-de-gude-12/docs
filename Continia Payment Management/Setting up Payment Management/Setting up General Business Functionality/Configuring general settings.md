---
title: Configuring Payment Management
description: Configure general settings of Payment Management, such as default payment notification setup
date: 30-09-2022
id: PM-2
lang: en
---

# Assisted Setups for Payment Management

> [!IMPORTANT] 
> Before you set up Payment Management, you must ensure that the app has been activated in the company. When you open Business Central for the first time after installing Payment Management, the Role Center will display a notification asking you to activate the app. For more information about activating Payment Management, refer to the articles [Using Continia Solution Management (online)](@PM-8) or [Managing Solutions (on-premises)](@PM-56).

Payment Management includes two mandatory assisted setups that must be completed before you can start using the solution:

- [Bank Account Setup](#to-set-up-bank-accounts)
- [Vendor Payment Setup](#to-set-up-vendor-payment-information)

> [!NOTE]
>
> An assisted setup for Payment Approval is available but not mandatory. For more information, see the article [Setting up Payment Approval Flows](@PM-254). 

## To set up bank accounts

You can use the Bank Account Setup to add bank accounts.

> [!NOTE]
> For more information on how to set up a bank account to use direct communication, navigate to the relevant [onboarding article](@PM-183) for your bank. 

To set up bank accounts using the Bank Account Setup:

1.  Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Account Setup**, then select the related link.

1. In the bank account overview, select a bank account you wish to set up with Payment Management and select **Next**. 

1. Fill in the fields in each step of the guide. Hover over a field to read a short description. 

    After you've set up the bank account, the status in the **Bank accounts** overview will be set to **Ready** if the bank account is ready for use.   

1. Repeat the previous steps to set up additional bank accounts.

> [!TIP]
> You can use the **Status** in the bank account overview to indicate whether the bank account is ready for use. If the status is **Not Ready**, you must select **Next** to start the bank account configuration. 

## To set up vendor payment information

Use the Vendor Payment Setup to replace the payment information on your vendors and vendor templates with Payment Management-supported payment information and to update the payment information on multiple vendors and vendor templates at the same time.

To set up vendor payment information:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Vendor Payment Setup**, then select the related link.

1. Follow the instructions in the guide and validate the payment information you want to update for your vendors.
   > [!TIP]
   > If you want to exclude a vendor from being updated by Payment Management, set a checkmark in the **Exclude** column, this will prevent Payment Management from updating the vendor information.

1. When the setup is completed, in the last step, close the assisted setup guide by selecting **Finish**. This will update your vendors concerning the vendor payment information reviewed in the guide. 

For more information on how to set up vendor payment information, see the article [Setting up Vendor Payment Information](@PM-5).



## Related information

[Using Continia Solution Management](@PM-8)  
[Setting up Direct Communication](@PM-42)  
[Setting up Payment Methods](@PM-4)

