---
title: The payment statuses in Continia Banking
description: How to read payment statuses in payment journals.
date: 28-05-2025
id: CB-111
lang: en
---

# The payment statuses

In Continia Banking, various statuses in the with Banking extended journals indicate the current state of each payment transaction. These statuses help you monitor and manage payments effectively, from validation to completion. Use the following list to interpret the meaning of each status:

| <div style="width:215px">Status</div>                  | Description                                                  |
| ------------------------------------------------------ | ------------------------------------------------------------ |
| Amount Adjusted <a href="#footnote-1"><sup>1</sup></a> | The bank has finalized the payment, and the payment amount has been adjusted for currency differences. This is common when there are discrepancies between the currency exchange rates used by Business Central and the bank. The Amount LCY (Local Currency) will be updated automatically if the bank supports this status. You can post the line. |
| Approved                                               | The payment has been approved by all necessary parties and is ready to be processed by the bank. |
| Invalid                                                | Errors exist on the payment line. Check the **Payment Journal Errors** section in the right panel to identify and correct these errors. |
| Manual                                                 | The payment method indicates a manual process; the payment won't be sent to the bank but handled manually. |
| Not Validated                                          | The payment hasn't been validated by Continia Banking, often due to missing or incomplete bank account details. If you haven't enabled automatic validation, you might have to select **Validate Payments**. |
| Paid <a href="#footnote-1"><sup>1</sup></a>            | The payment has been completed in the bank.                  |
| Pending Approval                                       | The line must be approved according to the setup before the payment lines can be sent. |
| Pending Return Direct Debit                            | The return of the Direct Debit payment is pending.           |
| Processing <a href="#footnote-1"><sup>1</sup></a>      | The payment has been sent to the bank through direct communication and is currently being processed. |
| Rejected <a href="#footnote-1"><sup>1</sup></a>        | The bank has rejected the payment, possibly due to issues like insufficient funds, errors in the payment details, or disapproval from a company approver. Investigate the rejection reason to resolve the issue. |
| Rejected Approval                                      | If an approver rejected an approval request, the status of the relevant lines in the payment journal  change to Rejected Approval. Review the comments in the right panel to find out why the line is rejected. Make the necessary adjustments to the line and resend it for approval or delete it. |
| Direct Debit Return                                    | The Direct Debit payment has been returned by the bank.      |
| Sent to bank                                           | The payment is sent to the bank.                             |
| Sent to online                                         | The payment has been exported and sent to Continia Online.   |
| Valid                                                  | The payment information is fully validated and ready to be sent to the bank, either directly or through a file export. |

 

 <small style>

<div class="footnotes">
  <hr />
  <ol>    
    <li id="footnote-1">This status can only be imported from the bank when using direct bank communication. In addition, the bank must support the given status update for you to receive it, as not all banks support the statuses specified in the list.</li>    
  </ol>
</div>

</small>

