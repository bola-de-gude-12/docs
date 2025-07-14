---
title: Frequently Asked Questions Continia Delivery Network
date: 21-06-2024
description: Frequently asked questions about Continia Delivery Network
id: DO-104
lang: en
---

# Continia Delivery Network FAQ
In this section, you can find answers to some of the most frequently asked questions about Continia Delivery Network. The answers provide information on subjects such as testing the Continia Delivery Network and how to solve a gateway error code.

## Can I test sending electronic documents through the Continia Delivery Network?
Due to regulations and the fact that the Continia Delivery Network is a live system, it is not permitted to send test documents. 

What you can do, though, is to post an invoice and set up your Output Profile in a way that allows you to either send the XML document as an attachment to an email, or you can download the XML file. The XML file in the email attachment/downloaded file and the XML file that would be sent through the Continia Delivery Network is, for all practical intents and purposes, the same. 

If you need to test sending out an electronic sales invoice with a specific protocol such as Peppol or OIOUBL, then you do that by modifying a codeunit.

Follow these steps: 

1. Open e-document setup 
2. Choose the protocol you want to test, for example Peppol 
3. Under the submenu Salesinvoice, remove the codeunit from salesinvoice delivery 

## How can I test my Continia Delivery Network connection in a sandbox environment?
Note that due to regulations and due to the fact that the Continia Delivery Network is a live system, it is not permitted to send test documents. Consequently, activating or onboarding in a sandbox environment is not possible.

For more information, refer to the [Trials and Subscriptions](/Continia Document Output/Getting Started/Trials and Subscriptions.md) article.

## How do I resend an e-doc through the CDN?

If you are unable to resend an e-doc, it is likely because the document has already been successfully sent. Resending is only possible when the e-doc encounters an error during the initial sending process. 

To resend an e-doc, it must have the error message "failed" displayed in the outgoing Network Documents menu. To check the status of your document, go to the [Outgoing Network Documents](https://docs.continia.com/en-us/continia-document-output/business-functionality/electronic-invoicing/outgoing-network-documents) page. If the status indicates "failed," you can proceed with the resending process: 

1. Open the source document of the e-doc with the "failed" status. 
2. Locate the Doc. Out FactBox, and select **Send e-document** to attempt resending the e-doc. 

Note that if the document status is "draft," the e-doc was not sent out initially and consequently can't be resent. In this case, ensure the document is prepared correctly and try sending it again.

## What does the gateway error code *Unhandled Error in the Continia Delivery Network API* mean?

There are some settings you need to check:

* E-doc setup -> PEPPOL (or respective profile) -> participations (is it filled in?)
* In the same menu, check that the code units are filled in properly.
* Is the customer information correctly filled in (it may be that the GLN number is used even though they are registered with VAT number or the other way around)?

You can check the identifier type on the customer card: Go to Document Output Factbox -> Output Profile -> Continia Delivery Network -> recipient type

## Why do I have difficulties sending out OIOUBL Peppol files?
First, make sure your [registration has been approved](@DO-12#to-view-the-registration-process-status). If the status is green, the final step is to attach the Participation ID to the e-document Setup Code. 

To accomplish this, locate the e-document setup menu and open the relevant profile (e.g., Xrechnung, Peppol, OIOUBL). Within the profile, navigate to the participation section and select the onboarded profile by clicking on the appropriate option, typically represented by a three-dotted line.

For more information, refer to the [Setting up the Continia Delivery Network](@DO-12#to-attach-the-participation-id-to-the-e-document-setup) article.

## My onboarding is complete. Why can I still not send out electronic documents?

This situation can emerge during the last part of the onboarding. The last step when onboarding is to select the participation.  

Check the following: Open E-document setup and select the type of protocol you have onboarded, such as Peppol or OIOUBL.
After clicking on it, you can then select the onboarded entity under the Continia Delivery Network, and now the onboarding is completely finished.