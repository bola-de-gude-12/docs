---
title: Handling fees
date: 22-07-2023
description:
id: EM-163
lang: en
---

# Handling fees

Banks commonly charge yearly or transaction fees for purchases made abroad in financial transactions. These fees can often become mixed in with regular expense and purchase transactions, making it challenging to distinguish them. 

Expense Management can help with this by excluding specific transactions from being posted by utilizing matching rules and assigning them to a designated expense type. This feature allows transactions to be identified based on specific keywords, and Expense Management then excludes those transactions from the posting process.

This functionality is particularly valuable when dealing with fee-related transactions. Credit card fees, for instance, are not considered expenses, and the bookkeeper may prefer to exclude them temporarily and handle them separately upon receiving the invoices from credit card providers.

Continia Expense Management provides two methods to exclude such fees:

1. You can exclude them from Continia Expense Management and manage them manually in your Finance department.
2. You can configure them not to require attachments and set up company policies to streamline the handling process automatically.

## Exclude specific transactions 

To automatically exclude fees, you can create a dedicated expense type specifically for fees and configure it to exclude transactions. Additionally, you can enable the **Hide from Expense** user feature to prevent users from inadvertently creating expenses for fees.

To implement this, you must first identify the fee. For instance, you can search for text containing the word "fee" or an Entry ID with a unique identifier. Here are a couple of examples:

* **Mastercard Smartdata fees** - these fees are labeled "Financial Adjustments"; you can filter based on that specific value or the entry type 5900.
* **Danske Bank Telekort fees** - these are fees, including credit card charges from purchases outside the EU, are booked under entry type 5100. Additionally, Danske Bank sends obsolete transactions with a specific Card Number that can be used as a filter criterion.

To exclude fees automatically:

1. Search for {{search}} **Expense Types**.

2. On the action bar, click **New** to add an expense type specifically for fees. 

3. Add a name and description.

4. Select the **Exclude Transactions** column checkbox and fill in the other relevant fields:
   * **Code** - specify the code, for example, FEE.
   * **Description** - add a description. For example, "Fees and charges".
   * **Search Name** - add a search name. For example, "Fees and charges".
   * **Hide from Expense User** - when selected, the expense type is hidden in the app and portal. For example, when you want the fee to be processed by bookkeepers only.
   * **Exclude Transactions** - if you select the checkbox, the bank transaction will not create expenses.

To identify the fee, you must add a rule: 

1. Search for {{search}} **Bank Transactions**.

2. On the action bar, click **Mapping Rules**. 

3. On the **Bank Mapping Rules** page, you can add a new rule using an identifier to find the fee. For example, to omit the Danske Bank Telekort fees, add:

   * **Rule No.** - add a rule number to determine when to apply the rule.

   * **Field No.** - add the field number to apply the rule to.

   * **Field Name** - specify the name of the field selected for the rule.

   * **Value** - add the value for which the rule must apply. In this example, 5100.

   * **Expense Type Code** - add FEE to categorize the expense.

When an expense matches the search term "Fee" or the designated rule for the entry type, it will be automatically assigned the expense type **Fee** and excluded from further processing within the system. Although it remains in the Bank transactions table, it is now hidden from view through the pre-set filter, therefore no postings were generated in the General Ledger for those excluded transactions. 

To view the excluded transactions:

1. Search for {{search}} **Bank Transactions**.

2. On the action bar, click **Show filter pane**.

3. On the Views panel, navigate to **Exclude Entry** and set the drop-down box to **No**.

## Automate the handling fees process

By adjusting the handling fees settings, you can automatically streamline the fee handling process and omit the requirement for attachments and implementing company policies.

To exclude fees using optional attachments:

1. Search for {{search}} **Expense Types**.

2. On the action bar, click **New** to add an expense type specifically for fees. 

3. Add a name, description, and set the **Attachment** column to **Optional**:
   * **Code** - specify the code to use, such as FEES TO POST.
   * **Description** - add a description, such as "Fees to post".
   * **Search Name** - add a search name, such as "Fees to post".
   * **Attachment** - specify if the company requires an attachment. The options are: **Recommended**, **Mandatory**, and **Optional**. To exclude fees automatically, set this to **Optional**.
   * **Hide from Expense User** - select this option if you want to prevent users from accidentally using it.

4. Search for {{search}} **Company Policies**.

5. Add a new policy to approve expenses below a certain amount automatically. For example, a policy to automatically approve expenses under 1000 euros would be:
   * **User Type** - User group
   * **User Code** - INT
   * **Action** - Automatically approve documents below 1000 euros.
   * **Amount** - 1,000, 00

 6. Search for {{search}} **Bank Transactions**.

 7. On the action bar, click **Mapping Rules**. 

8. On the **Bank Mapping Rules** page, you can add a new rule using an identifier to find the fee. For example, to exclude Danske Bank Telekort fees, add:

   * **Rule No.** - add the rule number to determine when to apply the rule.

   * **Field No.** - add the field number to apply the rule to.

   * **Field Name** - specify the name of the field selected for the rule.

   * **Value** - add the value for which the rule must apply (in this example the value is "Fee".

   * **Expense Type Code** - add FEES TO POST to categorize the expense.


Expense Management will then scan and match all bank transactions based on the keyword "Fee", or any other specified entry type rule. After the transactions are matched, they're assigned an Expense type, such as FEES TO POST. As mentioned in step 3, an attachment is not required, therefore the expenses will not be sent to the Expense user.

Subsequently, the configured Company Policy will be triggered, and both the expense and the bank transaction will change to the **Released** status, signifying that they're ready for posting.

