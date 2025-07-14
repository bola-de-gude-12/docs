---
title: Setting up payment identification search rules
description: How to set up payment identification search rules
date: 28-03-2024
id: PM-391
lang: en
---

# Setting up Payment Identification Search Rules

During the import of a bank account statement for reconciliation, standard reconciliation rules are typically applied to identify bank account lines for settlement within the bank account reconciliation journal. However, in rare cases where the payment reference is found in non-standard fields such as in the additional information, the description, or the notification, standard rules may not be sufficient for accurate matching. To solve this issue, payment identification search rules can be used to help locate bank account ledger entries, especially in cases where standard reconciliation rules may not be enough due to the unconventional placement of payment references.

To add a payment identification search rule:

1. On the **Bank Acc Reconciliation** page, on the action bar select **Rules** > **Payment Identification Search Rules**. On the **Pmt. Ident. Search Rules** page, on the action bar, and select **New** to add a rule. 

   Alternatively,  navigate to an unsolved line and select the information that is in the **Additional Information** column. On the **Additional Information** page, you can now find the text to help you find the matching bank account ledger entries. On the action bar, select **Actions** > **Payment Identification Search Rules**. 
2. On the **Payment Identification Search Rule** page, enter information for the following fields:
   * **Bank Account No.** - specifies the bank account number associated with the rule.
   * **Line No.** - specifies the line number relevant to the transaction.
   * **Reference Field** - select End-to-end ID or Payment Information ID, depending on the type of reference you're searching for.
3. In the **Search Text** field, you can now enter the text you want to search for. You must add an asterisk to be able to search the variable text. For example, if the transaction reference is in the **Kenmerk** field located in the **Additional Information**, add the following in the **Search Text** field: Kenmerk:*
   
   ![Payment Identification Search Rule](/images/PM365/payment-identification-search-rule.png)

4. Select the checkbox in the **Search in Description** and/or the **Search in Additional Information** to specify where you want to search for the text.