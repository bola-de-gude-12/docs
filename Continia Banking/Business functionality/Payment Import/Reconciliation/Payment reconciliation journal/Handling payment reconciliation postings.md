---
title: Handling payment reconciliation postings
description: Learn more about the different options for posting payment reconciliation				
date: 01-10-2024	
id: CB-105
lang: en
---

# Handling Payment Reconciliation Journal Postings

To ensure efficient payment reconciliation journal postings, you can enable specific settings that control how entries are posted. Key settings include:

* **Post Sum per Posting Date** - go to the [Banking Import Settings](@CB-14) page to activating this option. When enabled, it results in a single bank account entry for the entire bank statement, simplifying reconciliation. If the statement contains multiple posting dates, the system creates a sum posting for each date to maintain consistency. Additionally, the system posts a total amount for the statement.
* **Post Payments Options** - on the Payment Reconciliation Journal page, on the action bar, select **Home** and then select one of the options for posting payments:
  * **Post Payments Only** - leaves all bank account entries open after posting.
  * **Post Payments and Reconcile Bank Account** - closes all bank account entries after posting.
   - **Preview Postings** - provides a preview of the postings, listing the related entries and the number of entries.
* **Journal Template and Batch Name Requirement** - you can mandate the use of a template and batch name for posting by enabling **Journal Templ. Name Mandatory** in the General Ledger Setup. If you want to use this option, you must make sure the **Bank Acc. Recon. Template Name** and **Bank Acc. Recon. Batch Name** are filled in.
* **Force Document Balance** - the **Force Doc. Balance** setting in the General Journal templates is enabled by default and makes sure that the document is balanced before posting. If the document is not balanced, an error occurs unless you disable **Force Doc. Balance**.

