---
title: Installing the Continia File Service
date: 16-10-2023
description:  
id: DC-124
lang: en
---

# Installing the Continia File Service

> [!IMPORTANT]
> The Continia File Service only works with on-premises installations of Document Capture.

To install the Continia File Service, follow these steps:

1. Ensure that you're running a version of Continia Document Capture that supports the Continia File Service (Document Capture 2023 R1 (11.00) or later). 
1. Go to the [Continia PartnerZone](https://partnerzone.continia.com/) > **Downloads** (only available to Continia Partners), and download the relevant product package.
1. Extract the product package to a folder on your computer.
1. Run setup.exe from the root of the software directory to open the installer.
1. In the installer, select **File Service** > **Install**. Note that the Continia File Service must be installed on a server with access to the files.
1. Select **Close** to close the installer and finish the installation process.
1. Make sure that all applicable TCP ports are open in the relevant firewalls.
   > [!NOTE]
   > The TCP ports must be the same as the ones you enter in the Continia File Service Configuration tool when you [configure the Continia File Service](@DC-125).

You're now ready to configure a repository and authorization key for the service. For information on how to do this, see [Configuring the Continia File Service](@DC-125).