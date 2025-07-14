---
title: Overview of setting up general business functionality in Document Capture
date: 16-06-2025
id: DC-77
lang: en
---

# Overview of setting up general business functionality

The default Continia Document Capture configuration enables you to start processing documents immediately. However, Document Capture also offers a wide range of other configuration options that allow you to adjust the app to fit the exact needs of your organization.

The table below lists the most important of these:

| To                                                                                                                  | See                                                                                                                                                                                             |
| ------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Sign up to the Continia Delivery Network in order to start receiving Peppol and NemHandel invoices and credit memos | [Setting up the Continia Delivery Network](../../../Continia%20Document%20Capture/Setting%20up%20Document%20Capture/Setting%20up%20general%20business%20functionality/@DC-75/)                  |
| Define where to store documents if you prefer other locations than your Business Central database                   | [Setting up document storage](../../../Continia%20Document%20Capture/Setting%20up%20Document%20Capture/Setting%20up%20general%20business%20functionality/@DC-3/)                                |
| Change the company policy in order to allow or prevent the deletion of documents in your company                    | [Preventing the deletion of documents as a company policy](../../../Continia%20Document%20Capture/Setting%20up%20Document%20Capture/Setting%20up%20general%20business%20functionality/@DC-477/) |
| Define document status codes used in the document journal                                                           | [Defining document status codes](../../../Continia%20Document%20Capture/Setting%20up%20Document%20Capture/Setting%20up%20general%20business%20functionality/@DC-79/)                            |
| Set up a job queue to import documents at predefined intervals instead of importing them manually                   | [Setting up job queues](../../../Continia%20Document%20Capture/Setting%20up%20Document%20Capture/Setting%20up%20general%20business%20functionality/@DC-16/)                                     |
| Set up company identification texts                                                                                 | [Setting up company identification texts](../../../Continia%20Document%20Capture/Setting%20up%20Document%20Capture/Setting%20up%20general%20business%20functionality/@DC-443/)                  |
| Enable and set up the Secure Archive, including document activity logging                                           | [Setting up the Secure Archive](../../../Continia%20Document%20Capture/Setting%20up%20Document%20Capture/Setting%20up%20general%20business%20functionality/@DC-155/)                            |
| Set up retention periods for data maintenance and perform data maintenance actions                                  | [Setting up data maintenance](../../../Continia%20Document%20Capture/Setting%20up%20Document%20Capture/Setting%20up%20general%20business%20functionality/@DC-187/)                              |

\
When you run Document Capture on-premises or in a private cloud environment, the following additional configuration steps must also be taken before you can start working:\


| To                                                     | See                                                                                                                                                                         |
| ------------------------------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Configure whether to use cloud or on-premises OCR      | [Setting up cloud and on-premises OCR](../../../Continia%20Document%20Capture/Setting%20up%20Document%20Capture/Setting%20up%20general%20business%20functionality/@DC-142/) |
| Enable Document Capture to scan from a desktop scanner | [Connecting a desktop scanner](../../../Continia%20Document%20Capture/Setting%20up%20Document%20Capture/Setting%20up%20general%20business%20functionality/@DC-119/)         |

> \[!IMPORTANT] Document Capture connects documents with transactions in Microsoft Dynamics 365 Business Central via the transaction number. Therefore, it's important that the number series in Business Central are kept separate, and overlapping is avoided.
