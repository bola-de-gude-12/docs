---
title: Onboarding Sparebanken Sør
date: 25-03-2025
description: Onboarding Sparebanken Sør with direct communication
id: CB-226
lang: en
---

# Onboarding Sparebanken Sør

Sparebanken Sør is a Norwegian savings bank, headquartered in Kristiansand. Customers of Sparebanken Sør alliance can use Continia Banking to send and retrieve bank files between Sparebanken Sør and Microsoft Dynamics 365 Business Central. 

Continia Banking uses the digital service Tietoevry to establish the bank integration with the Sparebanken Sør bank, and this article covers the steps to set it up.

{{include "cb- kyc-verification-note"}}

## To set up direct communication

When your request for Sparebanken Sør bank integration has been approved, you can set up your bank accounts to use direct communication.

1. In Business Central, select the icon ![Search for page or report](/images/search_small.png), enter **Bank Account Setup**, and select the related link.

1. Click **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing Sparebanken Sør bank account, or create a new one by selecting **New Bank Account**.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

    > [!NOTE]
    >
    > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Specify notification email** page, fill in the information needed for the KYC verification and select **Next**. 

1. Now, select the **Establish connection with Tietoevry** link. This directs you to your online bank, where you can sign up for Sparebanken Sør integration.

    > [!IMPORTANT]
    >
    > Make sure you use the same VAT Registration No. as the VAT number you specified on the previous page.

1. Click **Next** to complete the bank account setup. When you return to the bank account overview, you'll see that the bank account status has been updated to Ready. <br>

> [!IMPORTANT]
>
> It can take up to 72 hours after you subscribe to the bank integration and complete the assisted Bank Account Setup before Sparebanken Sør approves the signup and the connection is established at Continia. You can start using direct communication when you receive a confirmation email from Continia.



## To sign up for Sparebanken Sør bank integration

Before you begin setting up direct communication in Continia Banking, you must request the integration using the integration form.

> [!IMPORTANT] You must be a registered business customer of Sparebanken Sør that uses online banking to request the integration.

To request access:

* Go to [www.sor.no](https://www.sor.no/felles/skjemaer/integrasjon-nettbedrift/) and fill in the [Integration form](https://www.sor.no/felles/skjemaer/integrasjon-nettbedrift/). In the Velg regnskapssystem field, from the drop-down box, select **Other**. In the **Legg til eventuell ekstra informasjon eller ønsker her (valgfritt)** field add *Continia and Business Central*.

  Sparebanken Sør now verifies the information, and if the request is approved, they send an encrypted email to Continia Software to notify them about the bank integration. The email contains information about the contact person, company name, and VAT number. Continia Banking uses the VAT number for the KYC (Know Your Customer) verification when establishing the connection in Business Central.   



## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Continia Banking by following the recommended steps as specified in the [Quick guide to setting up Continia Banking](@CB-03). 





 

