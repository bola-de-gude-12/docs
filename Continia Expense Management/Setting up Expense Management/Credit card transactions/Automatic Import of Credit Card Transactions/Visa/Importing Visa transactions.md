---
title: Importing Visa Transactions
date: 23-03-2021
description: Details on how to import Visa transactions into Continia Expense Management
id: EM-281
lang: en
---

# Importing Visa Transactions 
Continia supports the automatic import of Visa transactions directly into Continia Expense Management. This can be done in two ways:

* [Directly from Visa](#importing-transactions-directly-from-visa) (for Visa Corporate cards) – the recommended option
* [From your bank](#importing-transactions-from-your-bank) – for other card types or if direct import from Visa isn't supported

To learn more about each option and what's required to get the automatic import up and running, see the relevant sections below.

## Importing transactions directly from Visa
For Visa Corporate cards, you can have your credit card transactions imported into Expense Management straight from Visa. In order for this to happen, a transaction feed to Expense Management must be set up first. This is done by your bank, so please reach out to your banking relationship manager to get the process started.

> [!TIP]
> Your banking relationship manager is likely to find this [Visa feed setup guide](@EM-282) useful. We strongly recommend that you forward the guide to your banking relationship manager to ease the process.

## Importing transactions from your bank
If it isn't possible to import transactions directly from Visa, or if your organization uses other card types than Visa Corporate cards, your credit card transactions can be imported into Expense Management from your bank, provided that the bank is willing and able to send transactions to Expense Management. This is no problem at all for the vast majority of banks, but some banks do have technical setups that may pose certain challenges.

> [!IMPORTANT]
> Continia supports thousands of scenarios and numerous banks all over the world. If, however, you're unsure as to whether your bank can send transactions to Expense Management, please contact your bank and ask them to reach out to [your Continia partner](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md). Your Continia partner will then work with Continia to find the best possible solution for your organization.

To import Visa card transactions from your bank into Expense Management, an import agreement must be made with the bank. Once an agreement is in place, Visa transactions will automatically be imported into Microsoft Dynamics 365 Business Central on a daily basis.

Transactions are exchanged between your bank and Continia via SFTP, which is a very widely used network protocol for the transfer of files between clients and servers.


## Related information
[Automatic Import of Credit Card Transactions](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Overview.md)  
[Finding a Reseller of Continia Expense Management](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md)  
[Importing American Express Transactions](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Importing American Express transactions.md)  
[Importing Mastercard Transactions](@EM-279)  
[Importing Transactions from Other Cards](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Importing transactions from other cards.md)  
[Manual File Import](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Manual file import.md)  