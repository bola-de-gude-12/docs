---
title: HSBC and Payment Management
description: Integration with the bank system HSBC
date: 05-12-2024
id: PM-285
lang: en
---

# HSBC

With Payment Management, you can use manual and direct communication to send bank data between HSBC and Microsoft Dynamics 365 Business Central. To establish direct communication between your bank and Microsoft Dynamics 365 Business Central, you need to have an agreement in place with HSBC. 

This article lists the file format requirements for all communication methods.

To learn more about how to set up communication:

- Manual communication HSBC- refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article.
- Direct communication HSBC through Yapily - refer to the [Onboarding  Yapily with direct communication](@PM-268) article. 

> [!NOTE]
>
> Connecting banks through Yapily is only supported for Business Central version 24 or higher.

## To connect with HSBC manually

When initiating manual communication with HSBC, the following features are supported:

| Communication | Send payments                | Import status | Update status | Import payments | Reconcile                    |
| ------------- | ---------------------------- | ------------- | ------------- | --------------- | ---------------------------- |
| Manual        | [PAIN.001](@PM-123#PAIN.001) | {{cross}}     | {{cross}}     | {{cross}}       | [CAMT.053](@PM-123#CAMT.053) |

Refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article, for more information on how to set up the manual connection. 

## To connect with Yapily Connect

{{include "yapily-fees"}}
For direct communication between your bank and Microsoft Dynamics 365 Business Central, you can use Yapily Connect. Yapily is an Open Banking payment service provider. 

Before you can establish direct communication with your bank through Yapily, it is necessary to grant Yapily the required permissions. For more information about granting permissions, please contact your bank or refer to the [Preparing for Direct Communication Through Yapily](@PM-397) article. 

| Communication   | Send payments             | Import status | Update status             | Import payments | Reconcile                 |
| --------------- | ------------------------- | ------------- | ------------------------- | --------------- | ------------------------- |
| Direct (Yapily) | [Yapily Connect](@PM-268) | {{cross}}     | [Yapily Connect](@PM-268) | {{cross}}       | [Yapily Connect](@PM-268) |

> [!NOTE]
>
> Bank restrictions for bulk payments may apply. Refer to the [Bulk payments](https://docs.yapily.com/pages/payments/bulk-payments/additional-information/#known-restrictions) article on article on Yapily's documentation site.
>
> **Current Issue:**
> HSBC Corporate is experiencing issues with processing bulk payments.

### Supported functionality

{{include "yapily-payments"}}

| Functionality                                              | HSBC</br>UK Business                                  | HSBC</br> Kinetic<a href="#footnote-1"><sup>1</sup></a> | HSBC</br> Corporate<a href="#footnote-1"><sup>1</sup></a> |
| ---------------------------------------------------------- | ----------------------------------------------------- | ------------------------------------------------------- | --------------------------------------------------------- |
| Faster Payments Single                                     | {{checkmark}}                                         | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>)   | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>)     |
| Faster Payment Bulk                                        | {{checkmark}}                                         | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>)   | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>)     |
| International Single<a href="#footnote-2"><sup>2</sup></a> | ({{checkmark}}<a href="#footnote-2"><sup>2</sup></a>) | {{cross}}                                               | ({{checkmark}}<a href="#footnote-2"><sup>2</sup></a>)     |
| Bank Reconciliation                                        | {{checkmark}}                                         | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>)   | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>)     |
| Direct Debit                                               | {{cross}}                                             | {{cross}}                                               | {{cross}}                                                 |

<small style>

<div class="footnotes">
 <hr />
 <ol>
 <li id="footnote-1">Direct communication with this bank via Yapily is currently in beta. If you encounter any issues, please reach out to Continia Support for assistance.</li>
 <li id="footnote-2">International Single is only available in beta and is currently being tested.</li>
 </ol>
</div>

</small>

Refer to the [Onboarding  Yapily with direct communication](@PM-268) article, for more information how to set it up. 

## Related information

[About direct and manual bank communication](@PM-158)  

[Onboarding Yapily to use Direct Communication](@PM-268)
