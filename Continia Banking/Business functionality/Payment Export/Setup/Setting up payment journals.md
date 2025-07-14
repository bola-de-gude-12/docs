---
title: Setting up payment journals
description: How to set up payment journals.
date: 17-02-2025	
id: CB-40
lang: en
---
# Setting up payment journals

Continia Banking has enhanced the standard payment journal with additional features to improve the payment flow. It validates payment lines before submission to the bank, and each line includes a status indicator to show whether any further action is required.

## To set up payment journals

The first time you use a payment journal with Continia Banking enabled, you will be prompted to set it up. This setup forms the basis for the payment suggestions in the given payment journal.

To set up payment journals:

1. Search ({{search}}) for and select **Payment Journals**.
2. On the **Payment Journals** page, select the payment journal, and on the action bar, select **Prepare** > **Payment Journal Setup**.  
3. On the **Payment Journal Setup** page, you can configure several options for the payment journals you are currently working on. These options include selecting the Document Number Series to be used when creating lines in the payment journal, specifying the Required Posting Status that determines when posting of the journal lines is allowed, and setting various fields related to the approval workflow.

## To define the balance account on the payment journal

To assign a balance account to a payment journal:

1. Search ({{search}}) for and select **Payment Journal**.
2. On the payment journal header go to the **Batch name** selection, and select the three dots. This opens the **General Journal Batches**.
3. In the general journal batches list, select the payment journal for which you want to define **Balance Account No.**.
4. Fill in the **Bal. Account Type** and the **Bal. Account No.**, if you want a fixed balance account to be used for this journal. 

## To activate Continia Banking functionality for a journal

For payment journals to work with Continia Banking functionality, the **Banking Export Journal** column must be selected. 

1. Search ({{search}}) for and select **Payment Journals**. 

1. Go to the **Batch Name** field, select the three dots, and on the **General Journal Batches** page, select a journal and make sure the Banking Export Journal column contains a checkmark.   

## To switch between Standard and Advanced mode on journal batch level

To offer even more flexibility over payment processes, you have the possibility to set a different mode per journal batch. For example, companies can set the default mode to **Standard** in the Banking Export Setup for efficiency but enable **Advanced Mode** for specific journal batches that require more detailed handling. This is especially useful when managing vendors differently - such as enabling Advanced Mode for vendors with large volumes of payments, complex discount structures, or special due date considerations - while keeping a simpler setup for others.

To change the Banking Suggestion mode for a journal batch:

* On the General Journal **Batches** page, navigate to the journal and in the Banking Suggestion Mode column, select one of the following options:
  * **Empty** - uses the default setup.
  * **Advanced Mode** - enables advanced payment suggestions. First make sure all entries are posted in the payment journal before using payment suggestions. 
  * **Standard Mode** - uses standard payment suggestions.

> [!IMPORTANT]
>
> If a journal batch has a different mode than the **Banking Export Setup**, the batch setting takes precedence.
