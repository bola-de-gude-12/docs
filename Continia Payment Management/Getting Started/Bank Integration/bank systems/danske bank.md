---
title: Danske Bank and Payment Management
description: PM integration with the bank system Danske Bank
date: 15-07-2022
id: PM-118
lang: en
---

# Danske Bank

With Payment Management, you can use direct or manual communication to send bank data between Danske Bank and Microsoft Dynamics 365 Business Central. 

This article lists the file format requirements for both communication methods. 

To learn more about how to set up direct or manual communication:

* Direct communication Danske Bank- refer to the [Onboarding Danske Bank with Direct Communication](@PM-178) article.
* Manual communication Danske Bank - refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 



## File formats

How you can integrate your bank with Payment Management depends on the types of bank communication and files your bank supports. The table below displays what is supported for direct and manual communication with Danske Bank.

| Bank communication | Send payments                | Import status                                | Update status                                | Import payments                | Reconcile                    |
| ------------------ | ---------------------------- | -------------------------------------------- | -------------------------------------------- | ------------------------------ | ---------------------------- |
| Direct             | [PAIN.001](@PM-123#PAIN.001) | [PAIN.002](@PM-123#PAIN.002)                 | [CAMT.054D](@PM-123#CAMT.054D)               | [CAMT.054C](@PM-123#CAMT.054C) | [CAMT.053](@PM-123#CAMT.053) |
| Manual             | [PAIN.001](@PM-123#PAIN.001) | <p style="text-align: center;">{{cross}}</p> | <p style="text-align: center;">{{cross}}</p> | [CAMT.054C](@PM-123#CAMT.054C) | [CAMT.053](@PM-123#CAMT.053) |



## Related information

[About direct and manual bank communication](@PM-158)

