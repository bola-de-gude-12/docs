---
title: Scope of support services for Document Capture
date: 26-05-2025
id: DC-12
lang: en
description: What versions of Document Capture are supported, and until when.
---

# Scope of support services

Continia software is known for its excellent support, and always strives to help partners to the greatest extent possible. However, the combination of somewhat limited capacity and an ever-increasing demand for support often makes it necessary to control what support is provided to whom, in order to ensure that partners with critical issues and issues relating to supported versions of Continia Document Capture get the excellent support they've come to expect.

This article details what types of support Continia does and doesn't provide, thereby making it easier for you as a partner to understand when to rely on Continia for help, what Document Capture versions are supported – and what's outside the scope of support. The article also ensures that you know what skills you must possess to support any Microsoft Dynamics NAV or Business Central installation with Document Capture installed.

> \[!NOTE] With its 2024 spring release, Document Capture made a version leap from 12.00 to 24.00, meaning that versions 13.00–23.00 don't exist and never will. This was done in order to align the versioning of Document Capture with that of Microsoft Dynamics 365 Business Central.

## What does Continia support?

Continia provides ongoing support of all Document Capture releases for at least two years after each release date. Currently, the following versions of Document Capture are supported:

\


| Version                          | Release date | Support end date |
| -------------------------------- | ------------ | ---------------- |
| Document Capture 2025 R1 (26.00) | Apr 1, 2025  | Apr 1, 2027      |
| Document Capture 2024 R2 (25.00) | Oct 1, 2024  | Oct 1, 2026      |
| Document Capture 2024 R1 (24.00) | Apr 2, 2024  | Apr 2, 2026      |
| Document Capture 2023 R2 (12.00) | Oct 1, 2023  | Oct 1, 2025      |

\


Support for the following versions of Document Capture has recently ended:

\


| Version                          | Release date | Support end date |
| -------------------------------- | ------------ | ---------------- |
| Document Capture 2023 R1 (11.00) | Apr 1, 2023  | Apr 1, 2025      |
| Document Capture 2022 R2 (10.00) | Oct 1, 2022  | Oct 1, 2024      |
| Document Capture 2022 R1 (9.00)  | Mar 1, 2022  | Mar 1, 2024      |
| Document Capture 2021 R2 (8.00)  | Sep 1, 2021  | Sep 1, 2023      |

Upgrading to a supported Document Capture version is strongly recommended when end users using an unsupported version either 1) encounter issues that haven't been corrected in a service pack for the old version or 2) will clearly benefit from the enhanced functionality of the newer version.

Also, upgrading both the Document Capture and ABBYY OCR services, as well as the on-premises Continia Web Approval Portal, is recommended when end users experience issues using any of these components.

For all supported versions of Document Capture, service packs are released on an ongoing basis to ensure that any errors are corrected. It's highly recommended that you as a partner implement these service packs regularly. This is easy to do no matter if your version of Document Capture is FOB-based or app-based. For FOB-based versions, you only need to import new objects, and no data conversion is required – while app-based versions simply require you to upgrade the app as described in [Upgrading Continia Document Capture for app versions of Business Central](../../../Continia%20Document%20Capture/Development%20and%20Administration/Development%20and%20customization/@DC-6/).

With each service pack, end users of Document Capture get easy and quick access to all corrections and improvements in one go, thereby significantly increasing the stability of their systems. For more information about how to implement a service pack, see [Implementing service packs](../../../Continia%20Document%20Capture/Development%20and%20Administration/Development%20and%20customization/@DC-167/).

> \[!IMPORTANT] Individual patches and bug fixes can't be provided separately, so if you would like to implement a specific bug fix, you must install the service pack that it's part of.

When a client identifies an issue in a supported version of Document Capture and it's likely the problem is caused by Document Capture code, Continia offers help, debugging assistance, and determination of whether the issue was caused by a bug in Document Capture. If this is considered unlikely, you as a partner must document that the issue was indeed caused by Document Capture and not by standard NAV/Business Central functionality or by the presence of any other add-ons, extensions, or customizations.

When a Document Capture bug causes an issue, Continia makes sure that the issue is corrected as fast as possible – provided that it's a critical issue (one that blocks essential business processes and has no known workarounds). If the issue is non-critical, it's corrected in an upcoming service pack instead.

