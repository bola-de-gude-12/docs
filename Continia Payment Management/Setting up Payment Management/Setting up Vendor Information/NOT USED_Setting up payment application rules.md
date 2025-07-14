---
title: Setting up payment application rules
description: Set up payment application rules to identify the vendor who generated a payment in the payment reconciliation journal.
date: 02-08-2021
id: 
lang: en
---

# Setting up payment application rules

On the **Payment Application Rules** page, you set up rules to govern how payment text on a vendor transaction is used to identify to which vendor a payment belongs. 

Payment Management uses the payment ID, which is the reference to the associated payment or purchase document, to identify to which vendor the payment belongs. If the payment reference isn't available on the cash receipt journal line, Payment Management will use the vendor application rules to identify the vendor account number. 

The application rule will be used when importing vendor payments into the payment reconciliation journal. If the rule is met, i.e. the search text is identified in the **Description** or **Notification** of the journal lines, then "vendor" will be inserted on the journal line in **Account type**, and the associated vendor number will be inserted in **Account No.**



## To set up vendor application rules

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **vendor Application Rules**, then select the related link.
2. Define a new or edit a payment application rule by filling the fields on a line as described in the following table.

| Field | Description |
| --- | --- |
| Account No. | In **Account No.** chose the vendor account number that must be applied to the journal line, when the line meets the criteria of the search rule. |
| Search text | In **Search text** enter the text to be searched for in the vendor or vendor payment. |
| Search Principle | In **Search Principle** specify the criteria for when the search rule should be considered.<br /> <ul><li>**Exact** indicates that search text must be the exact same as the description or notification on the payment, for the rule to be met. </li><li>**From left** indicates that search text must match the first part of the description or notification on the payment, for the rule to be met. </li><li>**From right** indicates that search text must match the last part of the description or notification on the payment, for the rule to be met. </li><li>**Within** indicates that search text must just appear some place in the description or notification on the payment, for the rule to be met.</li></ul> |
| Search in Description | Select **Search in Description** if you want the search rule to search for the text defined in **Search text** in the description of the journal line. |
| Search in Notification | Select **Search in Notification** if you want the search rule to search for the text defined in **Search text** in the notification of the journal line. |

When you are done setting up vendor application rules you can close the page.

> [!NOTE]
>
> If you're creating more application rules for the same vendor account number, then the list is ranked with the highest priority from the top of the list.

