---
title: Outgoing Network Documents
date: 27-05-2024
description:
id: DO-73
lang: en
---

# Track document transfer status

The Outgoing Network Documents page provides a list of documents sent as XML files, where you can check the transfer status of e-documents and preview both the generated XML files and source documents.

It shows the documents transmitted through the Continia Delivery Network (CDN) and also documents sent using Document Output and a different Peppol access point. If you use another operator for transmission, you must export the XML files to an export folder and have the files collected by a component or service connecting to that operator.

To view the transfer status of e-documents:

* Select the {{search}} icon, enter **Outgoing Network Documents**, and then select the related link. You can now view the queue of sent documents. 

The time that passes before you know whether the transfer of an e-document was successful or not differs for the NemHandel and the peppol networks, respectively.

In the case of the Nemhandel network, feedback is generated only if OIOUBL documents contain errors. Consequently, if there's no feedback within 48 hours, the documents are assumed by Document Output to have been sent successfully.

On the other hand, Peppol documents yield feedback for both successful and unsuccessful transfers, and feedback is typically received within a few hours.

## Transfer statuses

In the **Status** column, you can see the transfer status of your sent documents.

* **Draft**: The electronic document hasn't been sent yet.
* **In transit**: The document is being sent and no feedback has been received so far,  which can take up to 48 hours in connection with Nemhandel documents.
* **Sent**: The document was successfully sent using the Continia Delivery Network.
* **Error**: The document was not sent due to an issue. In most cases, the built-in validator found one or more inconsistencies in the document. You can check the exact error(s) by clicking on the document in the top-right  corner and downloading the document receipt. This will give you an xml  file describing the issue.
