---
title: Inclusion of Document Capture files when reversing transactions registered in journals
date: 24-12-2024
description:
id: DC-424
lang: en
---

# Inclusion of Document Capture Files when Reversing Transactions Registered in Journals

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Inclusion of Document Capture files when reversing transactions registered in journals | - | - |

> [!NOTE]
> When reverting documents registered in journals, Business Central assigns the original document number to them. Therefore, the reference to attached documents remains active. For this reason, there's no need to change the functionality of Document Capture.

## Business value

Automatically attaching the original documents when reversing transactions registered in journals not only ensures legal compliance, but also makes it easy for you to access the original documents. It increases convenience and speeds up your workflow.

## Feature details

A common requirement in many countries is that every posted entry must include the original document as an attachment. However, it may be necessary for you to correct the posted entry – for example, in case of typos. In such cases, a reversing transaction is created to offset the original transaction.

To meet the requirement of always including original documents as attachments, this new feature will ensure that these originals are automatically attached to the reversing transaction.