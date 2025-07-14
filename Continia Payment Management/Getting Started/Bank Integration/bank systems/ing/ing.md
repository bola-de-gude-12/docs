---
title: ING and Payment Management
description: Integration with the bank system ING
date: 08-08-2022
id: PM-136
lang: en
---

# ING

With Payment Management, you can use direct or manual communication to send bank data between ING and Microsoft Dynamics 365 Business Central. For direct communication between your bank and Microsoft Dynamics 365 Business Central, Payment Management collaborates with Bizcuit, a PSD2-licensed payment service provider. 

This article lists the file format requirements for both communication methods. To learn more about how to set up communication:

* Direct communication ING - refer to the [Direct communication (using Bizcuit)](@PM-165) article.
* Manual communication ING - refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 



## To connect to ING

How to integrate your bank with Payment Management depends on the bank communication types and files your bank supports. The table below displays what is supported for direct and manual communication with ING.

If you use manual communication, follow the link for manual communication above for more information on how to order the files.  
<br>

| Communication | Send payments                | Import status | Update status       | Import payments                | Reconcile                    | Direct Debit        | G-accounts                     |
| ------ | ---------------------------- | ------------- | ------------------- | ------------------------------ | ---------------------------- | ------------------- | ------------------------------ |
| Direct | [PSD2 API](@PM-123)          | <p style="text-align: center;">{{cross}}</p> | [PSD2 API](@PM-123) | {{cross}}         | [PSD2 API](@PM-123)          | <p style="text-align: center;">{{cross}}</p> | {{cross}} <a href="#footnote-1"><sup>1</sup></a>        |
| Manual | [PAIN.001](@PM-123#PAIN.001) | <p style="text-align: center;">{{cross}}</p> | {{cross}} | [CAMT.054C](@PM-123#CAMT.054C) | [CAMT.053](@PM-123#CAMT.053) | [PAIN.008](@PM-123) | <p style="text-align: center;">{{cross}}</p> |

<small style> <div class="footnotes">  <hr />  <ol>   <li id="footnote-1">Only the transferring of funds from G-accounts is not supported.</li>  </ol> </div> </small>

## To connect to ING using Bizcuit

For direct communication between your bank and Microsoft Dynamics 365 Business Central, you can use Bizcuit. Bizcuit is an Open Banking payment service provider.

Bizcuit offers the following connections:

| Connection                  | Consent                                                   | Consent Period | Frequency     | Account type       | Payment flow          |
| --------------------------- | --------------------------------------------------------- | -------------- | ------------- | ------------------ | --------------------- |
| Standard<br />(PSD2)        | Legal representative<br />(*Wettelijk vertegenwoordiger*) | 90 days        | Every 30 mins | Basic bank account | Step-put<br />(Ideal) |
| Inside Business<br />(PSD2) | Administrator<br />(*Beheerder*)                          | 90 days        | Every 30 mins | Basic bank account | Step-put<br />(Ideal) |



## Related information

[About direct and manual bank communication](@PM-158)  
