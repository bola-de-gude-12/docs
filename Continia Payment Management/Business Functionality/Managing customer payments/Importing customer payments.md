---
title: Importing customer payments
description: How to import customer payments to the cash receipt journal
date: 19-05-2021
id: PM-96
lang: en
---

# Importing Customer Payments

You can use Payment Management to manage the import and application of customer payments. Use the cash receipt journal to register customer payments from bank account transactions and third-party payments. When the payments have been registered and posted in the cash receipt journal, you can reconcile your bank accounts, which requires applying the incoming payments to the customer ledger entries to close the sales invoices.

Depending on your agreement with the bank, you can import the payments using either manual or direct communication. 

## Prerequisites

The following prerequisites are required for Payment Management to manage customer payments:

- **Activate Payment Management** - Payment Management must have been activated on the cash receipt journal. To check this, select the Batch Name at the header of the cash receipt journal. On the  **General Journal Batches** page, check whether the **Payment Management Journal** column is selected. 

- **A payment card with OCR/FIK reference** - a payment card must have been enclosed with the invoices, reminders, interest notes, or account statements for Payment Management to interpret the customer payments. When a customer uses the payment card, the reference included on the card will follow the revenue from the customer to the bank and then back to the Business Central platform as the payment is imported to the cash receipt journal. Payment Management will use the information in the OCR string to import, apply, and post the payments. See the [Using the OCR reference interface](@PM-10) article for more details.

- **A balance account** - you must define a balance account on the cash receipt journal. The bank account must have been set up with Payment Management and **Bank Reg. No**. and **Bank Account No**. must have been defined for the bank account. We recommend adding the IBAN and SWIFT numbers - especially when importing payments using direct communication. For more information on how to set up bank accounts with Payment Management, see [Setting up bank accounts](@PM-3).


## To import customer payments

You can use the Cash Receipt journal for both customer payments from the bank and file imports from third-party Payment Service Providers (PSPs). 

To import payments:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Cash Receipt Journals**, then select the related link. 
2. Open the relevant journal, and select **Home** > **Import Payments**. If you are using direct communication, payments available in the bank will automatically be imported. If you use manual communication, you must select the file to be imported from your local desk.
3. On the **Import Payments** dialog box, depending on whether you are importing customer payments from the bank or PSP payments, you can specify the following:
   * **Journal Date** - specifies which date to use. The options are: **Cash Receipt Date** and **Posting Date**.
   * **Journal Description** - optional field. You can enter a description to use on all journal lines. If you do not enter a description, the description from the payment is used.
   * **Document No.** - specifies the document number to use. The default value is the next document number from the number series of the journal.
   * **New Document No. Per** - specifies a description to use on all journal lines. If you do not specify a description, the description from the payment is used. The options are **Journal** and **Line**.
   * **Customer Application Method** - specifies if you want to apply payments for all customers or exclude customers with the application method Apply to Oldest.
   * **Create Balancing Account Lines Per Day** - specifies if you want the balancing account lines to be created per posting date. With this option set, all the payments will be generated as **Account Type:** *Customer* in the cash receipt journal, and one summarized balance account line covering all the payments of the same date will be generated as **Account Type:** *Bank Account*.
   * **PSP Agreement** - if you import payments from a third-party provider,](@PM-299) you can select the [PSP agreement](@PM-298).

When the files are, imported, Payment Management will automatically apply the payments that can be applied using the information in the payment notification received from the bank.

## To import payments automatically

You can set up Payment Management to automatically import payments to the cash receipt journal. This way, you don't have to initiate the file import manually. A [job queue](@PM-324) will manage the essence in Business Central, where you can define how often the service should check for available bank files. 

To automatically import the payments that were made to your bank:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Bank Accounts**, then select the related link. 
2. Select the bank account card.
3. On the action bar, select **Actions** > **Enable Payment Receipt Import Job Queue**. The payments are now imported, created as journal lines, and applied automatically if possible.

## To apply imported payments

When generating the cash receipt lines, Payment Management will use the information from the payment notification to identify the customer to whom a payment belongs. 

To apply the imported payments:

* On the action bar, select **Home** > **Apply Imported Payments**.

Payment Management inserts an Applies-to Docs for payments on which the customer or invoice number is identified. No**. 

The application ID is not inserted if:

- On the customer card, if for the **Application Method** field, the **Apply to Oldest** option is selected:  
  - The application ID is not inserted for entries that don't make up for a unique match.
  - The application ID is not inserted if the amount paid does not match the balance of the invoice.

- If the entry has already been applied. In this case, it may be necessary to set the **Applies-to Docs. No** manually.

- If a line applies multiple documents, the **Applies-to ID** is set.

## To reapply imported payments

You can re-run the matching of journal lines without having to delete the lines and import them again.

To reapply imported payments:

* Select the lines in the journal you want to re-run the matching for, and on the action bar, select **Home** > **Apply Imported Payments**.



## To access information about a payment

While looking into a specific payment, various information will be available directly on the payment line and in the info box located on the right side of the payment journal. You can dive into more detailed information by selecting the information displayed in *green text*. The payment line covers information about the basic journal line details and document files.

Payment Management adds information about notifications if a notification is attached to the payment. 



## To access statistics

You can also view the cash receipt journal's statistics page for an overview of the total amounts for the different customers, bank accounts, currency codes, and G/L accounts. 

To open the journal statistics:

* Open the cash receipt journal, and on the action bar, select **Actions** > **Journal Statistics**. A matrix view shows you the applied amounts based on lines and sorted by date. 



## Common errors

If the import of payment lines did not turn out as expected, look into the following areas:

- Make sure that the bank account number in the file matches the bank account number stated on the cash receipt journal. 

- For bank accounts under BankConnect, the account number must be ten digits - you should prefix it with 0 if there are fewer than ten digits in the bank account number.

- Make sure the cash receipt journal has been set up with Payment Management.

- Verify that there are files available for import at the bank. 

- Look into the data imported from the bank on the page **Bank Export Data**:

  - CREMUL files always consist of a header line and several payment lines. If the bank can't be identified during import, the header is created without corresponding payment lines, and the import of the payment lines will be blocked. The solution for this issue is to select the header line in the Bank Export Data and choose the **Remove Imported To Company** action in the action bar. Investigate if the bank account information in the file matches the bank account information in Business Central, and try to import the file again. 

  - If lines are marked as **Imported To Company** by mistake, they can't be imported again. On the action bar, select **Actions** >  **Remove Imported To Company**, and try to import the file again.

    

## Related information

[Setting up customer application rules](@PM-174)
