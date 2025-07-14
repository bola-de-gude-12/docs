---
title: Document Output Setting up the Continia Delivery Network
date: 4-7-2023
description: Details on how to set up the Continia Delivery Network
id: 
lang: en
---

# Setting up the Continia Delivery Network

Continia must onboard all users of the Continia Delivery Network (CDN) before they can start using the system. To make sure you are fully prepared to connect to CDN and begin using its features, please consult the [Preparing for electronic invoicing using Continia Delivery Network](@DO-94) article.

## To run the Continia Delivery Network Onboarding wizard

To set up the Continia Delivery Network:

1. To open the assisted setup guide for onboarding, do one of the following:
   * Select the {{search}} icon, enter **Continia Delivery Network Onboarding**, and then select the related link.
   * Select the {{search}} icon, enter **Continia Delivery Network Participations**, and then select the related link. In the action bar, select **New** and then **Create new participation**.
1. The **Continia Delivery Network Onboarding** assisted setup guide opens. Select **Next**.
1. Fill in all fields as required. Some fields may be prefilled based on your Microsoft Dynamics 365 Business Central company details, but you can enter new details if necessary.
1. If you want other people and organizations to be able to find you in the [Peppol Directory](https://directory.peppol.eu/public) and to see that you're part of the Peppol network, enable the **Publish in Registry** toggle.
1. Under **Please select the profiles you want registered with**, add your preferred profile(s). In this context, a profile is a type of document that you want to be able to send/receive. You can add multiple profiles, and they can be added either individually or in groups. Note that the **PEPPOL BIS3.0** profile is mandatory for all participations.
   > [!NOTE]
   > In the **Profile Direction** column, you can choose the direction of each profile, i.e., whether you want to be able to send and receive this particular type of document. Choose the Output profile you wish to use supported in your country. See a list of supported document formats by country [here](@DO-57).
1. Select **Next** > **Finish** joining the Continia Delivery Network.

Your onboarding registration will have to be approved manually by Continia before you've officially joined the network. This can take up to two days and may require you to provide more information for Continia to validate your details.

## The registration process

After you registered for the Continia Delivery Network in Business Central, the process is as follows:

1. **ID validation** - Continia Software must perform a formal organization ID validation, matching the organization ID and A/D domain with the public company registration. This validation process can require a need for documents sent to Continia, confirming a company registration, or other kind of validation documents if information can’t be retrieved through official webpage lookups. A supporter from Continia Software will ask for this if needed.

2. **Contact person acknowledgment** - to acknowledge the registration on behalf of the organization of the end user, an email is sent to the assigned contact person. Responding to this email using the Vote menu or simply replying with "I Agree" in the text is a formal acknowledgment. This step validates to Continia that a legitimate representative of the organization confirmed the registration's intent. By conducting this validation, we ensure the prevention of unauthorized access by individuals with fraudulent intentions, safeguarding the integrity of the Peppol eDelivery Network and protecting companies from unauthorized representation.

3. **Registration** - Continia will conduct the technical registration to the global eDelivery Network. The time required to complete the technical registration may vary depending on the chosen framework, ranging from as little as one hour to a maximum of two days.

4. **Connected** - Continia will approve the onboarding, and the participation in Business Central will switch to “Connected”, after which Delivery Network will be ready for use.

## To view the registration process status

To monitor the status of the registration process:

* Select the {{search}} icon, enter **Continia Delivery Network Participations**, and then select the related link. This page will show you the progress of your registrations and provides the Participation Identifier. This identifier is important for the eDelivery Network to accept file transfers or for your vendors to send Peppol XML to you.

  The different statuses and their meaning:

  * **Yellow** - the registration is pending and being validated. 
  * **Red** - the registration has been rejected.
  * **Green** - the registration has been approved and is ready to be selected in the Continia Delivery Network section of the [e-document setup](#to-attach-the-participation-id-to-the-e-document-setup) for PEPPOL BIS3. 

## To attach the Participation ID to the e-document setup

When you've completed the **Continia Delivery Network Onboarding** assisted setup guide, you've created what's known as participation. Participation is any organization or legal entity that has joined – or requested to join – the Continia Delivery Network and is now registered.

Two of the fields you fill in when completing the assisted setup guide for onboarding are used to identify each participation: 

* **Identifier Type ID** - for example, DK:DIGST
* **Identifier Value** - for example, DK12345678

This means that although you can create multiple participations (for example, one for each legal entity within an organization), you can't create two or more participations using the same identifier ID and identifier value.

> [!IMPORTANT]
> If you've previously joined the PEPPOL network via another service provider than Continia, you must unregister with that service provider to join the Continia Delivery Network. If so, please contact your dedicated Continia partner for assistance.

Once you have finished registering for participation, you must add the Participation ID to the e-document set up to send documents.

To attach the Participation ID to the e-document setup:

1. Select the {{search}} icon, enter **e-document setup**, and then select the related link.
2. In the **General** section, the **Code** field automatically states PEPPOL BIS3 for a standard installation. 
3. If the [registration is approved](#to-view-the-registration-process-status), in the **Participation field**, select the ID to enable the automatic transmission to Continia Delivery Network.

## Editing or deleting a participation

You may want to edit a participation when you have changed providers or recipients and need to update the associated data. Similarly, you can delete a participation if it is no longer required or needs adjustments for accuracy and efficiency. 

To edit or delete a Participation: 

1. Go to **Continia Delivery Network Participations**. 
2. Select the line of the participation you wish to modify and on the action bar, select **Edit** or **Delete** to make the necessary changes. 

