---
title: Setting up the 60-Day Rule
date: 07-10-2025
description: Verify if a mileage is in compliance with the 60-day rule for the tax-free transport allowance (DK)
id: EM-59
lang: en
---
# Setting up the 60-Day Rule (DK)

> [!NOTE]
> The 60-day rule is only available in the Danish localization of Expense Management, and it will not be displayed in the Expense Management Setup in any other localization.

Expense Management can verify if a mileage is in compliance with the 60-day rule for the tax-free transport allowance, as mandated by the Danish tax authorities. For more information, see [The 60-day rule explained](https://skat.dk/en-us/businesses/employees-and-pay/transport-allowance/60-day-rule-for-tax-free-transport-allowance) (external link). 

When you import a mileage expense into Microsoft Dynamics 365 Business Central, Expense Management will count the number of days an employee has claimed mileage between the home address and the workplace during the last 12 months. If the number of days exceeds 60, a warning will be added to the mileage, it’s then up to the  approver to accept or reject the mileage.

> [!NOTE]
> Only mileage entries that start or end at the employee's home address will count towards the 60-day rule.

## Set up checks for the 60-day rule

To set up Expense Management to apply checks for the 60-day rule:

1. Search for {{search}} **Expense Management Opsætning**.
2. In the **Kørsel** FastTab, in **Overskridelse af 60-dagesregel**, you have three options: <ul><li>Leave the field blank. This is the default, and it means that the rule is not enabled.</li><li><b>Advarsel på kørsel</b>. The rule is enabled, and a message will be sent to an admin if the 60 day limit is exceeded.</li><li><b>Kørsel skattepligtig</b>. The rule is enabled. A new column named <b>Skattepligtig kontonr.</b> is added to the page <b>Bogføringsopsætning</b>. A new column named <b>Skattepligtig sats (RV)</b> is added to the page <b>Kørselssatser</b>.</li></ul>

## Understand triggers and warnings
Expense Management has created helpful automatic warnings that ensure essential details are included and accurate (for example, home address and GPS coordinates). The system automatically detects and suggests correct addresses with Google Maps suggestions and helps prevent users from creating mileage entries with the same home address for both, "From home" and "To home". Warnings will also trigger for the following circumstances:

* Mileage does not include a home address that is within range of a previously used home address
* The Mileage lacks GPS coordinates
* The home address is incorrect for Mileage

Moreover, in the Expense Portal, a 60-day counter on the Mileage page and the Expense Management Status Report.

The Expense Mobile App also prevents users from creating mileage entries with the same home address for both "From Home" and "To Home". Additionally, the app will:

- Auto-add the home address if the GPS is within 0-50 meters
- Provide suggestions from Google Maps if the GPS is within 50-500 meters
- Prevent Mileage from being submitted if the "From" and/or "To" fields were not selected from Google Maps suggestions
- Suggest the home address if an address close to home is selected (regardless of user location)

## Related information

[The 60-day rule explained](https://skat.dk/en-us/businesses/employees-and-pay/transport-allowance/60-day-rule-for-tax-free-transport-allowance)

