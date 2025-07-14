---
title: Managing the import of bank account statements
description: How to manage the import of bank account statements.
date: 23-06-2022
id: PM-31
lang: en
---

# Managing the Import of Bank Account Statements

There are two ways to import bank account statements for reconciliation: manual selection of a file or using a direct communication service to import statements directly from the bank. To ensure that files are imported correctly, you must define the file format and import criteria.

## To define file format for manual bank statement import
If you manually import bank account statements, you must define the file format to use for the import. 

To define the import file format:

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **Banks** then select the related link. This will open the list of banks.
1. Open the relevant bank card for which you want to define import format for manually imported bank statements.
1. On the bank card, on the **Import/Export** FastTab, in the **Bank Account Statement File Format** field, specify the file format to use when importing bank account statement files. You can only select the file format when you use manual communication.  

   > [!IMPORTANT]
   >
   > If you decide to utilize the **Data Exchange** option, please note that Continia will not assume responsibility for any errors that may occur during the import process. Due to the possibility of mapping errors, we strongly advise you to exercise caution when utilizing this feature. It is important that the Data Exchange definitions are configured correctly and that the imported data is verified for accuracy.


## To manage bank statement selection for import
If several bank account statements are available for import, you can define which bank account statement should be prioritized when using direct communication. 

To manage the selection of bank account statements:

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **Statement Intelligence Setup**, then select the related link. This will open the Payment Management Setup page.
1. On the **Statement Intelligence Setup** page, on the FastTab **General**, in the **Import Statement By** field, specify how you want to import bank account statements for reconciliation. Use the drop-down arrow to choose between the following selections:
   - **Statement Date**: The account statement with the earliest statement date will be imported.
   - **Entry No.**: The account statement with the lowest entry number will be imported.
   - **Manual Selection**: You will be asked to manually select which account statement to import.

## To manage the bank statement import method

You can specify how to import bank account statements on the bank account card. Indicating whether to import for reconciliation and when to start the reconciliation determines how the statement is imported and handled in the job queue.

>  [!IMPORTANT]
>
> Before activating job queues related to import and reconcile bank statements, customers with Dutch and UK banks must import and reconcile the first bank account to enable the job queues.

To select the bank account statement import method:

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **Bank Account**, then select the related link. Select a bank to open the bank card. 

2. On the **Statement Intelligence** FastTab, in the **Bank Account Statement Import Method** field select one of the following options:
   * Download only
   
   * Import for reconciliation
   
   * Import and start reconciliation automatically
   

If the bank account card is set to **Download Only,** job queue 6216550 will not be activated. Only **Import for Reconciliation** and **Import and Start Reconciliation Automatically** allows jobqueue 6216550 to be run and import the statements automatically. For more information about job queues, refer to the [Using job queues to schedule tasks](@PM-324) article.
