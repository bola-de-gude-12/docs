---
title: Using Extended Payment Discount Handling
date: 04-09-2024
description: Learn how to use extended payment discount handling.
id: CF-33
lang: en
---

# Using Extended Payment Discount Handling

Businesses in some countries frequently offer payment discounts to encourage prompt payments from customers. Managing these early payment discounts requires flexibility to handle exceptions and occasionally grant discounts beyond the original terms, as well as enhanced control and oversight when applying payments to entries.

This is where the Extended Payment Discount Handling feature in the Continia Finance Essential module comes in handy, providing more flexible and smoother options for handling discounts than standard Business Central.

## Prerequisites

Enable **Use Extended Application** on the **Continia Finance Setup** page in the **Extended Application** FastTab.

Enable **Extended Payment Discount Handling** on the **Continia Finance Setup** page in the **Extended Application** FastTab.



## To view and adjust payment discount details in entry lines 

Extended Payment Discount Handling provides a better overview of all relevant payment discounts for entry lines, such as in the cash receipt journal, and gives you an easy way of adjusting payment discount details directly in entry lines.

Entry lines gain four extra columns:

| Column                              | Description                                                  |
| ----------------------------------- | ------------------------------------------------------------ |
| Payment Discount Possible           | Displays the amount of discount that can be applied to the entry when considering the payment discount date |
| Payment Discount to Apply           | Can be manually adjusted to a different discount amount      |
| Application Payment Discount Amount | Displays the content of **Payment Discount to Apply**        |
| Payment Discount %                  | Can be manually adjusted to a different discount rate        |

For applied entries, the fields in the payment discount columns display in bold green text, which provides an easier overview when you work with multiple lines.



## To adjust payment discount amounts and rates

The Extended Payment Discount Handling feature also provides you with tools to quickly adjust payment discount amounts when applying entries, such as in the cash receipt journals.

The **General** FastTab will have three extra fields:

| Field                            | Description                                                  |
| -------------------------------- | ------------------------------------------------------------ |
| **Ignore Payment Discount Date** | Allows you to quickly apply the set discount to all entry lines regardless of whether posting date is after the payment discount date |
| **Build Payment Differences**    | Allows you to apply the discount regardless of the payment discount date, and then creates an Open Amount for the difference between the applied amount and the entry amount with the original discount |
| **Use Payment Discount %**       | Allows you to apply a different payment discount than the discount originally set for all the entries |



## To handle partial payments with discount amounts

With Extended Payment Discount Handling, you can also handle partial payments that include a partial payment discount.

Simply adjust the amounts in these columns:

* Either **Payment Discount to Apply** or **Payment Discount %**
* **Payment Amount**

The **Open Amount** column will display the remaining amount for the entry. 







<style>

 .content table tr td:nth-child(1) {

 width: 200px;

 }

 .content table tr td:nth-child(2) {

 width: 600px;

 }

</style>
