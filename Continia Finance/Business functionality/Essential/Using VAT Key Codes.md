---
title: Assigning VAT Key Codes in Continia Finance
date: 23-05-2024
description: Learn how to save time by adding VAT key codes.
id: CF-77
lang: en
---

# Assigning VAT Key Codes

VAT key codes can automatically populate VAT fields in Business Central. This removes the necessity of filling in VAT details manually each time. 

> [!NOTE]
>
> The VAT Key Codes feature is part of the Essential module that you can use free of charge. Go to the [Introduction to the Essential Module](@CF-74) article to learn more about activating the module.

## To assign a VAT key code

Once you generate the VAT key codes and link them to the relevant VAT fields in Business Central, the system will automatically fill in the corresponding data whenever you use the VAT key code, saving you time and lowering the risk of errors in VAT reporting.

To add a VAT key:

1. Select the {{search}} icon, enter **VAT Key Codes**, and then select the related link.

2. Select **New**.

3. For the new VAT key, enter the following information:

   | Field                    | Description                                                  |
   | ------------------------ | ------------------------------------------------------------ |
   | Code                     | Enter the VAT code. For example, V19.                        |
   | Gen. Posting Type        | Select the posting type for the VAT key code. For example, Sales. |
   | Gen. Bus. Posting Group  | If necessary, you can specify a different General Business Posting Group here. |
   | Gen. Prod. Posting Group | If applicable, enter the General Product Posting Group.      |
   | VAT Bus. Posting Group   | Define the VAT Business Posting Group, if required.          |
   | VAT Prod. Posting Group  | If needed, you can specify a different VAT Product Posting Group at this stage. |
   

## To check VAT keys

In each GL account, there is an option to check if the VAT key added to the Posting FastTab is being used in a general journal or an invoice. This option is called **Check VAT Key**. When you activate this check, you cannot use a different code than the one already used for the account. This ensures that the VAT code used in the transaction is the correct one and prevents any errors. 

To enable the Check Tax Key:

* On the G/L Account Card, navigate to the **Continia Finance** FastTab, and enable **Check Tax Key**. If the VAT key on an invoice differs from the one specified in the **Posting** FastTab, an error occurs. 

<style>

 .content table tr td:nth-child(1) {

 width: 200px;

 }

 .content table tr td:nth-child(2) {

 width: 600px;

 }

</style>
