---
title: Exchange Configuration Through Web Service Using OAUTH2.0
date: 27-03-2023
description: 
id: DO-68
lang: en
---

# Exchange Configuration Through Web Service Using OAUTH2.0

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Exchange configuration through web service using OAUTH2.0 | {{checkmark}} Mar 2023 | {{checkmark}} Apr 2023 |

## Business value

This feature will make it possible to use OAUTH2.0 for authentication in older versions of Business Central or NAV.

## Feature details

With this feature, any Document Output-supported version of NAV or Business Central can connect to an Azure app to connect to O365.

Basic authentication is being depreciated slowly to strengthen security when sending emails. OAUTH2.0 is not supported in older versions of Business Central or NAV. However, if emailing through web service calls is supported, as this features aims at, it will be possible to enable OAUTH2.0 regardless.