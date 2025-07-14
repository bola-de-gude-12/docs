---
title: Continia Banking Supported Bank Files
description: Information about the Continia Banking Supported Bank Files
date: 01-10-2024
id: CB-49
lang: en
---

# Continia Banking supported bank files

Continia Banking supports various file types for exporting and importing data between Business Central and your bank. This article outlines the supported file formats and their implications, noting that availability and requirements may vary by bank. For information about which file formats are supported by your bank, go to the article dedicated to the bank. 

## View communication settings

For details on the communication settings for a bank account, you can view the Bank Account Communication Setup page.

To open the Bank Account Communication Setup page for a bank account:

1. Open the Bank Account Card, and on the action bar select **Related** > **Communication Setup**.
2. On the **Bank Account Communication Setup** page, you can now view the supported file types for the different transaction types. 
3. In the **Enabled** column, you have the option to enable or disable the file type. 
4. In the **Transfer** column, you can specify the method of transfer - direct or manual.

When creating an agreement with your bank, some banks will ask you to specify in which format you want to send payments to the bank. 

> [!NOTE]
>
> Your bank may require subscriptions or purchases for certain files. Contact your bank to learn more about their terms and conditions regarding file transfers. Additionally, the information imported into Business Central from banks may vary between institutions.

## Supported files

Refer to the table below for a list of files supported by Continia Banking. For further details about each file format, select the name. 

