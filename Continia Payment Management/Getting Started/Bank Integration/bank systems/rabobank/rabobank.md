---
title: Rabobank and Payment Management
description: Integration with the bank system Rabobank
date: 04-09-2024
id: PM-164
lang: en
---

# Rabobank

With Payment Management, you can use direct or manual communication to send bank data between Rabobank and Microsoft Dynamics 365 Business Central. For direct communication between your bank and Microsoft Dynamics 365 Business Central, you can integrate with Rabobank manually, directly through Continia, or directly through Bizcuit, a PSD2-licensed payment service provider. 

This article lists the file format requirements for all different communication methods. To learn more about how to set up communication:

* Manual communication Rabobank - refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 
* Direct communication Rabobank - refer to the [Onboarding Rabobank to use Direct Communication](@PM-274). 
* Direct communication Rabobank using Bizcuit- refer to the [Direct communication (using Bizcuit)](@PM-165) article.

## To connect to Rabobank 

To use direct communication, you must subscribe to the Rabobank bank integration and set up your Rabobank bank accounts to use direct communication in Business Central. For more details on how to set it up, get in touch with [Continia Support](@PM-21). 

> [!IMPORTANT]
>
> Available for Payment Management version 5.3.0 or higher.



### File formats

| Bank communication | Send payments                                                | Import status                                                | Update status                                                | Import payments                                              | Reconcile                    | Direct Debit        | G accounts<a href="#footnote-1"><sup>1</sup></a> |
| ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ---------------------------- | ------------------- | ------------------------------------------------ |
| Manual             | [PAIN.001](@PM-123#PAIN.001)                                 | {{cross}}                                                    | {{cross}}                                                    | [CAMT.054C](@PM-123#CAMT.054C)                               | [CAMT.053](@PM-123#CAMT.053) | [PAIN.008](@PM-123) | {{cross}}                                        |
| Direct             | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal" ) | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal" ) | [CAMT.054](@PM-123#CAMT.054 "Update status in the payment journal" ) | [CAMT.054](@PM-123#CAMT.054 "Update status in the payment journal" ) | [CAMT.053](@PM-123#CAMT.053) | [PAIN.008](@PM-123) | {{checkmark}}                                    |


<small style>


<div class="footnotes">


 <hr />
 <ol>
 <li id="footnote-1">A G account is a frozen account that you can only use to make payroll taxes or VAT payments to the Tax Administration. The recipient deposits the estimated amount of payroll taxes or VAT payments into your g account. You can use this amount solely to pay payroll taxes or VAT.</li>
 </ol>

</div>
</small>



## To connect to Rabobank using Bizcuit
For direct communication between your bank and Microsoft Dynamics 365 Business Central, you can use Bizcuit. Bizcuit is an Open Banking payment service provider. 

Bizcuit offers the following connections:

| Connection      | Consent method                     | Consent Period | Frequency     | Account type                                           | Payment flow          |
| --------------- | ---------------------------------- | -------------- | ------------- | ------------------------------------------------------ | --------------------- |
| Standard (PSD2) | Owner</br>BeheerderPlus            | 90 days        | Every 6 hours | Basic bank account</br>G account                       | Step-out (e.g. Ideal) |
| Premium (RDC)   | Bank mandate (*Papieren volmacht*) | Ongoing        | Every 15 mins | Basic bank account</br> Savings account </br>G account | In-app                |



### File formats

| Bank communication   | Send payments       | Import status | Update status       | Import payments | Reconcile           | Direct Debit | G accounts<a href="#footnote-1"><sup>1</sup></a> |
| -------------------- | ------------------- | ------------- | ------------------- | --------------- | ------------------- | ------------ | ------------------------------------------------ |
| Direct using Bizcuit | [PSD2 API](@PM-123) | {{cross}}     | [PSD2 API](@PM-123) | {{cross}}       | [PSD2 API](@PM-123) | {{cross}}    | {{checkmark}}                                    |

<small style>


<div class="footnotes">



 <hr />
 <ol>
 <li id="footnote-1">A G account is a frozen account that you can only use to make payroll taxes or VAT payments to the Tax Administration. The recipient deposits the estimated amount of payroll taxes or VAT payments into your g account. You can use this amount solely to pay payroll taxes or VAT.</li>
 </ol>

</div>
</small>

## Related information

[About direct and manual bank communication](@PM-158)  

[Direct communication (using Bizcuit)](@PM-165)

[The Netherlands and PM FAQ](@PM-400)
