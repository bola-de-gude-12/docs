---
title: Integration to Azure BLOB Storage
date: 29-09-2023
description: 
id: DO-69
lang: en
---

# Integration to Azure BLOB Storage

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Integration to Azure BLOB Storage | - | {{checkmark}} Oct 2023 |

## Business value

When using Business Central as a cloud solution, this feature provides the option to securely store log files and emails outside of Business Central.

## Feature details

Introducing a new storage type for cloud solutions, as database storage may not be suitable and file systems are not an option. To use this new storage type, you will need to set up access to your company's Azure storage and direct the Document Output setup to it. This will free up space in the database by removing log entries and sent emails.

You can find more information about this feature in the [Storing your Document Output Log in Azure Blob Storage](@DO-130) article.