---
title: Supported on-premises versions for Document Capture
date: 11-07-2025
description: An overview of the supported on-premises versions of NAV and Business Central.
id: DC-44
lang: en
---

# Supported on-premises versions of NAV and Business Central
This page provides an overview of all supported on-premises versions of Microsoft Dynamics NAV and Microsoft Dynamics 365 Business Central. For information on what countries/regions Continia Document Capture is available in and what languages are supported for these on-premises versions, see [Country/Regional availability and supported languages for FOB](Countries and languages On-Premises.md). For information on the types of support Continia does and doesn't provide, see [Scope of support services](@DC-12).

> [!NOTE]
> Up until Document Capture 2024 R2 (25.00), every new major version of Document Capture was released for the last three major versions of Business Central and for Business Central April 2019 (BC v14). However, Document Capture 2025 R1 (26.00) was only released for the last three major versions of Business Central – that is, not including Business Central April 2019 (BC v14).
>
> Older versions of NAV/Business Central are still supported through the release of service packs for older Document Capture versions.

Note that Continia only releases code for major FOB versions (RTM) of NAV/Business Central. If Microsoft releases a cumulative update (CU) that renders any Continia code nonfunctional, Continia doesn't release code for this CU. In such cases, you must instead ask your Continia partner to perform any necessary code changes in order to make your Continia software fully functional again.

As regards app versions of Business Central, Continia releases code for all available CUs whenever a version of Document Capture is released (applies to both major versions and service packs). Each newly released CU from Microsoft is only supported as of the next service pack released by Continia. If you need to upgrade to a currently unsupported Business Central CU – the latest one, for example – and can't wait until Continia has released a Document Capture service pack that supports this, please reach out to the Continia support team by creating a support ticket. Continia will then provide you with a fully functional package that supports the relevant Business Central CU.

> [!NOTE]
> Although versions 13 and 14 of Business Central (Business Central October 2018 and Business Central April 2019) both came in app-based versions in addition to the FOB-based ones, Continia only supports apps as of Business Central 2019 release wave 2 (BC v15) CU1.

## Compatibility matrix

The following table provides an overview of what versions of Document Capture (DC) are compatible with the different versions of NAV/Business Central:

<br>

| Version | DC 2025 R1 (26.00) | DC 2024 R2 (25.00) | DC 2024 R1 (24.00)<a href="#footnote-5.3"><sup>3</sup></a> | DC 2023 R2 (12.00) | DC 2023 R1 (11.00)<a href="#footnote-5.1"><sup>1</sup></a> | DC 2022 R2 (10.00)<a href="#footnote-5.1"><sup>1</sup></a> | DC 2022 R1 (9.00)<a href="#footnote-5.1"><sup>1</sup></a> | DC 2021 R2 (8.00)<a href="#footnote-5.1"><sup>1</sup></a> | DC 2021 R1 (7.00)<a href="#footnote-5.1"><sup>1</sup></a> |
|---------|---------------------|---------------------|---------------------|---------------------|------------------------------------------------------------|------------------------------------------------------------|-----------------------------------------------------------|-----------------------------------------------------------|-----------------------------------------------------------|
| BC v26 | {{checkmark}} | | | | | | | | |
| BC v25 | {{checkmark}} | {{checkmark}} | | | | | | | |
| BC v24 | {{checkmark}} | {{checkmark}} | {{checkmark}} | | | | | | |
| BC v23 | | {{checkmark}} | {{checkmark}} | {{checkmark}} | | | | | |
| BC v22 | | | {{checkmark}} | {{checkmark}} | {{checkmark}} | | | | |
| BC v21 | | | | {{checkmark}} | {{checkmark}} | {{checkmark}} | | | |
| BC v20 | | | | | {{checkmark}} | {{checkmark}} | ({{checkmark}})<a href="#footnote-5.2"><sup>2</sup></a> | | |
| BC v19 | | | | | | {{checkmark}} | {{checkmark}} | ({{checkmark}})<a href="#footnote-5.2"><sup>2</sup></a> | |
| BC v18 | | | | | | {{checkmark}} | {{checkmark}} | {{checkmark}} | ({{checkmark}})<a href="#footnote-5.2"><sup>2</sup></a> |
| BC v15 - BC v17<a href="#footnote-5.5"><sup>5</sup></a> | | | | | | {{checkmark}} | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| BC v14, FOB<a href="#footnote-5.4"><sup>4</sup></a> | | {{checkmark}} | {{checkmark}} | {{checkmark}} | {{checkmark}} | {{checkmark}} | {{checkmark}} | {{checkmark}} | {{checkmark}} |
| NAV 2013 - BC v13<a href="#footnote-5.4"><sup>4</sup></a> | | | | | | | | {{checkmark}} | {{checkmark}} |
| NAV 2009 R2, RTC | | | | | | | | | {{checkmark}} |
| NAV 2009 R2, FOB | | | | | | | | {{checkmark}} | {{checkmark}} |
| NAV 3.70 - NAV 2009 SP1 | | | | | | | | {{checkmark}} | {{checkmark}} |

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-5.1">Although you can still choose to run this version of Document Capture, it's important to note that it's no longer officially supported by Continia, meaning that new functionality, updates, bug fixes, product support and similar won't be provided for this and previous versions anymore. For more information see <a href="/continia-document-capture/development-and-administration/on-premises/deployment/lifecycle-policy-on-premises">Software Lifecycle Policy and Continia Document Capture On-Premises</a>.</li>
    <li id="footnote-5.2">This requires service pack 1 or later.</li>
    <li id="footnote-5.3">With its 2024 spring release, Document Capture made a version leap from 12.00 to 24.00, meaning that versions 13.00–23.00 don't exist and never will. This was done to align the versioning of Document Capture with that of Business Central.</li>
    <li id="footnote-5.4">BC v13 and BC v14 both came in two different versions: an app-based and a FOB-based one. However, Continia only supports apps as of BC v15 CU1.</li>
    <li id="footnote-5.5">Note that the RTM version of Microsoft Dynamics 365 Business Central 2019 release wave 2 (BC v15) isn't supported for Continia Document Capture 6.50 and later. Only CU1 and newer cumulative updates are supported. The reason why the RTM version isn't supported is that Document Capture 6.50 and later versions use internal events, which are only supported in the BC-v15 CU1 and newer cumulative updates.</li>
  </ol>
</div>
</small>