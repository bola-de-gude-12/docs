---
title: Overview of the Continia File Service
date: 16-10-2023
description:  
id: DC-123
lang: en
---

# Overview of the Continia File Service

The Continia File Service is a storage type that enables you to continue using local file system storage and on-premises OCR in Continia Document Capture while staying compliant with Microsoft's Business Central Universal Code initiative.

> [!IMPORTANT]
> The Continia File Service only works with on-premises installations of Document Capture.

The service acts as a replacement for the older **File System** storage type, which isn't cloud-compatible. The Continia File Service, on the other hand, is cloud-optimized and hosts a web service that serves as a sort of intermediary between Microsoft Dynamics 365 Business Central and your file system. The web service loads or saves files into predefined repositories, which are self-contained units pointing to a specific folder that's accessible to the user who runs the Continia File Service. This folder can be either local or shared.

To prevent unauthorized access, each repository is secured by its own unique name and authorization key. You specify both the name and the authorization key freely as part of the configuration process.

To set up the Continia File Service, you must carry out the following actions in the order specified:

* [Install the Continia File Service](@DC-124).
* [Configure the Continia File Service](@DC-125).
* [Set up the Continia File Service in Business Central](@DC-126).

For more information, click each of the links above to open detailed articles with how-to guides for each of the steps in the process.

## Related information

[Setting up Document Storage](@DC-3)  
[Considerations when migrating to the cloud](@DC-106#considerations-when-migrating-to-the-cloud)  