---
title: Updating and Resetting the payment status in Continia Banking
description: How to use the Continia Banking functionality in payment journals.
date: 19-03-2025
id: CB-112
lang: en
---

# Updating and resetting the payment status

In Continia Banking, payment statuses in extended payment journals provide real-time validation and updates on your payments. These statuses ensure your payment information complies with bank requirements and keep you informed about the necessary actions and payment progress.

For direct bank communication, Continia Banking automatically imports status updates from your bank, though the update frequency can vary. Most banks use the ISO PAIN.002 status file, which provides two types of updates:
* **Initial Status** - sent immediately after the bank receives the ISO PAIN.001 payment file, indicating:
  * *Processing* - the payment file format is valid and is being processed.
  * *Rejected* - the payment file is invalid and has been rejected.
* **Subsequent Status** - sent after the bank validates the payment lines, indicating for example:
    * *Amount Adjusted* - The payment amount has been modified. This adjustment has been made by the bank and could be due to a change in the currency exchange rate.
    * *Rejected* - the bank did not accept the payment.
    * *Paid* - the payment has been completed.
    

For a complete overview of all statuses, refer to the [Payment Statuses](@CB-111) article. 

## To update the status

When a status file is available in the bank, you can import the file.

To update the status:

1. Search ({{search}}) for and select **Payment Journals**. 
1. On the payment journal page, in the page header, go to the **Batch Name** field and choose the payment journal.
1. On the payment journal, go to the action bar and select **Home** > **Update Status**. If any status files are available from the bank, the status of the payment lines will be updated. If the account uses manual communication and the bank supports it, a file dialog will appear, allowing you to select a CAMT.054 file.

## To reset the payment status

You can reset the status of a payment line that has been sent or exported if you need to modify the payment details or resend/reexport the payment. For payments sent via direct bank communication, you must first contact your bank to cancel the payment before resetting the status.

To reset the payment status:
1. Search ({{search}}) for and select **Payment Journals**.
2. On the Payment Journals page, select the lines you want to reset.
3. On the action bar, select **Bank** > **Void Payments**.
