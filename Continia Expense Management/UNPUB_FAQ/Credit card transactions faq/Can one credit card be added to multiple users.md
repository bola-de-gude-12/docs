---
title: Can one Credit Card be Added to Multiple Users (Shared Card)?
date: 18-10-2023
description: Export and import of customer data 
id: EM-193
lang: en
---

# Can one Credit Card be Added to Multiple Users (Shared Card)?

## Question

I want to add one credit card for multiple expense users. Is that possible?

## Answer

Yes, in Expense Management, you can assign one credit card to multiple users, including travel cards and virtual cards. 

There are two ways of doing this. 

### Without setting anything up

The bank transaction will be stopped in the inbox, and you have to select the user that a particular transaction belongs to. The error message looks like this:

*Card no: xxxx xxxx is used for more than one user. You must therefore manually select Continia User ID*

Select the user in the dropdown menu in **Continia User ID**. Do this for each transaction.

### With multiple user setup and user card mapping

For this to work, the bank or travel agent must be able to send an identifier that connects the user with the transaction data, for example an employee name or number. 

Credit card user mapping is used to identify users. The first step in this process is to enable mutiple users for your credit card of choice, and this is how you do it:

1. Go to **Payment Types**.
2. Select the payment type that you want to be added to multiple users.
3. In the **Bank Transactions/Credit Card** FastTab, under **Credit Card**, toggle **Enable multiple users** on.

You have now made it possible to assign multiple users to a credit card. The next step is to begin assigning users to it.

This functionality is designed for travelcards where the issuer can send employee names in a certain field, helping to identify who the expense is for.

1. Go to **Continia User Setup**.
2. Select the user to whom you want to assign the credit card.
3. In the action bar, select **Credit Cards**.
3. Under **Card No.**, enter the card number of the credit card. 
4. Under **Payment Type**, select a payment type via lookup.
5. Under **Field Mapping Count**, select the number in the field to open details for field mapping count.
6. Select **New**.
7. Under **Field No.**, enter the number for the field that contains the information that identifies the employee that's used the card. Two examples of what you could enter in this field are **Employee No.** and **Travel Passenger Name**.
8. Under **Value**, enter the employee name. Make sure that what you enter here uniquely identifies the employee, so you might have to enter a surname as well as a first name.

