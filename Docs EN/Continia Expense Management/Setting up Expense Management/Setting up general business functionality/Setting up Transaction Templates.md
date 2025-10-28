---
title: Setting up transaction templates
date: 28-07-2025
description: Set up a transaction template to see how bank transaction files are processed
id: EM-42
lang: en
---
# Setting up transaction templates

Before importing bank transactions from your bank into Expense Management, you need to set up a transaction template. Each template is associated with a bank, and it’s possible to have multiple templates for the same bank. Each template includes several rules and configurations, and they determine how bank transaction files are processed.

To set up a new transaction template, follow these steps:

1. Search for {{search}} **Banks**. 

2. Choose a bank on the list. If you can't find the bank you want to import the transactions on the list, you need to create a new one.

3. On the action tab, click **Related** > **Bank** > **Transaction Template**. 

4. Under **General**, fill out the information as required. 

The following table outlines specific fields that may require some explanation:

| Field | Description |
| --- | --- |
| Data Formats | Select a predefined data format for the Date and Decimal fields. If the required date or decimal format is not defined in the lookup list, it's possible to enter one directly via free text. |
| Lines to be ignored | In the No. of Header Lines and No. of Footer Lines fields, you can determine if certain lines at the beginning or end of the file should be ignored during import, such as lines containing header information. |
| Enable/Disable Template Rules | This option helps you set whether the card number should be read from the name of the transaction file. If the credit card number is specified in the file name and not in the transaction itself, enabling the **Card number in the file name** will extract the card number from the file name using the card number start position and length. The **Line Rules** section lets you exclude lines from the file, such as lines containing the word "Total," resulting in those lines not being imported. |
| Field Mapping | This section allows you to map bank file fields to Expense Management fields. For example, when transactions are imported from the Bank file into the Expense Management system, the *Description* field in the Bank file might contain details about the transaction, such as the vendor name, transaction type, or a brief expense description. By mapping the *Description* field from the Bank file to the *Business Name* field on the transaction template using the Column No., the system can automatically populate the *Business Name* field with the relevant information from the Bank file during the import process.<br>When dealing with files containing negative amounts, you *must* enable the Reverse sign option manually. This is necessary because credit transactions should be imported into the transaction journal as positive amounts. |