**For supported versions of Document Capture**, Continia provides support covering the following components and scenarios:

* Help and debugging assistance when errors occur in the Document Capture code
* Help and advice concerning functionality that doesn't work as intended
* Errors in add-ins
* Incorrect recognition of text in PDF and XML files
* Performance issues related to Document Capture functionality
* Support for the on-premises Continia Web Approval Portal
* Support for the Document Capture OCR service, including ABBYY

**For unsupported versions of Document Capture**, Continia provides support covering the following components and scenarios:

*   Questions about Document Capture functionality - all questions about the functionality of any version of Document Capture are answered to the extent that the Continia staff is capable of answering them without in-depth research. If the staff doesn't know the immediate answer to a question relating to an unsupported version of Document Capture, the staff will instead explain how the corresponding functionality works in a supported version.

    > \[!NOTE] Continia doesn't spend time investigating the operability of old, unsupported versions of Document Capture.
*   Questions about Document Capture errors - all questions about specific Document Capture errors are answered to the extent that the Continia staff is capable of answering them without in-depth research. If the staff doesn't know the immediate answer to a question relating to an unsupported version of Document Capture, the staff will instead explain how to deal with the error in a supported version.

    > \[!NOTE] Continia doesn't spend time investigating why the error occurs in old, unsupported versions of Document Capture.
* Questions and issues related to:
  * Activation
  * Communication with Continia Online, including export of users, download of emails, and activation of missing email domains in Continia online
* Questions about any of the following:
  * Demo licenses and the issuing of new demo licenses
  * The licensing of Document Capture and the Continia Web Approval Portal
  * Client credentials
  * How to upgrade Document Capture
  * What to do and consider when renaming companies
  * Add-in errors
  * The Document Capture Service, including upgrading
  * ABBYY, including upgrading
  * The OCR Engine and incorrect recognition of text in PDF files, including missing or misplaced files (files ending up in the error folder or never appearing in NAV/Business Central)
* The online Continia Web Approval Portal, including:
  * Login issues
  * Reset of passwords
  * Permission errors
  * Problems performing specific actions, such as errors in connection with invoice approval
  * Performance issues

## What does Continia not support?

Continia doesn't support issues relating to NAV/Business Central code for unsupported versions of Document Capture. This means that for these versions, Continia does not help debug any issues in NAV/Business Central or develop hotfixes for errors in the code. If an error is identified in an unsupported version of Document Capture, customers must either upgrade to a supported version or correct the issue themselves. If the error is still present in a supported version of Document Capture, it's only corrected in the supported version.

**For any version of NAV/Business Central or any version of Document Capture**, Continia doesn't support any of the following:

* Standard NAV/Business Central errors
* Issues likely to be caused by infrastructure, including network configuration, firewalls, and proxy servers
* Email exchange, except if an email sent directly to the Continia Cloud OCR email service doesn't arrive in NAV/Business Central
* Problems with emails that arrive when _sent_ directly to the Continia Cloud OCR email service but not when they're forwarded to the Cloud OCR email service
* Estimation of time required to implement or upgrade Document Capture
* Help and assistance in customizing Document Capture – just as for standard NAV/Business Central, partners are expected to know the solution and/or have the skills to investigate how it works when customizations are to be made
* Customization of the Continia Web Approval Portal

**For unsupported versions of Document Capture**, in addition to the above, Continia doesn't support any of the following:

* Errors in the Document Capture NAV/Business Central code, including debugging assistance
* Performance issues
* Issues with functionality that doesn't work as expected
* Incorrect recognition of text in PDF and XML files
* Issues with the on-premises Continia Web Approval Portal
* Issues with the Document Capture OCR service, including ABBYY

## Related information

\[Resources for help and support]\(/Continia Document Capture/Getting Started/Help and Support.md)\
[How to implement a service pack](https://continia.zendesk.com/hc/en-us/articles/360001183609-How-to-implement-a-Service-Pack)\
[Software lifecycle policy and Continia Document Capture on premises](../../../Continia%20Document%20Capture/Development%20and%20Administration/Development%20and%20customization/@DC-13/)
