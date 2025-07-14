---
title: Introducing Transaction Ports
description: Learn how Transaction Ports in Continia Banking help you import third-party CSV transaction files into Business Central. 
date: 28-03-2025	
id: CB-134
lang: en
---

# Introducing transaction ports

With Continia Banking, you can establish integrated communication between Business Central and third-party CSV transaction files. This integration allows you to import customer payment files directly from external sources into the Payment Reconciliation Journal, handle .csv files, and enable mapping of transaction information to the corresponding fields in the Payment Reconciliation Journal, enabling invoice imports while separating fees and other charges from CSV files.

## How it works

To facilitate the import process of account transactions from external files, our system uses CSV reconciliation ports. Importing and mapping transactions from CSV files involves configuring CSV parameters such as the separator, date format, delimiters, and whether to invert amounts for specific columns. The process begins by mapping CSV file headers, such as MessageID and Currency Code, followed by LineIDs like Posting Date and Description. You can maintain these mappings in the Transaction Port Card interface, which you can access on the Transaction Port List page.

The **Alternative Posting Description** field is used to map a secondary description when the primary posting description is empty. This field is crucial for identifying transactions with additional details, such as fees. Specify the corresponding column in the alternative description import file to provide these fallback descriptions. For instance, if the primary description is missing, the system will use the alternative description to ensure transaction details are comprehensively captured.

## To analyze the file

Before creating a new Transaction Port, it's crucial to analyze the file that you want to import and identify separators, delimiters, and other formatting elements. This allows you to map each column in the CSV file to a corresponding field in the Payment Reconciliation Journal. Use the **Skip Lines** fields to exclude unnecessary columns from the import process.

Review whether essential fields, such as currency, are available in the CSV file. If this field is missing, you can manually add it to your Transaction Port configuration in the Currency field. For instance, if the file includes multiple currencies, Continia Banking will create a separate interface for each currency during the import.

Best practices include:

* **Use a copy** - prevent conflicts by working with a duplicate file.
* **Review the data** - open a sample file and confirm key details before setup. Key identifiers to look for:
  * **Separator** - determine the character used to separate values within each line.
  * **Delimiter** - identify the character used to separate different fields. It can be single or double quotes.
  * **Column headings** - confirm if the first line includes headers describing each column.
  * **Headers and footers** - check for any additional information at the beginning or end of the file that may affect data parsing.
  * **Date format** - note the format in which dates are presented within the file to ensure accurate interpretation during import.
  * **Currency** - identify the currency denomination used throughout the transactions for correct financial reporting.

By reviewing these aspects of your statement file, you'll be well-prepared to configure your Transaction Port and ensure the accurate and efficient importation of bank transactions into Continia Banking.

For detailed steps on setting up a new Transaction Port, refer the [Setting up Transaction Ports](@CB-124) article. 