---
title: Secure communication using Continia Delivery Network and Peppol
date: 29-03-2023
description:  
id: DO-92
lang: en
---

# Secure communication using Continia Delivery Network and Peppol
Peppol (Pan-European Public Procurement Online) is a widely adopted framework that helps to standardize and secure communication between organizations across different industries and countries, including electronic invoicing. Peppol achieves security by establishing a network of trusted access points that handle the secure transmission, encryption, and validation of electronic documents. 

Because Continia is a certified Peppol access point, when you sign up for the Continia Delivery Network, you're automatically set up and enabled to send documents in encrypted form to all recipients in the global Peppol eDelivery Network. If you are using a cloud-based Business Central solution, you won't have to worry about developing a local solution to export XML files or installing additional components for connecting with other operators. This offers a significant advantage since Continia serves as your single supplier, responsible for generating and transporting XML files for your electronic invoices.

The following diagram presents an overview of the Peppol four-corner model in a scenario involving Document Output as the sender, Document Capture as the receiver, and CDN used as an access point for both receiver and the sender:

![Electronic invoicing using Peppol and CDN](/images/COPP/en-us/cdnelectronicinvoicing.png)
1. **The document sender** - the document in encrypted XML format is sent directly from Business Central using electronic invoicing by Document Output. 
2. **The sender's Peppol access point** - you need a certified access point to send your document to the Peppol network, where the ID and document type are validated. 
3. **The receiver's Peppol access point** - you need a certified access point to receive your document from the Peppol network. 
4. **The document receiver** - the document can be imported directly into Business Central, using Document Capture. 
   > [!NOTE]
   >
   > Peppol's four-corner model doesn’t require unique point-to-point connections or for both parties to use the same provider.



