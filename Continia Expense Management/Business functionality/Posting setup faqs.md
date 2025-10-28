---
title: Posting setup FAQs
date: 17-10-2025
description: Learn what kind of posting setup fits your needs
id: EM-378
lang: en
---
# Posting setup FAQs

See which kind of posting setup fits your company's and user's needs.

## What kind of posting setup do I need?

Do you want to create a purchase invoice or have postings as ledger entries in the General Journal lines? Posting with purchase invoices is useful when the expense bank account also needs to be a vendor, (though, you cannot do this as a ledger entry).

To find these options:

*  Search for {{search}} **Expense Management**, under **Purchase Doc. Posting Setup**. By default this will post Gen. Journal lines.

>[!NOTE]
>
>**Purchase Doc. Posting Setup** is hidden by default. If this is the case for you, then under **General** > **Application Areas**, in the **Expense Report** field, select **Disabled** from the dropdown menu.

## Do I group documents or post them individually?

You can use single documents or group them on an expense report when posting journal lines, see [Group employee and vendor ledger entries in expense reports or by document type](@EM-300) They are posted with the same posting date, though the document date is the date used for each individual document. This is helpful if you want to register everything from a trip, for example. You can add both the mileage and expense to one expense report. Moreover, if you've used a purchase invoice setup, then the documents will be grouped per user, by default. 

Expense reports cannot be combined with the Purchase Invoice Setup. For more information about posting on expense types, see [Setting up expense types](@EM-41)

To use this functionality:

* Search for {{search}} **Expense Management Setup** and toggle **Enable Expense Report** to on.

## When do I post bank transactions when importing them?

As a best practice, if you’re using expense reports, then you must import the bank transactions immediately. Then you ensure consistency between the imported bank transactions and the posted expenses. After the bank transactions are imported they are immediately posted against an intermediate GL Account that is specified in the Intermediate Bank Account. 

This is helpful when carrying out reconciliations, and checking if all the bank transactions match with the posting of the expenses. When you have posted all of the documents, the balance on the Intermediate Bank Account is expected to be 0 (zero).

To use this functionality:

* Search for {{search}} **Expense Management Setup** and set the **Post Bank Transactions on Import** to true.

## Which currency do I post the expenses in?

Do you post expenses in the currency they were made or in the local currency of the system?

You can post expenses in the currency where the purchase was made, not just in the local currency. If the bank account has a currency specified, it always posts in the currency of the bank account. Therefore, the expenses must be posted in that specific currency.

To post in the expense currency:

* Search for {{search}} **Expense Management Setup** and use **Post in Expense Currency**.

## Related information

To dive a little deeper into posting with Expense Management, see:

[Posting expenses](@EM-11)
[Posting mileage expenses](@EM-12)
[Posting per diem expenses](@EM-13)
[Use a vendor as a porting account type on credit card transactions](@EM-248)
[Posting project expenses in Business Central independently of the reimbursement method](@EM-284)
[Editing posting in the Web Approval Portal](@EM-321)
[Bank transaction posting description configuration](@EM-335)