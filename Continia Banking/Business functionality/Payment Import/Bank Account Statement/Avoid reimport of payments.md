---
title: Preventing Bank Statement Reimport in Reconciliation
description: How to delete a duplicate line and avoid reimporting payments.
date: 31-03-2025
id: CB-151
lang: en
---

# Preventing bank statement reimport in reconciliation

Continia Banking uses an ID to prevent importing duplicate transactions. However, certain situations can still result in duplicates. For example, if you are using manual communication and the bank file lacks an unique ID, Continia Banking can't determine if the file was previously imported. Similarly, with direct communication, calling the same file multiple times generates new reference IDs for each call, which may cause the same transaction to be imported again.

The following sections outline how to prevent the reimport of duplicate lines in both the Payment Reconciliation Journal and the Bank Account Reconciliation.

## To avoid reimport in the Payment Reconciliation Journal

To prevent future imports of duplicate payments, you can manually delete the duplicate payment reconciliation journal lines and mark them as imported.

To delete a duplicate line in the Payment Reconciliation Journal:

1. Search {{search}} for and select **Payment Reconciliation Journal**.
2. Open the relevant journal.
3. On the action bar, select **Page** > **Show More Columns**.
4. Select the payment line that you want to eliminate for reimport.
5. On the action bar, select **Related** > **Details** > **Delete and set as imported**.

The selected line will be removed, and the corresponding entry in **Bank Transactions - Continia Banking** will be updated to show **Imported to the Company**. This status indicates that the transaction has already been processed and cannot be imported again, ensuring it won’t be duplicated in future imports.

## To avoid reimport in the Bank Acc Reconciliation

To prevent future imports of duplicate payments, you can manually delete the duplicate payment lines and mark them as imported.

To delete a duplicate line in the Bank Acc Reconciliation:

1. Search {{search}} for and select **Bank Acc Reconciliation**.
2. Open the relevant journal.
3. On the action bar, select **Page** > **Show More Columns**.
4. Select the payment line that you want to eliminate for reimport.
5. On the action bar, select **Actions** > **Other** > **Delete and set as imported**.

The selected line will be removed, and the corresponding entry in **Bank Transactions - Continia Banking** will be updated to show **Imported to the Company**. This status indicates that the transaction has already been processed and cannot be imported again, ensuring it won’t be duplicated in future imports.
