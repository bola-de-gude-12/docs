---
title: Handling fees
date: 13-07-2023
description:
id: EM-163
lang: en
---

# Handling Fees

Banks commonly charge yearly or transaction fees for purchases made abroad in financial transactions. These fees can often become mixed in with regular expense and purchase transactions, making it challenging to distinguish them. 

Expense Management can exclude specific transactions from being posted by utilizing matching rules and assigning them to a designated expense type. This feature allows transactions to be identified based on specific keywords, and Expense Management will exclude them from the posting process.

This functionality is particularly valuable when dealing with fee-related transactions. Credit card fees, for instance, are not considered expenses, and the bookkeeper may prefer to exclude them temporarily and handle them separately upon receiving the invoices from credit card providers.

Continia Expense Management provides two methods to exclude fees:

1. Exclude them from Continia Expense Management and manage them manually in the Finance department.
2. Configure them not to require attachments and set up company policies to streamline the handling process automatically.

## To exclude specific transactions by utilizing matching rules

To automatically exclude fees, you can create a dedicated expense type specifically for fees and configure it to exclude transactions. Additionally, you can enable the **Hide from Expense** user feature to prevent users from inadvertently creating expenses for fees.

To implement this, you will first need to identify the fee. For instance, you can search for text containing the word "fee" or an Entry ID with a unique identifier. Here are a couple of examples:

* **Mastercard Smartdata fees** - these fees are labeled as *Financial Adjustments*; you can filter based on that specific value or the entry type 5900.
* **Danske Bank Telekort fees** - fees, including credit card charges from purchases outside the EU, are booked under entry type 5100. Additionally, Danske Bank sends obsolete transactions with a specific Card Number that can be used as a filter criterion.

To exclude fees automatically:

1. Select the {{search}} icon, enter **Expense Types**, and then select the related link.

2. On the action bar, select **New** to add an expense type specifically for fees. Add a name, description and make sure to select the **Exclude Transactions** column checkbox. For example:
   * **Code** - specify the code, for example, *FEE*.
   * **Description** - add a description. For example, *Fees and charges*.
   * **Search Name** - add a search name. For example, *Fees and charges*.
   * **Hide from Expense User** - when selected, the expense type is hidden in the app and portal. For example, when you want the fee to be processed by bookkeepers only.
   * **Exclude Transactions** - when selected, the bank transaction will not create expenses. For this example, select the checkbox.

3. To identify the fee, you must add a rule. Select the {{search}} icon, enter **Bank Transactions**, and then select the related link.

4. On the action bar, select **Mapping Rules**. 

5. On the **Bank Mapping Rules** page, you can add a new rule using an identifier to find the fee. For example, to rule out the Dansk Bank Telekort fees, add:

   * **Rule No.** - add the rule number to determine when to apply the rule.

   * **Field No.** - add the field number to apply the rule on.

   * **Field Name** - specifies the name of the field selected for the rule.

   * **Value** - add the value for which the rule must apply. In this example, 5100.

   * **Expense Type Code** - add FEE to categorize the expense.

When an expense matches the search term *Fee* or the designated rule for the entry type, it will be automatically assigned the expense type **Fee** and excluded from further processing within the system. Although it will remain in the Bank transactions table, it will be hidden from view through the pre-set filter, and no postings have been generated in the General Ledger for these excluded transactions. 

To view the excluded transactions:

1. Select the {{search}} icon, enter **Bank Transactions**, and then select the related link.

2. On the action bar, select the **Show filter pane**.

3. On the Views panel, navigate to **Exclude Entry** and set the drop-down box to **No**.



## To exclude fees by making attachments optional

The fee handling process can be automatically streamlined by adjusting the settings to eliminate the requirement for attachments and implementing company policies.

To exclude fees using optional attachments:

1. Select the {{search}} icon, enter **Expense Types**, and then select the related link.

2. On the action bar, select **New** to add an expense type specifically for fees. Add a name, description, and make sure to set the **Attachment** column to *Optional*. For example:
   * **Code** - specify the code, for example, *FEES TO POST*.
   * **Description** - add a description. For example, *Fees to post*.
   * **Search Name** - add a search name. For example, *Fees to post*.
   * **Attachment** - specifies if the company requires an attachment. The options are: *Recommended*, *Mandatory*, and *Optional*. To exclude fees automatically, set this to *Optional*.
   * **Hide from Expense User** - select this option if you want to prevent users from accidentally using it.

3. Select the {{search}} icon, enter **Company Policies**, and then select the related link.

4. Add a new policy to approve expenses below a certain amount automatically. For example:
   * **User Type** - User group
   * **User Code** - INT
   * **Action** - Automatically approve documents below 1000 euros.
   * **Amount** - 1,000, 00

 4. Select the {{search}} icon, enter **Bank Transactions**, and then select the related link.

 5. On the action bar, select **Mapping Rules**. 

7. On the **Bank Mapping Rules** page, you can add a new rule using an identifier to find the fee. For example, to rule out the Dansk Bank Telekort fees, add:

   * **Rule No.** - add the rule number to determine when to apply the rule.

   * **Field No.** - add the field number to apply the rule on.

   * **Field Name** - specifies the name of the field selected for the rule.

   * **Value** - add the value for which the rule must apply. In this example, *Fee*.

   * **Expense Type Code** - add FEES TO POST to categorize the expense.


Expense Management will scan and match all bank transactions based on the keyword *Fee* or any other specified entry type rule. Once matched, the transactions will be assigned the Expense type, such as the FEES TO POST expense type. As you indicated, an attachment is not required, so these expenses will not be sent to the Expense user.

Subsequently, the configured Company Policy will be triggered, and both the expense and the bank transaction will be transitioned to the *Released* status, signifying their readiness for posting.

