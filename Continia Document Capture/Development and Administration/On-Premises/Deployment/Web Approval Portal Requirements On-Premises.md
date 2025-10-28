---
title: Requirements for using the Continia Web Approval Portal on premises
date: 24-07-2025
description: A list of the requirements for using the Web Approval Portal with Business Central on premises.
id: DC-454
lang: en
---

# Requirements for using the Continia Web Approval Portal on premises
This article lists the requirements for using the Web Approval Portal with Microsoft Dynamics 365 Business Central on premises. For the online requirements, see [Minimum requirements for using Document Capture](@DC-453#continia-web-approval-portal).

Documents can be approved using either the Business Central web client or the Continia Web Approval Portal. The Web Approval Portal is built on the standard approval functionality used in Business Central, but it’s a separate service that can be accessed by licensed users from any supported web browser. [The web browsers that are supported for Continia Document Capture](/continia-document-capture/getting-started/frequently-asked-questions/minimum-requirements/additional-guidelines#browsers) are also supported for the Web Approval Portal.

Note that the Web Approval Portal is supported on mobile devices, with few exceptions. One notable exception is that styled XML files aren't displayed in the portal in mobile mode. To view an XML file on a mobile device, switch to desktop mode in your mobile browser.

## Requirements for all portal installations, regardless of hosting type

The Web Approval Portal can be hosted either by Continia (continiaonline.com) or on a local server. Both types are accessed via web browsers, so the difference only has to do with how they’re hosted. The information in this section applies to both types of hosting.

To use the Web Approval Portal on premises, you must be running Microsoft Dynamics NAV 2009 R2 or later. Certain Microsoft Dynamics NAV/Business Central web services – SOAP and OData – must be enabled too, as this is how the Web Approval Portal communicates with Dynamics NAV/Business Central.

> [!IMPORTANT]
> As the Web Approval Portal requires web services, it only works in conjunction with the runtime version of Dynamics NAV 2009 R2 or later. The runtime version enables you to use the Web Approval Portal with NAV versions older than 2009 R2.

> [!NOTE]
> Security filters are not supported in the Web Approval Portal. To control what's visible and accessible to users in the portal, use account and dimension permissions instead. These can be configured either for [individual users](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#configuring-account-and-dimension-permissions) or for [groups of users](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/approval-user-groups#to-configure-account-and-dimension-permissions-for-a-group).

In addition, you must meet the requirements listed below – depending on your version of NAV/Business Central. Note that all users must be licensed according to the Microsoft licensing terms, which may differ from version to version.

> [!IMPORTANT]
> Always consult the Microsoft licensing terms for the actual legal requirements, regardless of how these are interpreted on Continia Docs or in any other Continia documentation. In particular, check the **Team Members** section in the Microsoft Dynamics 365 Business Central Licensing Guide, available for download on the [Business Central](https://dynamics.microsoft.com/business-central/overview/) website.

Continia’s current interpretation of the Microsoft terms is as follows:

| NAV/BC version | Description |
| -------- | -------- |
| Microsoft Dynamics 365 Business Central  | Every user of Dynamic 365 Business Central must have a named user license. A “named user license” is a separate user subscription license (SL) that's specific to each user and can’t be shared with others, as opposed to [concurrent user licensing](https://en.wikipedia.org/wiki/Concurrent_user).<br /><br />For approval users that only approve documents and change purchase lines, Team Member licenses are sufficient, subject to Microsoft licensing conditions. In all other cases, Continia only supports users with Essentials or Premium licenses.<br /><br />For details about the Team Member license and how add-ons may affect the use of this, see the Microsoft Dynamics 365 Business Central Licensing Guide. You can download this guide on the [Business Central](https://dynamics.microsoft.com/business-central/overview/) website. |
| Microsoft Dynamics NAV 2013 R2 to NAV 2018 | For Microsoft Dynamics NAV 2013 R2 to NAV 2018, every user must be present in the user table, either as a Full User or a Limited User. When a user accesses the website, the user session is active for two hours for Full Users and 15 minutes for Limited Users. |
| Microsoft Dynamics NAV 2013 | Access to Microsoft Dynamics NAV 2013 requires a concurrent user license. Data requests are very limited and disconnect the NAV session immediately after the web page has been loaded. In most cases, this results in effectively only one concurrent NAV user – even though multiple web users access the site simultaneously. |
| Microsoft Dynamics NAV 2009 R2 | A Light User is required for each named web user. |

>[!NOTE]
>Users of the Web Approval Portal are also automatically able to access Business Central once they've been granted a Team Member license. The reason for this is that the Web Approval Portal is built on standard Business Central functionality and was never intended to exclude anyone from accessing Business Central.

**Supported authentication methods**

* Windows authentication 
* For Microsoft Dynamics NAV 2009 R2: only Windows authentication 
* For Microsoft Dynamics NAV 2013 and later: both Windows and NAVUserPassword authentication  
* For Microsoft Dynamics NAV 2018 and later: Office 365 authentication

As of version 1.16.0, the Web Approval Portal is able to connect with multiple NAV and/or Business Central databases at the same time, thereby enabling users from different databases to sign in simultaneously.

However, none of the previous versions of the Web Approval Portal support the simultaneous signing in of users from different databases. This means that if your organization has more than one database in Business Central and exports users from one of these databases to the Web Approval Portal, only those newly exported users are able to sign in to the Web Approval Portal – all existing users previously exported from another database are deleted from the Web Approval Portal and are unable to sign in.

**User termination**

* To prevent access to the Web Approval Portal for a specific database user, the user’s web service key in NAV must be renewed. 
* To prevent access to the Web Approval Portal for a Microsoft 365 user, the user must be disabled in Microsoft Entra (formerly known as Azure Active Directory).

## Requirements for locally hosted portal installations

As opposed to the above section, which applies to both types of hosting (continiaonline.com or local server), the following requirements only apply to locally hosted Web Approval Portal installations.

You can only use the locally hosted version of the Web Approval Portal if you’re using Business Central on premises. The server that the Web Approval Portal is installed on must have the following components installed to meet the minimum requirements:

* Windows Server 2008 R2 Service Pack 1 or later 
* Internet Information Services 7.5 or later 
* Microsoft .NET Framework 4.7.2
* The latest Windows service packs and hotfixes

In the table below, you can see what versions of NAV/Business Central are compatible with each of the two versions of the Web Approval Portal (WAP):

| Version | Older than NAV 2009 R2 runtime<a href="#footnote-1"><sup>1</sup></a> | NAV 2009 R2 runtime | Business Central cloud | Business Central on-premises |
| --- | --- | --- | --- | --- |
| WAP hosted by Continia | | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| Locally hosted WAP |  | {{checkmark}} | | {{checkmark}} |

<br>

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">Note that the runtime version enables you to use the Web Approval Portal with NAV versions older than 2009 R2.</li>
  </ol>
</div>
</small>

## Related information
[Minimum requirements for using Continia Document Capture on premises](Minimum Requirements.md)  
[Business Central website](https://dynamics.microsoft.com/business-central/overview/)  