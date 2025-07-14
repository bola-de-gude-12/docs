---
title: ING InsideBusiness
description: Integration with the bank system ING InsideBusiness
date: 08-08-2022
id: PM-170
lang: en
---

# ING InsideBusiness

With Payment Management, you can use direct or manual communication to send bank data between ING InsideBusiness and Microsoft Dynamics 365 Business Central. 

For direct communication between your bank and Microsoft Dynamics 365 Business Central, Payment Management collaborates with Bizcuit, a PSD2-licensed payment service provider. 

This article lists the file format requirements for both communication methods. To learn more about how to set up communication:

* Direct communication ING InsideBusiness - refer to the [Direct communication (using Bizcuit)](@PM-165) article.
* Manual communication ING InsideBusiness - refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 



## File formats

How to integrate your bank with Payment Management depends on the bank communication types and files your bank supports. The table below displays what is supported for direct and manual communication with ING InsideBusiness.

| Bank communication | Send payments                                                | Import status | Update status       | Import payments                                              | Reconcile                                                    | Direct Debit        | G-accounts                                           |
| ------------------ | ------------------------------------------------------------ | ------------- | ------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------- | ---------------------------------------------------- |
| Direct             | [PSD2 API](@PM-123)                                          | Not supported | [PSD2 API](@PM-123) | Not supported                                                | [PSD2 API](@PM-123)                                          | Not supported       | Not supported <a href="#footnote-1"><sup>1</sup></a> |
| Manual             | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal") | Not supported | Not supported       | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal") | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments") | [PAIN.008](@PM-123) | Not supported                                        |

<small style> <div class="footnotes">  <hr />  <ol>   <li id="footnote-1">Only the transferring of funds from G-accounts is not supported.</li>  </ol> </div> </small>



## Related information

[About direct and manual bank communication](@PM-158)  
