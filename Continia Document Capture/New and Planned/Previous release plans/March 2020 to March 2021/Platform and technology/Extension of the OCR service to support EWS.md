---
title: Extension of the OCR service to support exchange web services (EWS) instead of IMAP
date: 11-12-2024
description:
id: DC-373
lang: en
---

# Extension of the OCR Service to Support Exchange Web Services (EWS) Instead of IMAP

| Feature | General availability on-premises | General availability online | Public preview |
| --- | :-: | :-: | :-: |
| Extension of the OCR service to support Exchange Webservices (EWS) instead of IMAP | {{checkmark}} Sep 1, 2020 | {{checkmark}} Oct 1, 2020 | - |

> [!NOTE]
> Microsoft's retirement of Basic Authentication for Exchange Online was originally scheduled to take place on October 13, 2020, but has since been postponed several times. For more information, see [this Microsoft blog post](https://techcommunity.microsoft.com/t5/exchange-team-blog/basic-authentication-and-exchange-online-september-2021-update/ba-p/2772210).

## Feature details
During the first half of 2021, Microsoft will retire and stop supporting Basic Authentication in Exchange Online. As a consequence of this, Continia will extend the OCR service to support Exchange Web Services (EWS) instead of IMAP in order to support Oauth 2.0 for Exchange Online.

Continia has chosen to support EWS instead of IMAP because Microsoft doesn't support API application permissions for IMAP, which is necessary for Continia's service to work without user interaction when authenticating with Exchange Online. Please note that IMAP support will still be available for all other mail services.