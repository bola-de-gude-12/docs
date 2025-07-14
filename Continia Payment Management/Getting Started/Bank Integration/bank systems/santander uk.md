---
title: Santander UK
description: Integration with the bank system Santander UK
date: 15-07-2024
id: PM-292
lang: en
---

# Santander UK

With Payment Management, you can use direct communication to send bank data between Santander UK and Microsoft Dynamics 365 Business Central. For direct communication between your bank and Microsoft Dynamics 365 Business Central, [Payment Management collaborates with Yapily](@PM-268), an Open Banking payment service provider. 

This article lists the file format requirements for direct communication. To learn more about how to set up communication with Santander UK, refer to the [Onboarding Yapily to use Direct Communication](@PM-268) article.

> [!NOTE]
>
> Connecting banks through Yapily is only supported for Business Central version 24 or higher.

## To connect with Yapily Connect

{{include "yapily-fees"}}
For direct communication between your bank and Microsoft Dynamics 365 Business Central, you can use Yapily Connect. Yapily is an Open Banking payment service provider. 

| Bank communication | Send payments             | Import status                                | Update status             | Import payments                              | Reconcile                 |
| ------------------ | ------------------------- | -------------------------------------------- | ------------------------- | -------------------------------------------- | ------------------------- |
| Direct             | [Yapily Connect](@PM-268) | <p style="text-align: center;">{{cross}}</p> | [Yapily Connect](@PM-268) | <p style="text-align: center;">{{cross}}</p> | [Yapily Connect](@PM-268) |



> [!NOTE]
>
> Bank restrictions for bulk payments may apply. Refer to the [Bulk payments](https://docs.yapily.com/pages/payments/bulk-payments/additional-information/#known-restrictions) article on doc.yapily.com for more information.



### Supported functionality

{{include "yapily-payments"}}

| <div style="width:175px">Functionality</div> | <p style="text-align: center;">Santander UK</p>  |
| -------------------------------------------- | ------------------------------------------------ |
| Faster Payment Single                        | <p style="text-align: center;">{{checkmark}}</p> |
| Faster Payment Bulk                          | <p style="text-align: center;">{{checkmark}}</p> |
| International Single                         | <p style="text-align: center;">{{cross}}</p>     |
| Bank Reconciliation                          | <p style="text-align: center;">{{checkmark}}</p> |
| Direct Debit                                 | <p style="text-align: center;">{{cross}}</p>     |







## Related information

[About direct and manual bank communication](@PM-158)  
