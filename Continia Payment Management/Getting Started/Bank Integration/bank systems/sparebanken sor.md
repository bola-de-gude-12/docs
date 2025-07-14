---
title: Sparebanken Sør Banks
description: Integration with Sparebanken Sør using the bank system Tietoevry
date: 16-01-2024
id: PM-315
lang: en
---

# Sparebanken Sør 

Sparebanken Sør is a Norwegian savings bank, headquartered in Kristiansand. Payment Management collaborates with the digital service Tietoevry to send bank data between the Sparebanken Sør and Microsoft Dynamics 365 Business Central.

{{include "pm- kyc-verification-note"}}

With Payment Management, you can use direct or manual communication to send bank data between your bank and Business Central. This article lists the file format requirements for both communication methods and the Tietoevry reference numbers for banks.

To learn more about how to set up communication:

* Direct communication Sparebanken Sør - refer to the [Onboarding Sparebanken Sør with Direct Communication](@PM-317) article.
* Manual communication Sparebanken Sør- refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 



## File formats

How you can integrate your bank with Payment Management depends on the types of bank communication and files your bank supports. The table below displays what is supported for direct and manual communication with Sparebanken Sør.

| Bank communication | Send payments| Import status| Update status| Import payments| Reconcile|
| --- | --- | --- | --- | --- | --- |
| Direct | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal" ) | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal" ) | [CAMT.054D](@PM-123#CAMT.054D "Update status in the payment journal" ) | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal" ) | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments" ) |
| Manual | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal" ) | {{cross}}                                                    | <p style="text-align: center;">{{cross}}</p> | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal" ) | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments" ) |



## Tietoevry bank references

When you set up your Sparebanken Sør bank account with direct communication, Business Central uses the following Tietoevry bank references.

| Tietoevry Bank Reference | Bank |
| --- | --- |
| 2844                                                   | Sparebanken Sør |



## Related information

[About direct and manual bank communication](@PM-158)

