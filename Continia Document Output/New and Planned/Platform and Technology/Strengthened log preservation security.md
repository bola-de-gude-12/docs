---
title: Strengthened Log Preservation Security
date: 31-03-2024
description: 
id: DO-206
lang: en
---

# Strengthened Log Preservation Security

| Feature | Public preview | General availability |
| --- | :-: | :-: |
| Strengthened log preservation security | {{checkmark}} Mar 2025 | {{checkmark}} Apr 2025 |

## Business value

The Document Output log provides a complete record of all sent documents, essential for maintaining an audit trail and verifying document delivery. This feature ensures that only authorized users, granted permission by an admin, can delete log entries. By restricting log deletion, organizations can protect historical data, improve compliance, and provide transparency across document workflows.

## Feature details

This functionality will most likely be implemented through a new permission set that allows specific users to clean up the log. Only users assigned this permission set will be able to delete log entries, giving administrators control over log management. 
