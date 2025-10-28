---
title: Unsupported standard features in Document Capture
date: 23-06-2025
description: A list of features that are currently not supported by Document Capture.
id: DC-134
lang: en
---

# Unsupported standard features

Continia Document Capture provides a wealth and depth of functionality that covers the vast majority of business needs and wants. This, combined with its overall outstanding level of performance, easily makes it the market's most complete and advanced solution for the import, OCR-processing, registering, approving, and archiving of business documents in Microsoft Dynamics 365 Business Central.

That said, there are a few standard features that are currently not supported in Document Capture. These include the ones [mentioned below](#currently-unsupported-features).

## Currently unsupported features

The following features are currently neither supported nor planned for future development (although they may very well be added in the more distant future):

* Background posting – or posting via job queues – of invoices/credit memos matched against orders/return orders.
* When you match against a purchase order, Continia receives the purchase order before invoicing the invoice. As there are commits in the receiving process, the preview functionality has been blocked. If you need the preview functionality, you must match against a receipt.
* Deferral codes in allocations.
* Certain workflow options:
   * For the workflow response option **Approver Type**, Document Capture doesn't support the options **Approver** and **Workflow User Group** – only **Salesperson/Purchaser** is accepted. For advanced approval, the only supported type is **Approver**.
   * For the workflow response option **Approver Limit Type**, Document Capture doesn't support the options **Direct Approver**, **First Qualified Approver** and **Specific Approver** – only **Approver Chain** is accepted.

## Newly supported features

The following previously unsupported features are now supported in Document Capture:

* As of Document Capture 2023 R1 (v11), prepayments are supported. For more information, see [To register prepayment invoices](@DC-67#to-register-prepayment-invoices).
* As of Document Capture 2024 R1 SP2 (v24), using the standard **Merge duplicate records** feature available in Business Central results in the merging of Document Capture documents associated with the merged customers/vendors.
* As of Document Capture 2024 R2 (v25), it's possible to use Business Central's fixed allocation accounts. For more information, see [Using allocation accounts](@DC-226).
* As of Document Capture 2025 R1 (v26), documents attached to a posted purchase invoice are copied as drag-and-drop attachments to the resulting document when using **Correct**, **Cancel**, or **Create Corrective Credit Memo** on the posted purchase invoice. Note that, as of Document Capture 2025 R1 SP2 (v26.2), this doesn't apply to documents attached to a posted purchase invoice from a purchase order.

## Related information

[Business functionality](@DC-50)  