---
title: Expense Management Overview of the Continia File Service
date: 29-03-2023
description:  
id: EM-141
lang: en
---

# Overview of the Continia File Service

The Continia File Service is a storage type that enables you to continue using local file system storage in Continia Expense Management while staying compliant with Microsoft's Business Central Universal Code initiative. 

The service acts as a replacement for the older **File System** storage type, which isn't cloud-compatible. The Continia File Service, on the other hand, is cloud-optimized and hosts a web service that serves as a sort of intermediary between Microsoft Dynamics 365 Business Central and your file system. The web service loads or saves files into predefined repositories, which are self-contained units pointing to a specific folder that's accessible to the user who runs the Continia File Service. This folder can be either local or shared.

To prevent unauthorized access, each repository is secured by its own unique name and authorization key. You specify both the name and the authorization key freely as part of the configuration process.

To set up the Continia File Service, you must carry out the following actions in the order specified:

* [Install the Continia File Service](@EM-140).
* [Configure the Continia File Service](@EM-139).
* [Set up the Continia File Service in Business Central](@EM-142).

For more information, click each of the links above to open detailed articles with how-to guides for each of the steps in the process.

## Related information

[Setting up Document Storage](@EM-144)  
[Migrating Expense Management from Business Central On-Premises to Cloud](@EM-112)  