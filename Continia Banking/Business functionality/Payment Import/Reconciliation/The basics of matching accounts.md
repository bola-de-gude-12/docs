---
title: The Basics of Matching Accounts in Continia Banking
date: 20-08-2024
description: Learn more about the account matching process in Continia Banking.
id: CB-108
lang: en
---
# The basics of account identification in Continia Banking

In Continia Banking, an essential step in effective financial management is the process of account identification. This involves matching identifiers such as BBAN, IBAN, and names (including address and city) to ensure accuracy in financial records. It involves comparing transactions recorded in a company's internal records with those on external documents, such as bank statements or invoices. The system identifies transactions and matches them with corresponding accounts. Sometimes, it recognizes an account but can't create an application due to missing information. In such cases, the system informs users and sets the Reconciliation Status on the Bank Account Reconciliation Line to notify users that it found an account.

## The matching process

If bank statement lines lack sufficient details to match using date, document number, and amount, you can set up search rules to identify matching ledger entries using text. Search rules help identify accounts by searching for specific text in the bank account reconciliation lines within both the Bank Account Reconciliation and Payment Reconciliation Journal. 

Business Central uses the term *Related Party* to refer to the other party involved in the transaction. Continia Banking uses standard fields, including Related-Party Name, Address, City, and Bank Account Number, to store and match data received from the bank. This transparent display ensures users can easily access and verify all related information. Account identification is about matching identifiers such as IBAN, BBAN, name, address, city. 

The matching process in Continia Banking follows a specific order to identify the correct account:

1. **Bank Rules** - the system first checks for any [predefined search rules](@CB-104) related to the party’s bank details.
2. **Bank Account No. or IBAN** - it then looks for matches based on the bank account number or IBAN. In Continia Banking, you can benefit from the automatic learning functionality to identify accounts based on IBAN and other relevant information. When a statement arrives, the system captures and stores the IBAN (or BBAN), using it to assist in identifying the correct account. Initially, the IBAN/BBAN and the assigned account number are inserted into the Related Party Rule field when this combination is posted for the first time. Subsequently, future account statements can use this stored information for accurate mapping. You can enable or disable automatic mapping via the **Related Party Rule** field on the [Banking Import Settings page](@CB-14).
3. **Name, Address, and City** - if no match is found, the system checks the combination of name, address, and city.
4. **Name** - lastly, if the name alone is unique among customers, vendors, and employees, the account is assigned.

## To view detailed matching information

For each journal line, you can view detailed matching information on the status, match confidence, tolerance, and so on.

To view detailed matching information:

* On the **Bank Account Reconciliation** page, on the action bar, select **Matching** > **Match Details**. 
* On the **Payment Reconciliation Journal** page, navigate to the **Match Details** FactBox on the right of the page.
* On the **Bank Account Reconciliation** page, on the Home tab of the action bar, select **Application Proposals**.
* On the **Payment Reconciliation Journal** page, on the Home tab of the action bar, select **Application Proposals**.