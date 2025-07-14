---
title: Importing multiple bank statements in Continia Banking
date: 01-07-2025
description: Learn how to set up the possibility to import multiple bank statements.
id: CB-245
lang: en
---

# Importing multiple bank statements

With Continia Banking, you can efficiently import and process multiple bank statement files (CAMT.053 and CAMT.054) within a single bank account reconciliation or payment reconciliation journal. The system gives you the flexibility to group statements by day, week, month, or without any time restriction, according to your organization’s needs. If a statement includes transactions that fall outside your defined aggregation period, you have the option to let the system automatically create a new reconciliation for those transactions.

The configuration for this feature is managed on the Bank Account Card by selecting **Related** > **Reconciliation Import Setup** from the action bar.

> [!NOTE]
>
> You can enable Importing multiple bank statements from the **Continia Feature Management** page.

To enable importing multiple statements:

1. On the **Continia Feature Management** page, enable **Importing multiple bank statements**.
2. Search ({{search}}) for and select **Bank Accounts**.
3. Open the Bank Account Card and on the action bar, select **Related** > **Reconciliation Import Setup.**
4. On the **Import Reconciliation Setup** page, you can work with the following settings:
   * **Transaction Type** - select the type of bank transaction to import:
     * **Account Statement** - imports full account statements.
     * **Transactions** - imports individual transaction records.    
   * **Aggregation period** - select how to group transactions during import:
     - **All** - no time restriction; all statements can be imported into the same reconciliation, regardless of date.     
     - **Daily** - group statements by individual day. Each reconciliation includes only statements from the same date.     
     - **Weekly** - group statements by week. Only statements with dates within the same week are included in one reconciliation.     
     - **Monthly** - group statements by month. Only statements with dates within the same month are included in one reconciliation.
   - **Allow new Reconciliations** - select to automatically create a new bank reconciliation for statements that fall outside the selected aggregation period.
   - **Import with Job Queue** - select to run the import as a background job using the job queue. This allows imports to be processed without interrupting your work using the `71554352 CTS-PI Bank Recon JobQueue` codeunit.
   - **Job Queue Import Method** - select how the job queue processes the import.
     - **Import** – import statements only.
     - **Import and Match** – import statements and automatically match transactions.
     - **Download (Processing only)** – download statements without importing them.
   - **Job Queue Statement Type** - select the statement type for job queue imports. Options are Bank Reconciliation or Payment Reconciliation.

   