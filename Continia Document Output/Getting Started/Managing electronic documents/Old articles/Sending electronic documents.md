---
title: Sending Electronic Documents
date: 27-04-2023
description: 
id: DO-86
lang: en
---

# Sending Electronic Documents

Sending electronic documents can mean many things depending on which document types you refer to. You could argue that an email with a PDF attachment is more electronic than printing, enveloping or emailing, but when invoicing we can take it a step further by using a defined XML format and sending this encrypted through a common network. Electronic invoicing is limited to the document types invoices and credit memos.

Though electronic invoicing formats are named individually from one country to another, they are in many cases based on the internationally agreed Peppol BIS format, and can be distributed via the international eDelivery Network hosted by the Open Peppol organization. Continia Software is part of the Open Peppol community, and the Continia Delivery Network is Continia's service access point to connect to the Peppol network.

The following table lists the countries and electronic invoicing format name, marks if this format can be transmitted through Continia Delivery Network (indirectly indicating if this format is also based on Peppol), and also if there are other invoicing standard in the mentioned country supported by Document Output (outgoing) or Document Capture (ingoing).

| Country         | E-invoicing format                     | CDN supported | Comments                                                     | Other invoicing fomats                                       |
| --------------- | -------------------------------------- | ------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Australia       | Peppol BIS3 Billing                    | Yes1          | Officially the electronic  invoicing format in Australia     |                                                              |
| Austria         |                                        |               | Peppol BIS3 is only one of more  supported formats in Austria |                                                              |
| Belgium         | Peppol BIS3 Billing                    | Yes           | All BE companies are registered as  Peppol receivers in the BOSA registry, but can be re-routed through Continia  Delivery Network | FACTUR-X: A PDF-A standard with an  embedded Cross Industry XML (must be emailed) |
| Denmark         | Peppol (BIS3 Billing)  OIOUBL (UBL2.1) | Yes  Yes      | Denmark has a legacy format and network  called NemHandel for transmitting OIOUBL. This can be onboarded separately in  Continia Delivery Network, enabling support of both document types in one  solution | OIOUTS: This is a Cross Industry  format used mainly by the supply chain and telecom industry. It can only be  attached to a OIOUBL Invoiced and sent internally in companies connected to  the Danish NemHandel Network. Document Output can connect to NemHandel  network through Delivery Network, but Document Output can’t create the OIOUTS  specification XML |
| United Kingdom  | Peppol BIS3 Billing                    | Yes           | There is no requirement for Peppol  in the UK, but the NHS has implemented the ability to receive the files. |                                                              |
| Finland         | Peppol BIS3 Billing                    | Yes           | There are 3 different electronic  invoicing standards in Finland. Document Output only supports Peppol, and the  receiver must also be connected to a Peppol Access Point to receive the  Peppol XML files | Finvoice and TEAPPSXML are other  electronic invoicing formats, but these are not supported in Document Output,  and files can’t be handled by Delivery Network |
| France          | Peppol BIS3 Billing                    | Yes           | No requirement by law in France  yet, but work is in progress | FACTUR-X: A PDF-A standard with an  embedded Cross Industry XML (must be emailed) |
| Germany         | XRECHNUNG 2.0 (Peppol BIS3  Billing)   | Yes           | No requirement by law, but format  is supported by all government entities. The XRECHNUNG is a German Peppol  variant | ZUGFeRD: A PDF-A standard with an  embedded Cross Industry XML (must be emailed) |
| Ireland         | Peppol BIS3 Billing                    | Yes           | No requirement by law, but  delivery method has been decided in Ireland |                                                              |
| Luxemburg       | Peppol BIS3 Billing                    | Yes           |                                                              |                                                              |
| Netherlands     | Peppol BIS3 Billing                    | Yes1          | No requirement by law, but format  is being adopted by businesses and public authorities. |                                                              |
| New Zealand     | Peppol BIS3 Billing                    | Yes1          | Officially the electronic  invoicing format in New Zealand   |                                                              |
| Norway          | EHF 3.0 (Peppol BIS3 Billing)          | Yes           | EHF is the Norwegian localization  of Peppol. B2B and B2G must use the EHF format for electronic invoicing.  Registration in Peppol requires an update in ELMA network also, but this is  handled by Continia during registration to Delivery Network. | Legacy formats EHF 2.0 is now  obsolete. Norway has an eFaktura XML format for B2C customer invoicing. This  format is NOT supported in Document Output. |
| Poland          | Peppol BIS3 Billing                    | Yes           | Accepted by B2G and in process for  B2B                      |                                                              |
| Sweden          | SweFaktura 2.0 (Peppol BIS3  Billing)  | Yes           | Formally the country standard for  B2G and being adopted to B2B | Legacy format was also called  SveFaktura 1.0. This format is not supported by Document Output |
| Other countries |                                        | Yes2          | Companies from countries which do  not have rules about Peppol, can also send Peppol BIS3 Billing if the  receiver is also attached to a Peppol Access Point. If used the standard  Peppol invoicing format is used. As of 2023 the standard format is still Peppol  BIS3 Billing, but this will be replaced by the Peppol PINT variant soon. |                                                              |

 1Special rules apply to onboard customers from this country. Continia Delivery Network should open for this during 2023

