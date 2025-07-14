---
title: Preventing Approvers from Changing the On-Hold Status of Documents for Approval
date: 29-11-2024
description:
id: DC-360
lang: en
---

# Preventing Approvers from Changing the On-Hold Status of Documents for Approval

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Preventing approvers from changing the on-hold status of documents for approval | - | {{checkmark}} Oct 2023 |

## Business value

When a purchase document for approval has been put on hold, this on-hold status (which also applies to vendor ledger entries) helps control if the document is processed correctly. For invoices, for example, the on-hold status determines whether or not they're paid. When an approver approves an invoice on hold, the approver is presented with a **Remove On Hold** dialog asking him to either remove or keep the on-hold status. Making the wrong choice here may result in the invoice not being paid, but approvers don't always realize this and may therefore choose somewhat haphazardly, which is of course undesirable.

The introduction of a toggle that enables you to hide this dialog from the approvers will prevent any such unwanted actions. 

## Feature details

A new action, **Keep On Hold**, will be added to the **Document Capture Setup**. If you enable this, the **Remove On Hold** dialog won't be displayed to approvers when they approve documents that have been put on hold. Instead, the on-hold status will be kept by default throughout the approval process.

For more information, see [To set up purchase approval](@DC-22#to-set-up-purchase-approval).

## Related information

[Document Capture Permissions](@DC-140)  