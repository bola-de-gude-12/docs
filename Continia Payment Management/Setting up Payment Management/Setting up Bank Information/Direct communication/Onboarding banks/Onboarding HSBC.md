---
title: Onboarding HSBC
date: 26-02-2024
description: Onboarding HSBC with direct communication
id: PM-383  
lang: en
---

# Onboarding HSBC with Direct Communication

As a customer of HSBC, you can send and receive bank files automatically between HSBC and Microsoft Dynamics 365 Business Central using the Payment Management Direct Communication service. 

This article covers the steps to set up direct communication between HSBC Connect and Payment Management.  


## To set up direct communication


To set up your HSBC bank account in Payment Management: 

1. Use the {{search}} icon, enter Set up Bank Accounts, and select the related link.

1. Create your HSBC bank account and enter your HSBC IBAN.

1. Select **Next** and start the signup process. Download the public key.

1. Exit the signup process. 

1. Use the {{search}} icon, enter **Banks**, and open the HSBC bank card. 

1. On the bank card, on the action menu select **Connection** > **Export Public Key** and download the Continia Public key. 

1. Exit the Assisted Setup once the Continia Public key is downloaded.

1. Send the exported public key and your contact information (Name, Email, and Phone Number) to your HSBC contact, typically the Client Integration Manager. This step occurs outside of Business Central.

    After completing this step, HSBC will send you emails that contain the following information:

    - Profile ID
    - Client ID
    - HSBC public key
    - Client Secret 


## To finalize the setup in Payment Management

To complete the setup process after your HSBC Connect signup has been approved, follow these steps:

1. Upon receiving the necessary information mentioned earlier, proceed to the next stage of the assisted setup. Open the assisted setup for bank accounts and select the HSBC bank account previously chosen.
1. Input and import the information provided by HSBC into the respective fields. The status of the bank account should now be updated to *Ready*.
1. Test whether the Payment Management system has successfully connected with HSBC by initiating a payment through the payment journal or importing a bank statement via bank account reconciliation.




## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Payment Management by following the steps specified in the [Quick Guide to setting up Payment Management](@PM-226). 
