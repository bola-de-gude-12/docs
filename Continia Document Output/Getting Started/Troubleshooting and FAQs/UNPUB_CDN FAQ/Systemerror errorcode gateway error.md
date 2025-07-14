---
title: Error Code Gateway Error - Unhandled Error in the Continia Delivery Network API
date: 05-02-2024
description: Learn why you cannot send documents through CDN in a sandbox environment. 
id: DO-160
lang: en
---

# Error Code Gateway Error - Unhandled Error in the Continia Delivery Network API


## Question
Why am I getting this message and how can I solve it?

## Answer

There are some settings you need to check:

* E-doc setup -> PEPPOL (or respective profile) -> participations (is it filled in?)
* In the same menu, check that the code units are filled in properly.
* Is the customer information correctly filled in (it may be that the GLN number is used even though they are registered with VAT number or the other way around)?

You can check the identifier type on the customer card: Go to Document Output Factbox -> Output Profile -> Continia Delivery Network -> recipient type
