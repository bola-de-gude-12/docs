---
title: Onboarding DNB
date: 17-01-2024
description: Onboarding DNB with direct communication
id: PM-249  
lang: en
---

# Onboarding DNB with Direct Communication

As a customer of DNB, you can use the corporate internet bank, DNB Connect, to send and receive bank files automatically between DNB and Microsoft Dynamics 365 Business Central using the Payment Management Direct Communication service. 

This article covers the steps to set up direct communication between DNB Connect and Payment Management.  

> [!NOTE] 
>
> To add bank accounts to an *existing* DNB agreement, open the DNB bank card in Payment Management and select **Connection** > **DNB Signup**.




## To set up direct communication


To set up your DNB bank account in Payment Management: 

1. In Business Central, select the icon ![Search for page or report](/images/search_small.png), enter **Bank Account Setup**, and select the related link.

1. Select **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing bank account, or create a new one by selecting **New Bank Account**.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

    >  [!NOTE]
    >
    > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Specify notification email** page, enter the email address that Continia Software should use to notify you that the connection to DNB has been established. 

1. On the **Establish the connection to DNB** page, depending on whether you are setting up a Norwegian DNB bank account, you must do the following:

   - If you're a Norwegian DNB customer, select **Start DNB signup flow**. Use your DNB Connect credentials to sign in to the DNB corporate internet bank and sign up for DNB direct communication. For an overview of the supported bank files, see the article [DNB](@PM-122). 

     When you've completed the signup flow, return to the assisted Bank Account Setup guide and select **Next**. 
     
     >[!IMPORTANT]
     >
     >If you have multiple companies using DNB bank accounts, in the DNB signup flow, you must select all the bank accounts you want to integrate via the DNB Corporate Internet bank, even though you are now only configuring Payment Management for one company. If you rerun this digital signup flow for just one bank account, you will overwrite any settings you had before. 
     
   - If you're a DNB customer outside Norway, you must request to use direct communication with your bank manually. Contact the Cash Management adviser at your bank and request an application form and the [relevant bank files](@PM-122). Note that you can continue setting up your bank accounts in Payment Management even before DNB approves your request. Select **Next**.  

1. When you return to the overview of bank accounts, you will see that the bank status is updated to Ready. Even though the status is Ready, you can't use direct communication before you have received a confirmation email from Continia Software and finalized the setup as described below.

    > [!NOTE]
    >
    > It can take up to two days before DNB approves the signup and the connection is established at Continia Payment Management. 

## To finalize the setup in Payment Management

You can finalize the setup when your signup to DNB Connect has been approved and you have received the two email messages: 

   - An email from DNB with the relevant information needed to complete the setup.
   - An email from Continia Software states that your onboarding signup has been approved.  

To complete the setup on the bank card:

1. Select the icon ![Search for page or report](/images/search_small.png), enter **Bank**, and then select the related link.

1. Open the relevant DNB bank card.

1. On the bank card, navigate to the **Communication Agreement** FastTab and enter the information you received from DNB in the following fields:
   
   - **Kundenummer** (Customer number) - enter the customer number listed in the confirmation email. The customer number must be 11 digits, so make sure to add '00' in front of the 9-digit Kundenummer.
   - **Divisjonsnummer** (Division number) - enter the division number listed in the confirmation email. The division number must be three digits, so make sure to add '00' in front of the number if it exists of one number only.
   
1. Log in to DNB corporate internet bank, go to **Administration and Division**, and assign the needed permissions to the relevant users of the division you specified in the previous step.

You have now completed the setup, and when you receive the bank files from DNB, you are ready to start using Payment Management Direct Communication. 



## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Payment Management by following the recommended steps as specified in the [Quick guide to setting up Payment Management](@PM-226). 
