---
title: Handling reverse charges in Document Capture
date: 25-07-2025
description: How to handle reverse charges in Document Capture.
id: DC-446
lang: en
---

# Handling reverse charges

This article describes how to handle reverse charges in Continia Document Capture.

## Definition

The reverse charge mechanism is a special arrangement in the VAT system, where the responsibility for reporting and paying VAT shifts from the vendor to the recipient of the items or services. Reverse charges are typically used for cross-border transactions within the European Union (EU) to simplify VAT reporting and reduce VAT fraud.

## To handle a reverse charge

Before following the steps below, make sure to configure the VAT posting setup in Microsoft Dynamics 365 Business Central to handle reverse charges. For more information, see [Set up calculations and posting methods for value-added tax](https://learn.microsoft.com/en-us/dynamics365/business-central/finance-setup-vat) (Microsoft article).

1. Search ({{search}}) for and select **Document Categories**.
2.	Click the relevant document category code – for example, **PURCHASE** – to open the document journal.
3.	In the list of documents, select the one whose template you want to edit.
4.	When recognizing the document, make sure that both the amounts including and excluding VAT are captured. The actual VAT amount should neither be stated on the invoice nor captured.
5.	In the action bar, click **Template > Accounts for Amounts** to open the **Accounts for Amounts** page.
6.	Select the desired account type and the account number. Under **VAT Prod. Posting Group**, select the posting group you created to handle reverse charges. E.g.: FULL REVERSE.  
7.	When the document is registered, the appropriate G/L entries are created.

>[!TIP]
>Alternatively, you can create a lookup template header field (tied to the **VAT Product Posting Group** source table) to select the FULL REVERSE posting group directly in the document – instead of under **Account for Amounts**.
This provides a better overview and faster processing when handling the total invoice amount. If you post invoice amounts across multiple accounts, use the Accounts for Amounts approach.

