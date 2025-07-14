---
title: Introduction to reconciliation with Continia Banking
date: 01-10-2024
description: Learn how you can reconcile book entries using Continia Banking's enhanced reconciliation solution.
id: CB-13
lang: en
---

# Introducing reconciliation with Continia Banking

Reconciling book entries with bank statements can be a challenging task as it requires repeatedly switching between financial statements and the general ledger while making adjustments. Continia Banking makes this process easier and saves time. With Continia Banking, you can import the bank statement and automatically match it with your books. It provides an intuitive interface that enables you to reconcile the bank entries that couldn't be matched, allowing you to finish the reconciliation process in just a few clicks.

Continia Banking supports and enhances the Microsoft Business Central ways of reconciling bank accounts and payments, offering customized reconciliation solutions to meet customers' specific needs.

1. **Bank Account Reconciliation** - this thorough reconciliation method involves importing bank account statement files for reconciling bank account ledger entries directly. Posting all transactions directly on the bank ensures meticulous reconciliation based on bank data. For more information, refer to the [Bank Account Reconciliation articles](@CB-135).
2. **Payment Reconciliation Journal** - this reconciliation solution grants you more authority. With this option, you can import bank account statement files. Transactions are posted directly on the bank or on a G/L account, depending on specific preferences. In the payment reconciliation journal, users can match transactions according to their needs. You can apply various entries, and the system reconciles bank account ledger entries during the posting process. For more information, refer to the [Payment Reconciliation Journal articles](@CB-138).

## The matching procedure

Continia Banking has developed an enhanced matching procedure for both Bank Account Reconciliation and Payment Reconciliation Journal, replacing the current Business Central standard matching.
1. **Initial setup** - activate Continia Banking and set the necessary permissions.
2. **Multi-level rule processing** - apply a range of rules, including Transaction Code Rules, Search Rules, and Related Party Rules, to ensure more accurate matching. This feature facilitates the addition of new rules and supports advanced scenarios. For more information, refer to the [The basics of matching accounts](@CB-108)
3. **Account identification** - match on identifiers such as BBAN, IBAN, and names (including address and city).
4. **Ledger entry matching** - match entries and use identifiers to identify individual transactions as well as batch transactions. This secures a single, unique and easy matching of most transactions.  For information on reconciling transactions in the Payment Reconciliation Journal, refer to the [Working in the Payment Reconciliation Journal](@CB-26) article.
5. **Payment application proposals** - candidates found for matching.
7. **Manual handling** - allows you to manage any unsolved transactions.

