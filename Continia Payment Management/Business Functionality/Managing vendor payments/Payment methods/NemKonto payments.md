---
title: NemKonto Payments
description: Information on how to pay vendors with the payment method NemKonto
date: 27-11-2024
id: PM-203
lang: en
---

# NemKonto Payments

All citizens, associations, and companies in Denmark are required to have a NemKonto. A NemKonto is a regular bank account that has been assigned as a Nemkonto. The NemKonto bank account is used by the public sector in Denmark to insert payments such as TAX and VAT refunds. 

As a private person or company, you can also use the NemKonto payment system to process payments to a vendor's or employee's NemKonto without having access to the vendor's or employee's bank account number, as the payments can be processed using the vendor's or employee's *CPR number*, *VAT number*, *SE number*, or *P number*.

Payment Management comes with a selection of supported NemKonto payment methods. No further setup in Business Central is needed as the setup is integrated in the Payment Management solution.

> [!IMPORTANT]
>
> To perform NemKonto payments, a NemKonto connection agreement must have been established at your bank. Also, before processing the first NemKonto payment, the vendor must be notified that NemKonto will be used for future payments.

## To pay vendors and employees by NemKonto

You can use the NemKonto payment system in Denmark to process payments to vendors or employees without needing their bank account details. Payments can be made using identifiers such as the *CPR number*, *VAT number*, *SE number*, or *P number*. 

To pay vendors and employees by Nemkonto:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Vendors** or **Employees**, then select the related link. 
1. Open the relevant card.
1. On the vendor or employee card, navigate to the FastTab **Payments**.
1. In the field **Payment Method Code**, choose one of the following available NemKonto payment methods:
   - **NKC**: Payments will be processed using the vendor's or employee's CPR number. To use this payment method, a CPR number (social security number) must have been filled in on the vendor card under the FastTab **Invoicing**.
     > [!NOTE]
     >
     > As a social security number is considered sensitive personal information, you may consider controlling the access to this information with user permission sets.
   - **NKSE**: Payments will be processed using the vendor's or employee's *SE number*. To use this payment method, a SE number must have been filled in on the vendor card under the FastTab **Invoicing**.
   - **NKV**: Payments will be processed using the vendor's or employee's *VAT number*. To use this payment method, a VAT registration number must have been filled in on the vendor card under the FastTab **Invoicing**.
   - **NKVP**: Payments will be processed using the vendor's or employee's *VAT number and P number*. To use this payment method, a VAT registration number and a P number must have been filled in on the vendor card under the FastTab **Invoicing**.
   - **NKVSE**: Payments will be processed using the vendor's or employee's *VAT number and SE number*. To use this payment method, a VAT registration number and a SE number must have been filled in on the vendor card under the FastTab **Invoicing**.

