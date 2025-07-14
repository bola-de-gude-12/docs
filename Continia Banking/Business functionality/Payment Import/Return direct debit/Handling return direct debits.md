---
title: Handling returned direct debits
description: Learn how to work with returned direct debits by choosing a processing method.
date: 11-06-2025	
id: CB-243
lang: en
---

# Handling returned direct debits

When a direct debit payment is returned by the bank after initial processing it must be identified, matched, and handled appropriately in the system. Continia Banking lets you process returned direct debits after they have been identified and matched, and offers configuration settings that control how these transactions are handled automatically or manually.

## To set up the handling of returned direct debits

To enable handling of returned direct debits:
1. On the **Continia Feature Management** page, enable **Direct Debit Return**.
2. On the **Banking Import Setup** page, in the **Direct Debit Return** FastTab, enable **Direct Debit Return Matching**. 
3. In the **Default Direct Debit Return Processing** field, select on of the following options to process matched returned direct debits:
   * **Apply to original payment** - unapply the original invoice and payment, then apply the open payment to the return direct debit transaction in the reconciliation. Optionally, set the invoice **On Hold** using the configured setting in **Banking Import Setup**.
   * **Reverse original payment** - reverse the full payment using either the original posting date or the bank statement date. The reversed entry is automatically posted in the reconciliation.
   * **Apply to account** - leave the original transaction unchanged and post the return direct debit as an on-account entry.

4. Under **Direct Debit Return Mode**, select **Manual** or **Automatic**. If set to **Automatic**, return direct debit processing is fully automated during the regular matching routine.
5. Use the **On Hold** field to automatically place the invoice on hold if the invoice is reopened due to the return. This applies when using the **Apply to original payment** or **Reverse original payment** options. 
6. If you selected **Reverse original payment**, you can use the **Reverse Posting Date** field to determine the date used for the reversal. Options are: **Statement Date** and **Posting Date**.

## To handle return direct debits

Once a return direct debit has been identified and matched, you can process it using one of the available methods. The processing behavior follows the default method defined in the [Banking Import Setup](#to-set-up-the-handling-of-return-direct-debits) and can be initiated from several locations:

- **Payment Application Review Page** - on this page the **Direct Debit Return Entries** section lists the returned entries for you displaying the **Return Reason Code** and **Return Reason Description**. You can select a pending return direct debit and on the action bar, select **Process Direct Debit Return** to process it.
- **Payment Reconciliation Journal** - select the line or multiple lines with status **Direct Debit Return** and Apply Automatically. The status now changes to **Pending Direct Debit Return**. On the action bar, select **Direct Debit Return Processing**.
- **Bank Account Reconciliation**: select the line or multiple lines and select **Direct Debit Return Processing**.

After processing, the status of the line will change based on the chosen processing method:

- If reversed, the line status changes to **Complete**.
- If reapplied or unchanged:
  - In **Bank Account Reconciliation**, the status may change to **Pending Cash Receipt Journal**, indicating that the return has been processed but further action is needed to close the transaction.
  - In the **Payment Reconciliation Journal**, the line status changes directly to **Completed**, regardless of the processing type.

