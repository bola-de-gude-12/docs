---
title: Ability to delegate documents to specific users
date: 11-12-2024
description:  
id: DC-268
lang: en
---

# Ability to Delegate Documents to Specific Users

| Feature | General availability on-premises | General availability online | Public preview |
| --- | :-: | :-: | :-: |
| Ability to delegate documents to specific users | {{checkmark}} Sep 1, 2020 | {{checkmark}} Oct 1, 2020 | - |

## Feature details
It’s now possible to delegate any Document Capture document to a specific user. A new column, **Delegated To User ID**, has been added to the document journal. This column is hidden by default, but you can display it by selecting **Settings** in the upper-right corner and then choosing **Personalize**. You can manually delegate any document by entering a user ID in the **Delegated To User ID** field for the chosen document. If set up to automatically generate delegation comments, the system will attempt to automatically delegate the document to the relevant user. The user is identified by the mapping of **Our Contact** to a purchaser code, which is then used to identify the user ID through **Continia User Setup**.

In addition, a new tile, **Delegated to me**, which shows the number of delegated documents, has been added to the **Continia Document Capture Activities** section of the Role Center. You can open the list of delegated documents by selecting this tile or by searching for **Delegated Document List**.