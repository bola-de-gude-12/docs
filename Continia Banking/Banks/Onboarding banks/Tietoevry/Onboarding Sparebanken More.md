---
title: Onboarding Sparebanken Møre in Continia Banking
date: 25-03-2025
id: CB-225
lang: en
description: Onboarding Sparebanken Møre with direct communication in Continia Banking.
---

# Onboarding Sparebanken Møre

Sparebanken Møre is a Norwegian savings bank, headquartered in Ålesund, Norway. Customers of Sparebanken Møre alliance can use Continia Banking to send and retrieve bank files between Sparebanken Møre and Microsoft Dynamics 365 Business Central.

Continia Banking uses the digital service Tietoevry to establish the bank integration with the Sparebanken Møre bank, and this article covers the steps to set it up.

\{{include "cb- kyc-verification-note"\}}

## To set up direct communication

When your request for Sparebanken Møre bank integration has been approved, you can set up your bank accounts to use direct communication.

1. In Business Central, select the icon ![Search for page or report](../../../../images/search_small.png), enter **Bank Account Setup**, and select the related link.
2. Click **Next** to begin the assisted setup.
3. On the **Bank Accounts** page, select an existing Sparebanken Møre bank account, or create a new one by selecting **New Bank Account**.
4.  In the **Communication** column, ensure that **Direct Communication** is selected for the bank account, and then select **Next**.

    > \[!NOTE]
    >
    > If any bank account information is missing, you may be prompted to verify or update the information.
5. On the **Specify notification email** page, fill in the information needed for the KYC verification and select **Next**.
6.  Now, select the **Establish connection with Tietoevry** link. This directs you to your online bank, where you can sign up for Sparebanken Møre integration.

    > \[!IMPORTANT]
    >
    > Make sure you use the same VAT Registration No. as the VAT number you specified on the previous page.
7. Click **Next** to complete the bank account setup. When you return to the bank account overview, you'll see that the bank account status has been updated to Ready.\


> \[!IMPORTANT]
>
> It can take up to 72 hours after you subscribe to the bank integration and complete the assisted Bank Account Setup before Sparebanken Møre approves the signup and the connection is established at Continia. You can start using direct communication when you receive a confirmation email from Continia.

## To sign up for Sparebanken Møre bank integration

Before you begin setting up direct communication in Continia Banking, you must request access to the Sparebanken Møre bank integration.

1. Go to [Nettbedrift - Integrasjon/filoverføring - skjema - Sparebanken Møre (sbm.no)](https://www.sbm.no/bedrift/nettbedrift/nettbedrift---integrasjonfiloverforing---skjema/)
2. Navigate to **Bestillingen gjelder** and from the **Integrasjon inkludert filoverføring - velg økonomisystem** drop-down box, select Continia Software.
3. Select the **Betalinger**, **Kontoininformasjon**, **Innbetalinger** checkboxes.
4. Go to the **Sender dere/skal dere sende faktura med KID?** field and select Ja or Nei.
5. Select **Fortsett**.

Sparebanken Møre now verifies the information, and if the request is approved, Sparebanken Møre sends an encrypted email to Continia Software to notify them about the bank integration. The email contains information about the contact person, company name, and VAT number. Continia Banking uses the VAT number for the KYC (Know Your Customer) verification when establishing the connection in Business Central.

## Recommended next steps

When you have set up your bank accounts to use direct communication, you can continue the setup of Continia Banking by following the recommended steps as specified in the [Quick guide to setting up Continia Banking](../../../../Continia%20Banking/Banks/Onboarding%20banks/Tietoevry/@CB-03/).
