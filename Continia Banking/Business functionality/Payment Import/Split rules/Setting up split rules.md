---
title: Setting up split rules
description: Automate allocating incoming payments over multiple accounts using split rules
date: 07-05-2025
id: CB-216
lang: en
---
# Setting up split rules
Split rules help automate how incoming payments are allocated across multiple accounts based on predefined logic. This can include splitting charges for foreign payments, returned direct debits, or allocating amounts to different cost categories—such as separating insurance and maintenance fees from a leasing contract. By applying Split Rules, you ensure consistent and accurate posting across your financial records.

## To set up a split rule

To define how amounts should be split and where they should be posted:
1. Search ({{search}}) for and select **Banking Import Setup**. 
2. On the action bar, select **Manual Setup** > **Split Rules**. Alternatively, search for Split Rules. 
3. On the **Split Rule** page, on the **General** FastTab, add a new split rule. Alternatively copy and adapt a rule by selecting **Copy Split Rule**. Enter information for the following fields:
   * **Code and Description** - enter a unique code to identify the new rule and provide a meaningful description that explains the purpose of the rule.  
   * **Separators** - make sure that the **Thousand Separator** and **Decimal Separator** are correctly set for your needs. These fields are prefilled based on your regional settings. If necessary, you can adjust the separators by selecting **Show More** for additional options.
4. Add one or more split rule lines. Each line defines:

   * How the amount is calculated (e.g. fixed, percentage)
   * The target account, posting groups, and dimensions
5. In addition to the split rule type-specific fields, there are general fields that apply to all split rules. Some of these fields are mandatory and are marked with an asterisk (*). For more information about these general fields and their function, refer to the [Split rule fields](@CB-234) article.
> [!TIP]
   >
   > If your Split Rule is incomplete, a notification will appear when you open either the **Bank Account Reconciliation** or the **Payment Reconciliation Journal**. You can resolve the issue by selecting **Open Split Rules** to complete the rule.

## To add a split rule based on a fixed amount
* To add a split rule that is based on a fixed amount enter information for the following fields:

  * Split by - from the drop-down, select Fixed Amount.

  * Fixed Amount - enter the specific amount to allocate to this line. 

  * Account No. - select the account to assign to the line when the split rule is applied.

  * Amount type - defines how the split amount is signed relative to the original bank line:
    - **Same sign** – uses the same sign as the bank reconciliation line.
    - **Opposite sign** – reverses the sign of the bank reconciliation line.
    - **Positive** – always splits the amount as positive.
    - **Negative** – always splits the amount as negative.

## To add a split rule based on a search text
This method allows splits based on keywords found in transactions:
   * **Search Text** - in the **Search Text** field, specify the text to search for when the rule is used on the bank account reconciliation lines to identify a match. 
   * **Add Additional Search Texts** - use this action to include multiple search terms.
   * **Search Method** - in the **Search Method** field, specify how the search is performed when looking for the specified search text. The options are:
     - **Exact**: The search text must match all the fields.
     - **From left**: The search text must match the first part of the fields.
     - **From right**: The search text must match the last part of the fields.
     - **Within**: The search text must appear somewhere in the fields.
   * **Search Field Template** - define where to look for the text. For more information, refer to the [Using field templates in Banking Import](@CB-161) article. Multiple fields can be included in the search. If the text matches any field in the template, the rule is applied to bank statement lines or payment reconciliation journal lines.
     - By default, common search field templates are available.
     - To create a new template, select the three dots to open the **Search Field Templates** page, then choose **New**.
     - Enter a **Template Code**, **Template Description**, and define the **Field Selection Text** in this format: `<Table|Field>`.
   * Account Type - select the account type.
   * Account No. - select the account to assign to the line when the split rule is applied.

## To add a split rule based on percentage

This method distributes a percentage of the original amount to one or more accounts:

- Specify the percentage for each target account.
- Each line’s amount is calculated as a percentage of the total and automatically reduces the base line.
- In the **Payment Reconciliation Journal**, go to **Apply Rule** > select the appropriate **Split Rule Code**.
- The original transaction amount remains visible in **Match Details**.

> [!TIP]
> Percentage-based split rules are often combined with search rules. The search rule handles the main transaction, while the split rule manages the distribution of amounts across accounts.

**Example:** 
You lease a car and want to separate the monthly payment:

- **Insurance**: Fixed amount of €50  
- **Maintenance**: 25% of the total  
- **Remaining**: Base amount is reduced accordingly and posted to the leasing account
