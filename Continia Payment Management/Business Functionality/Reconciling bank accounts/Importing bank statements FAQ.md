---
title: Importing Bank Statements FAQ
date: 03-04-2025
description: Find the answer to frequently asked questions about importing bank statements.
id: PM-405
lang: en
---

# Importing Bank Statements FAQ

If you’re having trouble importing bank statements for reconciliation, the answers to the following questions can help resolve the most common issues.

## How can I verify my settings?
To ensure **Statement Intelligence** works correctly, check the following:
- Navigate to **Payment Management Setup** > **Usage Area Settings** and verify that **Statement Intelligence** is enabled.
- For the **Bank Card**, select your bank, then select **Edit**, and confirm that the correct file format is selected.
- For the **Bank Account**, double-check that all required fields are filled out.
  ![](/images/PM365/import-faq-bank-account-check.png)

## How can I solve an interrupted statement import?
If you encounter an issue where the import of your account statement has been interrupted, this may be due to one of the following causes:
- Files imported in the wrong order.
- Deleted or corrected lines in previously imported statements.

To resolve this:
1. Because the new statement balance won’t match the calculated balance, create a new statement to continue reconciliation
2. Disable **Statement Intelligence** by navigating to the **Bank Account Card**, and on the **Statement Intelligence** FastTab, turn off the **Import all Available Statements** field.
3. Manually import the statements until the error occurs again. Once the error appears, create a new reconciliation to identify the issue.

## How can I resolve missing imported entries?
If you see the message:
*"No account statement files were found for bank account XXXXX. Statements for other bank accounts or periods may be available."*

Verify the following:
- Make sure that the account and period selected match the data you're attempting to import.
- Check that files are available for the correct bank account and period.

## How can I handle duplicate entries in Statement Intelligence?
If duplicate entries appear during reconciliation, you can remove them to ensure accurate processing:
1. **Remove duplicates** in **Bank Export Data** before reconciling. To do this, first delete the duplicate entries from the account statement.
3. Filter the data by:
   - **Bank Account No.**  - select the account you're working on.
   - **Record Type** - set to Account Statement.
   - **Record Subtype** - select Header.
4. Once filtered, mark the entry as **Imported to Company** to proceed with the reconciliation.

## How can I resolve missing bank account ledger entries?
If you cannot find a specific bank account entry during reconciliation:
1. Navigate to **Bank Account Ledger Entries**. Entries that are already posted will not appear in the reconciliation. Look for a checkmark in the **Open** column to confirm the entry's status.
2. If the entry is not visible, verify whether it has already been closed or posted.
