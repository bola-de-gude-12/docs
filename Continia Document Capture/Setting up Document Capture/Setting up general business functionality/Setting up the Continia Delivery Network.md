---
title: Setting up the Continia Delivery Network
date: 12-03-2025
id: DC-75
lang: en
description: Details on how to set up the Continia Delivery Network.
---

# Setting up the Continia Delivery Network

Before you can start using the Continia Delivery Network, you must be onboarded by Continia. Currently, you can onboard to the [Peppol eDelivery Network](<Setting up the Continia Delivery Network.md#onboarding-to-the-peppol-edelivery-network>) and/or to the [NemHandel network](<Setting up the Continia Delivery Network.md#onboarding-to-nemhandel-only-for-danish-organizations>) (only for Danish organizations), as described below.

> \[!NOTE] The Continia Delivery Network isn't available in sandbox environments.

## To onboard

To connect with the NemHandel and/or Peppol networks:

1. Open the assisted setup guide for onboarding by doing one of the following:
   * Choose the \{{search\}} icon, enter **Continia Delivery Network Onboarding**, and then choose the related link.
   * Choose the \{{search\}} icon, enter **Continia Delivery Network Participations**, and then choose the related link. On the action bar, click **New** and then **Create new participation**.
2. The **Continia Delivery Network Onboarding** assisted setup guide opens. Select **Next**.
3. Enable one or more networks, depending on your needs (e.g.: if you're only conducting business in Denmark, enable **NemHandel**). Then, select **Next**.
4.  Fill out all fields as required. Some of the fields may be prefilled based on your Microsoft Dynamics 365 Business Central company details, but you can enter new details if necessary.\


    | **Field**            | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                              |
    | -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
    | Identifier Type ID   | The type of identifier. If you don't know the company's identifier, search for it in the [NemHandelsregistret](https://registration.nemhandel.dk/NemHandelRegisterWeb/) (only for NemHandel) or in the [Peppol Directory](https://docs.peppol.eu/edelivery/codelists/) under Participant Identifier Schemes (only for Peppol). For more information, see [Identifier types](<Setting up the Continia Delivery Network.md#identifier-types>). |
    | Identifier Value     | The value of the identifier. This is the name under which the company is registered, and how others can find it on the Peppol network. E.g.: DK77777777.                                                                                                                                                                                                                                                                                     |
    | Company Name         | The name of the company. E.g.: CRONUS UK Ltd.                                                                                                                                                                                                                                                                                                                                                                                                |
    | VAT Registration No. | The local registration code that identifies the company. E.g.: VAT, DK:CVR, NO:ORG, SE:ORG, etc.                                                                                                                                                                                                                                                                                                                                             |
    | Address              | The address of the company.                                                                                                                                                                                                                                                                                                                                                                                                                  |
    | Post Code            | The postal code of the company.                                                                                                                                                                                                                                                                                                                                                                                                              |
    | Country/Region Code  | The code of the country or region where the company is based. E.g.: GB.                                                                                                                                                                                                                                                                                                                                                                      |
    | Your Name            | The name of the person authorized to sign and set up the Continia Delivery Network for the company, such as a partner or consultant.                                                                                                                                                                                                                                                                                                         |
    | Contact Name         | The name of the point of contact at the company.                                                                                                                                                                                                                                                                                                                                                                                             |
    | Contact Phone No.    | The phone number of the point of contact at the company.                                                                                                                                                                                                                                                                                                                                                                                     |
    | Contact Email        | The email address of the point of contact at the company. Note that if the domain of this email address doesn’t match the **Company Name**, additional questions are asked to verify the connection between the two. E.g.: Entering CRONUS UK Ltd. under **Company Name** and user@contoso.com under **Contact Email** triggers this check.                                                                                                  |
5. If you want other people and organizations to be able to find you and see that you're part of the network, enable the **Publish in Registry** toggle.
6.  Under **Please select the profiles you want to be registered with**, add your preferred profile(s). A profile is a type of document that you want to be able to send and/or receive. You can configure multiple profiles, either individually or in groups.

    > \[!NOTE] In the **Profile Direction** column, you can choose the direction of each profile, that is, whether you want to be able to send and/or receive this particular type of document. If you select **Inbound** or **Both**, you must enter a Document Capture category in the **Document Category** column, so the Continia Delivery Network knows what category to import incoming documents into for this profile.
7. Select **Next** > **Finish** to join the Continia Delivery Network.

Your onboarding registration has to be approved manually by Continia before you've officially joined the network. This can take 2-4 days and may require you to provide more information in order for Continia to be able to validate your details.

## The list of participations

When you've completed the **Continia Delivery Network Onboarding** assisted setup guide as described above, you've created what's known as a participation. A participation is basically any organization or legal entity that has joined – or requested to join – the Continia Delivery Network and is now registered as such. The participation is also what enables that organization or legal entity to send and receive documents using the Continia Delivery Network.

Two of the fields you fill out when completing the assisted setup guide for onboarding are used to uniquely identify each participation: **Identifier Type ID** and **Identifier Value**. This means that although you can create multiple participations (for example one for each legal entity within an organization), you can't create two or more participations with the same pair of identifier ID and identifier value. The identifier ID and its corresponding value are unique to the participation they were used to create, and they can therefore only be used once.

> \[!NOTE] It’s possible to use the same GLN on Peppol and NemHandel.

> \[!IMPORTANT] If you've previously joined the Peppol or NemHandel networks via a service provider other than Continia, you must unregister with that service provider in order to be able to join the Continia Delivery Network. If this is the case for you, please contact [your dedicated Continia partner](../../../Continia%20Document%20Capture/Setting%20up%20Document%20Capture/Setting%20up%20general%20business%20functionality/@DC-15/) for assistance.

All the participations you create are added to the list of participations. To open this list, choose the \{{search\}} icon, enter **Continia Delivery Network Participations**, and then choose the related link. The list provides an overview of your participations and their respective statuses:

* Pending approval - all newly created participations get this status immediately upon creation and keep it until they've been manually approved by Continia.
* Connected - this is the status given to all participations that have been approved by Continia. With this status, you can send/receive documents via the Continia Delivery Network.
* Rejected - participations that Continia has been unable to approve are marked as rejected, typically accompanied by a note on the cause of the rejection.

Submitting incorrect information under the **Identifier Type ID** and **Identifier Value** fields results in the immediate rejection of the onboarding request. However, if your participation is rejected you can edit and resubmit it directly from the participations list.

## Identifier types

### NemHandel

These are the identifier types available in the NemHandel network.

| **Identifier** | **Description**                                                                                                |
| -------------- | -------------------------------------------------------------------------------------------------------------- |
| DK:CVR         | Det Centrale Virksomhedsregister (Central Business Register), used by businesses in Denmark.                   |
| GLN            | Global location number, used internationally to identify physical locations, legal entities, or other parties. |

### Peppol

These are some of the most common identifier types in the Peppol network.

| Identifier | Description                                                                                                    |
| ---------- | -------------------------------------------------------------------------------------------------------------- |
| BE:EN/VAT  | Belgian VAT number for businesses.                                                                             |
| DE:VAT     | German VAT number for businesses.                                                                              |
| DK:DIGST   | Danish digital government services identifier.                                                                 |
| FI:OVT2    | Finnish VAT identifier for businesses.                                                                         |
| GLN        | Global location number. Used internationally to identify physical locations, legal entities, or other parties. |
| NL:VAT     | Dutch VAT number for businesses.                                                                               |
| NO:ORG     | Organisasjonsnummer (Norwegian organization number).                                                           |
| SE:ORGNR   | Organisationsnummer (Swedish organization number).                                                             |

## Related information

[Finding a Reseller of Continia Document Capture](../../../Continia%20Document%20Capture/Setting%20up%20Document%20Capture/Setting%20up%20general%20business%20functionality/@DC-15/)
