---
title: Transferring a line to the journal for manual handling
date: 08-04-2025
description: Transferring a line to the journal for manual handling.
id: CB-170
lang: en
---
# Transferring a line to the journal for manual handling

With Continia Banking, when bank statements are imported, transactions are matched to customer, vendor and employee ledger entries, automatically creating corresponding journal lines. However, some transactions might be new or previously unknown, requiring manual journal line creation. In these cases, you can manually transfer a Bank Acc. Reconciliation Line to a journal, post the entry, and reconcile it automatically.

The [**Banking Import Setup**](@CB-14) page, on the **Bank Account Reconciliation** FastTab, contains a the **Manual Handling** section where you can configure settings for manual line handling. The following fields are available:
- **Show Dialog** - a Boolean setting that lets controls whether the manual reconciliation dialog appears during the import process. The default value is true.
- **Default Journal Type** - specifies the default journal type for manual journal lines. Options include **Account Type**, **Cash Receipts**, **General**, and **Payments**. The default value is **General**. If **Account Type** is selected, the template type is determined by the account type of the bank account statement line.

When a bank statement line requires manual transfer, you can choose the account to post the journal line to, either directly on the Bank Account Reconciliation Line or within the journal after the line is created. Alternatively, when you select **Create Journal Line**, a dialog box appears with a prompt guiding you on how to post it.

To manually transfer a line to a journal:

1. On the **Bank Acc. Reconciliation** page, locate the bank statement line that you want to transfer. 
2. On the action bar, select **Manual Application** > **Set Manual Handling**. This changes the Reconciliation Status to **Manual** (this can only be done for lines with the status **Unsolved**). Flagging the line for manual handling ensures it is skipped when using the **Match Automatically** function, allowing you to process it later.
3. Select the lines to transfer, and on the action bar, select **Manual Application** > **Create Manual Journal Line**. If the **Show Dialog** option on the **Banking Import Setup page** is enabled, the dialog will contain settings similar to those for handling amount differences:
   - The **Amount** field will automatically display the Statement Amount from the Bank Acc. Reconciliation Line.
   - The **Journal Template Type** field will be prefilled with the default setting, but you can change it if needed.
   - You will need to select the appropriate account in the **Account Type** and **Account No.** fields for the journal line.
   - Ensure that the selected **G/L Account** allows direct posting.
   - The **Description** field will be prefilled with the description from the Bank Acc. Reconciliation Line, which you can modify as necessary.
4. Complete the process as needed.