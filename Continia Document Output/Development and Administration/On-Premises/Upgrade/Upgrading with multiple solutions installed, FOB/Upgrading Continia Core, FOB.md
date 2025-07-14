---
title: Upgrading Continia Core (FOB)
date: 10-07-2024
description:  
lang: en
---

# Upgrading Continia Core (FOB)

Continia Core is a module that's essential in order for all Continia solutions to function properly. It's used for activation and for registering consumption but also includes a range of other very important features used by multiple Continia solutions, such as frameworks for handling telemetry and web communication. For more information, see [Understanding Continia Core](@DO-113).

> [!NOTE]
> Continia Core objects are included in the FOB files for all Continia products.

Although the module is designed to be backward- and forward-compatible, we strongly recommend that you always install the latest version of it whenever you install a new Continia solution or upgrade one or more of your existing solutions for any FOB version of Microsoft Dynamics 365 Business Central.

## Installing the latest version of Continia Core

When you upgrade a Continia solution to a later version or service pack, you must import objects using the **Import Worksheet**. As you do this, make sure that the latest version of Continia Core is selected for all objects displayed in the worksheet. Continia Core objects have the following version list structure: 

* `CC[localization][NAV version].[major version].[service pack].[hotfix]`

To illustrate what this structure translates into in practice, the following table provides two examples of actual version lists:

<br>

| Version | Version list |
| --- | --- |
| Continia Core version 1, service pack 1, for Microsoft Dynamics NAV 2018, W1 localization | CCW111.00.00.1.01 |
| Continia Core version 1, service pack 2, hotfix 1, for Microsoft Dynamics NAV 2018, DK localization | CCDK11.00.00.1.02.01 |

<br>

Normally, we recommend that you select **Replace All** when importing objects in connection with a Continia product upgrade. However, this is not necessarily the case for Continia Core objects, as you must always have the latest versions of these objects installed and product packages sometimes include older Continia Core objects. You can use the built-in intelligence of the **Import Worksheet** to determine when you should – and when you shouldn't – replace all objects, as illustrated in the following examples:

### Example 1

In this scenario, the task is to upgrade Continia Document Capture to version 6.50.03 in a system that has the following applications installed: 

* Continia Document Capture 6.00.05
* Continia Document Output 4.00
* Continia Payment Management 4.01
* Continia Core 4.01 

The Document Capture 6.50.03 product package contains objects for version 3.00.03 of Continia Core, meaning that the product package objects are older than the ones already installed in the system. The **Import Worksheet** will automatically detect this and set the **Action** to **Skip** (rather than **Replace**), which means that you should *not* replace all Continia Core objects but simply select **OK** instead.

### Example 2

In this scenario, the task is to upgrade Document Capture to version 8.01 in a system that has the following applications installed:

* Document Capture version 7.01
* Document Output 4.00
* Payment Management 4.01
* Continia Core 4.01 

The Document Capture 8.01 product package contains objects for version 5.01 of Continia Core, meaning that the product package objects are newer than the ones already installed in the system. The **Import Worksheet** will automatically detect this and set the **Action** to **Replace** (rather than **Skip**), which means that you can select **Replace All** to replace all Continia Core objects.

## See also

[Understanding Continia Core](@DO-113)  