---
title: Bunq and Payment Management
description: PM integration with the bank system bunq
date: 08-08-2022
id: PM-172
lang: en
---

# Bunq

Payment Management collaborates with Bizcuit, a PSD2-licenced payment service provider, to communicate bank data between Microsoft Dynamics 365 Business Central and your bank. With Payment Management, you can use direct communication to send bank data between your bank and Business Central. 

To learn more about how to set up direct communication with Bunq, refer to the [Direct communication (using Bizcuit)](@PM-165) article.

Bizcuit offers the following connections:

| Connection      | Consent method                          | Consent period | Frequency | Account type       | Payment flow |
| --------------- | --------------------------------------- | -------------- | --------- | ------------------ | ------------ |
| Standard (PSD2) | Every user with access who gave consent | 90 days        | Realtime  | Basic bank account | Step-out     |

## Related information

[About direct and manual bank communication](@PM-158)
