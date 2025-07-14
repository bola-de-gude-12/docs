---
title: Customer Vendor Links in Continia Finance
date: 27-05-2024
description: Learn how to connect customers and vendors and assess their entries together.
id: CF-94
lang: en
---
# Linking Customers and Vendors

The Association module enables you to connect customers and vendors, creating a customer/vendor link. This link simplifies financial procedures by allowing you to assess their entries together. Although you can assign multiple vendors to a customer and vice versa through vendor associations, it is more common to link a customer to a vendor, especially when a customer also acts as a vendor.

The Extended Application window displays all associations and their linked items. 

To create a customer/vendor link:
1. Select **Associations** > **Customer/Vendor Link**. 

2. The list of the created customer/vendor links opens. On the action bar, select **More Options** > **Related** > **Link/Customer/Vendor Card** to open an existing connection or create a new link by selecting **New**.

3. On the **Customer/Vendor Link Card,** the following fields are available:

   | **Option**                          | **Description**                                              |
   | :---------------------------------- | :----------------------------------------------------------- |
   | Customer No.                        | Specifies the customer account number that the entry is linked to. The Customer Name and City fields will auto-populate with the corresponding details. |
   | Vendor No.                          | Specifies the vendor account number that the entry is linked to. The Vendor Name and City fields will auto-populate with the corresponding information. |
   | Linked Customer Balance (LCY)       | This field shows the current balance of the linked customer in client currency, automatically calculated from the Amount (LCY) field in customer entries. Use filters based on specific Global Dimension Values 1 and Global Dimension Values 2. Click the Assist button on the right to view the customer entries contributing to this amount. |
   | Linked Cust. Balance at Date (LCY)  | The balance of the linked customers in local currency up to the end date of the date filter entered. The application automatically calculates and updates the value based on the Amount (LCY) field in the Detailed Customer Ledger Entries table. You can filter the Balance (LCY) field so that its content is based only on certain Global Dimension Values 1 and Global Dimension Values 2. The customer entries that make the amount can be accessed by clicking on the amount displayed in the field. |
   | Linked Customer Net Change (LCY)    | This field indicates the net change of the connected customer for the period entered in the date filter of the Customer/Vendor Link table in client currency. The application calculates and updates the contents of the automatic field using the Amount (LCY) field of the entries in the Detailed Customer Ledger Entries table. You can filter the field net change (LCY) so that its content is based only on certain Global Dimension Values 1, Global Dimension Values 2, and Data. You can display the customer entries that make up the amount by clicking on the amount displayed in the field. |
   | Linked Vendor Balance (LCY)         | This field displays the current balance of the connected vendor in client currency. The application automatically calculates and updates the contents of the field using the Amount (LCY) field of the entries in the Detailed Vendor Ledger Entries table. You can filter the Balance (LCY) field so that its content is based only on certain Global Dimension Values 1 and Global Dimension Values 2. You can display the vendor entries that make up the amount by clicking on the amount displayed in the field. |
   | Linked Vendor Balance at date (LCY) | The balance of the linked vendor in client currency up to the end date of the entered date filter in the Customer/Vendor Link table. The application automatically calculates and updates the value based on the Amount (LCY) field of the Detailed Vendor Ledger Entries table. You can filter the Balance (LCY) field so that its content is based only on certain Global Dimension Values 1 and Global Dimension Values 2. You can display the vendor entries that make up the amount by clicking on the amount displayed in the field. |
   | Linked Vendor Net Change (LCY)      | The balance of the linked vendor in client currency up to the end date of the entered date filter in the Customer/Vendor Link. The application automatically calculates and updates the value based on the Amount (LCY) field of the Detailed Vendor Ledger Entries table. You can filter the Balance (LCY) field so that its content is based only on certain Global Dimension Values 1 and Global Dimension Values 2. You can display the vendor entries that make up the amount by clicking on the amount displayed in the field. |
   | Sum Balance (LCY)                   | This field displays the total balance between the linked customer and vendor accounts. |
   | Sum Net Change (LCY)                | Displays the total net change between linked customers and vendors based on the current date filter. |

   > [!NOTE]
   >
   > When deleting a customer or vendor, the system automatically checks for any linked accounts and removes the link if it exists.

<style>
 .content table tr td:nth-child(1) {
 width: 230px;
 }
 .content table tr td:nth-child(2) {
 width: 570px;
 }
</style>
