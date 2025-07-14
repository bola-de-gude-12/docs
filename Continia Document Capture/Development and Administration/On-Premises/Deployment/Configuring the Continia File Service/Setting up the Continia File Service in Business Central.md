---
title: Setting up the Continia File Service in Business Central
date: 07-08-2023
description:  
id: DC-126
lang: en
---

# Setting up the Continia File Service in Business Central

When you've [set up a repository and authorization key](@DC-125) for the Continia File Service, you must configure the service in Microsoft Dynamics 365 Business Central. You can do this in two ways:

* For [standard configuration](#standard-configuration), use the dedicated assisted setup guide.
* For [more advanced setup options](#advanced-setup), use the **Document Capture Setup**.

Both methods are described in more detail in the sections below.

> [!IMPORTANT]
> The details you entered in the configuration tool [when you configured the Continia File Service](@DC-125) must be reused when you set up the service in Business Central, so it's important that they're identical with the ones you enter when following the guides below.

> [!NOTE]
> When you migrate from the File System to the File Service, the actual location of the files typically doesn't change – it's only the way the files are accessed that changes. For that reason, Continia Document Capture doesn't automatically move any files during a migration to the Files Service. If any files have to be moved, you must do so manually.

## Standard configuration

To configure the Continia File Service in Business Central using the standard assisted setup guide, follow these steps:

1. Choose the {{search}} icon, enter **Storage Migration Assisted Setup Guide**, and then choose the related link.
1. Follow the on-screen instructions.
1. When you're done, select **Finish** to close the guide and implement your settings.

The Continia File Service is now fully configured and ready for use as your default document storage type.

## Advanced setup

To configure the Continia File Service in Business Central using the **Document Capture Setup** for more advanced settings, follow these steps:

1. Search {{search}} for and select **Document Capture Setup**. 
1. On the **General** FastTab, under **Document Storage Type**, select **File Service**.
1. A dialog appears, asking you if you want to migrate your files to **File Service**. Select **Yes** to confirm and close the dialog. The **Update Storage Settings - File Service** page opens.
1. Fill out the **Server**, **Server Port**, **Repository**, and **Authorization Key** fields, and modify the paths and the **Disk File Directory Structure**, if necessary.
   > [!IMPORTANT]
   > Your **Server Port**, **Repository**, and **Authorization Key** entries must be identical with the corresponding entries you added in the configuration tool [when you configured the Continia File Service](@DC-125). Also, the paths must correspond to the root folder you specified in the configuration tool.
1. **Optional**: If your server setup requires a secure connection using cryptography, SSL, or similar, enable **Use Secure Connection**.
1. **Optional**: To verify the setup, select the three dots at the top, and then select **Test Connection**. A dialog with connection details appears. Select **OK** to close it.
1. On the **Update Storage Settings - File Service** page, select **OK** to continue.
1. Follow the on-screen instructions to complete the guide.

The Continia File Service is now fully configured and ready for use as your default document storage type.