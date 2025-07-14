---
title: Minimum Requirements for Using Continia Expense Management On-Premises
date: 27-09-2024
description:
id: EM-51

lang: en
---

# Minimum Requirements for Using Continia Expense Management On-Premises
This article describes the minimum requirements and recommendations for using Expense Management in Microsoft Dynamics 365 Business Central *on-premises*. Note that these minimum requirements are different from the ones relating to the _online_ version of Business Central, which can be found [here](@EM-83). 

> [!IMPORTANT]
> As Expense Management is an integrated part of Business Central, the minimum requirements for Business Central also apply to Expense Management.

## Browsers
We recommend using one of the following web browsers with the latest updates applied:

* Google Chrome 
* Mozilla Firefox 
* Apple Safari 
* Microsoft Edge

Using Internet Explorer can cause errors and rendering issues. If Internet Explorer is the only option, it must be updated to the latest version.

## Screen resolution
The screen resolution must be at least 1440 × 900, as lower resolutions will make it difficult to use the Expense Management document viewer properly. We recommend using a screen resolution of 1680 × 1050 or higher.

Note that zooming in your browser or changing your display’s scale and layout settings may disturb the viewing experience, as this isn’t fully supported.

## Mobile devices
Expense Management is [used differently by different users](/continia-expense-management/getting-started/overview#get-familiar-with-expense-management) and covers several applications that can be accessed either via web browsers or as mobile apps:

* The Continia Expense App (mobile app) – used by expense users
* The Continia Expense Portal (web portal) – used by expense users
* The Continia Web Approval Portal (web portal) – used by approvers
* Business Central (web client and mobile app) – used by approvers and bookkeepers (see info on limitations when using the mobile app below under **Business Central**)

**The Expense App** is a dedicated mobile app that's fully supported on mobile devices. For more information, see [Continia Expense App](/continia-expense-management/development-and-administration/on-premises/deployment/minimum-requirements#continia-expense-app) below.

**The Expense Portal** can, technically speaking, also be accessed on mobile devices, but this is not recommended, as it's *not* optimized for mobile. When you use mobile devices to submit expenses, we therefore recommend using the dedicated mobile Expense App instead.

> [!TIP]
>Use the dedicated mobile Expense App instead of the Expense Portal to submit expenses on mobile devices.

**As for the Web Approval Portal**, this is fully supported on mobile devices. The Web Approval Portal is a dedicated Continia client, so the use of this lies outside of Business Central. More information can be found [below](/continia-expense-management/development-and-administration/on-premises/deployment/minimum-requirements#continia-web-approval-portal).

**Business Central** is generally optimized for mobile and easily accessible on mobile devices, but the look and feel is different from when you use it on a computer. While most Expense Management features in Business Central will indeed work on mobile devices, this isn’t officially supported, meaning that not all functionality is available in the mobile version of Business Central.

## Dynamics NAV Web client requirements 
Expense Management only supports the Dynamics NAV Web client from Microsoft Dynamics NAV 2016 or later.

## Continia Expense App
The Expense App is compatible with any Android or iOS device that meets the following software requirements:

**Android:**  
Versions supported: 9.0 or later versions.  
Click [here](https://www.continia.com/continia-expense-app/) to install the app on your device.

**iPhone:**  
Versions supported: iOS 14 or later versions.  
Click [here](https://www.continia.com/continia-expense-app/) to install the app on your device.

##Continia Web Approval Portal
The requirements for using the Continia Web Approval Portal with Business Central on-premises can be found [here](Web Approval Portal Requirements On-Premises.md). 

##Firewall requirements
The firewall must allow outgoing traffic on ports 80 and 443 (HTTPS) from the computer that performs the Continia Expense Management activation and downloads the Expense Management configuration and document files. For classic NAV clients, this is the actual computer that you’re using. For NAV RTC, it’s the computer running the NAV Service Tier.

To take full advantage of Expense Management during both setup and daily use, you must have access to the internet. You may also have to configure the following firewall settings to activate Expense Management and to ensure that your setup is secure – but note that this is often not necessary.

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
| license.continiaonline.com | 443 | Outgoing | Production |
| demolicense.continiaonline.com | 443 | Outgoing | Test |
| codownloads.blob.core.windows.net | 80, 443 | Outgoing | Both |
| cem.continiaonline.com | 443 | Outgoing | Production |
| democem.continiaonline.com | 443 | Outgoing | Test |
| notification.continiaonline.com | 443 | Outgoing | Production |
| demonotification.continiaonline.com | 443 | Outgoing | Test |

<br>

To be able to send emails to expense users and approvers, you must allow outgoing traffic to the following server on the specified port:

| Address  | Port(s)  | Direction  | Environment |
| --- | --- | --- | :-: |
|  Your email server | 25 (unsecured SMTP) as standard, but can be others | Outgoing | N/A |

<br>

When using the Continia Web Approval Portal hosted by Continia Software (www.continiaonline.com), you must allow incoming traffic from the following addresses and ports to the NAV/Business Central Web Services server:

| Address  | Port(s)  | Direction  | Environment |
| --- | --- | --- | :-: |
| EUN IP: 23.102.56.117 (Ireland, covering Northern Europe) | SOAP service (default: 7047) | Incoming | Production |
| USC IP: 13.89.38.96 (Iowa, covering Central US) | SOAP service (default: 7047) | Incoming | Production |
| AUE IP: 23.101.213.2 (New South Wales, covering East Australia) | SOAP service (default: 7047) | Incoming | Production |
| DEMO IP: 40.118.71.119 | SOAP service (default: 7047) | Incoming | Test |

<br/>

> [!IMPORTANT]
> For all of the above, please make sure that no proxy server, antivirus software or the like is blocking your internet access. Always consult the relevant IT department to ensure that this is in accordance with company rules and regulations.

##Add-in requirements
The minimum required version of .NET Framework for add-ins is version 4.

The drag-and-drop functionality can be used by anyone with a limited or Team Member license. Note that the drag-and-drop feature only works when you use a limited/Team Member license from Expense Management version 6.00 Service Pack 2 or later.

##Click Once requirements
When Click Once is used to distribute Microsoft Dynamics NAV or Business Central to clients, the Expense Management client components must be included in the Click Once basic image.

##Archive file server
Expense Management stores all files that are related to imported documents in an archive directory. This directory should be formatted as Windows (NTFS). 

For this archive directory, you must set the security permissions listed below. Note that this goes for *all users* when classic versions of Microsoft Dynamics NAV are used, and for the *service account* when a service tier is used:

* Modify
* Read & execute
* List folder contents
* Read
* Write

If you’re using a classic version of Microsoft Dynamics NAV and the selected directory is a network-shared folder, this folder must be accessible to all users.

> [!NOTE]
> In order for Azure Blob storage to work, the Dynamics NAV/Business Central service tier must be configured to use the TLS 1.2 security protocol.

##See also
[Minimum Requirements for Using Continia Expense Management (Online)](@EM-83)  
[Overview of Business Functionality](/Continia Expense Management/Getting Started/Business Functionality.md)  
[Requirements for Using Continia Web Approval Portal On-Premises](Web Approval Portal Requirements On-Premises.md)  
[Business Central website](https://dynamics.microsoft.com/en-us/business-central/overview/)  


<style>
  .content table tr td:nth-child(1) {
    width: 500px;
  }
  .content table tr td:nth-child(2) {
    width: 230px;
  }  
</style>