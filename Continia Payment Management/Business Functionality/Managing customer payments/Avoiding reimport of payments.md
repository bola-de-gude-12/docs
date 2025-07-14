---
title: Avoiding reimport of payments
description: How to avoid reimporting cash receipt lines to the cash receipt journal
date: 02-06-2021
id: PM-95
lang: en
---

# Avoiding Reimport of Payments

Payment Management uses the payment reference ID to prevent importing duplicate payments. However, there may be situations where the same payment is imported multiple times in Business Central.

Here are some examples of what can cause the import of duplicate payments:

- When using manual communication, the bank file may not have a unique reference ID. Without a unique ID, Payment Management can't determine if the file has already been imported.
- With direct communication, the same file can be called multiple times, resulting in a new reference ID for each call.
- If a payment line is manually created in the payment journal and then settled with the invoice, it can cause duplication. 

If a payment line is created more than once in the payment journal, it can't be applied to the invoice, as a previous payment line has already been applied. In this case, an error message displays at the bottom of the cash receipt journal, notifying you that the associated invoice has already been applied to another payment and has been posted.

## To delete a duplicate payment line and avoid reimport

To prevent future imports of duplicate payments, you can manually delete the duplicate payment lines and mark them as imported. 

To delete a duplicate payment line:

1. Use the ![Search for page or report](/images/search_small.png) icon and search for **Cash Receipt Journals**, then select the related link. 
2. Open the relevant journal.
3. Select the payment line that you want to eliminate for reimport.
4. On the action bar, select **Related** > **Delete and set as imported**.

The selected line will now be deleted from the cash receipt journal. The corresponding line in Bank Export Data will be marked as **Imported to the Company**, indicating that it can't be imported again.

