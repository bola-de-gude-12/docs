---
title: Mapping bank currency codes
date: 23-09-2025
description: Learn how to map bank currency codes
id: EM-371
lang: en
---
# Mapping bank currency codes

Some banking institutions (Mastercard for example), send currencies in a three-digit numeric code format. These codes must be mapped to an alphabetic currency code in NAV or Business Central. For more information, see [a list of ISO standards used by Mastercard]([ISO - ISO 4217 — Currency codes](https://www.iso.org/iso-4217-currency-codes.html)).

You know you'll need to map these codes if you receive the following error in the Bank Transaction Inbox. 

* *"The Bank Currency Map does not exist, identification fields and values bank code="XX"..."*

## Map bank currencies

To map bank currency codes:

1. Search for {{search}} **Bank Transaction Inbox**

1. On the action bar, click **Bank** > **Currency Map**.

1.  In **Bank Currency Map**, on the action bar, click **Edit List**.

1. In the **Currency Code (Bank)** column, enter the three-digit numeric code for the currency you want to include, for example "036".
 >[!TIP]
 >Refer to the [IBAN list of currency code numbers](https://www.iban.com/currency-codes) to map out your currencies.

5. In the **Currency Code** column, add the corresponding code. So for "036", the matching code would be
   "AUD".

1. Repeat steps 4 and 5 for all the currencies your organization is likely to encounter.

1. For your local currency, enter the currency code in the **Currency Code (Bank)** column, leave the **Currency Code** column blank, and in the **Local Currency** column, select the checkbox. Use the following table for reference.

| Currency Code (Bank) | Currency Code | Local Currency (GBP) |
| --- | :-: | :-: |
| 826 |  | {{checkmark}} |
| 840                  |      USD      |         [ ]          |
| 978                  |      EUR      |         [ ]          |
| 036                  |      AUD      |         [ ]          |

## Related information

For more information about bank mapping rules, see:

[How bank mapping rules work](@EM-330)
