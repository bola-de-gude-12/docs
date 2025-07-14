---
title: Support for the Business Central Universal Code Initiative
date: 11-12-2024
description:
id: DC-376
lang: en
---

# Support for the Business Central Universal Code Initiative

| Feature | Public preview | General availability on-premises | General availability online |
| --- | :-: | :-: | :-: |
| Support for the Business Central Universal Code initiative | {{checkmark}} Mar 2023 | {{checkmark}} April 2023 | - |

> [!IMPORTANT]
> Unfortunately, it wasn't possible to complete this feature in time for it to be included in Continia Document Capture 2022 R2. The feature is included in Document Capture 2023 R1 instead.
>
> What effect does this have?
>
> Our interpretation is that:
> 1. This doesn't impact clients who bought Microsoft Dynamics 365 Business Central on-premises before April 2022, as they're not required to license non-Universal Code modules in their current configuration.
> 1. Clients who licensed Business Central on-premises from April 2022 onward may have to license the module “Implemented code is not cloud-optimized”. However, this module is priced at $0 in 2022 and 2023.
>
> See full details [here](https://partner.microsoft.com/en-US/resources/collection/microsoft-publisher-program#/).


## Business value

You'll be able to continue using all Document Capture on-premises features without having to pay Universal Code fees to Microsoft.

> [!IMPORTANT]
> Document Capture will now also support local file system storage using cloud-optimized code. 

## Feature details

Microsoft has introduced a new program called Business Central Universal Code initiative. The program introduces increasing fees for using non-cloud-ready code over the coming years. 
In short, end users must license a new module, “Implemented code is not cloud-optimized”, if they use non-cloud-optimized extensions. The module is free to license in 2022 and 2023. 
You can read more about the program and the prices [here](http://aka.ms/BCUniversalcode).

Today, Document Capture already supports the Business Central Universal Code Initiative when only the base Document Capture app (Continia Document Capture) is installed and used on-premises. However, if you want to use the on-premises OCR service, for example, you must also install the on-premises app (Continia Document Capture OnPremise). For more information, see [Installing Continia Document Capture On-Premises](@DC-51). 

With this feature, the base Document Capture app will be rewritten to enable you to continue using virtually all existing Document Capture features – including local file system storage – without having to pay Universal Code fees to Microsoft. As support for local file system storage using cloud-optimized code is now included in the release, you'll be able to choose the document storage option **File Service** (replacing the older **File System** storage type) without incurring Universal Code fees from Microsoft.

For more information, see [Overview of the Continia File Service](@DC-123).

## Related information

[Support for Local File System Storage with the Business Central Universal Code Initiative](@DC-377)