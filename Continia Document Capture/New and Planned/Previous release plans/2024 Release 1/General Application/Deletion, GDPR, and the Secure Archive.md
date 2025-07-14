---
title: Deletion, GDPR, and the Secure Archive
date: 26-11-2024
description:
id: DC-260
lang: en
---

# Deletion, GDPR, and the Secure Archive

| Feature | Public preview | General availability online |
| --- | :-: | :-: | 
| Deletion, GDPR, and the Secure Archive | {{checkmark}} Mar 2024 | {{checkmark}} Apr 2024 |

## Business value

This feature is introduced to allow you to comply with GDPR regulations in the EU/EEC and similar legislation in other parts of the world. Seeing that business documents may very well contain personal details, we recommend that you periodically delete the ones you're not legally obliged to keep. This feature will make it very easy for you to do so.

The feature will relate to the [Secure Archive](@DC-154) in particular and adhere to the settings of this, but you'll also be able to use it when the Secure Archive is disabled.

## Feature details

Actions will be added to Continia Document Capture, allowing you as an admin to manually delete captured words, generated values, and entire documents as needed. If you choose to delete words and/or values, you can do so freely without any restrictions in terms of the secure period (known as **Minimum Archive Period** in [the Secure Archive setup](@DC-155)), whereas the secure period will be respected when it comes to the deletion of entire documents, provided that the Secure Archive has been enabled.

Whenever you delete documents for a certain period of time, log entries from that period will also be deleted, and a single entry stating that the period has been deleted will then be added to the log instead.

If you use an action to delete words or values, the **CDC Document Word** and **CDC Document Value** tables will be cleaned up automatically, while deleting an entire document and its related data will result in an automatic cleanup of all the tables and files/objects below:

* **CDC Document** table
* **CDC Document Word** table
* **CDC Document Value** table
* **CDC Document Email** table
* **CDC Document Page** table
* **CDC Document Comment** table
* BLOBs or files with data 

For more information, see [Setting up Data Maintenance](@DC-187).

