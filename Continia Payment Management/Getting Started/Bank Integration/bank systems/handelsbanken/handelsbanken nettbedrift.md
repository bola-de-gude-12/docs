---
title: Handelsbanken Nettbedrift
description: Bank integration with Handelsbanken Nettbedrift.
date: 16-01-2024
id: PM-220
lang: en
---

# Handelsbanken Nettbedrift

Payment Management collaborates with the digital service Tietoevry to send bank data between Handelsbanken Nettbedrift and Microsoft Dynamics 365 Business Central.

{{include "pm- kyc-verification-note"}}

With Payment Management, you can use direct or manual communication to send bank data between your bank and Business Central. 

To learn more about how to set up direct or manual communication:

* Direct communication Handelsbanken Nettbedrift - refer to the [Onboarding Handelsbanken Nettbedrift to use Direct Communication](@PM-221) article.
* Manual communication Handelsbanken Nettbedrift - refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 



## File formats

How you can integrate your bank with Payment Management depends on the types of bank communication and files your bank supports. The table below displays what is supported for direct and manual communication with Handelsbanken Nettbedrift.

| Bank communication | Send payments                                                | Import status                                                | Update status                                                | Import payments                                              | Reconcile                                                    |
| ------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Direct             | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal") | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal") | [CAMT.052](@PM-123#CAMT.052 "Update status in the payment journal") | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal") | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments") |
| Manual             | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal") | Not supported                                                | Not supported                                                | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal") | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments") |

## Related information

[About direct and manual bank communication](@PM-158)

