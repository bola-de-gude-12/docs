---
title: Expense Management Configuring the Continia File Service
date: 28-03-2023
description:  
id: EM-139
lang: en
---

# Configuring the Continia File Service

Once you've [installed the Continia File Service](@EM-140), you must set up a repository and authorization key for it. Note that this process requires you to use the Continia File Service configuration tool – Continia File Service Configuration – which is installed on the same server as the Continia File Service itself, as part of the installation process.

> [!IMPORTANT]
> The details you enter in the configuration tool when following the guide below must be reused later when you [set up the Continia File Service in Business Central](@EM-142), so it's important that they're identical with the ones you enter during that setup process. You can enter any repository and authorization key you prefer in free text below, as long as you take note of them and reuse them exactly as is later.

To set up a repository and authorization key for the Continia File Service, follow these steps:

1. Open Continia File Service Configuration.
1. Depending on your IT infrastructure policies, select **Enable HTTP**, **Enable HTTPS**, or both.
1. For the option(s) you enabled in step 2 above, enter the port number(s). The standard port for HTTP is **5000**.
1. Under **Repositories**, add the entries you want to use. Be sure to enter the correct path(s) and to take note of your entries, as you'll need them later.
   > [!NOTE]
   > The following is an example of a possible setup. Note that all entries will be automatically lowercased once they've been entered into the table:
   > 
   > | Repository | Authorization Key | File Path |
   > | --- | --- | --- |
   > | documentcapture | d93msbx52oem | c:\dc |
   > | continiaexpensemanagement | 398dhjf4kkm67owly | c:\em |
1. In the **Service** section, under **Service user**, select a service user with access to the directory.
1. Below the **Repositories** table, select **Save** to save your changes. 
1. In the **Service** section, under **Service status**, select **Start** to start the service.
1. When you're done, select **Close** to exit.

You're now ready to perform the final configuration of the Continia File Service. For information on how to do this, see [Setting up the Continia File Service in Business Central](@EM-142).








<style>
  .content table tr td:nth-child(1) {
    width: 150px;
  }
  .content table tr td:nth-child(2) {
    width: 130px;
  }
  .content table tr td:nth-child(3) {
    width: 250px;
  }  
</style>