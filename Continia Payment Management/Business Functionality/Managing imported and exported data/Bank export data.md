---
title: Bank export data 
description: Learn more about how the Bank Export Data page lists all imported bank data
date: 01-11-2021
id: PM-206
lang: en
---

# Bank Export Data

The Bank Export Data page contains a table that lists all imported bank data, such as customer payments, vendor payments, status lines, and bank account statement lines. Payment Management creates the Bank Export Data from files imported to the file archive (manually imported and imported files using direct communication). 

In case you are experiencing issues with imported bank data, you can use the Bank Export Data to investigate what's causing the problem. You can also use the Bank Export Data to manage whether data can be reimported into the system.

The Bank Export Data columns:

* **Record Type** - specifies the type of entry received from the bank. The entry type can be account statements, customer payments, and vendor payments:
  - **Inhouse** - Continia's payment file format. They are used for the payment file before it is converted to the bank's file format.
  - **Status** - ISO PAIN.001, ISO PAIN.002 – first and second edition, ISO CAMT.054.
  - **Camt.52** - update status in Payment Journal.
  - **Account Statement** - ISO CAMT.053 files, both standard and extended.
  - **Payment Receipt** - PBS Sector file, Total-IN, BG-MAX.
  - **CREMUL** - ISO CAMT.054C.
  - **DEBMUL** - ISO PAIN.008.
  - **Direct Debit** - ISO PAIN.008.
  - **Payment Service Provider** - files from the supported providers in the PSP module Amazon, BOL, etc.

* **Entry No.** and **Parent Entry No.** - use to identify if the lines originate from the same file.
* **Message ID** - specifies a unique identification of the line. Payment Management uses the Message ID to ensure that a file or a line is not imported more than once unless the **Imported to Company** is blank.

For more details on supported file formats, refer to the [Payment Management Supported Bank Files.](@PM-123)



## Permitting or granting the reimport of bank data

When payment lines are imported into Business Central, they will be created in Bank Export Data with a checkmark in the column **Imported to Company**, stating that a line has been imported into the system. This checkmark ensures that payment lines are not reimported the next time a file is imported into the system. 

If payment lines or bank statement lines are deleted in a payment journal or a bank account reconciliation, the checkmark in the column **Imported to Company** in Bank Export Data will be cleared for the corresponding lines. This means that the bank data for the given lines will be reimported the next time a payment file or a bank statement is imported into the system. You can permit or grant a reimport of payments or bank statement lines by selecting the following actions: **Set Imported to Company** to grant reimport, or the action **Remove Imported to Company** to permit reimport. The two actions are located in the action bar on the **Bank Export Data** page. 

> [!IMPORTANT]
>
> The imported lines for a given file contain a **Record Subtype** stating if a line is the file *Header* or a file *Line*. When using the action **Remove Imported to Company**, we strongly recommend that you work with the concept of *all or nothing*, meaning that you should only use the action *for all lines* (both header and lines) for a given payment file or bank account statement. This is to avoid issues when reimporting the file.



## Finding causes for expected data to be missing

The following table, lists some of the most common issues causing expected data to be missing in the Bank Export Data table:

| Validate | Description |
| --- | --- |
| Is the file imported into the File Archive? | In case the expected data is not available in the Bank Export Data table, you should check if the related file has been imported into the File Archive. Read more about the File Archive [here](@PM-162). If the expected file is not available in the File Archive, the file must be reordered in the bank. |
| Has data been created from the file? | If the expected file is available in the file archive, but the data hasn't been created in Bank Export Data, the file should be reimported in the File Archive. You reimport a file from the action bar on the page **File Archive**. |
| Does the table contain an empty header? | You should validate that the Bank Export Data does not contain an *empty header line* with no associated lines. This might be the case if Payment Management has tried to import files from the bank when no file is available. In this case, you must select the line, and use the action **Remove Imported to Company.** |
| Does the account number correspond to the registration number and account number on the bank credit card? | The account number in the file must correspond to the registration number and the account number on the bank credit card, otherwise, the data can't be created. |

