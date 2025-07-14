---
title: BEC and Payment Management
description: PM integration with the bank system BEC
date: 20-09-2022
id: PM-125
lang: en
---

# BEC

BEC provides IT services to smaller and larger financial companies such as Danish banks, foreign banks in Denmark, and other institutions in the Danish financial sector. You can find an overview of the banks and institutions using the services of BEC [here](https://www.bec.dk/en/becs-customers/).

Payment Management uses the bank system Bank Connect to send bank data between BEC and Microsoft Dynamics 365 Business Central. You can set up your bank accounts to use either direct or manual communication. 

This article lists the file format requirements for both communication methods. To learn more about how to set up communication:

* Direct communication BEC - refer to the [Onboarding Bank Connect Banks with Direct Communication](@PM-179) article.
* Manual communication BEC- refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 



## File formats

How to integrate your bank with Payment Management depends on the bank communication types and files your bank supports. The table below displays what is supported for direct and manual communication with BEC.

For information about how and when to order these files, follow the links above.

| Bank communication | Send payments| Import status| Update status| Import payments| Reconcile|
| --- | --- | --- | --- | --- | --- |
| Direct | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal") | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal") | [CAMT.052](@PM-123#CAMT.052 "Update status in the payment journal") | [CAMT.054](@PM-123#CAMT.054 "Import customer payments in the cash receipts journal") | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments") |
| Manual | [ERH](@PM-123#ERH "Send payments to your bank from the payment journal") | <p style="text-align: center;">{{cross}}</p> | <p style="text-align: center;">{{cross}}</p> | [PBS Sector](@PM-123#PBS "Import NETS PBS FIK DK customer payments in the cash receipts journal.") | [EKP format](@PM-123#EKP "Reconcile bank statements and import payments.")|

## Related information

[About direct and manual bank communication](@PM-158)
