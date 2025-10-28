---
title: Setting up web approval in Document Capture
date: 25-09-2025
description:  
id: DC-76
lang: en
---

# Setting up web approval

Documents can be approved using either the Microsoft Dynamics 365 Business Central web client or the Continia Web Approval Portal. The Web Approval Portal is built on the standard approval functionality used in Business Central, but it’s a separate service that can be accessed by licensed users from [any supported web browser](/continia-document-capture/getting-started/frequently-asked-questions/minimum-requirements/additional-guidelines#browsers).

> [!IMPORTANT]
> Although users of the Web Approval Portal need no access to Business Central whatsoever, they will in fact automatically be able to access it once they've been granted a license for the portal (typically a Team Member license). The reason for this is that the Web Approval Portal is built on standard Business Central functionality and was never intended to exclude anyone from accessing Business Central.

The Web Approval Portal can be hosted either by Continia (continiaonline.com) or by your own organization on a local server. Both types are accessed via web browsers, so the difference only has to do with how they’re hosted. Which of the two types of hosting you can use depends on your Business Central deployment:

* **If you’re using Business Central online**, you can't use the locally hosted version of the Web Approval Portal – only the Continia-hosted version can be used.
* **If you’re using Business Central on-premises**, you can use either the locally hosted version or the Continia-hosted version of the Web Approval Portal.

This means that there are slight differences in the way you set up the Web Approval Portal, depending on your overall setup. For more details on how to set up the Web Approval Portal, see the links provided in the table below:

| To | See |
| --- | --- |
| Enable the approval portal for online installations of Business Central | [Enabling the Web Approval Portal for Business Central online](@DC-480) |
| Enable the approval portal and set up portal connections and environments for on-premises installations of Business Central | [Enabling the Web Approval Portal for Business Central on premises](@DC-481) |
| Determine what each individual user can do with the Web Approval Portal | [Configuring users for the Web Approval Portal](@DC-129) |
| Customize the overall appearance of the approval portal and edit its basic settings | [Customizing the Web Approval Portal](@DC-164) |

## Related information

[Requirements for using the Continia Web Approval Portal online](@DC-453#continia-web-approval-portal)  
[Requirements for using the Continia Web Approval Portal on premises](@DC-454)  