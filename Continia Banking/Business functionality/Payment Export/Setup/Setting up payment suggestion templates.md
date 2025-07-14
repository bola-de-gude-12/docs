---
title: Setting up payment suggestion templates in Continia Banking
description: Save payment suggestion settings in templates and use a job queue to run it. 
date: 01-10-2024	
id: CB-89
lang: en
---
# Setting up payment suggestion templates

Saving specific settings for payment suggestions in templates benefits companies that work with multiple bookkeepers. Imagine a scenario where one bookkeeper manages international payments, another handles local payments, and a third oversees direct debits. Each bookkeeper requires distinct filters for their payment suggestions. By saving these specific settings, bookkeepers gain easy access to predefined sets, enabling them to focus on their specific responsibilities efficiently and effectively.

To add a payment suggestion template:

1. Search ({{search}}) for and select **Payment suggestion templates**. Alternatively, create a template directly from a payment proposal. 
2. On the **Payment Suggestion Templates** page, select the account type and on the action bar, select **Set Suggestion Filters**. Alternatively, select **New** and select the account type, add a name and a description.
3. The **Journal Template Name** and **Journal Batch Name** fields determine where you can find the payment suggestions once the template is applied. 
4. You can now define other settings for your template. 
   - **Description Template, Remittance Information Template, Remittance Reference Template, Sender Reference Template** - these fields define templates for journal line descriptions, remittance information, recipient references, and sender references. Continia Banking includes predefined templates on the setup server that eliminate the need to fill out these fields manually, thanks to default settings in the Banking Export Setup. 
   - **Find Payment Discounts** - if selected, available payment discounts are applied.
   - **Payment Discount Application Method** - this setting defines how payment discounts are applied based on the posting date. If you leave the field to blank, discounts will be applied only if the posting date is on or before the payment discount date. If you select *Always apply discount*, discounts will be given regardless of the posting date in relation to the payment discount date. This ensures that the discount is applied even if the payment is made after the payment discount date. This field is only applied if the **Find Payment Discounts** field is enabled.
   - **Include On Hold Entries** - only available when you have **Advanced Payment Suggestion** mode enabled. This field allows you to include entries that are on hold, not just those that are due. This provides an overview of all entries, not only those marked for application.
   - **Include All Entries** - only available when you have **Advanced Payment Suggestion** mode enabled. Enable this field to view all invoices, including those that are not yet due. This flexibility allows you to pay invoices ahead of their due dates when funds are available.
   - **Summarize per Account** - if selected, the batch job consolidates entries into one line per account for each currency in which the account has ledger entries. For example, if a account deals in two currencies, the batch job will create two payment lines in the journal. The applies-to ID field is then used during posting to link these lines to ledger entries. If not selected, the batch job creates one line per invoice.
   - **Including Backlog** - if selected, accounts with an overpayment (for example,  more credit memos than invoices)—typically excluded from payment proposals since no payment is required—will be included in the suggestions. An overpayment situation arises when the credits applied to an account exceed the charges. For example, if an account has $1,000 in credit memos but only $800 in invoices, the account would show an overpayment of $200. Normally, such accounts would not be included in payment proposals, since no payment is needed. However, if you wish to include these accounts, select the Including Backlog checkbox.
   - **Include Recurring Journal Entries** - only available when you have **Advanced Payment Suggestion** mode enabled. This field is useful for recurring payments such as monthly office rent. For example, if you have a contract requiring monthly payments.
   - **Use for Job Queue** - select to enable a job queue for this payment suggestion template. 
   - **Job Queue ID** - when the checkbox for **Use for Job Queue** is selected, the **Job** Queue ID displays the ID of the job queue entry. 
     To schedule templates at different intervals, you must create additional job queue entries and select the relevant ID in the **Job Queue ID** field. For each job queue entry, on the **Job Queue Entry Card**, make sure that the CTS-PE Create Pmt. Sugg. JQ codeunit is executed by setting:
     - **Object Type** to Codeunit
     - **Object ID** to 71553881.
   >[!TIP]
   >For general information on how to work with job queues, refer to the [Microsoft documentation](https://learn.microsoft.com/en-gb/dynamics365/business-central/admin-job-queues-schedule-tasks).
5. To apply the filter on the action bar, select **Create Suggestion** to initiate the Payment Suggestion Report, where all information from the template will be applied on the request page.
