There's a significant difference between running Document Capture in the on-premises version of Microsoft Dynamics 365 Business Central and using it online in the cloud version. This article describes the minimum requirements and things to note when running Document Capture in Business Central online. For the on-premises requirements, see [Minimum requirements for using Continia Document Capture on premises](@DC-135).

> [!IMPORTANT]
> As Document Capture is an integrated part of Business Central, the minimum requirements for Business Central also apply to Document Capture.

## Local scanner requirements 
Document Capture supports the scanning of documents using a local desktop scanner connected to a computer. This requires a separate Continia application to be installed as well as a TWAIN-compatible scanner. When you use the Business Central web client, both 32- and 64-bit versions of the Twain scanner driver are supported. However, note that 32-bit TWAIN scanner drivers are only supported in Document Capture 2021 R1 Service Pack 2 and later. For details on how to run the Document Capture Scanner Service as a 32-bit application, see [How to alter the Document Capture Scanner Service to run as 32-bit application](https://continia.zendesk.com/hc/en-us/articles/360022114180-How-to-alter-the-Document-Capture-Scanner-Service-to-run-as-32-bit-application).

> [!NOTE]
> When scanning multiple documents in one go, you must separate each of the documents with a blank page.

## Email requirements
You import documents into Document Capture simply by sending them via email to a predefined email address hosted by Continia. See [Additional guidelines for using Continia Document Capture](@DC-452) for technical requirements and things to note.

## PDF requirements
When you import PDF documents into Document Capture, we recommend that you send each document as a separate PDF file. However, it’s possible to [split a PDF file](/Continia Document Capture/Business functionality/Documents and templates/Splitting and merging documents.md) consisting of multiple documents automatically based on different criteria, for example based on barcode or invoice number.

The version of the PDF file must be PDF 1.7 or earlier, and it must conform to the PDF/A standard. Note that handwritten text isn't supported and is unlikely to be recognized well.

The following limitations also apply:

* Encrypted/password-protected PDF files are not supported.
* PDF files with electronic signatures may be processed successfully but are generally not supported.
* PDF files using the Adobe XML Forms Architecture (XFA) format are not supported.
* The maximum number of pages that can be processed for PDF files is 500.

To process files with any of these properties, you must republish them as new PDF files. You can do this using, for example, **Microsoft Print to PDF**, which is available for free in Windows 10. Republishing the files as new PDFs will remove the added features and produce 'flat' PDF files with no interactive elements.

## Continia Web Approval Portal 
Documents can be approved using either the Business Central web client or the Continia Web Approval Portal. The Web Approval Portal is built on the standard approval functionality used in Business Central, but it’s a separate service that can be accessed by licensed users from any supported web browser. [The web browsers that are supported for Continia Document Capture](/continia-document-capture/getting-started/frequently-asked-questions/minimum-requirements/additional-guidelines#browsers) are also supported for the Web Approval Portal.

Note that the Web Approval Portal is fully supported on mobile devices, with very few exceptions. One notable exception is that styled XML files aren't displayed in the portal in mobile mode, so if you want to view an XML file on a mobile device, we recommend that you switch to desktop mode in your mobile browser.

> [!NOTE]
> The Web Approval Portal can be hosted either by Continia (continiaonline.com) or on a local server. Both types are accessed via web browsers, so the difference only has to do with how they’re hosted. Note that you can't use the locally hosted version of the Web Approval Portal if you’re using Business Central online – only the Continia-hosted version of the Web Approval Portal can be used in conjunction with Business Central online.

To access the Web Approval Portal, you must be an authenticated Business Central user and have a named user license for Business Central. A “named user license” is a separate user subscription license (SL) that’s specific to each user and can’t be shared with others, as opposed to [concurrent user licensing](https://en.wikipedia.org/wiki/Concurrent_user). User SLs are the primary type of licenses for Business Central.

For approval users that only approve documents and change purchase lines, Team Member licenses are sufficient, subject to Microsoft licensing conditions (see below). In all other cases, Continia only supports users with Essentials or Premium licenses. For details about the Team Member license and how add-ons may affect the use of this, see the Microsoft Dynamics 365 Business Central Licensing Guide. You can download this guide on the [Business Central](https://dynamics.microsoft.com/business-central/overview/) website.

Note that users of the Web Approval Portal will also automatically be able to access Business Central once they've been granted a Team Member license. The reason for this is that the Web Approval Portal is built on standard Business Central functionality and was never intended to exclude anyone from accessing Business Central.

> [!IMPORTANT]
> Please always consult the Microsoft licensing terms for the actual legal requirements, regardless of how these are interpreted on Continia Docs or in any other Continia documentation. In particular, check the **Team Members** section in the Microsoft Dynamics 365 Business Central Licensing Guide, available for download on the [Business Central](https://dynamics.microsoft.com/business-central/overview/) website.

> [!IMPORTANT]
> As of version 1.16.0, the Web Approval Portal is able to connect with multiple NAV and/or Business Central databases at the same time, thereby enabling users from different databases to sign in simultaneously.
>
> However, all previous versions of the Web Approval Portal don't support the simultaneous signing in of users from different databases. This means that if your organization has more than one database in Business Central and exports users from one of these databases to the Web Approval Portal, only those newly exported users are able to sign in to the Web Approval Portal – all existing users previously exported from another database will be deleted from the Web Approval Portal and unable to sign in.

> [!NOTE]
> Security filters are currently not supported in the Web Approval Portal. If you want to control what's visible and accessible to users in the portal, use account and dimension permissions instead. These can be configured either for [individual users](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/continia-user-setup-for-approvals#configuring-account-and-dimension-permissions) or for [groups of users](/continia-document-capture/setting-up-document-capture/setting-up-document-approval/approval-user-groups#to-configure-account-and-dimension-permissions-for-a-group).

## Azure Blob Storage
For newer versions of Microsoft Dynamics NAV/Business Central (NAV 2013 or later), Document Capture supports archiving of document files using Azure Blob Storage. For more information on Azure Blob Storage, including details on pricing and configuration, see [Azure Blob Storage](https://azure.microsoft.com/en-us/services/storage/blobs/) (Microsoft article).

In order for Azure Blob storage to work, the Dynamics NAV/Business Central service tier must be configured to use the TLS 1.2 security protocol. For further setup details, see [Setting up Azure Blob Storage](/Continia Document Capture/Development and Administration/Setting up Azure Blob storage.md).

> [!IMPORTANT]
> It's strongly recommended that you enable [blob soft delete](https://docs.microsoft.com/en-us/azure/storage/blobs/soft-delete-blob-overview) for your Azure Blob Storage accounts, as this allows you to restore any documents or files that were deleted or overwritten by accident.

> [!CAUTION]
> It's crucial that Document Capture has full read/write/delete access to the relevant blob container. For example, configuring access policies with time-based retention isn't supported, and neither are immutability and legal hold. 

Continia has no further minimum requirements for the use of Azure Blob Storage to store Document Capture files. For any specific questions or requests regarding Azure – including setup, subscription types, and general architecture – please refer to Microsoft.

## Additional guidelines 
A number of other requirements and recommendations are relevant to mention, as they have an impact on how well Document Capture performs and how the app is used. These can all be found in [Additional guidelines for using Continia Document Capture](../additional-guidelines).

## Related information
[Additional guidelines for using Continia Document Capture](../additional-guidelines)  
[Overview of business functionality](/Continia Document Capture/Getting Started/Business Functionality.md)  
[Unsupported standard features](@DC-134)  
[Business Central website](https://dynamics.microsoft.com/business-central/overview/)  