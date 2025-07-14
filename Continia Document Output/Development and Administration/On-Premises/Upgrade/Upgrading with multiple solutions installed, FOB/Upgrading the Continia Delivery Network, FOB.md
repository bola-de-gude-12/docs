---
title: Upgrading the Continia Delivery Network (FOB)
date: 10-07-2024
description:
id: DO-114
lang: en
---

# Upgrading the Continia Delivery Network (FOB)

The Continia Delivery Network is a module that's currently used by Continia Document Capture and Continia Document Output. The module allows you to integrate with the PEPPOL eDelivery Network, thereby enabling your vendors to import or export business documents via this. For example, any vendor that's connected to the PEPPOL eDelivery Network can send documents into Continia Document Capture via this network using the Continia Delivery Network. For more information, see [Understanding the Continia Delivery Network](@DO-122).

> [!NOTE]
> Continia Delivery Network objects are included in the FOB files for Document Capture and Document Output.

Although the module is designed to be backward- and forward-compatible, we strongly recommend that you always install the latest version of it whenever you install a new Continia solution or upgrade one or more of your existing solutions for any FOB version of Microsoft Dynamics 365 Business Central.

## Installing the latest version of the Continia Delivery Network

When you upgrade a Continia solution to a later version or service pack, you must import objects using the **Import Worksheet**. As you do this, make sure that the latest version of the Continia Delivery Network is selected for all objects displayed in the worksheet. Continia Delivery Network objects have the following version list structure: 

* `DN[localization][NAV version].[major version].[service pack].[hotfix]`

To illustrate what this structure translates into in practice, the following table provides two examples of actual version lists:

<br>

| Version | Version list |
| --- | --- |
| Continia Delivery Network version 1, service pack 1, for Microsoft Dynamics NAV 2018, W1 localization | DNW111.00.00.1.01 |
| Continia Delivery Network version 1, service pack 2, hotfix 1, for Microsoft Dynamics NAV 2018, DK localization | DNDK11.00.00.1.02.01 |

<br>

Normally, we recommend that you select **Replace All** when importing objects in connection with a Continia product upgrade. However, this is not necessarily the case for Continia Delivery Network objects, as you must always have the latest versions of these objects installed and product packages sometimes include older Continia Delivery Network objects. You can use the built-in intelligence of the **Import Worksheet** to determine when you should – and when you shouldn't – replace all objects, as illustrated in the following examples:

### Example 1

In this scenario, the task is to upgrade Continia Document Output to version 3.27 in a system that has the following applications installed:

* Continia Document Capture 7.01
* Continia Delivery Network 1.01
* Continia Document Output 3.26 

The Document Output 3.27 product package contains objects for version 1.00.02 of the Continia Delivery Network, meaning that the product package objects are older than the ones already installed in the system. The **Import Worksheet** will automatically detect this and set the **Action** to **Skip** (rather than **Replace**), which means that you should *not* replace all Continia Delivery Network objects but simply select **OK** instead.

### Example 2

In this scenario, the task is to upgrade Document Output to version 5.01 in a system that has the following applications installed:

* Document Capture 7.01
* Continia Delivery Network 1.01
* Document Output 3.27

The Document Output 5.01 product package contains objects for version 2.01 of the Continia Delivery Network, meaning that the product package objects are newer than the ones already installed in the system. The **Import Worksheet** will automatically detect this and set the **Action** to **Replace** (rather than **Skip**), which means that you can select **Replace All** to replace all Continia Delivery Network objects.

## See also

[Understanding the Continia Delivery Network](@DO-122)  