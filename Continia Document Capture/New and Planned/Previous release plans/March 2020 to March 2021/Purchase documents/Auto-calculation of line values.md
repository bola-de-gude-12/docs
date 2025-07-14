---
title: Auto-Calculation of Line Values
date: 29-11-2024
description:
id: DC-325
lang: en
---

# Auto-Calculation of Line Values

| Feature | General availability on-premises | General availability online | Public preview |
| --- | :-: | :-: | :-: |
| Auto-calculation of line values | {{checkmark}} Sep 1, 2020 | {{checkmark}} Oct  1, 2020 | - |

## Feature details
More line values are now auto-calculated when documents are OCR-processed: If any of the fields **Unit Cost**, **Quantity**, or **Line Amount** aren't recognized during line recognition, the three fields are now calculated automatically instead. Previously, this was only the case for the **Quantity** field.

When one of the three fields is calculated, an error, warning, or information comment is displayed in the comments section, depending on your comment setup.

Also, a new integration event has been added: *OnBeforeAdjustMissingFields(VAR Document : Record “CDC Document”;VAR Handled : Boolean)*. If you wish to disable the auto-calculation of the three values mentioned above, you simply create an event subscriber that changes the handled value to **TRUE**.

> [!NOTE]
> The integration event *OnBeforeAdjustQty* (introduced in 6.0 SP3) is deprecated in this release and is expected to be removed in version 8.00 (due to be released one year after version 6.50).
