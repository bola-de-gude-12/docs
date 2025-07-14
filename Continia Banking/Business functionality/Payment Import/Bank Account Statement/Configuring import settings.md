---
title: Configuring Bank Statement Import Settings
description: How to change the import settings of bank account statements and payments.
date: 01-07-2025
id: CB-14
lang: en
---

# Configuring bank statement import settings

Continia Banking simplifies the process of importing your bank account statements, whether through uploading files or direct bank communication. Once you import the statement, Continia Banking converts the bank's file format to list all the information needed to reconcile your bank account. On the **Banking Import Setup** page, you can customize automatic matching of entries, establish tolerances for payment proposal variations, and define essential details to ensure precise reconciliation. By default, the most relevant settings are pre-configured to streamline your banking operations.

Additionally, to facilitate reconciling Bank Account Ledger Entries without an existing entry, you can link a Cash Receipt, General, and/or Payment Journal to the Bank Account Reconciliation. This setup ensures that any payment proposals not directly associated with a Bank Account Ledger Entry generate corresponding journal lines in the journal dedicated to Bank Account Reconciliation. This way, the user can stay on the [Bank Account Reconciliation page](@CB-22) and can make a posting elsewhere before continuing with the bank account reconciliation.

To configure bank statement import settings, follow these steps:

1. Select the {{search}} icon, enter **Banking Import Setup**, and select the related link.

2. On the **Import** FastTab, in the Default Bank Statement Description Field **Template** field, you can set the default field to be used as the statement description and transaction text when importing bank transactions. By giving priority to specified fields, such as the first line of additional information, blank descriptions from banks can be handled effectively during event imports.

3. On the **Matching** FastTab, you can edit the following settings:

   | Field                                                        | Description                                                  |
   | ------------------------------------------------------------ | ------------------------------------------------------------ |
   | Min. Search Length                                           | Specify the minimum number of words, necessary for the system to consider entries during the matching process, enhancing the accuracy of your reconciliations. |
   | Bank Ledger Entries, Customer Ledger Entries, Vendor Ledger Entries, Employee Ledger Entries | You can activate automatic matching for specific entries.    |
   | Allow Tolerance                                              | To ensure a balance between precision and flexibility in financial transactions, you can enable tolerances for payment proposals by defining allowable variances. |
   | Tolerance Amount                                             | Displays only if the **Allow Tolerance** option is enabled. Specifies the tolerance amount for automatic matching of Payment Application Proposals. If both the **Tolerance Amount** and **Tolerance Percentage** are set, the system calculates based on the percentage. If the calculated value is less than the tolerance amount, it's used; if greater, the tolerance amount is applied.<br />The tolerance value amount is always in LCY and cannot be negative.<br/><br/>The tolerance setup on the customer or vendor card is used if the Tolerance Value field contains an amount and if a customer or vendor is identified during the reconciliation. If the **Tolerance Value** field on the customer or vendor card is empty, the **Tolerance Value** field on the bank account is used. |
   | Tolerance Percentage                                         | If the **Allow Tolerance** option is enabled, this field specifies the tolerance percentage for automatic matching of Payment Application Proposals. If both the Tolerance Amount and Tolerance Percentage are set, the system calculates based on the percentage. If the calculated value is less than the Tolerance Amount, it's used; if greater, the Tolerance Amount is applied. |
   | Bank Transaction Code Rules                                  | Indicates whether bank transaction codes should be used to match account types automatically. |
   | Search Rules                                                 | If enabled, the matching process includes using search rules to find account types and numbers. |
   | Default Search Field Template                                | In this field, you can choose a default template for search rules. |
   | Payment Reference Rules                                      | If enabled, automatic matching includes entries based on predefined payment reference rules. |
   | Date and Amount                                              | If enabled, bank account ledger entries are matched based on the posting date and statement amount. Only entries with an exact date and amount match are used for reconciliation. This improves accuracy, speeds up matching, and prevents errors. It should be turned on when strict 1:1 matching is needed, especially if the bank provides accurate transaction dates. This setting depends on the **Bank Ledger Entries** field being enabled and is disabled by default. |
   | Related Party Rules                                          | When enabled, Continia Banking searches for related bank accounts to provide possible matches for transactions that require additional information to complete the reconciliation process. |
   | IBAN                                                         | When enabled, Continia Banking searches for related IBANs to provide possible matches for transactions that require additional information to complete the reconciliation process. |
   | Name and Address                                             | When enabled, Continia Banking searches for related names and addresses to provide possible matches for transactions that require additional information to complete the reconciliation process. |
   | Exact Name                                                   | When enabled, Continia Banking searches for related transactions using the same name to provide possible matches for transactions that require additional information to complete the reconciliation process. |

