---
title: Stop Asking to Set G/L Account as Standard G/L Account
date: 28-11-2024
description:
id: DC-284
lang: en
---

# Stop Asking to Set G/L Account as Standard G/L Account

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Stop asking to set GL account as standard GL account | - | {{checkmark}} Oct 2022 |

## Business value
When working in the Document Journal and changing the value in the G/L Account No. header field, you are asked to either update the setup or keep the existing account configuration. This feature will ease processing documents where you often need to change the G/L account from the value on the template.

## Feature details
For certain vendors, the G/L Account No. used is always determined depending on the items or services bought. In this situation, you do not want to set up a stand G/L Account on the template. With this feature, it will be possible to indicate that the system should not ask if the chosen G/L Account should be set up as the standard G/L Account on the related template.
