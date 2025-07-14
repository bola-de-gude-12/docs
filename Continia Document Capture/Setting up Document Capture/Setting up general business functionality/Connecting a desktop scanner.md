---
title: Connecting a desktop scanner in Document Capture
date: 04-07-2025
description:  
id: DC-119
lang: en
---

# Connecting a desktop scanner
Continia Document Capture supports the scanning of documents using a desktop scanner plugged directly into your laptop or desktop computer. Once a connection has been established, Document Capture can communicate with the scanner and initiate scanning directly from Microsoft Dynamics 365 Business Central.

> [!NOTE]
> With desktop scanners, scanning can only be performed from computers that have the scanner plugged in, which is why it’s not the first choice for most companies. Instead, they typically either receive documents via email or scan them using a network scanner. However, your organization is free to use all of these methods in combination – opting for a desktop scanner doesn’t prevent you from importing documents via email or network scanners as well.

Before you can start using a desktop scanner, you must ensure that both the scanner and your computer meet the minimum requirements. For more information, check out the local scanner requirements for [Business Central online](@DC-482#local-scanner-requirements) or for [Business Central on premises](@DC-135#local-scanner-requirements) – depending on what version you use.

When you’ve plugged your scanner into a user PC, connect it by following these steps:
1. Install the required software. To get access to this software, please reach out to your [dedicated Continia partner](/Continia Document Capture/Getting Started/Resellers and Partners/Overview.md).
1. Run the software provided by your partner. In the setup guide, select the installer that matches the version of Microsoft Dynamics NAV/Business Central you're using, and select **Install**.
1. In Business Central, search {{search}} for and select **Document Capture Setup**.
1. On the **General** FastTab, enable the use of your attached scanner by turning on the **Enable Local Scanner** setting.
1. To verify that the scanner has been enabled, search {{search}} for and select **Scanning & OCR**. In the **Scanning & OCR** window that opens, your scanner should now appear in the **Scanner** box.
1. On the action bar, click **Scan** to scan a document.

Refer to your scanner manufacturer's website to download the required drivers.

> [!NOTE]
> If you're accessing Business Central via Microsoft Edge, you'll need to allow Edge to communicate with local HTTP services. Otherwise the **Scanning & OCR** window will display the message “Document Capture scanning service not running” instead of the name of your scanner, thereby effectively making you unable to scan. In order to allow Edge to communicate with the Document Capture Scanning Service, open a command prompt with administrative privileges and enter the following command:
> 
> **CheckNetIsolation LoopbackExempt -a -n=Microsoft.MicrosoftEdge_8wekyb3d8bbwe**
> 
> Your scanner should now appear in the **Scanning & OCR** window, in the **Scanner** box, and you should be able to scan documents.
