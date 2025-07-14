---
title: Automatic import of cash receipts and bank statements
description: Automatic import of cash receipts and bank statements files including the creation of notifications.
date: 30-09-2022
id: PM-74
lang: en
---

# Automatic Import of Cash Receipts and Bank Statements

| Feature | General availability online | Public preview |
| --- | :-: | :-: |
| Automatic import of cash receipts and bank statements files including the creation of notifications | {{checkmark}} Mar 2023 | - |

## Business value

Automation of the payment process is one of our focus areas within Payment Management. We aim to help users with important and valuable tasks and reduce the time spent on trivial, yet important tasks. This will free up time to do other tasks in a busy workday.

## Feature details

When bank statements and cash receipts are available in the bank to be imported to Business Central with direct bank communication, Payment Management will support the automatic import of these to the bank account reconciliation and to the cash receipt journal. This service ensures that the bank data is imported to Business Central as soon as it is available at the bank so that you do not have to initiate the file import manually. When a file has been imported by the service, a notification will appear stating that a file has been imported and processed by Payment Management.

The import will be managed by a [job queue](@PM-324) in Business Central from where you can define how often the service should call the bank for available bank files. If files have been imported by the service, a notification will appear with further information about the import. 

For more information on importing payments automatically, see the [Importing Customer payments](@PM-96) article.

For more information on importing bank statements automatically, see the [Importing and Reconciling Bank Statements](@PM-48) article.

