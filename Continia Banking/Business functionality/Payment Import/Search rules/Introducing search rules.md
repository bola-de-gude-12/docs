---
title: Introducing search rules Continia Banking
description: Learn more about the search rule process in Continia Banking.
date: 20-08-2024
id: CB-87
lang: en

---

# Introducing search rules

If bank account reconciliation lines lack sufficient details to match using date and amount, you can set up search rules to identify matching ledger entries using text. Search rules help identify accounts by searching for specific text in the imported transaction within both the Bank Account Reconciliation and Payment Reconciliation Journal. 

You can create custom rules to locate accounts based on text criteria, specifying where the system should look. Default search fields include descriptions and additional information, but you can also customize templates for more precise searches. Search rules apply to various account types, such as G/L Accounts, banks, customers, employees, and vendors. Once you set up these rules, they assist in the matching process by automatically assigning transactions or data entries to specific accounts based on the defined criteria. 

The process:

1. **Define search rules** - add search rules or use templates to define search fields and filters to specify conditions for rule application. For more information on add search rules, refer to the [Setting up search rules](@CB-104) article.
2. **Matching and posting** - if a match is found, the account type and number are assigned to the reconciliation line. Search rules can also adjust posting details, such as document type, dimensions, and posting groups. 

The search rules determine the creation of journal lines or the making of postings depending on whether you are working in the Bank Account Reconciliation or the Payment Reconciliation journal.

* When you use [Bank Account Reconciliation](@CB-22), the search rules are processed by creating journal lines based on the outcome of the search rules. Depending on your settings in the **Banking Import Setup**, whether the journal line is created automatically or you should manually trigger this using the **Create journal line from search rule** action on the **Payment Application Review** page or the **Bank Account Reconciliation** page. On the Bank Account Reconciliation page, you can decide whether to create journal lines for the selected record, all records, or active records. 
* In [Payment Reconciliation Journal](@CB-26), the search rules control how payments are processed. They adjust the amount applied and the number of entries matched on the statement line. When this adjustment is made, the line's reconciliation status changes to Completed, indicating it's ready to be posted.

> [!TIP]
>
> To disable search rules, go to the **Banking Import Setup** page, and in the **General** FastTab, deactivate **Search rules**.

