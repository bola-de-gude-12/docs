---
title: Jyske bank via Bank Connect, Bankdata
description: Integration with the bank system Jyske Bank via Bank Connect, Bankdata
date: 08-08-2022
id: PM-142
lang: en
---

# Jyske Bank via Bank Connect, Bankdata

Payment Management uses the bank system Bank Connect to send bank data between Jyske Bank and Microsoft Dynamics 365 Business Central. You can set up your bank accounts to use either direct or manual communication. 

This article lists the file format requirements for both communication methods. 

To learn more about how to set up communication:

* Direct communication Jyske Bank- refer to the [Onboarding Bank Connect Banks with Direct Communication](@PM-179) article.
* Manual communication Jyske Bank - refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 



## File formats

How to integrate your bank with Payment Management depends on the bank communication types and files your bank supports. The table below displays what is supported for direct and manual communication with Jyske Bank.

| Bank communication | Send payments                | Import status                | Update status                | Import payments                | Reconcile                    |
| ------------------ | ---------------------------- | ---------------------------- | ---------------------------- | ------------------------------ | ---------------------------- |
| Direct             | [PAIN.001](@PM-123#PAIN.001) | [PAIN.002](@PM-123#PAIN.002) | [CAMT.052](@PM-123#CAMT.052) | [CAMT.054C](@PM-123#CAMT.054C) | [CAMT.053](@PM-123#CAMT.053) |
| Manual             | [BDF](@PM-123#BDF)           | {{cross}}                    | {{cross}}                    | [PBS Sector](@PM-123#PBS)      | [BD-V3](@PM-123#BD-V3)       |

## Related information

[About direct and manual bank communication](@PM-158)