## The Advantage of using Continia Delivery Network as transport layer

It is possible to use Document Output to create a Peppol XML file, and send it towards other Peppol Access Points rather than Continia Delivery Network. If using another operator for transmission you need to export the XML files to an Export folder, and have the file collection by a component or service connecting to the other operator.

By using Continia Delivery Network, you enable direct communication between Business Central and the Delivery Network through Web Service features, and the transaction of the XML is encrypted from the second it’s generated with no opportunity to be accessed or tampered with during the sending process. If your Business Central is a cloud solution, you will not need to work on a solution enabling local resources to export the XML file to, and no installation of local component to connect to other operators. This is an advantage as you will then have Continia as your single supplier with the responsibility for the XML generation and transport of your electronic invoices.

## Prepare for Continia Delivery Network/considerations

If a company is not already registered in a Peppol Access Point else using the same Identifier as intended for Delivery Network, a registration validation process is normally completed within approx. 2 working days. If already registered with another Access Point Provider, Continia Software can’t request to created a new Identifier in the Peppol eDelivery Network until this has been released by the other operator. The responsibility of the de-registration with another operator lies with the company owning the registration id. 

A registration can be prepared and scheduled for a specific target data (on a working day), meaning that Continia can complete the registration validation and await the technical registration. This is convenient to plan the shift to Delivery Network on a specific date. The technical registration can be completed within aprox. an hour.

## The Onboarding Process

You start the Onboarding to Delivery Network in Business Central in the wizard **Continia Delivery Network Onboarding**. This will start a Form containing the data needed to complete the registration smoothly. Please be special aware that the **Identifier Type ID** matches an ID from your country, and select a value (e.g. VAT) matching the Identifier Value you want to register with. [This table](#_Preferred_Identifier_Types) shows out preferred identifier value and format in the countries we have successfully registered users in. 

The onboarding validation process consists of 4 steps. 

1. Continia Software must perform a formal organization ID validation, matching organization ID and A/D domain with the public company registration.

a.    This validation process can require a need for documents sent to Continia, confirming a company registration or other kind of validation documents, if information can’t be retrieved through official webpage lookups. A supporter from Continia Software will ask for this, if needed.

2. An email is send to the contact person of the company requesting to be registered in Continia Delivery Network. A response to this email using the Vote menu, or simply replying “I Agree” in text, indicates a formal acknowledgement that registration is carried out on behalf of the organization of the End User.

a.    This process validates to Continia, that an actual person, representing the organization validated in step 1, is acknowledging that this registration is intended. By performing this visual and email validation, we are able to ensure that no one with fraudulent intentions are allowed into the Peppol eDelivery Network and acting on behalf of a company they shouldn’t 

3. Continia will carry out registration on the global eDelivery Network.
4. Continia will approve the onboarding, and the participation in Business Central will switch to “Connected”, after which Delivery Network will be ready for use.

## Enabling Delivery Network in Document Output

You can monitor the status of the registration process in Business Central page called **Continia Delivery Network Participations**. This Page will display any registration in progress including the Participation Identifier, which is the value which must be know by the eDelivery Network for it to accept files to be transferred, or the ID your Vendors need to know if they can send Peppol XML to you. The status of the registration can be Yellow **Pending Approval**, meaning that the Onboarding validation process is in progress. When the Onboarding agent at Continia Software rejects or approves the registration, this is automatically updated in the Registration Status field on this page. 

When a Participation has been Approved, it can be selected in the field **Participation** in the Continia Delivery Network section of the e-document Setup covering PeppolBIS3. This filed should be set automatically upon an approved registration.

## The cost of Delivery Network

There is no cost or transaction fee related to Delivery Network. The only requirement is the purchase of Document Output or Document Capture from Continia Software, and you are ready to get onboarded to the service. In Business Central as a cloud solution, the required add on module XML Export, is included with the Essentials module as no cost. In an OnPremise installation you need also to purchase XML Export as an Add-on module. XML documents are charged at the same rate as sending an email using Document Output. This rate applies regardless if documents are sent through Delivery Network or another operator. Please look into the Price sheet for the current transaction rates.

### Preferred Identifier Types

| **Country** | **Identifier Type ID** | **Example** |
| ----------- | ---------------------- | ----------- |
| DK          | DK:DIGST               | DK12345678  |
|             |                        |             |

 
