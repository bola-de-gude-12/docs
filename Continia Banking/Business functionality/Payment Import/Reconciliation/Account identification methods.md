---
title: Transaction Type Identification in Continia Banking
description: Learn how Continia Banking identifies accounts using codes and rules. 
date: 07-05-2025	
id: CB-33
lang: en
---

# Transaction type identification

Continia uses bank transaction code rules to accurately sort and manage entries within financial statements when handling financial transactions. By utilizing standardized lists such as ISO Transaction Codes and unique Proprietary Transaction Codes, these rules help accurately identify various transaction types, including payments, fees, and other financial activities.

> [!WARNING]
>
> Do not change the default code rules unless you fully understand their implications. Modifying these codes without proper knowledge can lead to misclassification of transactions, inaccurate financial reporting, and potential compliance issues. 

## Bank transaction code rules

Continia Banking uses the Bank Transaction Code Rule table to match account types to Bank Transaction Codes. These rules associate bank transaction codes with internal posting logic and customer/vendor accounts. Common combinations are preconfigured and automatically inserted when the **Banking Import App** is installed.

Account identification is supported by matching the **Bank Transaction Code** from the imported bank statement to an entry in the rule table. Each rule specifies the relevant account type (e.g., Customer, Vendor, Bank, G/L Account) to guide how the transaction is posted or matched during reconciliation.

In addition to standard matching, the **Bank Transaction Code Rules** table includes a field that allows specific transaction codes to be marked as **Direct Debit Return** related. If a rule contains a return indicator, any matching transaction will automatically have its **Return** field set in the bank reconciliation line. This assists in identifying return direct debits even when no reversal indicators or return reason codes are transmitted in the CAMT file. If return information cannot be determined automatically, the **Return** field remains editable, allowing manual tagging of return-related transactions. These rules can be viewed and managed from the **Bank Transaction Code Rules** page. 

Matching by transaction code is enabled by default in the **Banking Import Setup**, but this behavior can be adjusted if needed.

## ISO transaction codes

Continia Banking automatically inserts ISO Bank Transaction Codes, which are standardized codes defined by the International Organization for Standardization (ISO), upon installation. These codes ensure uniformity and clarity in financial reporting across different systems and institutions. Continia stores the transmitted ISO bank transaction code in the bank account reconciliation line during import, with descriptions displayed in review and match details.

To update ISO codes, navigate to the **ISO Bank Transaction Codes** page, and on the action bar, select **Update ISO Bank Transaction Codes**.

## Proprietary transaction codes

In banking systems, proprietary bank transaction codes are used to classify specific transaction types. These codes vary across banks and systems, requiring a flexible setup to accommodate differences. In Continia Banking, proprietary bank transaction codes and transformation rules help manage these variations efficiently. Banks often develop their own unique codes to supplement standardized ISO transaction codes, and these proprietary codes are included in MT940 and CAMT statement files.

When Continia Banking is installed, the system automatically downloads proprietary bank transaction codes along with standard transaction data. During import, if a statement file contains a proprietary code, the system stores it within the bank account reconciliation line. The code’s description is also displayed on the review page and in match details for easy reference.

> [!TIP]
>
> Descriptions associated with transaction codes are visible on the Payment Application Review Page. This provides users with information about the type of transaction, which can be especially useful when automatic matching fails and manual handling is required.

