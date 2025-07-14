---
title: Supported on-premises versions for Document Capture
date: 30-06-2025
id: null
lang: en
description: An overview of the supported on-premises versions of NAV and Business Central.
---

# Supported on-premises versions of NAV and Business Central

This page provides an overview of all supported on-premises versions of Microsoft Dynamics NAV and Microsoft Dynamics 365 Business Central. For information on what countries/regions Continia Document Capture is available in and what languages are supported for these on-premises versions, see \[Country/Regional Availability and Supported Languages for FOB]\(Countries and languages On-Premises.md). For information on the types of support Continia does and doesn't provide, see [Scope of Support Services](../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/@DC-12/).

> \[!NOTE] Up until Document Capture 2024 R2 (25.00), every new major version of Document Capture was released for the last three major versions of Business Central and for Business Central April 2019 (BC v14). However, Document Capture 2025 R1 (26.00) was only released for the last three major versions of Business Central – that is, not including Business Central April 2019 (BC v14).
>
> Older versions of NAV/Business Central are still supported through the release of service packs for older Document Capture versions.

Note that Continia only releases code for major FOB versions (RTM) of NAV/Business Central. If Microsoft releases a cumulative update (CU) that renders any Continia code nonfunctional, Continia doesn't release code for this CU. In such cases, you must instead ask your Continia partner to perform any necessary code changes in order to make your Continia software fully functional again.

As regards app versions of Business Central, Continia releases code for all available CUs whenever a version of Document Capture is released (applies to both major versions and service packs). Each newly released CU from Microsoft is only supported as of the next service pack released by Continia. If you need to upgrade to a currently unsupported Business Central CU – the latest one, for example – and can't wait until Continia has released a Document Capture service pack that supports this, please reach out to the Continia support team by creating a support ticket. Continia will then provide you with a fully functional package that supports the relevant Business Central CU.

> \[!NOTE] Although versions 13 and 14 of Business Central (Business Central October 2018 and Business Central April 2019) both came in app-based versions in addition to the FOB-based ones, Continia only supports apps as of Business Central 2019 release wave 2 (BC v15) CU1.

## Compatibility matrix

The following table provides an overview of what versions of Document Capture (DC) are compatible with the different versions of NAV/Business Central:

\


