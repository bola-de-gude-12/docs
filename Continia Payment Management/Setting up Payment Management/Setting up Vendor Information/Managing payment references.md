---
title: Setting up payment references
description: How to set up and manage payment references
date: 11-08-2021
id: PM-43
lang: en
---

# Setting up Payment References

The payment reference is a message created on the payment with information about the payment. The payment references are used by the payment recipient, while sender references are used in the bank account reconciliation to match and apply the bank statement lines. 

Payment Management comes with a list of predefined payment reference templates which can be added to the vendor and the bank account. If the predefined templates do not contain the needed payment information, you can edit the existing templates or you can create new templates.

> [!WARNING]
>
> You should let the creation and editing of payment reference templates be a task for a Continia partner who is familiar with the Payment Management setup, as changing the settings to a payment reference will have a direct effect on the payment- and bank account reconciliation processes.



## To turn on or turn off payment references

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Management Setup** then select the related link.
1. In the **Purchase and Payments** FastTab, *turn on* or *turn off* the **Generate Payment Reference** action. 

When the action is turned on and you are using a payment method that generates a payment reference such as FIK or KID, Payment Management will generate a payment reference. However, situations could occur where you want to disable this functionality. 



## To assign a payment reference template to a vendor

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Vendors** then select the related link.
1. In the list of vendors, select the vendor for whom you want to assign a payment reference template code.
1. On the vendor card, on the **Payments** FastTab, under the **Payment Information** section, in the **Payment Reference Template Code** field, choose a payment reference template code.

The payment reference template has now been added to the vendor. The next time you pay this vendor, a payment reference will be generated for the payments. The payment references will follow the payments to the bank, and when the payments have been processed in the bank, the references will appear on your recipient's bank statement. 



## To assign a sender reference template to a bank account

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Accounts** then select the related link.
1. In the list of bank accounts, select the bank account for which you want to assign a sender reference template code.
1. On the bank account card, on the **Transfer** FastTab, in the **Sender Reference Template Code** field, choose a sender reference template code.

The sender reference template has now been added to the bank account. The next time you pay a vendor using this bank account the sender reference will be generated for the payments. 

The sender reference will follow the payment to the bank, and back to the bank account reconciliation. When the bank account transactions are imported to the bank account reconciliation, the sender reference will feature information about the payment which will be used to match and apply the bank statement lines to the bank account ledger entries. If the sender reference contains a UPR number (unique payment reference number) Payment Management will always be able to match the payment. 



## To define new payment reference templates

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Reference Templates**, then select the related link.
1. On the **Payment Reference Templates** page, select **New** to create a new payment reference template.
1. Specify a **Code** and **Description**.
1. In the **Template** column, define a template for the reference using the lookup function to add fields to the template. 
   > [!TIP]
   >
   > If you're creating a sender reference template, it's recommended that you add the field **UPR No.** (unique payment reference) to the template, as this will be used by Statement Intelligence to identify a unique payment match in the bank account reconciliation.
1. If needed, edit the template field properties. For more information see the section [To edit template field properties](#to-edit-template-field-properties).
1. In the **Template Type** column, select:
   - *Blank* if the payment reference template should be used for payment references.
   - **Sender Reference Template** if the payment reference template should be used for sender references. A sender reference is defined on the bank account and will be used in the bank account reconciliation to match and apply the bank statement lines.
1. When finished setting up the payment reference template, close the page.

The payment reference template has been created and can be added to the vendor card or bank account. 



## To edit template field properties

   1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Reference Templates**, then select the related link.     
   1. Select the payment reference template, for which you wish to edit the template field properties.     
   1. In the **Template** column, select the ![Review or Update](/images/three-horizontal-dots.png) symbol (the symbol furthest to the right). This will open the **Template Field Property** page.     
   1. Define the properties for each of the template fields.
      | **Field Property** | Description |
      | --- | --- |
      | **Length** | In this field, specify the number of characters the field should occupy. <br>Be aware that the Danish payment methods FIK/GIK always end with a modulus check cipher line. It is not necessary to assign length on modulus ciphers as it is always one character. |
      | **Place Before** | In this field, specify which character should be placed before in case the field value is shorter than the required field length. |
      | **Place After** | In this field, specify which character should be placed after in case the field value is shorter than the required field length. |
      | **Opposite Sign** | Select this if opposite sign should be used for the field value. |
      | **Truncate From Left** | Select this if the field value should be truncated in case the field value exceeds the required number of characters specified in the field **Length**. |
   1. When you have edited the template field properties, select **OK** to close the form





