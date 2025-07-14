---
title: Onboarding Sparebanken Møre
date: 16-01-2024
description: Onboarding Sparebanken Møre with direct communication
id: PM-316
lang: en
---

# Onboarding Sparebanken Møre with Direct Communication

Sparebanken Møre is a Norwegian savings bank, headquartered in Ålesund, Norway. Customers of Sparebanken Møre alliance can use the Payment Management Direct Communication service to send and retrieve bank files between Sparebanken Møre and Microsoft Dynamics 365 Business Central. 

Payment Management uses the digital service Tietoevry to establish the bank integration with the Sparebanken Møre bank, and this article covers the steps to set it up.

{{include "pm- kyc-verification-note"}}

## To set up direct communication

When your request for Sparebanken Møre bank integration has been approved, you can set up your bank accounts to use direct communication.

1. In Business Central, select the icon ![Search for page or report](/images/search_small.png), enter **Bank Account Setup**, and select the related link.

1. Select **Next** to begin the assisted setup.

1. On the **Bank Accounts** page, select an existing Sparebanken Møre bank account, or create a new one by selecting **New Bank Account**.

1. In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

    > [!NOTE]
    >
    > If any bank account information is missing, you may be prompted to verify or update the information.

1. On the **Specify notification email** page, fill in the information needed for the KYC verification and select **Next**. 

1. Now, select the **Establish connection with Tietoevry** link. This directs you to your online bank, where you can sign up for Sparebanken Møre integration.

    > [!IMPORTANT]
    >
    > Make sure you use the same VAT Registration No. as the VAT number you specified on the previous page.

1. Select **Next** to complete the bank account setup. When you return to the bank account overview, you'll see that the bank account status has been updated to Ready. <br>

> [!IMPORTANT]
>
> It can take up to 72 hours after you subscribe to the bank integration and complete the assisted Bank Account Setup before Sparebanken Møre approves the signup and the connection is established at Continia. You can start using direct communication when you receive a confirmation email from Continia.



## To sign up for Sparebanken Møre bank integration

Before you begin setting up direct communication in Payment Management, you must request access to the Sparebanken Møre bank integration.

1. Go to [Nettbedrift - Integrasjon/filoverføring - skjema - Sparebanken Møre (sbm.no)](https://www.sbm.no/bedrift/nettbedrift/nettbedrift---integrasjonfiloverforing---skjema/) 
1. Navigate to **Bestillingen gjelder** and from the **Integrasjon inkludert filoverføring - velg økonomisystem** drop-down box, select Continia Software.
1. Select the **Betalinger**, **Kontoininformasjon**, **Innbetalinger** checkboxes. 
1. Go to the **Sender dere/skal dere sende faktura med KID?** field and select Ja or Nei.
1. Select **Fortsett**.

Sparebanken Møre now verifies the information, and if the request is approved, Sparebanken Møre sends an encrypted email to Continia Software to notify them about the bank integration. The email contains information about the contact person, company name, and VAT number. Payment Management uses the VAT number for the KYC (Know Your Customer) verification when establishing the connection in Business Central.   



## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Payment Management by following the recommended steps as specified in the [Quick guide to setting up Payment Management](@PM-226). 



 

