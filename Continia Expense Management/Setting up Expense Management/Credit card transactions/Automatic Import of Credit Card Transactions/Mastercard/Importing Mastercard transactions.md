---
title: Importing Mastercard Transactions
date: 12-11-2020
description: Details on how to import Mastercard transactions into Continia Expense Management
id: EM-279
lang: en
---

# Importing Mastercard Transactions 
Continia supports the automatic import of Mastercard transactions directly into Continia Expense Management. This can be done in two ways:

* [Directly from Mastercard](#importing-transactions-directly-from-mastercard) using Mastercard Smart Data (only for Mastercard corporate cards) – the recommended option
* [From your bank](#importing-transactions-from-your-bank) – for other card types or if Mastercard Smart Data isn't supported

To learn more about each option and what's required to get the automatic import up and running, see the relevant sections below.

## Importing transactions directly from Mastercard
For Mastercard corporate cards, you can have your credit card transactions imported into Expense Management straight from Mastercard using Mastercard Smart Data (if available – see note below). In order for this to happen, a transaction feed to Expense Management must be set up first. This is done by your bank, so please reach out to your banking relationship manager to get the process started.

> [!TIP]
> Your banking relationship manager is likely to find this [Mastercard feed setup guide](@EM-280) useful. We strongly recommend that you forward the guide to your banking relationship manager to ease the process.

> [!NOTE]
> Mastercard Smart Data is fully supported by Continia, but not by all banks. To find out if your bank supports it, please contact your banking relationship manager.

## Importing transactions from your bank
If your bank doesn't support Mastercard Smart Data or your organization uses other card types than Mastercard corporate cards, your credit card transactions can be imported into Expense Management from your bank, provided that the bank is willing and able to send transactions to Expense Management. This is no problem at all for the vast majority of banks, but some banks do have technical setups that may pose certain challenges.

> [!IMPORTANT]
> Continia supports thousands of scenarios and numerous banks all over the world. If, however, you're unsure as to whether your bank can send transactions to Expense Management, please contact your bank and ask them to reach out to [your Continia partner](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md). Your Continia partner will then work with Continia to find the best possible solution for your organization.

To import Mastercard transactions from your bank into Expense Management, an import agreement must be made with the bank. Once an agreement is in place, Mastercard transactions will automatically be imported into Microsoft Dynamics 365 Business Central on a daily basis.

Transactions are exchanged between your bank and Continia via SFTP, which is a very widely used network protocol for the transfer of files between clients and servers.

## See also
[Automatic Import of Credit Card Transactions](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Overview.md)  
[Finding a Reseller of Continia Expense Management](/Continia Expense Management/Getting Started/Resellers and Partners/Find a Reseller.md)  
[Importing American Express Transactions](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Importing American Express transactions.md)  
[Importing Visa Transactions](@EM-281)  
[Importing Transactions from Other Cards](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Importing transactions from other cards.md)  
[Manual File Import](/Continia Expense Management/Setting up Expense Management/Credit card transactions/Automatic Import of Credit Card Transactions/Manual file import.md)  