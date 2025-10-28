---
title: Accessing the source code in Document Capture
description: 
date: 16-06-2025
id: DC-485
lang: en
---

# Accessing the source code

Continia recognizes the need for access to our apps' source code for testing, integration, or problem-solving purposes. To access the source code, follow these steps:

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com/) > **Downloads**, and download the relevant product package.
1. Extract the product package to a folder on your computer.
1. Click the **App** folder and then the **Source** folder.
1. Select the ZIP file that matches your Microsoft Dynamics 365 Business Central (BC) version, including the correct cumulative update.
1. Extract the file(s) you need.


Note that the **Source** folder contains two different kinds of Document Capture source code zip files:

* One for all base functionality, named "DC [version number] - [BC version number] (BC commercial name) Source.zip" (for example **DC 9.0.0.0 - 19 (BC 2021 Wave 2) Source.zip**)
* One for on-premises functionality, named "DC on-premises [version number] - [BC version number] (BC commercial name) Source.zip" (for example **DC on-premises 9.0.0.0 - 19 (BC 2021 Wave 2) Source.zip**)

The base app is used for both cloud and on-premises deployments, but note that for on-premises installations you'll need both the base app and the on-premises app.

> [!NOTE]
> If you're looking for the source code files in an older product package, they might be located in a different folder: **App** folder > relevant Business Central version folder > **Document Capture** folder.