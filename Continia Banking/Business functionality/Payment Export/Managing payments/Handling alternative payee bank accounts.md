---
title: Adding an alternative account holder
description: Learn how to direct payments meant for a vendor or customer to a different party.
date: 31-03-2025
id: CB-218
lang: en
---
# Adding an alternative account holder

In some cases, payments meant for a vendor or customer need to be directed to a different party, such as a factor, a debt manager or another contact person. For example, if a vendor is bankrupt and a debt manager is handling payments, or when a company wants to charge an individual instead of a department, Continia Banking allows you to specify an alternative account owner to ensure payments are routed correctly.

When a payment or direct debit is intended for a different account holder, the **Alternative Account Owner** fields on the vendor/customer bank account card can store the alternative payee’s information. If these fields are filled, the system will automatically include this alternative account in the payment suggestion and export it to the payment file. For example, in cases where a vendor is bankrupt and a debt manager is now handling the payments, this feature ensures that payments are directed to the debt manager’s account instead of the vendor's original account.

To add an alternative account holder:

* Open the vendor or customer bank account card, and on the **General** FastTab navigate to the following fields:
  * **Alternative Account Owner** - specify the name of the alternative account owner. 
    When this field is filled, the system uses this information for payments instead of the original account holder. If this field is left empty, the system will default to the original account holder.
  * **Alternative Account Owner Contact** - select a contact. This is especially useful for international payments or when a postal address is required. If this field is populated, the system will pull contact details from the Business Central contact card.