| Version                                                                         | DC 2025 R1 (26.00) | DC 2024 R2 (25.00) | DC 2024 R1 (24.00)[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-5.3>) | DC 2023 R2 (12.00) | DC 2023 R1 (11.00)[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-5.1>) | DC 2022 R2 (10.00)[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-5.1>) | DC 2022 R1 (9.00)[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-5.1>) | DC 2021 R2 (8.00)[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-5.1>) | DC 2021 R1 (7.00)[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-5.1>) |
| ------------------------------------------------------------------------------- | ------------------ | ------------------ | -------------------------------------------------------------------------------- | ------------------ | -------------------------------------------------------------------------------- | -------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| BC v26                                                                          | \{{checkmark\}}    |                    |                                                                                  |                    |                                                                                  |                                                                                  |                                                                                 |                                                                                 |                                                                                 |
| BC v25                                                                          | \{{checkmark\}}    | \{{checkmark\}}    |                                                                                  |                    |                                                                                  |                                                                                  |                                                                                 |                                                                                 |                                                                                 |
| BC v24                                                                          | \{{checkmark\}}    | \{{checkmark\}}    | \{{checkmark\}}                                                                  |                    |                                                                                  |                                                                                  |                                                                                 |                                                                                 |                                                                                 |
| BC v23                                                                          |                    | \{{checkmark\}}    | \{{checkmark\}}                                                                  | \{{checkmark\}}    |                                                                                  |                                                                                  |                                                                                 |                                                                                 |                                                                                 |
| BC v22                                                                          |                    |                    | \{{checkmark\}}                                                                  | \{{checkmark\}}    | \{{checkmark\}}                                                                  |                                                                                  |                                                                                 |                                                                                 |                                                                                 |
| BC v21                                                                          |                    |                    |                                                                                  | \{{checkmark\}}    | \{{checkmark\}}                                                                  | \{{checkmark\}}                                                                  |                                                                                 |                                                                                 |                                                                                 |
| BC v20                                                                          |                    |                    |                                                                                  |                    | \{{checkmark\}}                                                                  | \{{checkmark\}}                                                                  | (\{{checkmark\}})[<sup>2</sup>](<Copy of Versions On-Premises.md#footnote-5.2>) |                                                                                 |                                                                                 |
| BC v19                                                                          |                    |                    |                                                                                  |                    |                                                                                  | \{{checkmark\}}                                                                  | \{{checkmark\}}                                                                 | (\{{checkmark\}})[<sup>2</sup>](<Copy of Versions On-Premises.md#footnote-5.2>) |                                                                                 |
| BC v18                                                                          |                    |                    |                                                                                  |                    |                                                                                  | \{{checkmark\}}                                                                  | \{{checkmark\}}                                                                 | \{{checkmark\}}                                                                 | (\{{checkmark\}})[<sup>2</sup>](<Copy of Versions On-Premises.md#footnote-5.2>) |
| BC v15 - BC v17[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-5.5>)   |                    |                    |                                                                                  |                    |                                                                                  | \{{checkmark\}}                                                                  | \{{checkmark\}}                                                                 | \{{checkmark\}}                                                                 | \{{checkmark\}}                                                                 |
| BC v14, FOB[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-5.4>)       |                    | \{{checkmark\}}    | \{{checkmark\}}                                                                  | \{{checkmark\}}    | \{{checkmark\}}                                                                  | \{{checkmark\}}                                                                  | \{{checkmark\}}                                                                 | \{{checkmark\}}                                                                 | \{{checkmark\}}                                                                 |
| NAV 2013 - BC v13[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-5.4>) |                    |                    |                                                                                  |                    |                                                                                  |                                                                                  |                                                                                 | \{{checkmark\}}                                                                 | \{{checkmark\}}                                                                 |
| NAV 2009 R2, RTC                                                                |                    |                    |                                                                                  |                    |                                                                                  |                                                                                  |                                                                                 |                                                                                 | \{{checkmark\}}                                                                 |
| NAV 2009 R2, FOB                                                                |                    |                    |                                                                                  |                    |                                                                                  |                                                                                  |                                                                                 | \{{checkmark\}}                                                                 | \{{checkmark\}}                                                                 |
| NAV 3.70 - NAV 2009 SP1                                                         |                    |                    |                                                                                  |                    |                                                                                  |                                                                                  |                                                                                 | \{{checkmark\}}                                                                 | \{{checkmark\}}                                                                 |

***

1. Although you can still choose to run this version of Document Capture, it's important to note that it's no longer officially supported by Continia, meaning that new functionality, updates, bug fixes, product support and similar won't be provided for this and previous versions anymore. For more information see [Software Lifecycle Policy and Continia Document Capture On-Premises](../../../continia-document-capture/development-and-administration/on-premises/deployment/lifecycle-policy-on-premises/).
2. This requires service pack 1 or later.
3. With its 2024 spring release, Document Capture made a version leap from 12.00 to 24.00, meaning that versions 13.00–23.00 don't exist and never will. This was done to align the versioning of Document Capture with that of Business Central.
4. BC v13 and BC v14 both came in two different versions: an app-based and a FOB-based one. However, Continia only supports apps as of BC v15 CU1.
5. Note that the RTM version of Microsoft Dynamics 365 Business Central 2019 release wave 2 (BC v15) isn't supported for Continia Document Capture 6.50 and later. Only CU1 and newer cumulative updates are supported. The reason why the RTM version isn't supported is that Document Capture 6.50 and later versions use internal events, which are only supported in the BC-v15 CU1 and newer cumulative updates.

For more details and full version names, see the tables below, which list all NAV and Business Central versions supported by the latest Document Capture releases.

## Document Capture 2025 R1 (26.00)

| Supported versions                                                   |
| -------------------------------------------------------------------- |
| Microsoft Dynamics 365 Business Central 2024 release wave 1 (BC v24) |
| Microsoft Dynamics 365 Business Central 2024 release wave 2 (BC v25) |
| Microsoft Dynamics 365 Business Central 2025 release wave 1 (BC v26) |

## Document Capture 2024 R2 (25.00)

| Supported versions                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------- |
| Microsoft Dynamics 365 Business Central April 2019 (BC v14)[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-4.1>) |
| Microsoft Dynamics 365 Business Central 2023 release wave 2 (BC v23)                                                      |
| Microsoft Dynamics 365 Business Central 2023 release wave 1 (BC v24)                                                      |
| Microsoft Dynamics 365 Business Central 2024 release wave 2 (BC v25)                                                      |

***

1. BC v13 and BC v14 both came in two different versions: an app-based and a FOB-based one. However, Continia only supports apps as of BC v15 CU1.

## Document Capture 2024 R1 (24.00)

> \[!NOTE] With its 2024 spring release, Document Capture made a version leap from 12.00 to 24.00, meaning that versions 13.00–23.00 don't exist and never will. This was done to align the versioning of Document Capture with that of Business Central.

| Supported versions                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------- |
| Microsoft Dynamics 365 Business Central April 2019 (BC v14)[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-4.1>) |
| Microsoft Dynamics 365 Business Central 2023 release wave 1 (BC v22)                                                      |
| Microsoft Dynamics 365 Business Central 2023 release wave 2 (BC v23)                                                      |
| Microsoft Dynamics 365 Business Central 2024 release wave 1 (BC v24)                                                      |

***

1. BC v13 and BC v14 both came in two different versions: an app-based and a FOB-based one. However, Continia only supports apps as of BC v15 CU1.

## Document Capture 2023 R2 (12.00)

| Supported versions                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------- |
| Microsoft Dynamics 365 Business Central April 2019 (BC v14)[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-4.1>) |
| Microsoft Dynamics 365 Business Central 2022 release wave 2 (BC v21)                                                      |
| Microsoft Dynamics 365 Business Central 2023 release wave 1 (BC v22)                                                      |
| Microsoft Dynamics 365 Business Central 2023 release wave 2 (BC v23)                                                      |

***

1. BC v13 and BC v14 both came in two different versions: an app-based and a FOB-based one. However, Continia only supports apps as of BC v15 CU1.

## Document Capture 2023 R1 (11.00)

| Supported versions                                                                                                        |
| ------------------------------------------------------------------------------------------------------------------------- |
| Microsoft Dynamics 365 Business Central April 2019 (BC v14)[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-4.1>) |
| Microsoft Dynamics 365 Business Central 2022 release wave 1 (BC v20)                                                      |
| Microsoft Dynamics 365 Business Central 2022 release wave 2 (BC v21)                                                      |
| Microsoft Dynamics 365 Business Central 2023 release wave 1 (BC v22)                                                      |

***

1. BC v13 and BC v14 both came in two different versions: an app-based and a FOB-based one. However, Continia only supports apps as of BC v15 CU1.

## Document Capture 2022 R2 (10.00)

| Supported versions                                                                                                                 |
| ---------------------------------------------------------------------------------------------------------------------------------- |
| Microsoft Dynamics 365 Business Central April 2019 (BC v14)[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-3.1>)          |
| Microsoft Dynamics 365 Business Central 2019 release wave 2 (BC v15)[<sup>2</sup>](<Copy of Versions On-Premises.md#footnote-3.2>) |
| Microsoft Dynamics 365 Business Central 2020 release wave 1 (BC v16)                                                               |
| Microsoft Dynamics 365 Business Central 2020 release wave 2 (BC v17)                                                               |
| Microsoft Dynamics 365 Business Central 2021 release wave 1 (BC v18)                                                               |
| Microsoft Dynamics 365 Business Central 2021 release wave 2 (BC v19)                                                               |
| Microsoft Dynamics 365 Business Central 2022 release wave 1 (BC v20)                                                               |
| Microsoft Dynamics 365 Business Central 2022 release wave 2 (BC v21)                                                               |

***

1. BC v13 and BC v14 both came in two different versions: an app-based and a FOB-based one. However, Continia only supports apps as of BC v15 CU1.
2. Note that the RTM version of Microsoft Dynamics 365 Business Central 2019 release wave 2 (BC v15) isn't supported for Continia Document Capture 6.50 and later. Only CU1 and newer cumulative updates are supported. The reason why the RTM version isn't supported is that Document Capture 6.50 and later versions use internal events, which are only supported in the BC-v15 CU1 and newer cumulative updates.

## Document Capture 2022 R1 (9.00)

| Supported versions                                                                                                                 |
| ---------------------------------------------------------------------------------------------------------------------------------- |
| Microsoft Dynamics 365 Business Central April 2019 (BC v14)[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-2.1>)          |
| Microsoft Dynamics 365 Business Central 2019 release wave 2 (BC v15)[<sup>2</sup>](<Copy of Versions On-Premises.md#footnote-2.2>) |
| Microsoft Dynamics 365 Business Central 2020 release wave 1 (BC v16)                                                               |
| Microsoft Dynamics 365 Business Central 2020 release wave 2 (BC v17)                                                               |
| Microsoft Dynamics 365 Business Central 2021 release wave 1 (BC v18)                                                               |
| Microsoft Dynamics 365 Business Central 2021 release wave 2 (BC v19)                                                               |
| Microsoft Dynamics 365 Business Central 2022 release wave 1 (BC v20)[<sup>3</sup>](<Copy of Versions On-Premises.md#footnote-2.3>) |

***

1. BC v13 and BC v14 both came in two different versions: an app-based and a FOB-based one. However, Continia only supports apps as of BC v15 CU1.
2. Note that the RTM version of Microsoft Dynamics 365 Business Central 2019 release wave 2 (BC v15) isn't supported for Continia Document Capture 6.50 and later. Only CU1 and newer cumulative updates are supported. The reason why the RTM version isn't supported is that Document Capture 6.50 and later versions use internal events, which are only supported in the BC-v15 CU1 and newer cumulative updates.
3. This requires service pack 1 or later.

## Document Capture 2021 R2 (8.00)

| Supported versions                                                                                                                                       |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Microsoft Navision NAV 3.70[<sup>1,</sup> ](<Copy of Versions On-Premises.md#footnote-1>)[<sup>2</sup>](<Copy of Versions On-Premises.md#footnote-2>)    |
| Microsoft Dynamics NAV 4.0[<sup>1,</sup> ](<Copy of Versions On-Premises.md#footnote-1>)[<sup>2</sup>](<Copy of Versions On-Premises.md#footnote-2>)     |
| Microsoft Dynamics NAV 4.0 SP1[<sup>1,</sup> ](<Copy of Versions On-Premises.md#footnote-1>)[<sup>2</sup>](<Copy of Versions On-Premises.md#footnote-2>) |
| Microsoft Dynamics NAV 4.0 SP2[<sup>1,</sup> ](<Copy of Versions On-Premises.md#footnote-1>)[<sup>2</sup>](<Copy of Versions On-Premises.md#footnote-2>) |
| Microsoft Dynamics NAV 4.0 SP3[<sup>1,</sup> ](<Copy of Versions On-Premises.md#footnote-1>)[<sup>2</sup>](<Copy of Versions On-Premises.md#footnote-2>) |
| Microsoft Dynamics NAV 5.0[<sup>1</sup>](<Copy of Versions On-Premises.md#footnote-1>)                                                                   |
| Microsoft Dynamics NAV 5.0 SP1                                                                                                                           |
| Microsoft Dynamics NAV 2009[<sup>3</sup>](<Copy of Versions On-Premises.md#footnote-3>)                                                                  |
| Microsoft Dynamics NAV 2009 SP1[<sup>3</sup>](<Copy of Versions On-Premises.md#footnote-3>)                                                              |
| Microsoft Dynamics NAV 2009 R2[<sup>3,</sup> ](<Copy of Versions On-Premises.md#footnote-3>)[<sup>4</sup>](<Copy of Versions On-Premises.md#footnote-4>) |
| Microsoft Dynamics NAV 2013                                                                                                                              |
| Microsoft Dynamics NAV 2013 R2                                                                                                                           |
| Microsoft Dynamics NAV 2015                                                                                                                              |
| Microsoft Dynamics NAV 2016                                                                                                                              |
| Microsoft Dynamics NAV 2017                                                                                                                              |
| Microsoft Dynamics NAV 2018                                                                                                                              |
| Microsoft Dynamics 365 Business Central (BC v12)                                                                                                         |
| Microsoft Dynamics 365 Business Central October 2018 (BC v13)[<sup>5</sup>](<Copy of Versions On-Premises.md#footnote-5>)                                |
| Microsoft Dynamics 365 Business Central April 2019 (BC v14)[<sup>5</sup>](<Copy of Versions On-Premises.md#footnote-5>)                                  |
| Microsoft Dynamics 365 Business Central 2019 release wave 2 (BC v15)[<sup>6</sup>](<Copy of Versions On-Premises.md#footnote-6>)                         |
| Microsoft Dynamics 365 Business Central 2020 release wave 1 (BC v16)                                                                                     |
| Microsoft Dynamics 365 Business Central 2020 release wave 2 (BC v17)                                                                                     |
| Microsoft Dynamics 365 Business Central 2021 release wave 1 (BC v18)                                                                                     |
| Microsoft Dynamics 365 Business Central 2021 release wave 2 (BC v19)[<sup>7</sup>](<Copy of Versions On-Premises.md#footnote-7>)                         |

***

1. Only supported with NAV 5.0 SP1 runtime.
2. NAV's purchase approval flow can be downgraded to version 3.70.
3. Only supported with the Classic Client, not the RoleTailored Client.
4. Due to a critical runtime bug in the NAV executables, the following builds aren't supported in Dynamics NAV 2009 R2: 6.0.32519 – 6.0.32599.
5. BC v13 and BC v14 both came in two different versions: an app-based and a FOB-based one. However, Continia only supports apps as of BC v15 CU1.
6. Note that the RTM version of Microsoft Dynamics 365 Business Central 2019 release wave 2 (BC v15) isn't supported for Continia Document Capture 6.50 and later. Only CU1 and newer cumulative updates are supported. The reason why the RTM version isn't supported is that Document Capture 6.50 and later versions use internal events, which are only supported in the BC-v15 CU1 and newer cumulative updates.
7. This requires service pack 1 or later.

## Related information

\[Country/Regional availability and supported languages for on premises]\(Countries and languages On-Premises.md)\
[Scope of support services](../../../Continia%20Document%20Capture/Development%20and%20Administration/On-Premises/@DC-12/)
