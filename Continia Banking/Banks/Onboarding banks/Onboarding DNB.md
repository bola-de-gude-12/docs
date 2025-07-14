---
title: Onboarding DNB in Continia Banking
date: 26-03-2025
description: Onboarding DNB with direct communication in Continia Banking.
id: CB-221 
lang: en
---

# Onboarding DNB

As a customer of DNB, you can use the corporate internet bank, DNB Connect, to send and receive bank files automatically between DNB and Microsoft Dynamics 365 Business Central using Continia Banking.

This article covers the steps to set up direct communication between DNB Connect and Continia Banking.  


## To set up direct communication

To add bank accounts to an *existing* DNB agreement:

1. Open the DNB bank card in Continia Banking and on the action bar, select **Actions** > **Authentication Keys**. 

2. On the **Authentication Entries** page, select **Related** > **Related Companies**. 

3. Now you can share DNB access with different companies. 

   >  [!IMPORTANT]
   >
   > To share access with a new company, you **must** be in a company that already has access.



To set up your DNB bank account in Continia Banking: 

1. Search ({{search}}) for and select **Bank Account Setup**.

1. Click **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing DNB bank account, or create a new one by selecting **New Bank Account**.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

    >  [!NOTE]
    >
    > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Specify notification email** page, enter the following information:

    * **Contact Email** - the email address that Continia Software should use to notify you that the connection to DNB has been established. 
    * Company Name
    * VAT Registration No.

1. On the **Establish the connection to DNB** page, depending on whether you are setting up a Norwegian DNB bank account, you must do the following:

   - If you're a Norwegian DNB customer, select **Start DNB signup flow**. Use your DNB Connect credentials to sign in to the DNB corporate internet bank and sign up for DNB direct communication. 

     When you've completed the signup flow, return to the assisted Bank Account Setup guide and select **Next**. 
     
     >[!IMPORTANT]
     >
     >If you have multiple companies using DNB bank accounts, in the DNB signup flow, you must select all the bank accounts you want to integrate via the DNB Corporate Internet bank, even though you are now only configuring Continia Banking for one company. If you rerun this digital signup flow for just one bank account, you will overwrite any settings you had before. 
     
   - If you're a DNB customer outside Norway, you must request to use direct communication with your bank manually. Contact the Cash Management adviser at your bank and request an application form and the relevant bank files. Note that you can continue setting up your bank accounts in Continia Banking even before DNB approves your request. Select **Next**.  

1. When you return to the overview of bank accounts, you will see that the bank status is updated to Ready. Even though the status is Ready, you can't use direct communication before you have received a confirmation email from Continia Software and finalized the setup as described below.

    > [!NOTE]
    >
    > It can take up to two days before DNB approves the signup and the connection is established at Continia Banking. 

## To finalize the setup in Continia Banking

You can finalize the setup when your signup for DNB Connect has been approved and you have received the two email messages: 

   - An email from DNB with the relevant information needed to complete the setup.
   - An email from Continia Software stating that your onboarding signup has been approved.  

To complete the setup on the bank card:

1. Select the {{search}} icon, enter **Bank**, and then select the related link.

1. Open the relevant DNB bank card.

1. Log in to the DNB corporate internet bank, go to **Administration and Division**, and assign the necessary permissions to the relevant users of the division you specified in the previous step.
   

You have now completed the setup, and when you receive the bank files from DNB, you are ready to start using Continia Banking Direct Communication. 

## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Continia Banking by following the recommended steps as specified in the [Quick guide to setting up Continia Banking](@CB-03). 
