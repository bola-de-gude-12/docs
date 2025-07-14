---
title: Enhanced XML Export Code
date: 05-03-2025
description: 
id: DO-218
lang: en
---

# Enhanced XML Export Code

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Enhanced XML export code | - | N/A |

> [!NOTE]
> The release of this feature has been postponed. A new release date has not yet been determined.

## Business value

With this new implementation of XML handling in Document Output, customers will benefit from a more unified and maintainable system that aligns with the eDocuments feature set from Document Capture. This transition ensures a consistent feature set across both solutions, streamlining development and support efforts. Additionally, by providing a feature option to switch to the new codebase at the customer's discretion, businesses can prepare for the transition without immediate disruption. This approach allows partners to adapt custom event handlers as needed before making the switch, reducing the risk of unexpected changes in functionality.

## Feature details

In future versions of Document Output, XML handling will be migrated to the same codebase as used in eDocuments, ensuring a shared feature set wherever possible. This transition introduces improvements in maintainability and compatibility across Continia solutions but may impact existing custom event handlers utilized by customers.

To mitigate potential disruptions, the transition will be implemented as an optional feature within Document Output. Customers can choose to adopt the new codebase, gaining access to future code fixes and new features, while retaining the ability to adapt or re-implement event handlers as needed. Those who opt to remain on the existing implementation can do so; however, minor fixes and updates will no longer be applied to the legacy codebase. This approach provides flexibility while encouraging a structured migration to the new XML handling framework.