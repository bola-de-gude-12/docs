---
title: Expense Management Setting up the Secure Archive
date: 24-07-2025
description:  
id: EM-190
lang: en
---

# Setting up the Secure Archive

The [Secure Archive](@EM-189) is available for both Continia Expense Management and Document Capture. Each  solution must be set up separately, depending on whether you want to use it for either, neither, or both of them. The setup procedures are very similar, see Related information for the link to the Document Capture version.

## Secure Archive for Expense Management

To set up the Secure Archive for Expense Management, follow these steps:

1. Search for {{search}} **Expense Management Setup**.
1. Under **Secure Archive and Logging**, toggle **Enable Secure Archive** on to enable the Secure Archive. This also automatically enables **Document Activity Logging**, and a number of new fields will be displayed.
   > [!TIP]
   > In case you only want to enable logging as an independent feature, select the **Document Activity Logging** toggle and leave **Enable Secure Archive** disabled. You can always enable the Secure Archive at a later point if you change your mind.
1. Under **Archive Period Type**, specify if you want the archive period to be based on calendar years or fiscal years. The default is calendar years.
1. Under **Minimum Archive Period**, specify the minimum number of years Document Capture should archive your documents. For some countries, a default number is displayed here, based on local or national legislation, but you're free to change this as you please.
   > [!NOTE]
   > The minimum archive period will be the entered number plus the current year, meaning that the current calendar/fiscal year is *not* included in the entered period. So if you've selected **Calendar Years** in step 3, enable the Secure Archive on July 1, and then enter "3" under **Minimum Archive Period**, the archive period will run for 3.5 years.
1. If you want documents to be digitally signed when they're imported, ensure **Sign Documents** is enabled (which it is by default).

All Expense Management documents used for bookkeeping will now be automatically stored in the Secure Archive (and signed upon import, if this is enabled), and all document activity will be systematically logged.

## Related information

[The Secure Archive](@EM-189) (Expense Management) 

[Setting up Secure Archive](@DC-155) with Document Capture