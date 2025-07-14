---
title: Use Payment Days to calculate due dates in Spain
date: 24-12-2024
description:
id: DC-421
lang: en
---

# Use Payment Days to Calculate Due Dates in Spain

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Use payment days to calculate due dates in Spain | {{checkmark}} Sep 2024 | {{checkmark}} Oct 2024 |

## Business value

This change aligns Continia Document Capture with Microsoft Dynamics 365 Business Central in terms of the **Payment Days** functionality, which is used to calculate due dates. This avoids manual work, as Document Capture automatically generates the actual due date – instead of the due date stated in the invoice.

## Feature details

If you're based in Spain and have configured **Payment Days** for a company or vendor, the calculated **Due Date** of a related document is based on both the vendor’s **Payment Term** and the configured **Payment Days**. If **Payment Days** isn't configured, the **Due Date** is calculated solely based on the vendor’s **Payment Term**.
