---
title: Preparing to set up electronic invoicing using CDN
date: 03-07-2023
description:  
id: DO-94 
lang: en
---

# Preparing for electronic invoicing using Continia Delivery Network

The Continia Delivery Network (CDN) integrates with the Peppol eDelivery Network, enabling electronic invoicing directly from Microsoft Dynamics 365 Business Central. It ensures secure communication and eliminates the need for third-party vendors. 

Before you proceed with setting up a CDN, it's important to consider a few essential aspects and make the necessary preparations:

To prepare the setup of Peppol and CDN, make sure to:

* **Register at one access point provider only** - if already registered with another Access Point Provider, Continia Software can’t request to create a new identifier in the Peppol eDelivery Network until this has been released by the other operator. The responsibility of the de-registration with another operator lies with the company owning the registration ID. Make sure to communicate when the deregistering process is done so that Continia can activate the CDN connection.
  
  If a company is not already registered in a different Peppol Access Point, the registration validation process takes up to 2 working days. 
  
* **Use the correct ID format** - determine the ID format your company must be registered with. For example, in Denmark, you use the CVR or the EAN number, and in Sweden, you use the ORG number. Navigate to the country in the [Electronic invoicing with Document Output](Overview.md) article to see the specification.

  >[!NOTE] 
  >
  >Although Continia can work with the CVR number, for Danish organizations, we recommend using the EAN because it's the most commonly used format. 

* **Register as a sender, receiver, or both** - determine what to enable. 

* **Enter the preferred activation date** - the registration can be prepared and scheduled for specific target data (on a working day), meaning that Continia can complete the registration validation and await the technical registration. Please communicate your preferred day of activation in the reply to the terms and conditions email (see the next bullet). This is convenient to plan the shift to Delivery Network on a specific date. The time required to complete the technical registration may vary depending on the chosen framework, ranging from as little as one hour to a maximum of two days.

* **Assign a contact person** - add the email address of the main contact. This contact must be someone within the registering company and not a partner. Continia requires this information to validate the registering company and will use the email address to send the terms and conditions. If you have a preferred activation date, please provide it in your reply to the terms and conditions email.


If you prepared all steps, go to Business Central, and run the [Continia Delivery Network Onboarding wizard](@DO-12) for a smooth setup. 

