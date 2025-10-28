---
title: Setting up the Secure Archive in Document Capture
date: 24-07-2025
description: How to set up the Secure Archive in Document Capture.
id: DC-155
lang: en
---

# Setting up the Secure Archive

The [Secure Archive](@DC-154) is available for both Continia Document Capture and Continia Expense Management and must be set up separately for each of these solutions, depending on whether you want to use it for both, either, or neither of them.

## Secure Archive for Document Capture

To set up the Secure Archive for Document Capture, follow these steps:

1. Search ({{search}}) for and select **Document Capture Setup**.
1. On the **Secure Archive and Logging** FastTab, turn on the **Enable Secure Archive** setting. This also automatically enables **Document Activity Logging**, and a number of new fields are displayed.
   > [!TIP]
   > If you only want to enable logging as an independent feature, enable the **Document Activity Logging** setting and leave **Enable Secure Archive** turned off. If you change your mind, you can enable the Secure Archive at a later point.
1. Under **Archive Period Type**, specify if you want the archive period to be based on calendar years or fiscal years. The default is calendar years.
1. Under **Minimum Archive Period**, specify the minimum number of years Document Capture should archive your documents. For some countries, a default number is displayed here, based on local or national legislation, but you're free to change this as you please.
   > [!NOTE]
   > The minimum archive period is the entered number plus the current year, meaning that the current calendar/fiscal year is not included in the entered period. If you've selected **Calendar Years** in step 3, enabled the Secure Archive on July 1, and then entered 3 under **Minimum Archive Period**, the archive period will run for 3.5 years.

All Document Capture documents used for bookkeeping will now be automatically stored in the Secure Archive, and all document activity will be systematically logged.

## Related information

[Setting up the Secure Archive in Expense Management](@EM-190)  