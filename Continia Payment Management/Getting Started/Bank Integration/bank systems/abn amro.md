---
title: ABN AMRO and Payment Management
description: Integration with the bank system ABN AMRO
date: 04-09-2024
id: PM-126
lang: en
---

# ABN AMRO

With Payment Management, you can use direct or manual communication to send bank data between ABN AMRO and Microsoft Dynamics 365 Business Central.

For direct communication between your bank and Microsoft Dynamics 365 Business Central, Payment Management collaborates with Bizcuit, a PSD2-licensed payment service provider. 

This article lists the file format requirements for both communication methods. To learn more about how to set up communication:

* Manual communication ABN AMRO - refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 
* Direct communication ABN AMRO - refer to the [Onboarding ABN AMRO to use Direct Communication](@PM-333) article.
* Direct communication ABN AMRO using Bizcuit - refer to the [Direct communication (using Bizcuit)](@PM-165) article.

## To connect to ABN AMRO manually

#### File formats

How to integrate your bank with Payment Management depends on the bank communication types and files your bank supports. The following table displays what is supported for manual communication with ABN AMRO.  

| Bank communication | Send payments                | Import status                                | Update status                                | Import payments                | Reconcile                    | Direct Debit                                 | G-accounts                                                   |
| ------------------ | ---------------------------- | -------------------------------------------- | -------------------------------------------- | ------------------------------ | ---------------------------- | -------------------------------------------- | ------------------------------------------------------------ |
| Manual             | [PAIN.001](@PM-123#PAIN.001) | <p style="text-align: center;">{{cross}}</p> | <p style="text-align: center;">{{cross}}</p> | [CAMT.054C](@PM-123#CAMT.054C) | [CAMT.053](@PM-123#CAMT.053) | <p style="text-align: center;">{{cross}}</p> | <p style="text-align: center;">{{cross}}</p><a href="#footnote-1"><sup>1</sup></a> |

<small style> <div class="footnotes">  <hr />  <ol>   <li id="footnote-1">Only the transferring of funds from G-accounts is not supported.</li>  </ol> </div> </small>
## To connect to ABN AMRO directly

> [!IMPORTANT]
>
> Available for Payment Management version 7.1.5.0 or higher.

ABN AMRO has two kinds of online banking services, and they both have some payment limitations related to international payments:

* **Internet Banking Business** - cross-border payments can only be done through a manual file upload or manually entered in the banking environment.
* **Access Online** - supports cross-border payments through direct communication, but only as single payments.

#### File formats

How to integrate your bank with Payment Management depends on the bank communication types and files your bank supports. The following table displays what is supported for direct with ABN AMRO.  

| Bank communication | Send payments                | Import status                                                | Update status                                                | Import payments | Reconcile                    | Direct Debit | G-accounts                                       |
| ------------------ | ---------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | --------------- | ---------------------------- | ------------ | ------------------------------------------------ |
| Direct             | [PAIN.001](@PM-123#PAIN.001) | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal" ) | [CAMT.054](@PM-123#CAMT.054 "Update status in the payment journal" ) | {{cross}}       | [CAMT.053](@PM-123#CAMT.053) | {{cross}}    | {{cross}} <a href="#footnote-1"><sup>1</sup></a> |

<small style> <div class="footnotes">  <hr />  <ol>   <li id="footnote-1">Only the transferring of funds from G-accounts is not supported.</li>  </ol> </div> </small>

## To connect to ABN AMRO using Bizcuit

For direct communication between your bank and Microsoft Dynamics 365 Business Central, you can use Bizcuit. Bizcuit is an Open Banking payment service provider. 

Bizcuit offers the following connections:

| Connection           | Consent Method          | Consent Period | Frequency     | Account type       | Payment flow                |
| -------------------- | ----------------------- | -------------- | ------------- | ------------------ | --------------------------- |
| Standard<br />(PSD2) | Owner<br />(*Eigenaar*) | 90 days        | Every 30 mins | Basic bank account | Step-out<br />(e.g., Ideal) |

#### File formats

| Bank communication   | Send payments | Import status | Update status | Import payments | Reconcile | Direct Debit | G-accounts                                       |
| -------------------- | ------------- | ------------- | ------------- | --------------- | --------- | ------------ | ------------------------------------------------ |
| Direct using Bizcuit | PSD2 API      | {{cross}}     | PSD2 API      | {{cross}}       | PSD2 API  | {{cross}}    | {{cross}} <a href="#footnote-1"><sup>1</sup></a> |

<small style> <div class="footnotes">  <hr />  <ol>   <li id="footnote-1">Only the transferring of funds from G-accounts is not supported.</li>  </ol> </div> </small>

## Related information

[About direct and manual bank communication](@PM-158)  

[The Netherlands and PM FAQ](@PM-400)
