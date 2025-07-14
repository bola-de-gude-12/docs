---
title: Set up search exception rules
description: A guide on how to set up search exception rules
date: 14-11-2023
id: PM-372
lang: en
---

# Setting up Search Exception Rules

In the Payment Management bank account reconciliation process, you can use search exception rules to exclude matching on specific accounts, such as vendors or customers, by excluding certain words. This feature enables users to specify IBANs that should be ignored for matching on designated accounts where consolidated customers or vendors share the same IBAN. This helps prevent unintended matches and ensures accurate reconciliation. 

To set up these rules, you can add specific search text to exclude. For instance, if the vendor and the customer are the same and you want to match the customer only, you can exclude the relevant IBANs.

To set up search exception rules:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Search Exception Rules**, then select the related link. Alternatively, on the **Bank Account Reconciliation** page, go to **Rules** > **Search Exception Rules**.
1. In the action bar, select **New** to create a new reconciliation rule.
1. In the **Search Term** column, enter the text to be searched for. For example, enter an IBAN that should be ignored for matching.
1. In the **Account Type** column, specify the account type for which the exclusion should apply.
1. In **Account No.** column, specify the account number for the related account.
1. After setting up reconciliation rules, you can close the page. 



