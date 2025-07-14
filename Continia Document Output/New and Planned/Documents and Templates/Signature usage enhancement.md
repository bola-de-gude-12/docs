---
title: Signature usage enhancement
date: 29-09-2023
description: New feature that enables users to change email signatures quickly.
id: DO-87
lang: en
---

# Enhancing email signature functionality

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Enhancing email signature functionality | - | {{checkmark}} Sep 2023 |

## Business value
Email signatures can either be permanent or contain temporary campaign information. Now, signatures can be created with a fixed duration of start and end dates. This ensures that temporary signatures are deactivated at the appropriate time.

## Feature details
The signature feature remains unchanged, but we have added an option to set an end date for the signature. This allows users to create a signature that will be valid for a specific period and also allows for timed modifications to the signature. If multiple signatures are defined, the active one will be displayed in bold. However, if none of the defined signature dates apply to the current date, the default signature will always be used.

Read more about how to create email signatures in [Creating Email Signatures](@DO-133).