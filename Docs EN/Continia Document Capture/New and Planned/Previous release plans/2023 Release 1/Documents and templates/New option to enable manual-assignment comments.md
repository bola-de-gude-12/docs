---
title: New Option to Enable Manual-Assignment Comments
date: 28-11-2024
description:
id: DC-297
lang: en
---

# New Option to Enable Manual-Assignment Comments

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| New option to enable manual-assignment comments | {{checkmark}} Mar 2023 | {{checkmark}} Apr 2023 |

## Business value

The option of prompting users to enter comments whenever they manually assign documents to other users will add transparency to the assignment process. Any entered comments will make it easier for assignees to understand why a given document has been assigned to them.

## Feature details

The new field **Comment on manual assignment** will be added to the **Document Capture Setup**. If this field is enabled, users that manually add another user in the **Assigned to User ID** field will be presented with a page that allows them to enter a free-text assignment comment (typically a reason for the assignment). The comment page will appear whenever a document is manually assigned to a user, and you either can or must enter a comment on the page, depending on which of the options has been selected in the setup.

You'll be able to choose between the following setup options:

* **No** (default): The comment page won't be displayed at all.
* **Optional**: The comment page will be displayed, but users can close it without adding any comments.
* **Mandatory**: The comment page will be displayed, and the system will return an error if no comments are added.
