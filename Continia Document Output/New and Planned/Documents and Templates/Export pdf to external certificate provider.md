---
title: Export PDF to External Certificate Provider 
date: 14-08-2024
description: 
id: DO-41
lang: en
---

# Export PDF to External Certificate Provider 

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Export PDF to external certificate provider | - | N/A |

> [!NOTE]
> Continia hasn't been able to get clarification on all the legal requirements for the French market in time for version 25.00. Therefore, the plan is to release this feature as part of a service pack.

## Business value

In some countries, it's required to employ additional security ensuring the validity of sent PDF files. France, for instance, has a particular requirement that all sent PDF files have a timestamp from a RGS2 certificate provider.

The feature is expected to be a closed add-on feature, as usage will carry a cost. There is no limitation to France, so the feature can be enabled in all countries where Document Output is available.

## Feature details

This feature will add the ability to make use of a RGS2 certificate provider. In essence, you send a generated PDF file to a RGS2 certificate provider, and they send it back with a RGS2 certificate attached to the file.

As use of this feature will carry a cost per document, it will also be possible to enable it for receiver setups only, where requested. It's expected to be enabled on Output Profiles as an additional option.
