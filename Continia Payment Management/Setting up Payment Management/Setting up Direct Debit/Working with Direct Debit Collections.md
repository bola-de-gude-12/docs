---
title: Working with Direct Debit Collections
date: 18-05-2022
description: How to set up Direct Debit Collections to respect payment discounts and group collection entries
id: PM-246
lang: en
---

# Working with Direct Debit Collections

> [!NOTE]
>
> To use Payment Management Direct Debit, some requirements apply. Refer to the [Setting up Direct Debit](@PM-223) article to learn more. 

Payment Management Direct Debit gives you an overview of all your direct debit collections. Before a direct debit collection is processed, PM automatically checks the cash receipt journals to ensure that the customer hasn't already paid a collection. You can set up the Direct Debit feature to include the payment discounts that your customers are eligible for. You can also group direct debit collections according to sequence type, lowering the risk of the direct debit files failing when uploaded to the bank.

## To create a direct debit collection

You create a direct-debit collection to instruct the bank to transfer the payment amount from the customer’s bank account to your company’s account. This collection contains information about the customer’s bank account, the affected invoices, and the direct-debit mandate.  

You can create a direct debit collection to determine how to collect the direct debit payments.  

> [!NOTE]
>
> If you created a direct debit collection and want to change the settings later, you must delete the lines in the collection and then create a new one.  

To create a direct debit collection:

1. Select the ![Search for page or report](/images/search_small.png) icon, enter **Direct Debit Collections**, and select the related link.
2. On the **Direct Debit Collections** page, on the Action bar, select **New** > **Create Direct Debit Collection**.
3. On the **Create Direct Debit Collection** page, enter information into the fields that determine how to collect the direct debit payments. For example, you can choose to select only the Invoices with a valid mandate ID, add a due date, and select the partner type. To include payment discounts that your customers are eligible for, enable the **Find Payment Discounts** setting.
4. Select **Ok** to request the direct debit lines. 

> [!NOTE]
>
> If the Direct Debit is already a part of a Cash Receipt Journal, it will be excluded from the collection.



## To group collection entries automatically

To collect payments via Direct Debit, it is necessary for your customer to provide you with a mandate. A Direct Debit mandate is the customer's authorization for future payment collection.

To streamline the process, Payment Management allows you to set up Direct Debit grouping based on the mandate ID. By associating multiple collection entries with the same customer ID, transfer date, and mandate ID, you can consolidate them into a single file. This feature enables the automatic grouping of entries under the mandate ID you create for each customer, simplifying the submission of multiple entries.

To group collection entries automatically:

1. On the relevant customer card, select **Customer** > **Direct Debit Mandates**.
1. Select **New** and for the new mandate ID, fill in the relevant fields, and select the **Group Entries** checkbox. 
1. On the customer card, navigate to the **Payments** FastTab, and in the **Preferred Mandate ID** field, select the mandate ID you added earlier. The mandate ID is automatically added to every invoice with this direct debit customer.
1. On the **Payments** FastTab, navigate to the **Intrastat Partner Type** field, and select whether the customer is a person or a company for reporting functionalities.

> [!IMPORTANT]
>
> If your bank can't process direct debit files that include entries of the sequence types First and Recurrent, make sure you have enabled **Separate by Sequence Type** in the [direct debit setup](@PM-223#to-set-up-direct-debit). This ensures that for groups that contain both sequence types, collection entries of the type First will always be exported before the entries of the type Recurrent.  

## To group collection entries manually

To group Direct Debit Collection entries manually:

1. Select the ![Search for page or report](/images/search_small.png) icon, enter **Direct Debit Collections**, and select the related link.

1. On the **Direct Debit Collection** page, open the relevant direct debit collection.

1. On the **Direct Debit Collection Entries** page, select the entries you want to include in groups and select **Group** > **Create groups**. This creates one or more groups, depending on how many groups the selected entries can be divided into.

In the FactBox pane, you can see an overview of any groups you just created, and in the list of entries, you can see that each grouped entry now has a group ID in the **Group ID** column. 



## To manage existing groups

To manage existing groups on the **Direct Debit Collection Entries** page, use the following actions in the action bar:

- Select **Group** > **Add Entries to Group** to add one or more selected entries to an existing group.
- Select **Group** > **Remove Entries from Group** to remove one or more selected entries from an existing group. If you remove all entries from the group, the group is deleted.
- Select a group ID in the **Group ID** column to view all the entries in that group. From here, you can also reject a group in situations where the bank can't process a group.  
- Select **Delete** to remove the direct debit collections that do not have any entries. 



## To export the direct debit collections file

From the direct debit collection entries, you can export an XML file that you send or upload to your bank for processing. Any payments that the bank can't process will be communicated to you by your bank, and you must manually reject the related direct debit collection entries. 

To export the direct debit file:

1. Select the ![Search for page or report](/images/search_small.png) icon, enter **Direct Debit Collections**, and select the related link.
2. On the **Direct Debit Collection** page, on the action bar, select **Export Direct Debit File** to create and download the *Pain.008* file. You must upload this file to the bank manually.
3. When the payment upload to the bank is completed, on the action bar, select **Process** > **Post Payment Receipts**.



If you require a specific filename for the Direct Debit file, you can enter that file name in the Payment Management Setup:

1. Select the ![Search for page or report](/images/search_small.png) icon, enter **Payment Management Setup**, and select the related link.
2. On the action bar, select **Troubleshooting**.
3. On the General FastTab, go the **File Name (Direct Debit File)** field and enter the name.



## To post a reversal

When you import a bank statement that includes reversals, the invoices that can't be handled automatically display in the Bank Account Reconciliation.

> [!IMPORTANT]
>
> Before you post a reversal, you must close the original customer ledger entry using the **Post Payment Receipt** action on the **Direct Debit Collection Entries** page of Payment Management Direct Debit Collections.

To post a reversal:

1. On the **Bank Acc. Reconciliation** dialog, navigate to the **Bank Statement Lines** section, and in the **Status** column look for the suggestions that say: *Reversal*.
2. In the **No. of Reconciliation Suggestions** column select the number of the invoices that are reversed. 
3. Select **Ok** to approve the reversal.
4. On the action bar, select **Journals** > **Reversals**.
5. On the **Edit - Reversals** dialog, the suggested lines you selected display. On the action bar, select **Post Reversals**.





## Related information

[Setting up Direct Debit](@PM-223)
