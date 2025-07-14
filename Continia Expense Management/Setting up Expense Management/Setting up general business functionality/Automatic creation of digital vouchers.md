---
title: Expense Management Automatic Creation of Digital Vouchers
date: 04-04-2024
description:
id: EM-223
lang: en
---

# Automatic Creation of Digital Vouchers

A fundamental principle in bookkeeping and accounting is that organizations must provide documentation for their transactions by storing supporting documents such as invoices and other business documents along with any related files. This ensures traceability and a robust audit trail, which is not only a legal requirement but also desirable for your organization as a safety measure.

In many organizations, these supporting documents – *vouchers* – are digitized for efficiency purposes. As a matter of fact, such digital vouchers are even required by law in some countries. In Microsoft Dynamics 365 Business Central, digital vouchers are stored under  **Incoming Documents**. 

> [!NOTE]
> Equivalent functionality exists in Document Capture, which you can read more about in the Document Capture article [Automatic Creation of Digital Vouchers](@DC-184).

## Standard Business Central functionality

With [the **Digital Voucher Setup** feature that's included in update 23.2 for Business Central 2023 release wave 2 (BC v23.2)](https://learn.microsoft.com/en-us/dynamics365/business-central/across-how-setup-digital-vouchers), you can set up Business Central to check if a digital voucher has been stored in **Incoming Documents** before posting. You can set this up for each transaction type. If you set it up to check for digital vouchers on expenses and none is detected, you must manually add a digital voucher to the transaction yourself in order to be able to post the transaction. In connetion with per diems and mileages, digital vouchers are created automatically, meaning you don't have to add anything yourself.

> [!NOTE]
> In Denmark, the new Danish Bookkeeping Act (in effect from July 1, 2024) makes this check mandatory for Danish organizations that use Business Central online, because Microsoft has registered Business Central online with the Danish Business Authority (Erhvervsstyrelsen) and had it approved as a standard digital bookkeeping system. This effectively means that when located in Denmark, you must somehow add a digital voucher to **Incoming Documents** in order to pass the check and post transactions.

## Enhanced Expense Management functionality

As of Expense Management 2023 R2 Service Pack 2, Expense Management can automatically create digital vouchers for incoming documents based on the Expense Management files (the files that were imported into Expense Management), so that you don't have to manually attach files yourself. When a document is registered as a purchase document or journal, Expense Management will automatically make a copy of all Expense Management files and attach them as digital vouchers under **Incoming Documents**, provided that you set it up to do so. The setup depends on your version of Business Central:

<br>

| Business Central version | How to set up |
| --- | --- |
| [From Business Central April 2019 (BC v14) to BC v23.1](#expense-management-setup-process-for-bc-v14-to-bc-v231) | The feature is configured in the **Expense Management Setup**. |
| [BC v23.2 and later](#expense-management-setup-process-for-bc-v232-and-later) | Expense Management will check the **Digital Voucher Entry Setup** to determine if the feature has been enabled for the type of document that's registered. |

When you enable the feature and register a purchase document, Expense Management will automatically copy all attached files into the **Incoming Documents** FactBox in the open purchase document, where they'll be listed as digital vouchers. This means that the files listed here are by default the same as the ones listed on the **General** FastTab under **Attachments**. However, there's no further link between these two sections, meaning that if you decide to delete a file in either one of them, the other section won't be automatically updated accordingly – the deleted file will still appear here.

To learn more about the setup process, see one of the sections below, depending on your version of Business Central. 

## Expense Management setup process for BC v14 to BC v23.1

To set up Expense Management to automatically create digital vouchers for older versions of Business Central (BC v14 to BC v23.1), follow these steps:

1. Choose the {{search}} icon, enter **Expense Management Setup**, and then choose the related link.
1. On the **General** FastTab, go to **Digital Vouchers**.
1. To enforce the check for attachments, enable **Create for Attachment before Posting of Purchase Document**.
1. To enable Expense Management to automatically create digital vouchers, enable **Create Digital Voucher from Document**.

For all documents that are registered, Expense Management will now create digital vouchers automatically according to your setup.

## Expense Management setup process for BC v23.2 and later

> [!NOTE]
> Expense Management checks the standard Business Central **Digital Voucher Entry Setup** to determine if the digital voucher feature has been enabled for the type of document that's registered. If so, Expense Management automatically transfers all Expense Management files to **Incoming Documents**.

To set up Expense Management to automatically create digital vouchers for [purchase allocations](@DC-41) for new versions of Business Central (BC v23.2 and later), follow these steps:

1. Choose the {{search}} icon, enter **Expense Management Setup**, and then choose the related link.
1. On the **General** FastTab, go to **Digital Vouchers**.
1. In **Status**, select  **Not configured**. This will take you to the Business Central standard page **Digital Voucher Entry Setup**. You can find the Microsoft guide to set up digital vouchers [here](https://learn.microsoft.com/en-us/dynamics365/business-central/across-how-setup-digital-vouchers).

For all documents that are registered, Expense Management will now create digital vouchers automatically according to your setup.