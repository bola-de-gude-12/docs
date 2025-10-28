---
title: Implementing service packs
description: 
date: 03-06-2025
id: DC-167
lang: en
---

# Implementing service packs

> [!NOTE]
> This article describes the process of implementing service packs for FOB versions of Microsoft Dynamics NAV/365 Business Central. For information on how to implement service packs for app versions, see [Upgrading Continia Document Capture for app versions of Business Central](@DC-6).

Since the release of Continia Document Capture version 4.50, Continia has regularly released service packs containing code corrections. The service packs are easy to implement, they require no data conversion, and you only have to import new objects, so we strongly encourage all Continia partners to implement them on a regular basis. 

Each service pack brings a lot of new features and bug fixes to Document Capture and significantly improves your overall user experience. As an example, service packs 1 to 3 for Document Capture 2022 R2 (v10.00) included more than 170 improvements, resulting in a noticeably more stable and feature-rich system compared to previous versions.

Continia generally releases new service packs when:

* Enough issues have been corrected to justify the release of a service pack.
* A critical issue has been identified and corrected.

After each release of a new major version of Document Capture, service packs are released at intervals of 2-3 months, or whenever critical issues are corrected. However, the frequency with which service packs are released typically decreases over time. Continia continues to release service packs for the two latest versions of Document Capture as long as critical issues are identified.

## To implement a service pack

You can implement a service pack by following these steps:

1. Go to the [Continia PartnerZone](https://partnerzone.continia.com/downloads/) (only available to partners).
1. In the **Downloads** section, identify the service pack that you want to download, and then click **Download**.
1. The downloaded ZIP file contains the entire product folder. Go to the **..\Objects\Document Capture** folder to locate the Document Capture objects. Note that the object files contain all document objects.
1. Extract the service pack objects from the object files.
1. Import the objects into NAV/Business Central using the **Object Designer**.

The service pack is now implemented and ready for use.

## Related information

[Upgrading to the latest version](@DC-58)  
[Software lifecycle policy and Continia Document Capture on premises](@DC-13)  
[Requesting events and external functions](@DC-27)  