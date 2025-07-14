---
title: Introducing returned direct debits
description: Learn more about Continia Banking's approach to handling returned direct debits.
date: 04-06-2025	
id: CB-242
lang: en
---

# Introducing direct debit returns

When an invoice is paid via a [Direct Debit Suggestion](@CB-130) or [Direct Debit Collection](https://learn.microsoft.com/en-us/dynamics365/business-central/finance-collect-payments-with-sepa-direct-debit#creating-sepa-direct-debit-collection-entries-and-export-to-a-bank-file), there may be cases where the bank is unable to execute the payment or where the payment is initially successful but later returned. This can occur for several reasons, such as a closed bank account, an expired mandate, insufficient funds, or a customer-initiated dispute. Unlike failed payments that bounce immediately, returned direct debits are processed after settlement and require manual follow-up. 

> [!NOTE]
>
> You can enable Direct Debit Return from the Continia Feature Management page.

Continia Banking automatically identifies returned direct debits during the import of CAMT statements by detecting reversal indicators and standardized [return reason codes](@CB-241) explaining why the payment was returned. Using information such as the end-to-end ID, the system matches the returned transaction to the original payment and stores it for further action. For more information on how Continia uses bank transaction code rules, refer to the [Accounts identification methods](@CB-33) article. 

You can configure the system's response to returned direct debits on the [Banking Import Setup](@CB-14) page. For example, if a customer frequently reverses payments, you can automatically place their related invoices on hold.

For more information, see the [Handling returned direct debits](@CB-243) article. 