| File format<a href="#footnote-1"><sup>1</sup></a>            | To                                                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| [ISO PAIN.001](#iso-pain001-and-iso-pain002-first-edition)   | Send payments to your bank from the payment journal and import the status into the payment journal. |
| [ISO PAIN.002 (first edition)](#iso-pain001-and-iso-pain002-first-edition) | Send payments to your bank from the payment journal and import the status into the payment journal. |
| [ISO PAIN.002 (second edition)](#iso-pain002-second-edition) | Import the status into the payment journal.                  |
| [ISO PAIN.008](#iso-pain008)                                 | Send SEPA Direct Debit collections to your bank. Only available in the DACH region. |
| [ISO CAMT.052](#iso-camt052)                                 | Update status into the payment journal.                      |
| [ISO CAMT.053 Standard](#iso-camt053-standard-and-extended)  | Reconcile bank statements and import payments.               |
| [ISO CAMT.053 Extended](#iso-camt053-standard-and-extended)  | Reconcile bank statements and import payments.               |
| [ISO CAMT.054D](#iso-camt054d)                               | Update status in the payment journal.                        |
| [ISO CAMT.054C](#iso-camt054c)                               | Import payments into the cash receipts journal.              |
| [ISO CAMT.054](#iso-camt054)                                 | Import payments into the cash receipts journal and update status in the payment journal. |
| [PSD2 API](#psd2-api)                                        | Send payments to your bank and reconcile bank statements and import payments. |
| [MT940](#mt940)                                              | Reconcile bank statements and import payments.               |
| [PBS-sector](#pbs-sector)                                    | Import NETS PBS FIK (DK) customer payments in the cash receipt journal. |

 <small style>

 <div class="footnotes">
   <hr />
   <ol>
     <li id="footnote-1">One file order per account per day applies to all file orders.</li>
   </ol>
 </div>
 </small>



## ISO PAIN.001 and ISO PAIN.002 (first edition)

The ISO PAIN.001 payment file is either automatically sent to the bank by Continia Banking via Transmit (direct communication) or exported for manual upload (manual communication). The bank then returns the ISO PAIN.002 file as a status update in two editions: the first confirms receipt and validation, while the second validates each payment line. Continia Banking auto-imports the first edition after a successful transfer (direct communication) and imports the second edition when you select Update status on the payment journal. The Status field on payment lines in the journal is updated as follows:
- **Exported to file** - exported manually; final status for manual communication.

- **Sent to online** - sent via direct communication and being processed.

- **Sent to bank** - sent from online to the bank.

- **Rejected** - rejected by the bank; use **Payment File Errors** to identify and fix issues.

  

## ISO PAIN.002 (second edition)
The ISO PAIN.002 file is sent by the bank in two editions. The first confirms receipt and validation, while the second is sent after each payment line is validated. When you select **Update Status** in the payment journal, Continia Banking imports the second edition if available. The second edition of the ISO PAIN.002 file updates the **Status** field on payment lines in the payment journal with the following results:
- **Awaiting** - the payment is awaiting approval from a second approver in the bank.
- **Rejected** - the payment has been rejected by the second approver or the bank. Use the Payment File Errors function to identify and fix errors or contact the second approver.
- **Paid** - the payment has been completed by the bank.

## ISO PAIN.008
Continia Banking Direct Debit uses this file when you export a Direct Debit Collection Entries to your bank. Only available in the DACH region.

## ISO CAMT.052
This is your intraday information report, providing a near real-time view of your account(s). ISO CAMT.052 is mostly used by banks that do not send the updated ISO PAIN.002 second edition but instead offer this file. When you select **Update status** in the payment journal, Continia Banking automatically searches for and imports the file if available. You can also manually import the file. The ISO CAMT.052 file updates the **Status** field on payment lines in the payment journal in the same way as the ISO PAIN.002 (second edition).

Additional benefits of using ISO CAMT.052:

- **Payment date change** - if the bank changes the payment date, it is automatically updated on the payment line in the payment journal, preventing incorrect posting dates.
- **Amount adjusted** - the payment line amount is adjusted to reflect currency differences. If a payment is made in a foreign currency, the exchange rate used by the bank is automatically updated in Business Central, ensuring accurate LCY amounts and facilitating bank statement reconciliation.

## ISO CAMT.054D
This is the final confirmation that outgoing payments (debits) have been made. Known as "DEBMUL," the file contains the day's completed outgoing payments, including changes in exchange rates on foreign payments. When you select **Update status** in the payment journal, Continia Banking automatically searches for and imports the file if available. The ISO CAMT.054D file updates the **Status** field on payment lines in the payment journal in the same way as the ISO PAIN.002 (second edition).

Additional benefits of using ISO CAMT.054D:

- **Payment date change** - if the bank changes the payment date, it is automatically updated on the payment line in the payment journal, preventing incorrect posting dates.
- **Amount adjusted** - the payment line amount is adjusted to reflect currency differences. If a payment is made in a foreign currency, the exchange rate used by the bank is automatically updated in Business Central, ensuring accurate LCY amounts and facilitating bank statement reconciliation.

## ISO CAMT.054C
This is the final confirmation that customer payments (credits) have been made. The file contains the day's completed incoming payments, including deposits via manual account transfers and OCR payments such as FIK, GIK, KID, or OCR payments. When you select **Import Payments** in the cash receipts journal, Continia Banking automatically searches for and imports the file if available. Manual import is also possible. The ISO CAMT.054C file is used by Continia Banking to import customer payments into the cash receipt journal, including both manual account transfers and OCR payments.

> [!TIP]
>
> We recommend importing the ISO CAMT.054C file before the ISO CAMT.053 file, as it contains extended information on all deposits, including associated notifications. This helps Continia Banking match the correct payment/invoice in Business Central.

> [!NOTE]
>
> The file must contain details of each payment (specified or detailed). Sum files are not supported, as they do not indicate who conducted the payment.

## ISO CAMT.054
This file can contain both statuses for the payment journal and information about customer payments to the cash receipt journal. When the CAMT.054 file is received in Business Central, Continia Banking will automatically allocate the payment information into the cash receipt journal and the payment journal. 

To read more about the data in the file, please see the sections CAMT.054D for information about updating status in the payment journal, and CAMT.054C for information about importing payments into the cash receipts journal.

## ISO CAMT.053 Standard and Extended
Provides detailed and structured information on all entries booked to your account for the previous day, including extended information on all deposits and withdrawals with associated notifications. This extended information helps Continia Banking accurately match and offset the correct entry/invoice and set the correct posting description in the reconciliation journal.

Bank account statement types:

* **ISO CAMT.053 Standard** - the standard bank account statement offered by most banks:
    - Provides detailed information on all entries booked to your account for the previous day, including deposits and withdrawals with notifications.
    - May require some manual matching of deposits due to a lack of notification information in some banks.
    - Recommended for customers with very few deposits.


- **ISO CAMT.053E Extended** - the extended bank account statement offered by some banks:
  - Provides detailed and structured information on all entries, including extended information on all deposits and withdrawals.
  - Recommended over the standard version if available.

Used for:
- When creating a Bank Account Reconciliation in Business Central, pressing **Import and Match** prompts Continia Banking to search for and import the file automatically. Manual import is also possible.
- The ISO CAMT.053 file helps reconcile bank entries in Business Central with the bank's account statements and create new entries for transactions not registered in Business Central.

Importing ISO CAMT.053 Includes:
- Import and matching of all withdrawals created with Continia Banking due to the Transaction ID.
- Import and matching of new withdrawals not created with Continia Banking using posting rules for fixed expenses.
- Import of new deposits from manual account transfers, matching entries in Business Central, and creating cash receipt lines ready for posting.
- Import of new deposits from OCR payments, matching entries in Business Central, and creating cash receipt lines ready for posting.
  

Because the PSD2 directive does not set specific requirements for file formats, security protocols and so on, we can't describe the integration in detail. We recommend you ask your PSD2 service provider for details. Unresolved entries, such as those with incorrect invoice numbers, can be transferred to a journal for manual posting proposals.

Not used for:
- ISO CAMT.053, either standard or extended, is not used for updating the status of outgoing payments, even if they appear in the payment journal. For manual communication, the status of outgoing payments must be updated manually.

> [!TIP]
>
> Ordering ISO CAMT.053E usually eliminates the need for ISO CAMT.054C files, as it contains all payment information. However, it must be ordered daily to import all new payments.
>
> It is still necessary to order ISO CAMT.054D, as the information in ISO CAMT.053E cannot update the status of outgoing payments in the payment journal.

## PSD2 API
Due to the absence of specific requirements for file formats and security protocols in the PSD2 directive, we are unable to provide a detailed explanation of the integration. We recommend you ask your PSD2 service provider for further details.

## MT940

MT940 is a format used by the [SWIFT](https://en.wikipedia.org/wiki/SWIFT) network to send and receive end-of-day [bank account statements](https://en.wikipedia.org/wiki/Bank_account_statement).

What's in the file:

* Bank account statement with a detailed description of all yesterday's transactions. One file is ordered per account.

Currently this format is not supported but it will be on short notice

<style>
 .content table tr td:nth-child(1) {
 width: 225px;
 }
 .content table tr td:nth-child(2) {
 width: 575px;
 }
</style>
