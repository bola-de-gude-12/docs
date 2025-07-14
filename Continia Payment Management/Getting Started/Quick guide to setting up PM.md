---
title: Quick Guide Payment Management
date: 30-09-2022
description: A guide to setting up the basics of Continia Payment Management 
id: PM-226
lang: en
---

# Quick Guide – Setting up Payment Management

The following steps take you through the required configurations before using Continia Payment Management with Microsoft Dynamics 365 Business Central.

<br>


| Step                                        | Task                                                         | Article                                                |
| ------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------ |
| Prepare your setup                          | To make it easier to start working with Payment Management, you must prepare your setup. | [Preparing your setup for Payment Management](@PM-311) |
| Prepare for direct or manual communication  | If you want to use manual communication, go ahead and order the relevant files from your bank. Navigate to your bank from the Bank integration article to see which files you must order. | [Bank Integration](@PM-98)                             |
|                                             | If you want to use direct communication, refer to the prerequisites in the onboarding article for your bank to see if you need to request any subscriptions or services with the bank. Navigate to your bank service from the Onboarding banks article. | [Onboarding Banks](@PM-183)                            |
| Install and activate Payment Management     | If you want to try out Payment Management.                   | [Install Payment Management Online](@PM-9)             |
|                                             | If you are using Business Central Online and  you want to try out Payment Management without the assistance of a Continia Partner, install Continia Payment Management and run a 30-day trial version | [Install Payment Management Online](@PM-9)             |
|                                             | To activate a new subscription or change from trial to subscription. | [Activate Payment Management](@PM-8)                   |
|                                             | If you are using Business Central On-premises, install Continia Payment Management On-Premises. To learn more about the different granules available for Payment Management on premises, refer to the [License and granules article](@PM-18). | [Install Payment Management On-Premises](@PM-64)       |
| Set up bank accounts                        | If you use manual communication, run the Set up Bank Accounts assisted setup guide. | [Set up Bank Accounts](@PM-2#to-set-up-bank-accounts)  |
|                                             | If you use direct communication, [enable the Direct Communication service](@PM-42) and follow the onboarding article for your bank service. Navigate to the relevant article from the Onboarding banks article. | [Onboarding Banks](@PM-183)                            |
| Set up payment information for your vendors | Run the Set up Vendor Payment Information assisted setup guide. For detailed information about how to set up balance accounts, see [Setting Up Balance Accounts](@PM-62). | [Set Up Vendor Payment Information](@PM-5)             |
| Set up Payment Approval                     | Create and set up a payment approval workflow for a payment journal. | [Create payment approval workflows](@PM-254)           |

<br>

### Recommended next steps

When you have completed the initial setup, we recommend following the steps and tasks below to verify or update a few noteworthy default settings.   
<br>

| Step                          | Task                                                         | Article                                                      |
| ----------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Set up the bank account cards | Define the payment ID masks used to interpret the payments made to each bank account. | [Define Payment ID Masks](@PM-92)                            |
|                               | Specify which journal templates should be used for managing vendor-, customer-, and employee amount differences. | [Define Journal Templates For Amount Differences](@PM-195#to-define-journals-for-vendor--customer--and-employee-amount-differences) |
|                               | Define the sender reference template code used for matching payments during bank account reconciliation. | [Define Sender Reference Template Code](@PM-194)             |
| Set up payment method mapping | If you use Document Capture, set up payment method mapping between Document Capture and Payment Management. | [Set Up Payment Method Mapping](@PM-244)                     |
| Set up the OCR interface      | Set up Payment Management's OCR reference interface used with customer documents such as invoices and reminders. | [Set Up The OCR Reference Interface](@PM-10)                 |
| Set up payment methods        | Configure default settings for the Payment Management supported payment methods and the associated payment notifications and payment references. | [Set up Payment Methods](@PM-4#setting-up-payment-methods-using-the-assisted-setup) |

## Related information

[Migrating Payment Management from FOB to app](@PM-53) 

<style>
table.table tbody td:empty {
  border-top: none;
}
</style>
