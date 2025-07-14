---
title: SDC
description: Integration with the bank system SDC
date: 07-06-2021
id: 
lang: en
---

# SDC

{{include "pm-bank-card-introduction"}}

| Bank communication   | Bank service | Countries | Bank system code |
| -------------------- | ------------ | --------- | ---------------- |
| Manual communication | SDC          | DK        | SDC01            |
| Direct communication | SDC          | DK        | SDC20022         |

{{include "pm-bank-card-file-formats"}}

| Bank communication | Send payments| Import status| Update status| Import payments| Reconcile|
| --- | --- | --- | --- | --- | --- |
| Manual communication | [KaSel](@PM-123#KaSel "Send payments to your bank from the payment journal" ) | Not supported                                             | Not supported                                             | [PBS Sector](@PM-123#PBS "Import NETS PBS FIK DK customer payments in the cash receipts journal." ) | [.DAT format](@PM-123#DAT "Reconcile bank statements and import payments." ) |
| Direct communication | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal" ) | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal" ) | [CAMT.052](@PM-123#CAMT.052 "Update status in the payment journal" ) | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal" ) | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments" ) |

## Onboarding SDC with direct communication

To use the functionality of direct communication the service must be enabled from the assisted bank account setup, for more information see [Setting up Direct Communication](@PM-42). For detailed information and guidance about signing up to SDC with direct communication using Bank Connect, see the article [Onboarding Bank Connect Banks](@PM-179).

