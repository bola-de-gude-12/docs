---
title: One Email for all Companies to Notify About Open Approval Entries Expense Management
date: 10-09-2024
description:  
id: EM-238
lang: en
---

# One Email for all Companies to Notify About Open Approval Entries

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| One email for all companies to notify about open approval entries | - | N/A |

>[!NOTE]
>This feature will be released in Expense Management 2024 R2 Service Pack 1.

## Business value

Until now, Continia Expense Management has notified document approvers about open approval entries by sending them a separate email for each company in the organization. With the introduction of this feature, the approvers will only receive one notification email covering all companies instead, to ensure a more streamlined experience.

## Feature details

A new codeunit will be added, enabling you to set up a job queue that can be run as frequently as you prefer. When the job queue is run according to your setup, a single notification email about open approval entries for all of your companies will then be sent out.