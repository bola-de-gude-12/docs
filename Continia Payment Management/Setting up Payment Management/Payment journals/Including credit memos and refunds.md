---
title: Including credit memos and refunds in payment suggestions
description: Information om how to include credit memos and refunds in the payment journal suggestions
date: 30-09-2021
id: PM-200
lang: en
---

# Including Credit Memos and Refunds in Payment Suggestions

As per default, the payment journal is intended for managing payments, i.e. to pay your vendors or employees. However, when creating payment suggestions, you can allow for credit memos and refunds to be included in the payment. 

Credit memos and refunds will be created with a *negative amount* in the payment journal, which can't be sent to the bank, as only positive payment lines can be imported into the bank. Therefore, you must manually summarize payments for the given vendor, so that the summarized payment line is a *positive amount*.

## To allow for negative amounts in the payment journal

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Payment Journals**, then select the related link. 
1. Open the relevant payment journal.
1. On the payment journal in the action bar, select **Prepare** > **Payment Journal Setup**.
1. On the Payment Journal Setup page under **General**, activate the option **Allow Negative Amounts**.

> [!NOTE]
>
> If payments are automatically summarized when creating a payment suggestion, the setup for summarizing payments will determine if credit memos are included. Otherwise, you must manually summarize the suggested payment lines, including credit memos and refunds, in order to obtain a positive payment line. For more information, see [Summarizing Payments](@PM-186).



## Related information

[Summarizing Payments](@PM-186)

