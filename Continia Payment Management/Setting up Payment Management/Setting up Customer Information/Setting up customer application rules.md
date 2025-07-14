---
title: Setting up customer application rules
description: Set up rules to identify the customer who generated a payment in the cash receipt journal.
date: 02-06-2021
id: PM-174
lang: en
---

# Setting up Customer Application Rules

On the **Customer Application Rules** page, you set up rules to control how payment text on a transaction is automatically matched to the customer who created the payment. 

Payment Management uses the OCR-related ID (payment ID), which is the reference to the associated invoice or sales document, to identify to which customer the payment belongs and uses the customer application rules to identify the customer account number if the payment reference is unavailable on the cash receipt journal line. 

When customer payments are imported into the cash receipt journal, the application rule will be used. If the rule is met, for example, if the search text is identified in the **Description** or **Notification** fields of the journal lines, then "Customer" will be inserted on the journal line in **Account type**, and the associated customer number will be inserted in the **Account No.** field.



## To set up customer application rules

You can set up rules to control how payment text on a transaction is automatically matched to the customer who created the payment. 

To set up customer application rules:

1. Use the ![Search for page or report](https://docs.continia.com/images/search_small.png) icon and search for **Customer Application Rules**, then select the related link.

2. Define a new payment application rule, or edit an existing one by entering information for the following  fields:

    | Field                  | Description                                                  |
    | ---------------------- | ------------------------------------------------------------ |
    | Account No.            | Choose the customer account number that must be applied to the journal line when the line meets the criteria of the search rule. |
    | Search text            | Enter the text to be searched for in the customer payment.   |
    | Search Principle       | Specify the criteria for when the search rule should be considered.<br /> <ul><li>**Exact** indicates that search text must be the same as the description or notification on the payment for the rule to be met. </li><li>**From left** indicates that search text must match the first part of the description or notification on the payment for the rule to be met. </li><li>**From right** indicates that search text must match the last part of the description or notification on the payment for the rule to be met. </li><li>**Within** indicates that search text must appear someplace in the description or notification on the payment for the rule to be met.</li></ul> |
    | Search in Description  | Select **Search in Description** if you want the search rule to search for the text defined in **Search text** in the description of the journal line. |
    | Search in Notification | Select **Search in Notification** if you want the search rule to search for the text specified in **Search text** in the notification of the journal line. |

    You can close the page when you're done setting up customer application rules.

> [!NOTE]
>
> If you're creating more application rules for the same customer account number, then the list is ranked with the highest priority from the top of the list.

