---
title: Using Split Characters
description: Specify the characters you want to use to split description and notification texts on a bank account statement line to improve the automatic matching.
date: 10-10-2022
id: PM-267
lang: en
---

# Using split characters

During the bank account reconciliation, Statement Intelligence uses the description and notification texts on the bank account statement lines to find and create matches. 

If you are experiencing problems matching or if you are working with very specific notations, you can use the **Split Characters** field to split a string into chunks that SI can use for recognizing entries. The string is split only when the specified delimiter character is found next to a number. 

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon, search for Statement Intelligence Setup, and select the related link.

1. On the **Statement Intelligence Setup** page, navigate to the FastTab **General**, and in the **Split Characters** field, enter the characters you want to use to split the string. Enter as many characters in the field as you want without using a delimiter. Space is also a split character.
   







