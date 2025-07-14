---
title: Voiding a payment
description: Learn how to (force) void a payment line.
date: 04-06-2025
id: PM-408
lang: en
---

# Voiding a payment

Occasionally, you may need to void payments. Maybe because of a mistake, a change in payment details, or a problem in the communication with the bank. Continia makes this easier by letting you void one or more payment journal lines at once, so you can manage payments more efficiently. 

> [!IMPORTANT]
>
> Voiding a payment in the payment journal only affects your accounting records in Business Central. It does NOT stop or recall the actual bank transaction. If the payment has already been processed by the bank, you must contact your bank to cancel or recall the payment.

Below are two workflows for voiding payments: the standard procedure and the force void option.

## Standard workflow: to void a payments after bank rejection

If you export payments to a file and the payment gets rejected, you can void it directly in the payment journal. 

To void a payment in the Payment Journal:

1. On the **Payment Journals** page, select the line you wish to void.
2. On the action bar, select **Bank** > **Void**.

## Special workflow: to force void payments

The Force Void function should only be used in special situations, such as when something has gone wrong with the normal process—for example, if there is a technical issue with direct bank communication.

> [!IMPORTANT]
> Always make sure to cancel the payment in your bank before using Force Void in Business Central. Force voiding does not cancel the payment at the bank; it only updates your accounting records.

To force void a payment:
1. On the **Payment Journals** page, select the line(s) you want to force void.
2. On the action bar, select **Actions > Functions > Force Void Payment**.
3. Confirm the action. The selected payment will be force voided in the journal.
