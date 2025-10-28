---
title: Data Maintenance Using a Job Queue for Continia Expense Management Tables
date: 05-04-2024
description:
id: EM-205
lang: en
---

# Data Maintenance Using a Job Queue for Continia Expense Management Tables

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Data maintenance using a job queue for Continia Expense Management tables | {{checkmark}} Mar 2024 | {{checkmark}} Apr 2024 |

## Business value

Introducing a cleanup job queue for transactional tables will enable you to automate the cleanup process, thereby ensuring smoother handling of document-related data. By automating the deletion of generated values and entire documents based on the status and age of each document, the feature will simplify data management, significantly reduce manual effort, streamline the database, and substantially improve overall system performance.

## Feature details

A job queue for deleting the content of the following tables will be added:

* **CEM Expenses** table
* **CEM Mileage** table
* **CEM Per Diem** table
* **CEM Expense Header** table
* **CEM Bank Transaction** table
* BLOBs or files with data

You can find further information in [Setting up Data Maintenance](@EM-224).
