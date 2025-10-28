---
title: Checking for Phone Numbers to Avoid Fraud
date: 29-11-2024
description:
id: DC-309
lang: en
---

# Checking for Phone Numbers to Avoid Fraud

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Checking for phone numbers to avoid fraud | {{checkmark}} Mar 2024 | {{checkmark}} Apr 2024 |

## Business value

To minimize fraud, additional checks will be added for any captured phone numbers.

## Feature details

To check that all phone numbers captured in incoming documents already exist for the relevant vendors in Microsoft Dynamics 365 Business Central, a new field, **Vendor Phone No.**, has been added to the **Purchase** and **Purchase Order** master templates for PDF documents. The field property **Required** is set to **False** by default, but this can easily be changed.

The **Is Valid** codeunit that's applied to the new template field checks that any phone number captured in a document actually exists for the vendor who sent the document. The codeunit then validates the recognized value against the **Phone No.** field on the **Vendor Card**. If the recognized phone number doesn't exist or is different from the one on the **Vendor Card**, an error-type comment is created (this can be customized through configuration though).

> [!NOTE]
> The function validates digits only. All other characters are ignored in the check.

For more information, see [Setting up Fraud Checks](@DC-213).