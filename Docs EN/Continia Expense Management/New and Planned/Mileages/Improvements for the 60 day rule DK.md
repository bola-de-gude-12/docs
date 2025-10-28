---
title: Improvements for the 60-day rule (DK)
date: 31-03-2025
description:  
id: EM-269
lang: en
---

# Improvements for the 60-Day Rule (DK)

| Feature                  | General availability on-premises | General availability online |     Public preview     |
| ------------------------ | :------------------------------: | :-------------------------: | :--------------------: |
| 60-day rule improvements |      {{checkmark}} Apr 2025      |   {{checkmark}} Apr 2025    | {{checkmark}} Mar 2025 |

## Business value

> [!NOTE]
> The following improvements are only applicable to Danish localization (DK). 

The 60-day rule updates include:

- Automatic warnings ensure essential details such as home address and GPS coordinates are included, reducing errors and enhancing compliance
- This update improves user experience by simplifying the mileage submission process by automatically detecting and suggesting correct addresses
- Prevents incorrect data entry by ensuring addresses are selected from Google Maps suggestions, enhancing data reliability and reporting accuracy

## Feature details
**In Business Central**

- A 60-day counter added to the Mileage page and the Expense Management Status Report
- Triggers if Mileage lacks a home address within the range of a previously used home address
- Triggers if Mileage lacks GPS coordinates
- Triggers if Mileage has an incorrectly marked home address
- Prevents users from creating mileage entries with the same home address for both, "From home" and "To home"

**In the Expense App**

- Prevents users from creating mileage entries with the same home address for both "From Home" and "To Home"
- Auto-adds the home address if the GPS is within 0-50 meters
- Provides suggestions if the GPS is within 50-500 meters
- Stops submission of mileage if "From" and/or "To" fields are typed text and not selected from Google Maps suggestions
- Suggests a home address if an address close to home is selected, regardless of user location

For more information, see [Setting up the 60-day rule](@EM-59).

