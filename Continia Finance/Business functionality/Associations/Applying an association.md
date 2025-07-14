---
title: Applying an Association in Continia Finance
date: 13-09-2024
description: Learn how to group related entities. 
id: CF-70
lang: en
---

# Adding an Association

Associations help you categorize and group related entities, simplifying the management of financial records and transactions.

To add an association:

1. On Continia Finance, navigate to **Associations** > **Associations**. 
2. To create a new association, select **New**.
3. On the **Association Card**, you can enter information for the association. The following table describes the fields that are essential:

   | **Option**                | **Description**                                              |
   | :------------------------ | :----------------------------------------------------------- |
   | Type                      | Specify the association type. The options are: customer or vendor. |
   | No.                       | Enter the association number in this field. If you want to use a number series, go to the Association Setup page and enter the corresponding number series code in the Association numbers field. There are three methods to enter the association number: <br /><ul><li>If you have set a number series as the default, press enter, and the application will automatically fill the field with the next higher number from the series.</li><li>If you have set up multiple series of numbers, select the assist button on the right side of the field and select the series you want to use. The application will then display the next number of the corresponding series in the field.</li><li>If you have not set up a number series or if the number series has a mark in the manual number field, you can assign a number manually. The field allows up to 20 characters, including both letters and numbers.</li></ul> |
   | Leading Account No.       | Enter the number of the leading account of the association.  |
   | Assoc. Credit Limit (LCY) | Enter the credit limit (LCY) for this association (debit only). To apply this limit, you must enable the Check Credit Limit field. |
   | Check Credit Limit        | Enabling this field triggers a check on the credit limit of the association in both the journal and the document (debit only). By selecting this checkbox, the credit limit becomes an active monitoring mechanism to safeguard your financial transactions. When entering an amount, the system checks if it exceeds the association's limit. If this happens, the system notifies the user of a credit limit check. The notification displays the details of the check, including the items that caused the credit limit to be exceeded. This provides the user with information and an overview of the situation. The user can then decide whether to continue or cancel the processing. |

1. On the action bar, click **Select Accounts** to assign customers to the association.

   <style>
   
    .content table tr td:nth-child(1) {
    width: 150px;
    }
    .content table tr td:nth-child(2) {
    width: 650px;
    }
   </style>
