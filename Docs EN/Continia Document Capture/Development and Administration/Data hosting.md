---
title: Data hosting
date: 07-04-2025
description: Where Continia's servers are located, and what type of data these servers process.
id: DC-399
lang: en
---

# Data hosting

This article describes where Continia's servers are located, and what type of data these servers process.

For information on how to select the center where your data is stored – which is possible as of Continia Document Capture 2024 R1 –, see [Data centers](@DC-215).

## Cloud OCR and Web Approval Portal

Continia's cloud OCR service is hosted by Microsoft Azure. While production environments are hosted in the regions listed by Microsoft as Australia East and North Europe, demo environments are hosted in West Europe. 

Continia’s Web Approval Portal is also hosted by Microsoft Azure. While production environments are hosted in the regions listed by Microsoft as Australia East, Central USA, and North Europe, demo environments are hosted in West Europe.

The only location data known to Continia is the Azure server that the Business Central user is assigned to. E.g.: if a Business Central user is assigned to a geolocation in Canada, the processing of their data occurs in the Central USA data center – as this is the closest Azure server to that location. 

Note that:

- OCR-processed documents are only stored until they’re downloaded, but Continia keeps a copy of the original email for 30 days. 

- If these OCR-processed documents are not downloaded – which is only relevant in rare cases, such as errors or manual download failures –, they’re automatically deleted within 180 days. 

- The retrieval and transport of emails is provided by Amazon Web Service (AWS) in Dublin, Ireland. Microsoft Azure doesn’t provide such service. 

- For the Web Approval Portal, PDFs are cached for 24-48 hours – depending on when the PDF is uploaded and when the cleanup job runs. 

- Company activation data is stored in Continia databases hosted in Dublin, Ireland. 

For more information on Microsoft's global infrastructure, see [Azure geographies](https://azure.microsoft.com/en-us/explore/global-infrastructure/geographies) (Microsoft article).

## Related information

[Data centers](@DC-215)