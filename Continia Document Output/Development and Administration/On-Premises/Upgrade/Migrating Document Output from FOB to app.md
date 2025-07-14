---
title: Migrating Document Output from FOB to App for Business Central On-Premises
date: 30-06-2021
description:  
lang: en
---

# Migrating Document Output from FOB to App for Business Central On-Premises

This article enables you to transfer your Continia Document Output data from a FOB-based version of Document Output to an app-based version that's compatible with Microsoft Dynamics 365 Business Central 2019 release wave 2 (v15) or later.

> [!NOTE]
> Note that in order to use Continia Document Output at all, you must be running Microsoft Dynamics NAV 2013 or later. The following guide assumes that this prerequisite has been met and, more specifically, that you're using a version in the range NAV 2013 to Business Central April 2019 (v14).

## To migrate from FOB to app

1. Upgrade your old FOB-based version of Document Output to the latest version: Go to the [Continia PartnerZone](https://partnerzone.continia.com/dashboard/) > **Downloads**, and download the relevant "FOB" product package. Using the setup guide from the product package, install Document Output as usual. This will automatically upgrade your software.
1. Upgrade to your desired Business Central version (Business Central 2019 release wave 2 or later), using [this Microsoft guide](https://docs.microsoft.com/dynamics365/business-central/dev-itpro/upgrade/upgrading-to-business-central).
1. Install the latest Document Output app: Go to the [Continia PartnerZone](https://partnerzone.continia.com/dashboard/) > **Downloads**, and download the relevant "APP" product package. Using the setup guide from the product package, install Document Output as usual. This will automatically upgrade your software.

When you install the app in the database that contains the old Document Output tables, the data will automatically be migrated to the new app tables.

> [!NOTE]
> Following any upgrade, you must download a new developer and customer license from Microsoft in order to obtain permissions for all new object numbers.

## See also
[Upgrading to Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/dev-itpro/upgrade/upgrading-to-business-central) (Microsoft article)  