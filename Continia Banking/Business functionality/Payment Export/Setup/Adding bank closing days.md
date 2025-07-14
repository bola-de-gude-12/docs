---
title: Adding bank closing days in Continia Banking
description: How to add bank closing days to determine banking and payment deadlines.
date: 11-06-2025	
id: CB-42
lang: en
---
# Adding bank closing days

The bank closing day schedule helps ensure accurate calculation of banking and payment deadlines by accounting for weekends and official SEPA-region holidays. By using the bank closing day schedule, you can proactively adjust payment dates either before or after bank closing days, helping you manage payment timing effectively. 

On the [Banking Export Setup page](@CB-23), you can configure how the **Payment Date** or **Payment Discount Date** should behave when it falls on a bank closing day (e.g., a Sunday or a public holiday). Options include moving the date forward, backward, or prompting the user for input..

Saturdays and Sundays are excluded by default. Continia’s setup files automatically populate common SEPA bank closing days. However, if your organization requires additional or region-specific closing days, you can configure these manually using the **Recurrence Pattern** feature.

To add bank closing days:

1. Search ({{search}}) and select **Bank Closing Days**.
2. On the action bar, select **Bank Closing Days Setup Wizard** for guided setup, or select **New** to add a date manually. 
3. When using the wizard, select the country, enter a description, and select the start and end date. 
4. Click **Next**.
5. If you need to define recurring non-processing days (e.g., the last Thursday of each month), use the **Recurrence Pattern** page and on that page, select the recurrence period type, the weekly interval, the day of the week, and click **Next**. 
6. Click **Finish** to complete the setup.

