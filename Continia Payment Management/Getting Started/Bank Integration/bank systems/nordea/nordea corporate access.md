---
title: Nordea Corporate Access
description: Integration with the bank system Nordea Corporate Access
date: 10-08-2024
id: PM-139
lang: en
---

# Nordea Corporate Access

With Payment Management, you can use direct or manual communication to send bank data between Nordea Corporate Access and Microsoft Dynamics 365 Business Central. 

This article lists the file format requirements for both communication methods. To learn more about how to set up communication:

* Direct communication Nordea Corporate Access - refer to the [Onboarding Nordea with Direct Communication](@PM-182) article.
* Manual communication Nordea Corporate Access - refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 



## File formats

How you can integrate your bank with Payment Management depends on the types of bank communication and files your bank supports. The table below displays what is supported for direct and manual communication with Nordea Corporate Access.  


| Bank communication | Send payments| Import status | Update status | Import payments| Reconcile|
| --- | --- | --- | --- | --- | --- |
| Direct | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal") | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal") | [CAMT.054D](@PM-123#CAMT.054D "Update status in the payment journal") | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal" ) | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments")<br />[CAMT.053E](@PM-123#CAMT.053 "Reconcile bank statements and import payments") |
| Manual <a href="#footnote-1"><sup>1</sup></a> | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal") | {{cross}} | {{cross}} | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal")<br />[PBS Sector](@PM-123#PBS "Import NETS PBS FIK DK customer payments in the cash receipts journal.")<br />[BG Max](@PM-123#BGMAX "Import BG Max SE customer payments in the cash receipts journal.")<br />[OCR-NO](@PM-123#OCR-NO "Import OCR-Giro NO customer payments in the cash receipts journal." )<br />[Total IN](@PM-123#Total-IN "Import Total IN SE customer payments in the cash receipts journal.") | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments")<br />[CAMT.053E](@PM-123#CAMT.053 "Reconcile bank statements and import payments") |

<small style>

<div class="footnotes">

 <hr />

 <ol>

 <li id="footnote-1">For manual communication, you must use the bank system code: NDEA-CORP.</li>



 </ol>

</div>

</small>



## Related information

[About direct and manual bank communication](@PM-158)

