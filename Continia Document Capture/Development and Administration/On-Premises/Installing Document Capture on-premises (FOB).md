---
title: Installing Continia Document Capture on premises (FOB)
date: 31-03-2025
description: How to install Document Capture in FOB versions of NAV/Business Central (on premises).
id: DC-17
lang: en
---

# Installing Continia Document Capture on premises (FOB)

This article describes how to install Document Capture in FOB versions of Microsoft Dynamics NAV/Business Central. Note that you must be assisted by your Continia partner when you install the software.

> [!IMPORTANT]
> The last FOB version of Document Capture is 2024 R2 (25.00). On-premises users can install the app version of Document Capture 2025 R1 (26.00).

To install Document Capture in a FOB version of NAV/Business Central, you must do the following in the order given:

1. [Download the installation package, and run the installer](#to-run-the-document-capture-installer).
1. [Import the objects downloaded in step 1 into your Business Central database](#to-import-the-objects).
1. [Compile all objects in the database](#to-compile-all-objects-in-the-database).

These actions are described in more detail in the guides below.

## To run the Document Capture installer

> [!NOTE]
> For all versions between NAV 2017 and Business Central April 2019 (BC v14), both server and client components are installed automatically, meaning that you can skip steps 5-6 in the guide below. For all previous versions of NAV, you must install these components manually – as described in the guide.

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com).
1. In the menu at the top, select **Downloads**.
1. Use the filters to locate the latest version of Document Capture, and select **Download** to download the installation package.
1. Extract the product package to a folder on the computer with the Business Central service tier. From this folder, run the setup.exe file to open the Document Capture installer.
1. In the installer, under **Dynamics NAV Server**, select **Server Components**, and then select your version of Business Central > **Install**.
   > [!NOTE]
   > The installer updates the **Add-ins** folder (client and/or server) in the standard installation path. If your installation path differs from the standard Microsoft path, copy the new **Add-ins** folder to the folder that your installation resides in.
1. Depending on your version of NAV/Business Central, select **Dynamics NAV RoleTailored Client** or **Dynamics NAV Classic Client**, and then select **Client Components**. If you have a RoleTailored client and selected **Client Components** in the corresponding section, you must also select your version of Business Central. Select **Install** to install the client components.
1. **Optional:** If you want to scan documents from the actual NAV/Business Central client, select **Dynamics NAV RoleTailored Client** or **Dynamics NAV Classic Client**, and then select **Scanner Components**. For RoleTailored clients, select your version of Business Central. Select **Install** to install the scanner components.

> [!IMPORTANT]
> The above guide describes what must be done for the computer with the Business Central service tier installed, but steps 6-7 actually apply to all computers using Document Capture. To install client components and – if relevant – scanner components on these computers, you must carry out these two steps for each of the computers, for example by distributing the downloaded product package to all relevant computers and then running the installer locally. Skip step 5 on all other computers than the one running the Business Central service tier.

## To import the objects

> [!NOTE]
> For NAV 2015 and later, steps 6-8 of the following guide must be carried out. For all other versions, these steps can be disregarded.

1. In the Microsoft Dynamics NAV Development Environment, go to **Tools** and select **Object Designer**.
1. In the menu bar, select **File** > **Import...** to open the **Import Objects** window.
1. Locate the installation package that you downloaded in step 3 of [the guide above](#to-run-the-document-capture-installer), and select the **Objects** folder.
1. Select the FOB file that matches your Business Central version, and then select **Open**.
   > [!IMPORTANT]
   > You must select the FOB file that corresponds to the database version of NAV/Business Central, even if you're running a runtime upgrade of NAV/Business Central.
1. A dialog box appears, notifying you about any potential conflicts. Do one of the following:
   * If there are conflicts, select **OK** to open the **Import Worksheet** window, and then resolve all conflicts. These are marked by an exclamation mark in the **Warning** column. Select **OK** when you're done.
   * If there are no conflicts, select **Yes** to import all FOB file objects.
1. The **Import fob** window opens. Under **Synchronize Schema**, select **Now - with validation** > **OK**.
1. A dialog box appears, asking you if you want to continue. Select **Yes** to close the box and start the synchronization of table changes.
1. When the **Synchronize Schema Changes** window displays the state **Operational**, select **Close**.
1. A dialog box confirms that the import has been completed. Select **OK** to close it.

## To compile all objects in the database

This stage of the process varies slightly depending on your version of NAV/Business Central, as described in the two guides below. Both guides are a direct continuation of [the object-import guide above](#to-import-the-objects).

   > [!NOTE]
   > The difference between the guides has to do with whether or not you installed the server and client components manually when [running the Document Capture installer](#to-run-the-document-capture-installer): 
   > * If you *didn't* do this manually (versions NAV 2017 to BC v14), you must run the assisted setup guide before compiling, in order to install the components automatically and avoid compilation errors.
   > * If you *did* install the components manually (all versions before NAV 2017), you must compile before running the Document Capture assisted setup guide.

### For versions earlier than NAV 2017:

1. In the Microsoft Dynamics NAV Development Environment, in the **Object Designer** table, select the **Version List** column, and then select **View** > **Field Filter...** to open the filter window.
1. In the filter field, enter the string **\*DC\*|\*EM\*|\*CC\*|\*DN\***, and select **OK** to apply the entered filter and close the window.
1. In the **Object Designer** table, select all entries (for example by selecting **Ctrl+A**), and then select **Tools** > **Compile**.
1. The **Compile** window opens. Under **Synchronize Schema**, select **Now - with validation** > **OK**.
1. When the compilation process is complete, an error list may be displayed. For the Scandinavian countries, this is likely to show the following codeunits as failed:
   * **6085715** (only for Denmark)
   * **6085745** (for Denmark, Norway, and Sweden)
   * **6085767** (only for Norway)
   * **6085768** (only for Sweden)
   If you don't have Continia Payment Management installed, you can safely ignore this and close the list, provided that no other errors are listed.
1. In NAV/Business Central, run the **Document Capture Assisted Setup Guide** and follow the on-screen instructions. You can run the guide either as part of [activating Document Capture](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-activate-a-solution) or by searching for **Document Capture Setup Wizard** and choosing the related link.

### For versions from NAV 2017 to BC v14 inclusive:

1. In NAV/Business Central, run the **Document Capture Assisted Setup Guide** and follow the on-screen instructions. You can run the guide either as part of [activating Document Capture](/continia-document-capture/development-and-administration/on-premises/managing-solutions/managing-solutions#to-activate-a-solution) or by searching for **Document Capture Setup Wizard** and choosing the related link.
1. In the Microsoft Dynamics NAV Development Environment, in the **Object Designer** table, select the **Version List** column, and then select **View** > **Field Filter...** to open the filter window.
1. In the filter field, enter the string **\*DC\*|\*EM\*|\*CC\*|\*DN\***, and select **OK** to apply the entered filter and close the window.
1. In the **Object Designer** table, select all entries (for example by selecting **Ctrl+A**), and then select **Tools** > **Compile**.
1. The **Compile** window opens. Under **Synchronize Schema**, select **Now - with validation** > **OK**.
1. When the compilation process is complete, an error list may be displayed. For the Scandinavian countries, this is likely to show the following codeunits as failed:
   * **6085715** (only for Denmark)
   * **6085745** (for Denmark, Norway, and Sweden)
   * **6085767** (only for Norway)
   * **6085768** (only for Sweden)
   If you don't have Continia Payment Management installed, you can safely ignore this and close the list, provided that no other errors are listed.