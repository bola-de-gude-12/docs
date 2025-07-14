---
title: Setting up Bank Holidays
description: Set up bank holidays and define how to handle purchases and payments that fall on a bank holiday
date: 17-02-2021
id: PM-7
lang: en
---

# Setting up Bank Holidays

Payment Management includes a bank holidays setup that defines how to handle purchases and payments that fall on a bank holiday or weekend. Payment Management will automatically update the dates for the listed bank holidays if the due date or cash discount date falls on a bank holiday. The default list includes bank holidays for the following countries: DK, NO, SE, FI, DE, and UK. You can add or delete bank holidays. 

> [!NOTE]
>
> Weekends are part of the bank holiday setup by default, even though they do not appear in the bank holiday list.

## To set up bank holidays

Bank holidays are automatically imported to Business Central when setting up the solution. You can change the default setup and decide how to handle bank holidays on purchase and payment fields.

To manually change the bank holiday setup: 

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Holiday Setup**, then select the related link. This will open a list of all available bank holidays. You can filter the list by **Country Code** and **Date**.
1. On the **Setup** FastTab, you can choose how Payment Management must handle bank holidays on purchase documents and payment journals in the **Handle Bank Holidays on Purchase** field and in the **Handle Bank Holidays on Payments** field. There are four options:
   
   | Option           | Consequence if cash discount date or due date falls on a bank holiday |
   | ---------------- | ------------------------------------------------------------ |
   | Field left empty | The date remains unchanged.                                  |
   | After            | The date is shifted forward to the next available weekday.   |
   | Before           | The date is adjusted to the previous available weekday.      |
   | Ask User         | A dialog prompts the user to select how bank holidays should be handled for the specific payment. This option is only applicable for managing payments on purchase documents. |



## To add or delete a bank holiday

To add or delete a bank holiday:

1. On the **Bank Holiday Setup** page, navigate to the **Bank Holidays** FastTab and select **Manage**.
2. Select **New Line** to add a bank holiday or select **Delete line** to remove a bank holiday from the list. For new lines, you must enter; the Country Code, the date, a description, and the day of the week. The **Country Code** determines a bank holiday for a specific country. The code is used on the balance account used for the payment. 

> [!WARNING]
>
> Be aware that the action **Update Bank Holidays** will update the entire list and deletes any potential manual changes in the list.



## To update bank holidays

When setting up the solution, bank holidays are automatically imported to Business Central. Occasionally, Continia updates the list of bank holidays, for example, to extend the list with more years or to delete years from the list. You can import Continia's updates to the list from Continia Online.

To update bank holidays:
1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Holiday Setup**, then select the related link.
1. In the page header, select  **Update Bank Holidays**. This will update the list of bank holidays to the latest bank holiday list available on Continia Online.

