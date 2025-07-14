---
title: Setting up Transaction Ports in Continia Banking
description: Learn how to add a Transaction Port, to start the import process, and to open the file in the Payment Reconciliation Journal.
date: 28-03-2025	
id: CB-124
lang: en
---

# Setting up transaction ports

Once you have [analyzed the file](@CB-134) you want to import and identified separators, delimiters, and other formatting elements, you are ready to map each column in the CSV file to a corresponding field in Continia Banking. 

## To add a transaction port

To set up a transaction port:

1. Search ({{search}}) for and select **Transaction Ports**. 
2. On the action bar, select **New** to create a new Transaction Port. 
3. On the **Transaction Port** page, enter a code and a description for the Transaction Port. The **Code** field is mandatory. 
4. Navigate to the **Setup** FastTab to enter the information to map the fields. Refer to the table for the fields and their possibilities:

| Field                                     | Description                                                  |
| ----------------------------------------- | ------------------------------------------------------------ |
| CSV Separator                             | Enter the separator type used in your CSV (Comma-Separated Values) files. The role of a separator is to demarcate two distinct entities so that they can be distinguished. These characters separate fields of data within each line. The most common CSV separators are: **Comma (,)**: Fields are separated by commas. Example: `total_sale_amount,total_fee_amount,total_return_amount,total_reversal_amount,...` **Semicolon (;)**: Used in some regions instead of commas. Example: `Account;Amount;Use;Date`. This field is mandatory. |
| Date Format                               | Enter the date format used in your CSV file. This setting is used during file import to ensure the correct formatting of the posting date. The date format is based on the [.NET DateTime format](https://learn.microsoft.com/en-us/dotnet/standard/base-types/custom-date-and-time-format-strings). For example, ddMMyyyy. |
| Decimal Separator                         | Specify the character used as a decimal point. For example, period or comma. |
| Thousands Separator                       | If used, specify the character used to separate thousands. For example, period or comma. |
| Delimiter                                 | Delimiters are used when files contain both commas as separators and descriptions with embedded commas. |
| Skip Lines From Start                     | Specifies the number of initial rows to skip during import. This is useful for excluding header rows or any introductory text that does not require importing. For instance, skip rows that solely contain header information or irrelevant introductory text. |
| Skip Lines From End                       | Enter the number of lines at the end of the file to skip during import. |
| First Line is Header Line                 | Enable if the first line of the file contains column headers. You can also use the **Skip Lines From Start** field. |
| Skip Alternative Description Import       | For example, if you have a column in your file representing a fee that you don't want to import, you can specify the specify the fee description in the line to exclude it  to exclude it. If you need to exclude multiple columns, separate their names with a comma. For instance, you can specify *Fee,VAT* to exclude both columns. |
| Invert Amount for Columns                 | This option allows you to reverse or invert the values in specified columns. |
| Invert Amount for Alternative Description | Specify the alternative descriptions for fees in the file for which the amounts should be inverted. To add multiple columns, separate the column names with a comma. For example, you can list them as *Column1,Column2*. |
| Fee Alternative Description               | Descriptions with invoice numbers, like Commisions, Transportation Fee, Transaction Fee, and so on, should not be included in the invoice price and should be treated as fees. |
| Handle Existing Records                   | Specify how to handle existing records during the import process. The Handling Existing Records field determines the action to take if duplicate data is detected during import. When the Message ID field is specified, the system checks all imported data in the file to prevent duplicates. This applies to both header and line messages. You can choose between two options:<ul><li>**Skip** - if a record with the same Message ID is found, the system will skip importing that record to avoid duplication.</li><li>**Replace** - if a record with the same Message ID is found, the system will delete the existing record and import the new one. If you already posted some of the lines, replacing is not possible and you will receive and error message and the new lines will be skipped.</li><br/>If you prefer to always import all data, it may be best to not use the Message ID field. |
| Header Message ID                         | This field maps the file identifier. Specify the exact position of the unique file identification (Header Message ID). For example, *B5*. |
| Line Message ID                           | This field maps the transaction identifier. Specify the exact position of the column with the unique transaction number that will never repeat. Please keep in mind to use it if all lines have it and it is unique always as duplicated records will be skipped or replaced. |
| Posting Description                       | This field maps the reference number of the invoice or any other reference data. The Posting Description field specifies the position of the reconciliation reference. For example, the order ID. You should select the specific column that contains the invoice number or relevant reference. You can enter the column index (for example, *3*) or the column letter in uppercase. For example, *C*. |
| Alternative Posting Description           | This field maps an alternative import field if the posting description is empty. For example, a fee identifier. Specify the column in the alternative description import file that contains alternative posting descriptions |
| Posting Date                              | This field maps the date of the payment. Specify the column in the file that contains posting dates. |
| Currency                                  | Specify the column in the file that contains currency information. The **Currency** field specifies the position of the currency information in the file you are importing. You can indicate the column number (for example, *2*) or the column letter in uppercase (for example, *B*). If the currency is not present in the file, you can manually enter the currency code in this field. For example, *EUR*. |
| Amounts                                   | Specify the columns in the file that contains amounts. The **Amounts** field specifies the position of the amount columns in the file. If there are multiple columns with amounts in the same currency, list these columns separated by commas. You can use column letters (for example, *D,F,G*), column numbers (for example, *4,5,6*), or a combination of both (for example, *D,4,5*). |
| Currencies and Amounts                    | The **Currencies and Amounts** field comes in handy if there are two or more amounts and two or more currencies in one line. Specify the positions of currencies and amounts in your import file. Different currency and amount positions should be separated by a comma, and each set should be separated by a semicolon. For example, *2,5;C,F;EUR,7*<br />`2,5`: Specifies currency at position 2 and amount at position 5.<br />`C,F`: Specifies currency in column C and amount in column F.<br />`EUR,7`: Specifies EUR currency and amount at position 7. |
| Internal Texts                            | This field maps additional information from the CSV file. Other important columns that contain texts that you want to import and map. The Internal Text field specifies the position of internal texts in your import file. If there are multiple text fields, you can specify their columns separated by commas. For example:<br/>*8,9*: Specifies internal texts in columns 8 and 9.<br/>*M,N*: Specifies internal texts in columns M and N. |

   

## To start the import process

To import the data:

1. On the **Transaction Port** page, on the action bar, select **Actions** > **Import**. 
1. You are now prompted to select the file for import. Continia converts the file and sends the data, making it possible to import the data to the Payment Reconciliation Journal.
1. After the import, you can review the results by navigating to the action bar and selecting **Related** > **Imported Headers**.  
1. On the **CSV Headers** page, navigate to the **Port Code** field to open the **Header Card**. 
1. On the **Header Card**, you can view a detailed log of imported transactions that helps you verify the accuracy and completeness of the data import. You can verify if your settings successfully imported the file. For example, check the invoice numbers, posting dates, and other important settings to ensure your separators and alternatives worked as intended, converting all data correctly. See the **Details** FactBox on the right panel to review the amounts and currency.

## To open the file from the Transaction Port into the Payment Reconciliation Journal

Once you mapped the fields of the CSV file on the Transaction Port page, the file is ready to be handled and reconciled. You can do this in the Payment Reconciliation Journal. 

To open the CSV file in the Payment Reconciliation Journal:

1. Search ({{search}}) for and select **Payment Reconciliation Journal**.
2. On the **Payment Reconciliation Journal** page, open the journal. The bank account needs to have both a currency code and a bank code specified, matching the currency in the imported transactions from the CSV file.
3. On the journal page, on the action bar, select one of the following options:
   * Import Transactions from CSV
   * Import Existing Transaction from CSV
4. On the **CSV Import Settings** page, you can now select the Transaction Port Code that you want to import. Depending on whether you have already imported the file or not, the system can prompt you to upload a file.  
5. You can now handle the lines in the journal. For more information about handling lines in the Payment Reconciliation Journal, refer to the dedicated [article](@CB-106).

<style>


 .content table tr td:nth-child(1) {
 width: 220px;
 }
 .content table tr td:nth-child(2) {
 width: 580px;
 }
</style>
