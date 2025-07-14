---
title: Allied Irish Banks and Allied Irish Bank Business in Payment Management
description: PM integration with Allied Irish banks.
date: 05-12-2024
id: PM-277
lang: en
---

# Allied Irish Banks (Business)

With Payment Management, you can use direct communication to send bank data between Allied Irish Banks (Business) and Microsoft Dynamics 365 Business Central through Yapily, an Open Banking payment service provider.

> [!IMPORTANT]
>
> To set up a connection with this bank, contact [Continia Support](@PM-21). They will assist you with the process.

To learn more about how to set up direct communication using Yapily,  refer to the [Onboarding Yapily to use Direct Communication](@PM-268).

## To connect with Yapily Connect

{{include "yapily-beta"}}

{{include "yapily-fees"}}

For direct communication between your bank and Microsoft Dynamics 365 Business Central, you can use Yapily Connect. Yapily is an Open Banking payment service provider. 

Before you can establish direct communication with your bank through Yapily, it is necessary to grant Yapily the required permissions. For more information about granting permissions, please contact your bank or refer to the [Preparing for Direct Communication Through Yapily](@PM-397) article. 

### File formats

How you can integrate your bank with Payment Management depends on the types of bank communication and files your bank supports. The following table displays what is supported for direct communication with the Allied Irish Banks.

| Bank communication | Send payments             | Import status | Update Status             | Import payments | Reconcile                 |
| ------------------ | ------------------------- | ------------- | ------------------------- | --------------- | ------------------------- |
| Direct             | [Yapily Connect](@PM-268) | {{cross}}     | [Yapily Connect](@PM-268) | {{cross}}       | [Yapily Connect](@PM-268) |



### Supported functionality using Yapily

{{include "yapily-payments"}}

> [!NOTE]
>
> Connecting banks through Yapily is only supported for Business Central version 24 or higher.

| Functionality                                              | Allied</br>Irish</br>Banks                            | Allied Irish Bank </br> Business                      |
| ---------------------------------------------------------- | ----------------------------------------------------- | ----------------------------------------------------- |
| Faster Payment Single                                      | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| Faster Payment Bulk                                        | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| International Single<a href="#footnote-2"><sup>2</sup></a> | ({{checkmark}}<a href="#footnote-2"><sup>2</sup></a>) | ({{checkmark}}<a href="#footnote-2"><sup>2</sup></a>) |
| Bank Reconciliation                                        | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| Direct Debit                                               | {{cross}}                                             | {{cross}}                                             |

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

[Onboarding Yapily to use Direct Communication](@PM-268)
