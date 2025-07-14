---
title: Barclays and Payment Management
description: PM integration with Barclays.
date: 05-12-2024
id: PM-222
lang: en
---

# Barclays

With Payment Management, you can use direct communication to send bank data between Barclays and Microsoft Dynamics 365 Business Central. For direct communication between your bank and Microsoft Dynamics 365 Business Central, you can integrate with Barclays directly or use Yapily, an Open Banking payment service provider.

This article lists the file format requirements for both communication methods. To learn more about how to set up communication:

- Manual communication Barclays - refer to the general [To set up bank accounts to use manual communication article](@PM-3). 
- Direct communication Barclays - refer to the [Onboarding Barclays with Direct Communication](@PM-306).
- Direct communication Barclays using Yapily - refer to the [Onboarding Yapily to use Direct Communication](@PM-268).

## To connect with Barclays manually

When initiating manual communication with Barclays, the following features are supported: 

* Payment export
* Statement import: 
  * file format XML

* Payment methods: 
  * FP
  * Chaps
  * SEPA
  * IC


| Bank communication | Send payments | Import status | Update status | Import payments | Reconcile |
| ------------------ | ------------- | ------------- | ------------- | --------------- | --------- |
| Manual             | MT103         | {{cross}}     | {{cross}}     | {{cross}}       | MT940     |

## To connect with Barclays directly

To use direct communication, you must subscribe to the Barclays bank integration and set up your Barclays bank accounts to use direct communication in Business Central. 

> [!IMPORTANT]
>
> If you want to connect with Barclays directly, get in touch with [Continia Support](@PM-21). 

### File formats

How you can integrate your bank with Payment Management depends on the types of bank communication and files your bank supports. The table below displays what is supported for direct communication with Barclays.

| Bank communication | Send payments                                                | Import status                                                | Update status                                                | Import payments                                              | Reconcile                                                    |
| ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Direct             | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal" ) | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal" ) | [CAMT.054](@PM-123#CAMT.054 "Update status in the payment journal" ) | [CAMT.054](@PM-123#CAMT.054 "Import customer payments in the cash receipts journal" ) | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments" ) |



## To connect with Yapily Connect

{{include "yapily-fees"}}

For direct communication between your bank and Microsoft Dynamics 365 Business Central, you can use Yapily Connect. Yapily is an Open Banking payment service provider. 

Before you can establish direct communication with your bank through Yapily, it is necessary to grant Yapily the required permissions. For more information about granting permissions, please contact your bank or refer to the [Preparing for Direct Communication Through Yapily](@PM-397) article. 

> [!WARNING]
>
> When activating an approval workflow within Barclays Corporate, payments may disappear after being approved in the bank. Barclays and Yapily are aware of this issue. Recommended workaround:
> Use the approval flow in Payment Management and configure a workflow for Barclays that does not require multiple approvals.

### File formats

How you can integrate your bank with Payment Management depends on the types of bank communication and files your bank supports. The following table displays what is supported for direct communication with the Barclaycard Commercial Payments, Barclays Business, and Barclays Corporate banks.

| Bank communication | Send payments             | Import status | Update Status             | Import payments | Reconcile                 |
| ------------------ | ------------------------- | ------------- | ------------------------- | --------------- | ------------------------- |
| Direct             | [Yapily Connect](@PM-268) | {{cross}}     | [Yapily Connect](@PM-268) | {{cross}}       | [Yapily Connect](@PM-268) |

> [!NOTE]
>
> Before importing the first bank statements, you must make sure that the starting balance is entered on the Bank Account Card.

### Supported functionality using Yapily

{{include "yapily-payments"}}

> [!NOTE]
>
> Connecting banks through Yapily is only supported for Business Central version 24 or higher.

| Functionality                                              | Barclays</br> Business</br> | Barclays </br>Corporate</br> | Barclaycard </br>Commercial </br>Payments             |
| ---------------------------------------------------------- | --------------------------- | ---------------------------- | ----------------------------------------------------- |
| Faster Payment Single                                      | {{checkmark}}               | {{checkmark}}                | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| Faster Payment Bulk                                        | {{checkmark}}               | {{checkmark}}                | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| International Single<a href="#footnote-2"><sup>2</sup></a> | {{checkmark}}               | {{checkmark}}                | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| Bank Reconciliation                                        | {{checkmark}}               | {{checkmark}}                | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| Direct Debit                                               | {{cross}}                   | {{cross}}                    | {{cross}}                                             |

<small style>

<div class="footnotes">
 <hr />
 <ol>
 <li id="footnote-1">Direct communication with this bank via Yapily is currently in beta. If you encounter any issues, please reach out to Continia Support for assistance.</li>
     <li id="footnote-2">International Single is only available in beta and is currently being tested.</li>
 </ol>
</div>

</small>

> [!NOTE]
>
> Bank restrictions for bulk payments may apply. Refer to the [Bulk payments](https://docs.yapily.com/pages/payments/bulk-payments/additional-information/#known-restrictions) article on doc.yapily.com for more information.

## Related information

[About direct and manual bank communication](@PM-158)

[Onboarding Yapily to use Direct Communication](@PM-268)
