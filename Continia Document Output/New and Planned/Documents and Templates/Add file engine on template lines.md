---
title: Add File Engine on Template Lines
date: 05-03-2025
description: 
id: DO-209
lang: en
---

# Add File Engine on Template Lines

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Add file engine on template lines | - | N/A |

> [!NOTE]
> The release of this feature has been postponed. A new release date has not yet been determined.

## Business value

This feature is relevant when the attachment could be a list of items from an Excel sheet for some customers and a PDF attachment for other customer types. The creation of these files is possible in the current version of Document Output but applies to all email templates of the selected type and can't be varied on the template lines as it is now. The file engine will still be dependent on the report selection gathering data to be able to put data into the selected data format (PDF, Excel or Word).

## Feature details

This feature introduces the ability to customize attachments at the template line level, allowing different file types (such as Excel, PDF, Word) to be selected for specific customer types within the same email template. The file engine remains connected to the report selection setup, ensuring that data is accurately formatted and inserted into the specified file type.
