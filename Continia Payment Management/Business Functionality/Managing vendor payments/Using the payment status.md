---
title: Using the payment status
description: How to use the Payment Management functionality in payment journals
date: 29-04-2021
id: PM-89
lang: en
---

# Using the Payment Status

Payment suggestions in Payment Management extended payment journals are automatically validated to ensure compliance with the bank's requirements and the presence of all necessary payment information. The status on the payment line keeps you informed about any required actions and the payment progress.

When utilizing direct bank communication, Payment Management will automatically import a status file from the bank. It's important to note that the frequency of status updates may vary. 

Most banks support the ISO PAIN.002 status file, which is sent back to the payment journal in two different editions: 

- First status update - occurs immediately after the bank has received the ISO PAIN.001 payment file. There are two possible statuses:
  - **Processing** - indicates that the payment file is in a valid format and is being processed successfully.
  - **Rejected** - indicates that the payment file is invalid and has been rejected.

- The following status update - occurs when the bank has validated the payment lines. The status can be:
  - **Awaiting**
  - **Amount Adjusted**
  - **Rejected**
  - **Paid**


Use the following list to interpret the meaning of the statuses:

| Status | Description |
| --- | --- |
| Not Validated | The payment has not yet been validated by Payment Management. This can be due to a missing bank account, making it impossible to validate the payment information. |
| Valid | All payment information has been validated, and the payment is ready to be sent using direct communication or exported in a file to the bank. |
| Invalid | One or more errors have been found on the payment line. Use the **Payment File Errors** in the lower right corner of the payment journal page to identify how to fix the errors. |
| Manual | The payment method of the payment line indicates that this is a manual payment. I.e. the payment will not be sent to the bank but must be processed by yourself. |
| Sent | The payment has been exported in a file using manual communication. This is the final status for payments being processed by manual communication. |
| Uncertain | It is uncertain whether the payment has been successfully processed, as we have not received any confirmation from the bank. You must update the payment status again, and if it remains unchanged, check the bank's online portal to see if the payment has been processed. If the payment is not visible in the bank, it might be due to a timeout during the communication process. In such a scenario, you must void the payment and send it again. |
| Processing <a href="#footnote-1"><sup>1</sup></a> | The payment has been sent to the bank using direct communication and is currently being processed in the bank. |
| Awaiting <a href="#footnote-1"><sup>1</sup></a> | The payment needs to be approved by a second approver in the bank. |
| Amount Adjusted <a href="#footnote-1"><sup>1</sup></a> | The payment has been finalized by the bank, and the payment line's amount has been adjusted based on currency differences. If you made the payment in a foreign currency, it's possible that the currency exchange rate used in Business Central might not match the bank's exchange rate. If your bank supports this type of status file, the currency exchange rate and the corresponding Amount LCY will be automatically updated on the payment line. This ensures accurate posting of the Amount LCY, avoids future exchange rate adjustments, and facilitates a seamless bank statement reconciliation process. |
| Rejected <a href="#footnote-1"><sup>1</sup></a> | The payment has been rejected by the bank for various reasons. This can occur if a second approver in your company rejects the payment, in which case you should consult with them to understand the reason for the rejection. Another possibility is that the payment was rejected due to errors found, such as an invalid bank account number. Additionally, depending on your bank agreement, insufficient funds in your account may result in payment rejection. |
| Paid <a href="#footnote-1"><sup>1</sup></a> | The payment has been completed in the bank. |

 

 <small style>

<div class="footnotes">
  <hr />
  <ol>    
    <li id="footnote-1">This status can only be imported from the bank when using direct bank communication. In addition, the bank must support the given status update for you to receive it, as not all banks support the statuses specified in the list.</li>    
  </ol>
</div>
</small>

## To update status

When a status file is available in the bank, you can import the file.

To update the status:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journals**, then select the related link. 
1. On the payment journal page, in the page header, go to the box **Batch Name** and choose the desired payment journal.
1. On the payment journal, go to the action bar and select **Bank** > **Update Status**. If any status files are available from the bank, the status of the payment lines will be updated.

To learn how to handle the updating of the payment journal line status on the bank card, refer to the [Managing Journal Lines](@PM-36) article

## To update the status automatically

To ensure that the payment status in the payment journal is always up to date, you can use the **Update Payment Journal Lines Status** setting on the bank card.

To update the status automatically:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Banks**, then select the related link. 
2. Open the bank card.
3. On the FastTab **Advanced**, navigate to the **Update Payment Journal Lines Status** field and select *Automatic*.

## To reset status

It is possible to reset the status of a payment line that has been sent or exported if the payment information should be changed or if you need to resend or reexport the payment. If the payment has been sent by direct communication, you must contact the bank and cancel the payment before resetting the status.

To reset the status:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journals**, then select the related link. 
1. On the payment journal page, mark the lines you wish to void.
1. Go to the action bar and select **Bank** > **Void Payments**.
