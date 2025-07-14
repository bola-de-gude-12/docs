---
title: Setting up the Payment Posting
description: How to set up payment postings
date: 01-10-2024	
id: CB-39
lang: en
---
# Setting up payment posting

This setup is important for determining the posting of payments and the corresponding accounts to be used. This additional setup enables the distinction between the bank account used for issuing payments and the one where they are posted. 

For example, when you schedule future payments to be sent to the bank 14 days ahead but want to post it. Rather than allowing payments for the next 14 days to reduce the balance, you can proactively post them to the G/L account. This immediate posting to the G/L account ensures that the bank account accurately reflects the correct balance in Business Central. 

To set up the payment posting:

1. Search ({{search}}) for and select **Payment Posting Setup**. 
2. Here, you can choose how to post payments based on the selected payment method and bank account. It is optional to pay from one bank account and post to another, or to a General Ledger (G/L) account. For example, you might make a payment from an operating bank account but want to post the transaction to a specific G/L account regardless of the payment method. This setup is provided as an option, not a requirement. 
   ![Payment bank account](/images/CB/payment-posting-setup.png)  