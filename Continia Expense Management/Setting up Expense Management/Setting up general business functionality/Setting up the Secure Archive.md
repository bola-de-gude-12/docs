---
title: Expense Management Setting up the Secure Archive
date: 29-09-2023
description:  
id: EM-190
lang: en
---

# Setting up the Secure Archive

The [Secure Archive](@EM-189) is available for both Continia Document Capture and Continia Expense Management and must be set up separately for each of these solutions, depending on whether you want to use it for both, either, or neither of them. The setup procedures are very similar and are both described below.

## Secure Archive for Document Capture

To set up the Secure Archive for Document Capture, follow these steps:

1. Choose the {{search}} icon, enter **Document Capture Setup**, and then choose the related link.
1. On the **Secure Archive and Logging** FastTab, select the **Enable Secure Archive** toggle to enable the Secure Archive. This will also automatically enable **Document Activity Logging**, and a number of new fields will be displayed.
   > [!TIP]
   > In case you only want to enable logging as an independent feature, simply select the **Document Activity Logging** toggle and leave **Enable Secure Archive** disabled. You can always enable the Secure Archive at a later point if you change your mind.
1. Under **Archive Period Type**, specify if you want the archive period to be based on calendar years or fiscal years. The default is calendar years.
1. Under **Minimum Archive Period**, specify the minimum number of years Document Capture should archive your documents. For some countries, a default number is displayed here, based on local or national legislation, but you're free to change this as you please.
   > [!NOTE]
   > The minimum archive period will be the entered number plus the current year, meaning that the current calendar/fiscal year is *not* included in the entered period. So if you've selected **Calendar Years** in step 3, enable the Secure Archive on July 1, and then enter **3** under **Minimum Archive Period**, the archive period will run for 3.5 years.

All Document Capture documents used for bookkeeping will now be automatically stored in the Secure Archive, and all document activity will be systematically logged.

## Secure Archive for Expense Management

To set up the Secure Archive for Expense Management, follow these steps:

1. Choose the {{search}} icon, enter **Expense Management Setup**, and then choose the related link.
1. On the **Secure Archive and Logging** FastTab, select the **Enable Secure Archive** toggle to enable the Secure Archive. This will also automatically enable **Document Activity Logging**, and a number of new fields will be displayed.
   > [!TIP]
   > In case you only want to enable logging as an independent feature, simply select the **Document Activity Logging** toggle and leave **Enable Secure Archive** disabled. You can always enable the Secure Archive at a later point if you change your mind.
1. Under **Archive Period Type**, specify if you want the archive period to be based on calendar years or fiscal years. The default is calendar years.
1. Under **Minimum Archive Period**, specify the minimum number of years Document Capture should archive your documents. For some countries, a default number is displayed here, based on local or national legislation, but you're free to change this as you please.
   > [!NOTE]
   > The minimum archive period will be the entered number plus the current year, meaning that the current calendar/fiscal year is *not* included in the entered period. So if you've selected **Calendar Years** in step 3, enable the Secure Archive on July 1, and then enter **3** under **Minimum Archive Period**, the archive period will run for 3.5 years.
1. If you want documents to be digitally signed when they're imported, make sure that **Sign Documents** is enabled (which is the default state).

All Expense Management documents used for bookkeeping will now be automatically stored in the Secure Archive (and signed upon import, if this is enabled), and all document activity will be systematically logged.

## See also

[Secure Archive](@EM-189)  