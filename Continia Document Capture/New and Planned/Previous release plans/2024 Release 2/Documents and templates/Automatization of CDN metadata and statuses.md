---
title: Automation of CDN metadata and statuses
date: 24-12-2024
description:
id: DC-315
lang: en
---

# Automation of CDN Metadata and Statuses

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Automation of CDN metadata and statuses | {{checkmark}} Sep 2024 | {{checkmark}} Oct 2024 |

## Business value

With this feature, you'll always have the latest metadata from the Continia Delivery Network (CDN) available, such as network data, identification types, network profiles, and various document data. The feature will also ensure that the statuses of documents sent via the Continia Delivery Network are updated automatically, so that you don't have to manually open the **Outgoing Network Documents** page to do this yourself.

## Feature details

The following two new job queues will be added to automate the updating of metadata and statuses for the Continia Delivery Network:

* **eDocuments metadata update**
* **eDocuments document update**

The **eDocuments metadata update** job queue is to be used for updating participations and network data. It's scheduled to run once a day at a random time between 6:00 PM and 5:00 AM.

The **eDocuments document update** job queue is to be used for updating document statuses and downloading new documents and receipts. It's scheduled to run every 30 minutes.