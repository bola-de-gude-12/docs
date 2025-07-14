---
title: Checking for Bank Account and VAT Numbers to Avoid Fraud
date: 28-11-2024
description:
id: DC-273
lang: en
---

# Checking for Bank Account and VAT Numbers to Avoid Fraud

| Feature | General availability on-premises | General availability online | Public preview |
| --- | :-: | :-: | :-: |
| Checking for bank account and VAT numbers to avoid fraud | {{checkmark}} Sep 1, 2021 | {{checkmark}} Oct 1, 2021 | - |

## Business value
To minimize fraud, additional checks are in place for any captured bank account number, IBAN, and VAT number.

## Feature details
The system checsk if all bank account numbers captured in incoming documents already exist in Microsoft Dynamics 365 Business Central. If a bank account doesn't exist in Business Central, an error-type comment is created. This can be customized through configuration.

In addition, the system checks that all incoming invoices contain an IBAN and a VAT number. If no IBAN and VAT number are detected, an error-type comment is created. This too can be customized via configuration.
