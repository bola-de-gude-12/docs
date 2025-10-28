---
title: Automatic Deactivation of Continia Solutions When Copying Companies
date: 26-11-2024
description:
id: DC-255
lang: en
---

# Automatic Deactivation of Continia Solutions When Copying Companies

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Automatic deactivation of Continia solutions when copying companies | - | {{checkmark}} Jun 2023 |

## Business value

By automatically deactivating your Continia solutions whenever a company is copied in on-premises versions of Microsoft Dynamics 365 Business Central, Continia Document Capture will ensure that there's no uncertainty about where to route incoming documents. This may be an issue when two completely identical companies exist in current installations, but with the introduction of this new feature, such issues should be eliminated entirely. By extension, the feature will also save you significant amounts of time, as you'll no longer have to deactivate your solutions manually to avoid any such issues.

## Feature details

Currently, when you use standard Business Central functionality to copy a company for on-premises versions of Business Central, the company is copied one to one with all existing settings and data, including your Continia solutions. With this new feature, all Continia solutions will be automatically deactivated in the copied company once the copy is made. In this way, the on-premises functionality for Continia solutions is brought up to par with that of online installations, and you'll avoid having documents routed to the wrong companies and any similar confusion.

For more information, see [To copy a company for use as an active company](@DC-151#to-copy-a-company-for-use-as-an-active-company).