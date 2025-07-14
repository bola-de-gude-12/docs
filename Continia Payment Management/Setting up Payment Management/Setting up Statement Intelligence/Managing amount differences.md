---
title: Managing amount differences in Payment Management
description: Information on how to manage amount differences
date: 14-09-2021
id: PM-195
lang: en
---

# Managing Amount Differences

Amount differences are stated in the bank account reconciliation on the imported bank statement lines as **Difference**. The amount differences occur when Statement Intelligence hasn't been able to match and apply reconciliation lines to bank account ledger entries. This can be a result of various reasons such as payments that haven't been posted, missing ledger entries (for example, fee or tax), missing Transaction ID or OCR ID, currency exchange rate, or a deviation of days or amount outside of the specified tolerances. 

In case the amount differences are caused by missing bank account ledger entries, Statement Intelligence will seek to suggest ledger entries to be posted from a temporary journal created in the bank account reconciliation. The suggestions will be based on various information such as date, amount, and reconciliation rules. You must define which journals Statement Intelligence must use to manage the suggested journal ledger entries.

Journal template and batch can be defined for the following journals:

- **General Journal**
- **Cash Receipt Journal**
- **Payment Journal**
- **Employee Payment Journal**

 


## To define a general journal for amount differences

In case of amount differences on the bank statement lines caused by missing ledger entries, you can specify a general journal to be used by Statement Intelligence for creating general ledger posting suggestions. <br>Examples of missing ledger entries could be coverings, interests, and fees. In this case, amount differences will be created as ledger entries in a general ledger journal ready to be posted. 

Follow the guide below to define a general journal template and general journal batch to be used in the bank account reconciliation.

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Accounts**, and then select the related link.
1. Open the relevant bank account card.
1. On the bank account card, navigate to the **Statement Intelligence** FastTab.
1. In the box **General Journal Template**, specify the general journal template to use in the bank account reconciliation when handling amount differences that have no related document.
1. In the box **General Journal Batch**, specify the general journal batch to use in the bank account reconciliation when handling amount differences that have no related document.



## To define journals for vendor-, customer- and employee amount differences

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Accounts**, and then select the related link.
1. Open the relevant bank account card and navigate to the **Statement Intelligence** FastTab.
1. Define the journal templates that will be used to manage amount differences for customers, vendors, and employees in the bank account reconciliation. This can be defined in the following boxes:
   - **Cash Receipt Journal Template**
   - **Vendor Journal Template**
   - **Employee Payment Journal Template**
1. Define the journal batches that will be used to manage amount differences for customers, vendors, and employees in the bank account reconciliation. This can be defined in the following boxes:
   - **Cash Receipt Journal Batch**
   - **Vendor Journal Batch**
   - **Employee Payment Journal Batch**



## To manage currency exchange rate differences

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **Statement Intelligence Setup**, then select the related link. 
1. On the **Statement Intelligence Setup** page, navigate to the FastTab **General**.
1. Enable **Create Currency Exchange Rate Amount Difference** if currency exchange rate amount differences must automatically be created as general journal lines when reconciling your bank account.

 

##  To handle amount differences in the Cash Receipt Journal

When reconciling cash receipt journal lines, you can remove differences using the **Insert Difference Journal Lines** action. Instead of merely updating the amount, additional journal lines are added for more clarity and accuracy:

* a line for the customer's posted amount
* a line for the difference amount to be posted on the G/L account
* a line for balancing the bank account and reflecting the reconciliation amount

To specify a G/L account for the difference amount:

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **Statement Intelligence Setup**, then select the related link. 

2. To be able to use the **Insert Difference Journal Lines** action, you must disable the **Renumber Journal Document Nos.** setting on the **General** FastTab. 

3. On the **Statement Intelligence Setup** page, navigate to the FastTab **Default Journals**, and select an account in the **Default Difference Amount G/L Account** field.

   

To invoke the Insert Difference Journal Lines action:

1. From the Bank Account Reconciliation card, open the Cash Receipt Journal.

2. On the **Home** tab, on the action bar, select **Insert Difference Journal Lines**.

   > [!NOTE]
   >
   > To be able to use the **Insert Difference Journal Lines** action, you must make sure to disable the **Renumber Journal Document Nos.** setting on the **General** FastTab. 

   
