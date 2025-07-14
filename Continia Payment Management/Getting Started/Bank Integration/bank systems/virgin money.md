---
title: Virgin Money	
description: Integration with the bank system Virgin Money	
date: 05-12-2024
id: PM-294
lang: en
---

# Virgin Money	

With Payment Management, you can use direct communication to send bank data between Virgin Money and Microsoft Dynamics 365 Business Central. For direct communication between your bank and Microsoft Dynamics 365 Business Central, [Payment Management collaborates with Yapily](@PM-268), an Open Banking payment service provider. 

> [!NOTE]
>
> Connecting banks through Yapily is only supported for Business Central version 24 or higher.

This article lists the file format requirements for direct communication. To learn more about how to set up communication with Virgin Money, refer to the [Onboarding Yapily to use Direct Communication](@PM-268) article.

> [!NOTE]
>
> B Bank, Clydesdale, and Yorkshire banks rebranded to Virgin Money.

## To connect with Yapily Connect

{{include "yapily-beta"}}

{{include "yapily-fees"}}
For direct communication between your bank and Microsoft Dynamics 365 Business Central, you can use Yapily Connect. Yapily is an Open Banking payment service provider.

Before you can establish direct communication with your bank through Yapily, it is necessary to grant Yapily the required permissions. For more information about granting permissions, please contact your bank or refer to the [Preparing for Direct Communication Through Yapily](@PM-397) article. 

| Bank communication | Send payments             | Import status | Update status             | Import payments | Reconcile                 |
| ------------------ | ------------------------- | ------------- | ------------------------- | --------------- | ------------------------- |
| Direct             | [Yapily Connect](@PM-268) | {{cross}}     | [Yapily Connect](@PM-268) | {{cross}}       | [Yapily Connect](@PM-268) |

### Supported functionality

{{include "yapily-payments"}}

| <div style="width:175px">Functionality</div>               | Virgin Money                                          |
| ---------------------------------------------------------- | ----------------------------------------------------- |
| Faster Payment Single                                      | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| Faster Payment Bulk                                        | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| International Single<a href="#footnote-2"><sup>2</sup></a> | {{cross}}                                             |
| Bank Reconciliation                                        | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| Direct Debit                                               | {{cross}}                                             |

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
