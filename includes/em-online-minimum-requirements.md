There's a significant difference between running Expense Management in the on-premises version of Microsoft Dynamics 365 Business Central and using it online in the cloud version. This article describes the minimum requirements and things to note when running Expense Management in Business Central *online*. You can find the _on-premises_ requirements [here](/Continia Expense Management/Development and Administration/On-premises/Deployment/Minimum Requirements.md).

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
* Business Central (web client and mobile app) – used by approvers and admins

**The Expense App** is a dedicated mobile app that's fully supported on mobile devices. For more information, see below under [Continia Expense App](#continia-expense-app).

**The Expense Portal** can, technically speaking, also be accessed on mobile devices, but this is not recommended, as it's *not* optimized for mobile. When you use mobile devices to submit expenses, we therefore recommend using the dedicated mobile Expense App instead.

> [!TIP]
>Use the dedicated mobile Expense App instead of the Expense Portal to submit expenses on mobile devices.

**As for the Web Approval Portal**, this is fully supported on mobile devices. The Web Approval Portal is a dedicated Continia client, so the use of this lies outside of Business Central. More information can be found below under [Continia Web Approval Portal](#continia-web-approval-portal).

**Business Central** is generally optimized for mobile and easily accessible on mobile devices, but the look and feel is different from when you use it on a computer. While most Expense Management features in Business Central will indeed work on mobile devices, this isn’t officially supported, meaning that not all functionality is available in the mobile version of Business Central.

## Continia Expense App
The Expense App is compatible with any Android or iOS device that meets the following software requirements:

**Android:**  
Versions supported: 9.0 or later versions.  
Click [here](https://www.continia.com/continia-expense-app/) to install the app on your device.

**iPhone:**  
Versions supported: iOS 14 or later versions.  
Click [here](https://www.continia.com/continia-expense-app/) to install the app on your device.

## Continia Web Approval Portal 
Documents can be approved using either the Business Central web client or the Continia Web Approval Portal. The Web Approval Portal is built on the standard approval functionality used in Business Central, but it’s a separate service that can be accessed by licensed users from any supported web browser. [The web browsers that are supported for Continia Expense Management](/continia-expense-management/getting-started/troubleshooting-and-faqs/minimum-requirements#browsers) are also supported for the Web Approval Portal.

> [!NOTE]
> Security filters are currently not supported in the Web Approval Portal.

The Web Approval Portal can be hosted either by Continia (continiaonline.com) or on a local server. Both types are accessed via web browsers, so the difference only has to do with how they’re hosted. Note that you can't use the locally hosted version of the Web Approval Portal if you’re using Business Central online – only the Continia-hosted version of the Web Approval Portal can be used in conjunction with Business Central online.

To access the Web Approval Portal, you must be an authenticated Business Central user and have a named user license for Business Central.  A “named user license” is a separate user subscription license (SL) that’s specific to each user and can’t be shared with others, as opposed to [_concurrent user licensing_](https://en.wikipedia.org/wiki/Concurrent_user). User SLs are the primary type of licenses for Business Central.

Only users with a Full/Essential/Premium license can change allocations on documents.

For approval users that only approve documents, Team Member licenses should be sufficient, subject to Microsoft licensing conditions (see below). In all other cases, Continia only supports users with Essentials or Premium licenses. For details about the Team Member license and how add-ons may affect the use of this, see the Microsoft Dynamics 365 Business Central Licensing Guide. You can download this guide on the [Business Central](https://dynamics.microsoft.com/business-central/overview/) website.

> [!IMPORTANT]
> Please always consult the Microsoft licensing terms for the actual legal requirements, regardless of how these are interpreted on Continia Docs or in any other Continia documentation. In particular, check the **Team Members** section in the Microsoft Dynamics 365 Business Central Licensing Guide, available for download on the [Business Central](https://dynamics.microsoft.com/business-central/overview/) website.

> [!IMPORTANT]
> As of version 1.16.0, the Web Approval Portal is able to connect with multiple NAV and/or Business Central databases at the same time, thereby enabling users from different databases to sign in simultaneously.
>
> However, no previous version of the Web Approval Portal supports the simultaneous signing in of users from different databases. This means that if your organization has more than one database in Business Central and exports users from one of these databases to the Web Approval Portal, only those newly exported users are able to sign in to the Web Approval Portal – all existing users previously exported from another database will be deleted from the Web Approval Portal and unable to sign in.

## Related information
[Overview of Business Functionality](/Continia Expense Management/Getting Started/Business Functionality.md)  
[Business Central website](https://dynamics.microsoft.com/business-central/overview/)  