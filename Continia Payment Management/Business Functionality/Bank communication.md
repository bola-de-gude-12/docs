---
title: Bank communication
description: Introduction to manual and direct banking communication.
date: 21-03-2022
id: PM-158
lang: en
---

# Bank Communication

Continia Payment Management supports manual and direct communication between banking systems and Business Central. With direct bank communication, you simplify the process of communicating data between Business Central and your bank. Instead of manually importing and exporting bank files, the Payment Management Direct Communication service uses web services to exchange bank data automatically. 

Whether direct communication is supported depends on your bank. In the section [Bank integration](@PM-98), navigate to your bank to see if it supports direct communication. 

Continia uses external service components for the bank integration to manage the exchange of data between the bank and Business Central, ensuring that all data meets the requirements of the banks. For more information, see [Understanding the CBIC and CBCC components](@PM-61).

## Direct communication

Direct communication, sometimes called web service or SFTP, is the preferred communication form, as all communication between the bank and Business Central is fully automatic.

For information on how to set up direct communication, see the  [Setting up direct communication](@PM-42).

The following example illustrates how using direct communication for communicating data between Business Central, and the bank can proceed when sending payments to the bank:

1. The payment suggestions are created and prepared in the Payment Journal and sent to the bank.
1. The payments are received in the bank.
1. A payment status with information on whether the payment is sent, received, paid, or rejected in the bank is automatically imported to the Payment Journal.
1. You correct any errors on the payment lines and then repeat steps 1 and 2.

The process is likewise automatic when importing payment-, status- or statement files from the bank and into Business Central using direct communication.



## Direct communication through open banking providers

To support direct communication between your bank and Microsoft Dynamics 365 Business Central, Payment Management collaborates with open banking providers such as Bizcuit (for the NL market).  

Additional steps may be required to complete the payment (approval).

 



## Manual communication

Manual communication is the traditional way of exchanging banking files between Business Central and your bank. Using manual import and export, all files must be saved on your desktop before they can be imported to the bank or Business Central. 

The following example illustrates how manual communication for communicating data between Business Central and the bank can proceed when sending payments to the bank:

1. The payment suggestions are created and prepared in the Payment Journal and exported to the bank.
1. The payment file is saved locally on the desktop.
1. The user logs in to the online bank.
1. The payment file is manually imported into the online banking system from the local desktop.
1. The user must manually follow up in the bank system and verify that the payments have been processed as expected.
1. You correct any payment errors manually on the payment lines in Business Central, and then repeat steps 1 through 5.

<br>

## Related information

[Setting up direct communication](@PM-42)

