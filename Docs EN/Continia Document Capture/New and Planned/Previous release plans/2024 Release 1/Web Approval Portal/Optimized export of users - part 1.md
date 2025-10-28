---
title: Optimized export of users – part 1
date: 12-12-2024
description:
id: DC-388
lang: en
---

# Optimized Export of Users – Part 1

| Feature | Public preview | General availability online |
| --- | :-: | :-: |
| Optimized export of users – part 1 | {{checkmark}} Mar 2024 | {{checkmark}} Apr 2024 |

## Business value

The optimization of the user export feature will be a massive time-saver for organizations with large numbers of users. Currently, such clients are potentially unable to use Continia Document Capture for extended periods of time whenever they export users, as the system may be locked while the export is in progress. The new and optimized feature will drastically reduce the amount of system downtime and any frustrations resulting from this.

## Feature details

In order to align user permissions and similar between Document Capture and the Continia Web Approval Portal, it's occasionally necessary to export user data to Continia Online – for example using the **Export Users** action on the **Continia Users** page. 

This user export feature will now be improved in various ways. The improvements will be implemented in two stages as follows:

**Improvement stage 1:** Before exporting all user information, Document Capture will check if any changes have been made to any users. Only if so, all user information will be exported, meaning that you avoid exporting data unnecessarily. This change was implemented in Document Capture 2024 R1, released in April 2024.

**Improvement stage 2:** The first stage of this feature, implemented in April 2024, addressed most problems related to the user update. Therefore, there's no longer need to implement the second stage of the optimization.

For more information, see [Configuring Users for the Web Approval Portal](@DC-129).