---
title: Setting up payment methods
date: 27-06-2022
description: Set up default parameters for the Payment Management supported payment methods.
id: 
lang: en
---

# Setting up Payment Methods

Payment methods define the way you wish to pay your vendors for a product or a service. The payment method can be assigned directly to the customer or vendor card, after which the payment method automatically will be assigned to the sales or purchase documents. 

When setting up your bank accounts for Payment Management, multiple predefined payment methods supported by the given bank will be imported into the system. The imported payment methods must be used when paying your vendors using Payment Management.

> [!IMPORTANT]
>
> After having completed the installation of Payment Management, the payment method defined on your existing vendors must be changed to a payment method supported by Payment Management, as the solution only runs with these payment methods. We recommend that you use the assisted Vendor Payment Information setup guide to update the payment methods on all existing vendors. For more information, see [To set up vendor payment information](@PM-2#to-set-up-vendor-payment-information).

The validation of a payment is highly based on the payment method definition specified on the purchase document, as the payment method settings and parameters are used by Payment Management to create a payment format that meets the requirements of the bank.



## Setting up payment methods using the assisted setup

You can define default settings for your payments using the Payment Management supported payment methods. Using the assisted Payment Method Setup, you can define default payment notification templates to use in accordance with the available payment methods, and specify how you wish to notify your vendors when using a given payment method. Furthermore, you can define which payment reference template to use for each of the payment methods, and specify a default payment method to be used with reference to a given country/region code.

To set up payment methods:
1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Assisted Setup of Payment Methods**, and then select the related link.
1. Follow the instructions in the guide and validate the parameters for using payment methods. Hover over a field to read a short description. 
1. When you've finished the setup, choose **Finish** to save the settings and close the guide.


## Manage available payment methods on vendors and purchase documents

When selecting a payment method on the vendor card or on the purchase document, Payment Management is per default set up to only show the payment methods available for the country/region code specified on the selected balance account (company bank account). 

If you wish to remove the payment method filter, thereby getting an overview of all available payment methods, use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Management Setup**, then select the related link. Under the FastTab **Purchase and Payments**, in the **Payment Method Filter** field, select **All**.



## To create a new payment method

> [!IMPORTANT]
>
> If you need a payment method that is not available in the Payment Management default list of payment methods, your dedicated Continia partner should contact Continia, to investigate if the requested new payment method is applicable and can be added to the default list of payment methods. The advantage of the default Payment Management payment methods is that they will be maintained by Continia, ensuring that they are up to date with the requirements of the bank. If your Continia partner still needs to create a new payment method, Payment Management provides an assisted setup (described in the following guide) that guides you through the process of defining new payment methods.

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Methods**, then select the related link.
1. On the **Payment Methods** page, in the action bar, select **New** > **Create Payment Method**.
1. Fill in the fields in each step of the guide. Hover over a field to read a short description.
   - In the first step of the guide, fill in the information that defines the new payment method (the fields marked with a red star are required and must be filled in to create the payment method).
   - In the second step of the guide, fill in the settings used by Payment Management to map the new payment method to a Payment Management-supported payment method. Based on this information, you will be able to select a Payment Management-supported payment method.
1. Finally, you'll be asked to save the new payment method. If you choose **Yes** the payment method will be saved in the system.
1. When you've finished the setup of the new payment method you must choose **Finish** to save the settings and close the guide.

You have now created a new Payment Management-supported payment method.

## Related information
[Setting up payment method mapping](@PM-244)  
[Setting up vendor payment information](@PM-2#to-set-up-vendor-payment-information)  
[Assisted Setups for the Payment Management Configuration](@PM-2)  

