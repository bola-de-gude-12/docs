---
title: Minimum Requirements for Using Continia Document Output On-Premises
date: 30-03-2023
description:  
lang: en
---

# Minimum Requirements for Using Continia Document Output On-Premises
This article describes the minimum requirements and recommendations for using Document Output in Microsoft Dynamics 365 Business Central *on-premises*. Note that these minimum requirements are different from the ones relating to the _online_ version of Business Central. 

> [!IMPORTANT]
> As Document Output is an integrated part of Business Central, the minimum requirements for Business Central also apply to Document Output.

##Browsers
We recommend using one of the following web browsers with the latest updates applied:

* Google Chrome
* Microsoft Edge

Mozilla Firefox and Apple Safari are likely to work too but aren't officially supported. Using Internet Explorer can cause errors and rendering issues. If Internet Explorer is the only option, it must be updated to the latest version.

##Mobile devices
Most Document Output features will work on mobile devices, although this isn’t officially supported. This goes for the use of Document Output in various mobile versions of Dynamics 365, including the mobile web client and the official Business Central app.

> [!NOTE]
>Not all Document Output features are visible or accessible on mobile devices. Even for features that work on mobile devices, the mobile user interface (UI) may look noticeably different from the corresponding computer UI, and certain features may also be accessed differently on mobile devices.

##Word and Outlook requirements
For all versions of Business Central on-premises up to and including version 14, you must have version 2010 or later of both Microsoft Outlook and Microsoft Word installed in order to use Document Output. If you use antivirus software, this must be recognized by Windows/Outlook.

##Firewall requirements
The firewall must allow outgoing traffic on ports 80 and 443 (HTTPS) from the computer that performs the Continia Document Output activation and downloads the Document Output configuration and document files. For classic NAV clients, this is the actual computer that you’re using. For NAV RTC, it’s the computer running the NAV Service Tier.

To take full advantage of Document Output during both setup and daily use, you must have access to the internet. You may also have to configure the following firewall settings to activate Document Output and to ensure that your setup is secure – but note that this is often not necessary.

> [!IMPORTANT]
> If you – like most companies – allow all outgoing traffic from your clients and servers, you don't have to configure any firewall settings for outgoing traffic. However, if your policies for outgoing network traffic are restricted in any way, you must configure your firewall to allow the traffic below.

> [!NOTE]
> All Continia resources are hosted in a Microsoft Azure environment. This means that the IP addresses associated with each domain name below are subject to change at Microsoft’s discretion. If the IP addresses do change, you can prevent sudden stop of all internet-related functionality by allowing URL filtering rather than IP filtering.

<br>

From all NAV/Business Central client and server computers, you must allow outgoing traffic to the following addresses on the specified ports:

| Address  | Port(s)  | Direction  | Environment |
| --- | --- | --- | :-: |
| auth.continiaonline.com | 443 | Outgoing | Production |
| demoauth.continiaonline.com | 443 | Outgoing | Test |
| license.continiaonline.com | 443 | Outgoing |  Production |
| demolicense.continiaonline.com | 443 | Outgoing | Test |
| codownloads.blob.core.windows.net | 80, 443 | Outgoing | Both |
| notification.continiaonline.com | 443 | Outgoing | Production |
| demonotification.continiaonline.com | 443 | Outgoing | Test |
| productsetup.continiaonline.com | 443 | Outgoing | Production |

<br>

In order to be able to send emails, you must allow outgoing traffic to the following server on the specified ports:

| Address  | Port(s)  | Direction  | Environment |
| --- | --- | --- | :-: |
|  Your email server | 143 (unsecured IMAP) or 993 (secure IMAP) | Outgoing | N/A |

<br>

When using the Continia Delivery Network, you must allow outgoing traffic from all NAV/Business Central client and server computers to the following addresses on the specified ports:

| Address  | Port(s)  | Direction  | Environment |
| --- | --- | --- | :-: |
| cdnapi.continiaonline.com | 443 | Outgoing | Production |
| codeliverynetworkprod.blob.core.windows.net | 80, 443 | Outgoing | Both |

<br/>

> [!IMPORTANT]
> For all of the above, please make sure that no proxy server, antivirus software, or the like is blocking your internet access. Always consult the relevant IT department to ensure this follows company rules and regulations.

##See also
[Overview of Business Functionality](/Continia Document Output/Getting Started/Business Functionality.md)  
[Business Central website](https://dynamics.microsoft.com/en-us/business-central/overview/)  


<style>
  .content table tr td:nth-child(1) {
    width: 370px;
  }
  .content table tr td:nth-child(2) {
    width: 330px;
  }  
</style>