---
title: Sparebanken Vest
description: Bank integration with Sparebanken Vest
date: 08-08-2022
id: PM-218
lang: en
---

# Sparebanken Vest

Payment Management collaborates with the digital service Tietoevry to send bank data between Sparebanken Vest and Microsoft Dynamics 365 Business Central.

With Payment Management, you can use direct or manual communication to send bank data between your bank and Business Central. 



This article lists the file format requirements for both communication methods. To learn more about how to set up communication:

* Direct communication Sparebanken Vest - refer to the [Onboarding Sparebanken Vest with Direct Communication](@PM-213) article.
* Manual communication Sparebanken Vest - refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 



## File formats

How you can integrate your bank with Payment Management depends on the types of bank communication and files your bank supports. The table below displays what is supported for direct and manual communication with Sparebanken Vest.

For information about how and when to order these files, follow the links above.

| Bank communication | Send payments| Import status| Update status| Import payments| Reconcile|
| --- | --- | --- | --- | --- | --- |
| Direct | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal" ) | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal" ) | [CAMT.054D](@PM-123#CAMT.054D "Update status in the payment journal" ) | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal" ) | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments" ) |
| Manual | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal" ) | <p style="text-align: center;">{{cross}}</p> | {{cross}} | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal" ) | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments" ) |



## Related information

[About direct and manual bank communication](@PM-158)
