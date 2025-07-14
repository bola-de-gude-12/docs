---
title: List of Documents Requiring Special Attention with Regard to the Secure Archive
date: 26-11-2024
description:
id: DC-264
lang: en
---

# List of Documents Requiring Special Attention with Regard to the Secure Archive

| Feature | Public preview | General availability online |
| --- | :-: | :-: | 
| List of documents requiring special attention with regard to the Secure Archive | {{checkmark}} Mar 2024 | {{checkmark}} Apr 2024 |

## Business value

Currently, whenever there's a hash issue with a document stored in the Secure Archive, you're not notified of this issue – you have to manually navigate to the posted document and then from there to the **Document Log Summary** page in order to find out. With the introduction of this feature, a centrally placed list will notify you up front of any hash check issues, so that you can take proactive action immediately.

## Feature details

[The Secure Archive](@DC-154) uses hash functions to ensure the originality of each document that's stored in the archive. To do this, it assigns a hash value to each imported document, calculates a hash value again when the document is viewed or posted, and then checks that hash value against the original hash value. If the hash check fails – that is, if the two values don't match – the document has somehow been altered and no longer matches the original document.

With this feature, you'll get easy access to a list of all documents for which a hash check has failed. The list will be featured in a central and prominent place and will enable you to access the **Document Log Summary** for more details.

In terms of functionality, the feature is related to the [List of Documents for Which Activity Log Entries Have Been Created Between Approval and Posting](List of documents for which activity log entries have been created between approval and posting.md).

For more information, see [Document Control Log](@DC-212).