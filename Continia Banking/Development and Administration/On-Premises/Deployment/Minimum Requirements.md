---
title: Minimum Requirements for Using Continia Banking On-Premises
date: 20-02-2024
description:  Minimum requirements for Continia Banking on-premises
id: CB-69
lang: en
---

# Minimum requirements for using Continia Banking on-premises

This article describes the minimum requirements and recommendations for using Continia Banking in Microsoft Dynamics 365 Business Central *on-premises*. 

> [!IMPORTANT]
> As Continia Banking is an integrated part of Business Central, the minimum requirements for Business Central also apply to Continia Banking.

## Browsers
We recommend using one of the following web browsers with the latest updates applied:

* Google Chrome 
* Mozilla Firefox 
* Apple Safari 
* Microsoft Edge

Using Internet Explorer can cause errors and rendering issues. If Internet Explorer is the only option, it must be updated to the latest version.

## Mobile devices

Most Continia Banking features will work on mobile devices, although this isn’t officially supported. This goes for the use of Continia Banking in various mobile versions of Dynamics 365, including the mobile web client and the official Business Central app.

> [!NOTE]
>Not all Continia Banking features are visible or accessible on mobile devices. Even for features that work on mobile devices, the mobile user interface (UI) may look noticeably different from the corresponding computer UI, and certain features may also be accessed differently on mobile devices.

## Bank requirements
Continia Banking supports direct and manual bank communication. Your options for communicating with the bank depend on which types of bank communication is supported by your bank. In order for Continia Banking to process the data communicated between the bank and Business Central, your bank must be supported by Continia Banking. For some banks subscription to files must be ordered in the bank. Also, if you'd like to use the Direct Communication module, you may need a valid certificate from your bank. For more information about individual requirements for each bank, please see the [Bank integration](@CB-38).

## Firewall requirements
The firewall must allow outgoing traffic on ports 80 and 443 (HTTPS) from the computer that performs the Continia Banking activation and downloads the Continia Banking configuration and document files. 

To take full advantage of Continia Banking during both setup and daily use, you must have access to the internet. You may also have to configure the following firewall settings to activate Continia Banking and to ensure that your setup is secure – but note that this is often not necessary.

> [!IMPORTANT]
> If you – like most companies – allow all outgoing traffic from your clients and servers, you don't have to configure any firewall settings for outgoing traffic. However, if your policies for outgoing network traffic are restricted in any way, you must configure your firewall to allow the traffic below.

> [!NOTE]
> All Continia resources are hosted in a Microsoft Azure environment. This means that the IP addresses associated with each domain name below are subject to change at Microsoft’s discretion. If the IP addresses do change, you can prevent sudden stop of all internet-related functionality by allowing URL filtering rather than IP filtering.

<br>

From all Business Central client and server computers, you must allow outgoing traffic to the following addresses on the specified ports:

| Address  | Port(s)  | Direction  | Environment |
| --- | :-: | :-: | :-: |
| auth.continiaonline.com | 443 | Outgoing | Production |
| demoauth.continiaonline.com | 443 | Outgoing | Test |
| license.continiaonline.com | 443 | Outgoing | Production |
| demolicense.continiaonline.com | 443 | Outgoing | Test |
| codownloads.blob.core.windows.net | 80, 443 | Outgoing | Both |
| bankapi.continiaonline.com | 443 | Outgoing | Production |
| demobankapi.continiaonline.com | 443 | Outgoing | Test |

<br/>

> [!IMPORTANT]
> For all of the above, please make sure that no proxy server, antivirus software or the like is blocking your internet access. Always consult the relevant IT department to ensure that this is in accordance with company rules and regulations.

For more information on the above-described minimum requirements, please reach out to [your dedicated Continia partner](@CB-09).

