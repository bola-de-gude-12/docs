---
title: Understanding return reason codes
description: Set up codes to track and identify the reasons for returned direct debits in transactions.
date: 07-05-2025	
id: CB-241
lang: en
---

# Understanding direct debit return reason codes

Return Reason Codes help track and identify the specific reasons why direct debits are returned in transactions. These codes are essential for managing rejected payments and improving transaction reconciliation. Continia Banking automatically populates this field during import if a reversal indicator or Return Reason Code is present in the CAMT file.

For example, these codes display in the **Return** field on the **Bank Account Reconciliation** page. 

Return Reason Codes are created and configured through the Setup Server. Each code consists of a standardized identifier and a detailed description, explaining why the payment was rejected. These codes can be accessed and managed through the **Banking Import Setup** page via manual setup. Examples of Return Reason Codes include: Incorrect account number, Closed account, Invalid debtor account number.

To view and update return reason codes:

1. Search ({{search}}) for and select **Direct Debit Return Reason Codes**. 
2. Alternatively, navigate to the **Banking Import Setup** page, select **Manual Setup**, and then choose **Direct Debit Return Reason Codes**. 