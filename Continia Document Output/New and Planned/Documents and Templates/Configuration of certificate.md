---
title: Configuration of certificate
date: 06-03-2025
description: 
id: DO-210
lang: en
---

# Configuration of certificate

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Configuration of certificate | - | N/A |

> [!NOTE]
> This release date for the feature has been postponed. The expected release date for this feature is April/May 2025.

## Business value

This feature allows Document Output to support multiple e-signature certificates, enabling specific certificates to be assigned based on customer, document type, and recipient. By restricting merge functionality for eSign certificates, it ensures compliance by preventing multi-invoice PDFs from being signed in a single file. Additionally, it anticipates the need for re-signing documents, extending certificate validity beyond the initial 5-year period.

## Feature details

This feature enables configuration of multiple certificate methods within Document Output, allowing users to select specific certificates per customer, document type, and recipient. When eSign certificates are used, document merging is disabled to maintain legal compliance. Future support for re-signing will extend certificate validity. Continia will also provide a standardized certificate option for all users, issued by trusted providers, with verified timestamps and provider information.
