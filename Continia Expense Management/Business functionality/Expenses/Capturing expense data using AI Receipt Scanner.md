---
title: Capturing expense data using the AI Receipt Scanner
date: 14-08-2025	
description: Capture expense data using the AI Receipt Scanner 
lang: en
---
# Capturing expense data using the AI Receipt Scanner

AI Receipt Scanner is an advanced feature that recognizes and captures data from scanned attachments, such as receipts and invoices, which significantly reduces the need for manual entry. Take a picture of your receipt, or share a PDF invoice from other apps or devices, then let AI Receipt Scanner automatically identify and extract relevant data. By capturing data directly from scanned receipts and PDF attachments using cutting-edge optical character recognition (OCR), AI Receipt Scanner saves you lots of time, minimizes errors, and streamlines the expense reporting process in general.

Whether you're using it for physical receipts or digital PDFs, AI Receipt Scanner ensures that expense reporting is fast, accurate, and hassle-free. It's designed to work on receipts from any country, regardless of origin, and it works for both the [Continia Expense App](#to-capture-data-using-the-expense-app) and the [Continia Expense Portal](#to-capture-data-using-the-expense-portal).

## What data is captured? 

For each expense, AI Receipt Scanner automatically identifies and fills in data for the following fields:

* **Amount**
* **Currency Code**
* **Document Date**
* **Payment Type**
* **Description** (merchant)
* **VAT Amount** (provided that this field has been added on the **Configured Fields** page, see [Setting up fields](@EM-80) in Continia Expense Management)
* Various ESG fields, depending on the value of the **Expense Type** field: 
   * **Electricity (kWh)**
   * **Attendees**
   * **Fuel Quantity**
   * **Number of Nights**
   * **Distance Traveled**
   * **From Airport**
   * **To Airport**
   * **Return Trip**
   * **From Harbor**
   * **To Harbor**
   * **From Station**
   * **To Station**
   > [!NOTE]
   > The ESG fields will only be visible in the user interfaces of the Expense App and the Expense Portal when certain values have been selected in the **Expense Type** field, such as **ELECTRICITY**, **FUEL-PETROL**, or **TRAVEL-FLIGHT**.

## Automatic splitting of differentiated VAT

If you want AI Receipt Scanner to automatically capture VAT data in your scanned attachments, you must add the **VAT Amount** field on the **Configured Fields** page in Continia Expense Management. For information on how to add this field, see [Setting up fields](@EM-80).

After you've added the **VAT Amount** field, AI Receipt Scanner identifies any relevant VAT data in the scanned attachments and automatically fills in the field. Furthermore, if two or more different kinds of VAT have been applied to an attachment, the AI Receipt Scanner automatically splits the VAT using the **Allocation** field. For example, a receipt with a total of $34.90 would be split accordingly:

| VAT % | VAT | Price excluding VAT | Total |
| --- | --- | --- | --- |
| 12.00% | 2.40 | 20.00 | 22.40 |
| 25.00% | 2.50 | 10.00 | 12.50 |
|   | 4.90 | 30.00 | 34.90 |

If you added this receipt to an expense in the Expense App, the **Allocation** field would read **Allocation lines: 2**, to indicate that the total is split over two lines. If you then select the **Allocation** field to open the **Allocations** page, it will display the $34.90 total at the top, followed by the two allocation lines of $22.40 (12.00%) and $12.50 (25.00%) respectively.

## Capture data using the Expense App

With AI Receipt Scanner, you can capture expense data using the Expense App, by taking a picture of your receipts in the app. 

To do this:

1. Open the Expense App, and tap **New Expense**.
1. In the row of icons at the top, tap the camera icon to access your phone's camera.
1. Take a picture of the receipt, and tap **Use Photo**. The photo is then attached to the expense, and the receipt data is automatically captured and entered into the relevant fields of the expense.
1. Tap **Expense Type** to open the list of expense types, and then select the relevant one.
1. Swipe the **Submit** button to submit the expense.

The expense is submitted for approval.

## Capture data using the Expense Portal

Although you can't take pictures of your receipts using the Expense Portal, capturing expense data in the portal works as smoothly as it does in the app in every other respect. 

To capture data in the Expense Portal using the AI Receipt Scanner functionality:

1. On the blue ribbon at the top, click **Expense**.
1. In the upper-left corner, click **New** to create an expense.
1. Do one of the following:
   * Locate the relevant receipt in your file browser, and drag it to the drag-and-drop field on the right.
   * On the action bar, click **Receipts** to open the list of uploaded receipts. From the list, locate the one you want to add to the expense, then click **Add**, to add the receipt.
1. The receipt data is automatically captured and entered into the relevant fields of the expense. Fill in the remaining details manually.
1. On the action bar, click **Submit** to submit the expense.

The expense is submitted for approval.