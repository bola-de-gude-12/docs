---
title: Eika Alliance and Payment Management
description: PM integration with Eika Alliance banks using the bank system Tietoevry
date: 16-01-2024
id: PM-377
lang: en
---

# The Eika Alliance

The Eika Alliance represents a collaboration among independent banks in Norway, operating on a shared platform. In partnership with Tietoevry, Payment Management facilitates the exchange of bank data between the Eika Alliance and Microsoft Dynamics 365 Business Central. 

{{include "pm- kyc-verification-note"}}

Within Payment Management, users have the option of utilizing either direct or manual communication channels to transfer bank data between their Eika Alliance bank and Business Central. This article provides the details on the file format prerequisites for both communication methods, along with the Tietoevry reference numbers corresponding to various banks.

To learn more about how to set up communication:

* Direct communication Eika Alliance - refer to the [Onboarding Eika Alliance with Direct Communication](@PM-313) article.
* Manual communication Eika Alliance- refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 



## File formats

How you can integrate your bank with Payment Management depends on the types of bank communication and files your bank supports. The table below displays what is supported for direct and manual communication with Eika Alliance.

| Bank communication | Send payments| Import status| Update status| Import payments| Reconcile|
| --- | --- | --- | --- | --- | --- |
| Direct | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal" ) | [PAIN.002](@PM-123#PAIN.002 "Import status in the payment journal" ) | [CAMT.054D](@PM-123#CAMT.054D "Update status in the payment journal" ) | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal" ) | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments" ) |
| Manual | [PAIN.001](@PM-123#PAIN.001 "Send payments to your bank from the payment journal" ) | <p style="text-align: center;">{{cross}}</p> | <p style="text-align: center;">{{cross}}</p> | [CAMT.054C](@PM-123#CAMT.054C "Import customer payments in the cash receipts journal" ) | [CAMT.053](@PM-123#CAMT.053 "Reconcile bank statements and import payments" ) |



## Tietoevry bank references

When you set up your Eika Alliance bank account with direct communication, Business Central uses the following Tietoevry bank references.

| Tietoevry Bank Reference | Bank |
| --- | --- |
| 2909 | Agder Sparebank |
| 2504                     | Andebu Sparebank                   |
| 1274                     | Aurskog Sparebank                  |
| 9619                     | Bank2 ASA                          |
| 1109                     | Berg Sparebank                     |
| 1729                     | Bien Sparebank ASA                 |
| 2884                     | Birkenes Sparebank                 |
| 4299                     | Bjugn Sparebank                    |
| 1028                     | Eidsberg Sparebank                 |
| 2142                     | Etnedal Sparebank                  |
| 2903                     | Evje og Hornnes  Sparebank         |
| 4611                     | Gildeskål Sparebank                |
| 4454                     | Grong Sparebank                    |
| 1839                     | Grue Sparebank                     |
| 4354                     | Haltdalen Sparebank                |
| 4478                     | Hegra Sparebank                    |
| 2698                     | Hjartdal og  Gransherad Sparebank  |
| 3354                     | Hjelmeland Sparebank               |
| 1284                     | Høland og Setskog  Sparebank       |
| 1449                     | Jernbanepersonalets  Sparebank     |
| 3294                     | Jæren Sparebank |
| 3081 | Kvinesdal Sparebank |
| 2514 | Larvikbanken |
| 1058 | Marker Sparebank |
| 4239 | Melhusbanken |
| 1874 | Odal Sparebank |
| 4269 | Oppdalsbanken |
| 4274 | Orkla Sparebank |
| 1459 | Oslofjord Sparebank |
| 4113 | Rindal Sparebank |
| 1287 | Romerike Sparebank |
| 4076 | Romsdal Sparebank |
| 4284 | Rørosbanken |
| 3263 | Sandnes Sparebank |
| 2609 | Skagerrak Sparebank |
| 2355 | Skue Sparebank |
| 3839 | SOGN Sparebank |
| 4335 | Soknedal Sparebank |
| 4529 | Sparebanken Narvik |
| 1314 | Strømmen Sparebank |
| 4039 | Sunndal Sparebank |
| 2629 | Tinn Sparebank |
| 2059 | Totens  Sparebank |
| 1144 | Trøgstad Sparebank |
| 3528 | Tysnes Sparebank |
| 4314                     | Trøndelag Sparebank                |
| 2149 | Valdres Sparebank |
| 2894 | Valle Sparebank |
| 9588 | Voss Veksel- og  Landmandsbank ASA |
| 4064 | Ørskog Sparebank |



## Related information

[About direct and manual bank communication](@PM-158)

