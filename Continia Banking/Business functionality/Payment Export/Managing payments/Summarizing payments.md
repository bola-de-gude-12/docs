---
title: Summarizing Payments in Continia Banking
date: 01-10-2024
description: Learn how to set up payment summarization. 
id: CB-24
lang: en
---

# Summarizing payments

Continia Banking provides an efficient solution for managing multiple outstanding payments. Through its summarizing function, you can consolidate two or more due ledger entries into a single payment, simplifying payment processes significantly. This feature can be particularly beneficial if the bank charge a fee for each payment line.

When the option to summarize payment lines on the vendor card and payment journal setup is enabled, the system automatically consolidates payments per vendor when making payment suggestions in the journal. It's important to note that certain limitations prevent the combination of all entries in a summarized payment. For payments to be consolidated:

- The entries must share the exact due date.
- The entries must be related to the same vendor, customer, or employee.
- The entries must be in the same currency.

## To set up summarization on the payment journal

From the payment journal, you can access the **Payment Summarizing Setup** page, which helps you control how payment summarization occurs and how to consolidate multiple payments efficiently. 

To set up summarization:

1. Search ({{search}}) for and select **Payment Journal**.
2. On the action bar, select **Related** > **Payments** > **Payment Summarizing Setup**.
3. On the **General** FastTab, you can set up how to consolidate ledger entries on date and dimensions:
   * **Date Deviation** - when consolidating payments, due dates on ledger entries usually need to match for summarization to happen. However, the Date Deviation field introduces flexibility as it enables users to input a date formula, which controls the allowed deviation in due dates for summarization to occur. For example, if you have two invoices due with dates two days apart, they might not be summarized by default. But these entries can be consolidated by setting up a formula such as "2D” (indicating a deviation of 2 days). The system will recognize them for summarization even with a slight date difference. It summarizes to be paid on the first of the two days. 
   * **By Dimension** - usually, dimensions are reset during summarization, but this feature enables users to specify specific dimensions that must match for consolidation. These dimensions can represent different aspects of a transaction, such as departments, projects, locations, or cost centers within an organization. By summarizing payments by dimension, you can group ledger entries with similar dimension values. For example, if you have different cost centers and want to summarize payments specific to each cost center, you select the cost center on the Dimension Selection page.
4. On the **Entry types that must not be summarized** FastTab, you have the option to exclude specific ledger entries from the summarization routine:
   * **Exclude Credit Memos** - enable to exclude credit memos from the summarization routine. In regular payment runs, credit memos, which are often used for refunds or adjustments, may not be required. Keeping credit memos separate prevents confusion and errors in accounting and gives accounting full manual control of when to pay and when to avoid overpaying. The options are: 
     * **Vendor-specific** - if selected, the summarizing routine is determined by the vendor card setup.
     * **No** - summarization is not executed, regardless of the vendor card's setup. 
     * **All** - all entries will be excluded from the summarizing routine, irrespective of the vendor card's setup.
   * **Exclude Refunds** - enable to exclude refunds from the summarization routine. Refunds or credit memos often represent unique transactions that require specific attention. They might result from returned goods, adjustments, or other special circumstances. By handling them separately, you make sure that these transactions are properly reviewed and processed to avoid overpayment. See the different options and their outcome in the description of the Exclude Credit Memos field. 
   * **Exclude Payments** - enable to exclude payments from the summarization routine. You can choose to exclude certain payments from summarization for various reasons, such as maintaining clarity or excluding complex transactions that require individual attention to ensure accuracy. See the different options and their outcome in the description of the Exclude Credit Memos field. 
5. On the **Fields that require matching values** FastTab, select fields where you can instruct the system to ensure specific values match before allowing summarization:
   * **Credit Memo Date**:
     * If enabled - the date on the credit memo must have the same value as the other entries before summarizing is allowed. 
     * If disabled - ledger entries are consolidated without considering the date on the credit memo, simplifying the summarization process without regard to specific dates.

## To enable summarization on the Vendor, Customer, or Employee card

To enable summarization, a few setup options are available on the Vendor, Customer, and Employee card.

> [!IMPORTANT]
>
> For the summarization details on the vendor card to take effect, the respective fields on the **Pmt. Summarizing Setup** page must be set to **Vendor-specific**. See the [To set up summarization on the payment journal](#to-set-up-summarization-on-the-payment-journal) section for more details.

To enable summarization on the Vendor, Customer, or Employee card:

1. Search ({{search}}) for and select **Vendors, Customers, or Employees**.
2. Open the card you want to set up summarization for. 
3. On the card, on the **Payments** FastTab, there are several fields to help decide whether to summarize payments and what to exclude:
   * **Allow Summarizing Payments** - enable to allow summarization for this vendor, customer, or employee when creating payment suggestions.
   * **Exclude Credit Memos When Summarizing Payments** - enable to exclude credit memos from the summarization routine. 
   * **Exclude Refunds When Summarizing Payments** - enable to exclude refunds from the summarization routine. Refunds or credit memos often represent unique transactions that require specific attention. They might result from returned goods, adjustments, or other special circumstances.
   * **Exclude Payments When Summarizing Payments** - enable to exclude payments from the summarization routine. You can choose to exclude certain payments from summarization for various reasons, such as maintaining clarity or excluding complex transactions that require individual attention to ensure accuracy. 