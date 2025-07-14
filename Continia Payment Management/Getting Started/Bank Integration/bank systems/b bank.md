---
title: B bank and Payment Management
description: PM Integration with the bank system B Bank
date: 03-02-2023
id: PM-308
lang: en
---

# B Bank

With Payment Management, you can use direct communication to send bank data between B Bank and Microsoft Dynamics 365 Business Central. For direct communication between your bank and Microsoft Dynamics 365 Business Central, Payment Management collaborates with Yapily, an Open Banking payment service provider. 

This article lists the file format requirements for direct communication. To learn more about how to set up communication with B Bank, refer to the [Onboarding Yapily to use Direct Communication](@PM-268) article.

> [!NOTE]
>
> B Bank is rebranded to [Virgin Money](@PM-294).



## File formats

How to integrate your bank with Payment Management depends on the bank communication types and files your bank supports. The table below displays what is supported for direct communication with B Bank.  

| Bank communication | Send payments             | Import status                                | Update status             | Import payments                              | Reconcile                 |
| ------------------ | ------------------------- | -------------------------------------------- | ------------------------- | -------------------------------------------- | ------------------------- |
| Direct             | [Yapily Connect](@PM-268) | <p style="text-align: center;">{{cross}}</p> | [Yapily Connect](@PM-268) | <p style="text-align: center;">{{cross}}</p> | [Yapily Connect](@PM-268) |



## Supported functionality

{{include "yapily-payments"}}

| <div style="width:175px">Functionality</div> | B Bank                                           |
| -------------------------------------------- | ------------------------------------------------ |
| Domestic Single - Immediate  Payments        | <p style="text-align: center;">{{checkmark}}</p> |
| Domestic Single - Scheduled  Payments        | <p style="text-align: center;">{{cross}}</p>     |
| Domestic Bulk - Immediate  Payments          | <p style="text-align: center;">{{checkmark}}</p> |
| Domestic Bulk - Scheduled  Payments          | <p style="text-align: center;">{{cross}}</p>     |
| International Single - Immediate Payments    | <p style="text-align: center;">{{cross}}</p>     |
| International Single - Scheduled Payments    | <p style="text-align: center;">{{cross}}</p>     |
| International Bulk - Immediate Payments      | <p style="text-align: center;">{{cross}}</p>     |
| International Bulk - Scheduled Payments      | <p style="text-align: center;">{{cross}}</p>     |
| Bank Reconciliation                          | <p style="text-align: center;">{{checkmark}}</p> |
| Status File                                  | <p style="text-align: center;">{{checkmark}}</p> |
| Direct Debit                                 | Not supported yet                                |

> [!NOTE]
>
> Bank restrictions for bulk payments may apply. Refer to the [Bulk payments](https://docs.yapily.com/pages/payments/bulk-payments/additional-information/#known-restrictions) article on doc.yapily.com for more information.



## Related information

[About direct and manual bank communication](@PM-158)  

[Onboarding Yapily to use Direct Communication](@PM-268)

