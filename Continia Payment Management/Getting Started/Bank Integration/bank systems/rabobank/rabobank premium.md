---
title: Rabobank Premium
description: Integration with the bank system Rabobank Premium
date: 04-09-2024
id: PM-167
lang: en
---

# Rabobank Premium

With Payment Management, you can use direct or manual communication to send bank data between Rabobank Premium and Microsoft Dynamics 365 Business Central. For direct communication between your bank and Microsoft Dynamics 365 Business Central, Payment Management collaborates with Bizcuit, a PSD2-licenced payment service provider. 

This article lists the file format requirements for both communication methods. To learn more about how to set up communication:

* Direct communication Rabobank Premium - refer to the [Direct communication (using Bizcuit)](@PM-165) article.
* Manual communication Rabobank Premium - refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 



## File formats

How to integrate your bank with Payment Management depends on the bank communication types and files your bank supports. The table below displays what is supported for direct and manual communication with Rabobank Premium.

| Bank communication | Send payments                | Import status | Update status       | Import payments                | Reconcile                    | Direct Debit        | G-accounts    |
| ------------------ | ---------------------------- | ------------- | ------------------- | ------------------------------ | ---------------------------- | ------------------- | ------------- |
| Direct             | [PSD2 API](@PM-123)          | Not supported | [PSD2 API](@PM-123) | Not supported                  | [PSD2 API](@PM-123)          | Not supported       | {{checkmark}} |
| Manual             | [PAIN.001](@PM-123#PAIN.001) | Not supported | Not supported       | [CAMT.054C](@PM-123#CAMT.054C) | [CAMT.053](@PM-123#CAMT.053) | [PAIN.008](@PM-123) | Not supported |



## Related information

[About direct and manual bank communication](@PM-158)  

[The Netherlands and PM FAQ](@PM-400)