4. On the **Amount Difference** FastTab, you can edit the following settings:
   | Field                        | Description                                                  |
   | ---------------------------- | ------------------------------------------------------------ |
   | Show Dialog                  | If enabled, the dialog for amount differences will be displayed when creating journal lines. For more information refer to the [Handling amount differences] |
   | Default Account Type         | Defines the account type used for amount difference lines. If set to **Account Type**, it defaults to the account type from the bank statement line or payment reconciliation journal line. |
   | Default Account No.          | Specifies the account number to be used for amount difference lines. |
   | Posting Description Template | Determines the default template to be used for posting descriptions when creating lines for discrepancies in amounts. |

5. The default journals for Bank Account Reconciliation are automatically set up upon activation of Continia Banking. You can customize the following settings on the **Bank Account Reconciliation** FastTab:

   | Field                                     | Description                                                  |
   | ----------------------------------------- | ------------------------------------------------------------ |
   | General Journal Template Name             | Allows you to define the default general journal template to use in reconciliation to post rent, fees, or other recurring entries. |
   | General Journal Batch Name                | Allows you to define the default general journal batch name to use in reconciliation to post rent, fees, or other recurring entries. |
   | Cash Receipt Journal Template Name        | Specifies the default cash receipt journal template to use in reconciliation for posting customer payments. |
   | Cash Receipt Journal Batch Name           | Specifies the default cash receipt journal batch to use in reconciliation for posting customer payments. |
   | Payment Journal Template Name             | Specifies the default name of the payment journal template to use in reconciliation for posting vendor payments. |
   | Payment Journal Batch Name                | Allows you to define the default payment journal batch name used in reconciliation for posting vendor payments. |
   | Default Create Journal Line Method        | When a search rule is applied, this specifies the default method for creating journal lines. |
   | Show Dialog                               | If enabled, the manual reconciliation dialog will be shown when creating journal lines manually. |
   | Journal Template Type (Manual handling)   | Defines the default journal template type used when manually creating journal lines. If **Account Type** is selected, the template type is determined by the account type of the bank account statement line. |
   | Journal Template Type (Amount difference) | Defines the default journal template type for creating journal lines related to amount differences. If **Account Type** is selected, the template type is based on the account type of the bank account statement line. |

6. On the **Payment Reconciliation** FastTab, you can enable the **Post Sum per Posting Date** functionality. This setting is only effective on Payment Reconciliation journals and means that when you activate it, only one balance account entry will be recorded for a specific posting date during payment reconciliation. In other words, all the transactions for that date will be combined into a single account entry. However, due to this consolidation, a few limitations exist:

   * **Same document number** - all entries share the same document number in the accounting records. This simplifies the tracking process but may limit detailed documentation for individual transactions.
   * **Limited dimension support** - detailed dimensions (extra categorizations of transactions, like departments or projects) cannot be fully supported in this consolidated balance account entry. The system won't capture this detailed information due to the summarization of entries.
   * **Rounding differences** - when dealing with foreign currencies, where exchange rates fluctuate, rounding differences may occur. These discrepancies might happen during the consolidation process due to the system rounding off amounts to simplify the entries.

7. On the **Payment Reconciliation** FastTab, the **Import Lines** field allows you to filter lines within CAMT.054 Payments by transaction type: **All**, **Credit**, or **Debit**. These filtering options can be configured on the Banking Import Setup page or directly on individual Bank Account cards, giving you flexibility in selecting which transactions to import.

8. On the **Direct Debit Return** FastTab, you can configure how the system should respond to return direct debits. The following fields are available:

   | Field                                       | Description                                                  |
   | ------------------------------------------- | ------------------------------------------------------------ |
   | Direct Debit Return Matching                | Enable this to allow the system to detect and match returned direct debit transactions during bank import. |
   | Default Direct Debit Return Processing Type | Choose how matched return direct debits should be processed by default:<ul><li>**Apply to original payment** – unapplies the original invoice and payment, then applies the return transaction in the reconciliation. You can optionally set the invoice **On Hold**.</li><li>**Reverse original payment** – reverses the entire payment using either the original posting date or the bank statement date. The reversed entry is automatically posted and applied.</li><li>**Apply to account** – leaves the original transaction unchanged and posts the return as an on-account entry.</li></ul> |
   | Direct Debit Return Processing Method       | Select **Manual** to process returns manually, or **Automatic** to process them automatically during the regular matching routine. |
   | On Hold                                     | Automatically sets the invoice to **On Hold** when a return reopens it - only applicable for the **Apply to original payment** or **Reverse original payment** options. |
   | Reverse Posting Date                        | If you selected **Reverse original payment**, you can use the **Reverse Posting Date** field to determine the date used for the reversal. Options are: **Statement Date** and **Posting Date**. |

   

   
