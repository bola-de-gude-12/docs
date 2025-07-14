---
title: Automatic Creation of Digital Vouchers
date: 07-03-2024
description:
id: DC-184
lang: en
---

# Automatic Creation of Digital Vouchers

A fundamental principle in bookkeeping and accounting is that organizations must provide documentation for their transactions by storing supporting documents such as invoices and other business documents along with any related files. This ensures traceability and a robust audit trail, which is not only a legal requirement but also desirable for your organization as a safety measure.

In many organizations, these supporting documents – *vouchers* – are digitized for efficiency purposes. As a matter of fact, such digital vouchers are even required by law in some countries. In Microsoft Dynamics 365 Business Central, digital vouchers are stored under  **Incoming Documents**. 

## Standard Business Central functionality

With [the **Digital Voucher Setup** feature that's included in update 23.2 for Business Central 2023 release wave 2 (BC v23.2)](https://learn.microsoft.com/en-us/dynamics365/business-central/across-how-setup-digital-vouchers), you can set up Business Central to check if a digital voucher has been stored in **Incoming Documents** before posting. You can set this up for each transaction type (sales document, sales journal, purchase document, purchase journal, or general ledger). If you set it up to check for digital vouchers and none is detected, you must manually add a digital voucher to the transaction yourself in order to be able to post the transaction.

> [!NOTE]
> In Denmark, the new Danish Bookkeeping Act makes this check mandatory for Danish organizations that use Business Central online, because Microsoft has registered Business Central online with the Danish Business Authority (Erhvervsstyrelsen) and had it approved as a standard digital bookkeeping system. This effectively means that when located in Denmark, you must somehow add a digital voucher to **Incoming Documents** in order to pass the check and post transactions.

## Enhanced Document Capture functionality

As of Document Capture 2023 R2 Service Pack 2, Document Capture can automatically create digital vouchers for incoming purchase documents based on the Document Capture files (the files that were imported or dragged into Document Capture along with and including the primary purchase document), so that you don't have to manually attach files yourself. When a document is registered as a purchase document or journal, Document Capture will automatically make a copy of all Document Capture files and attach them as digital vouchers under **Incoming Documents**, provided that you set it up to do so. The setup depends on your version of Business Central:

<br>

| Business Central version | How to set up |
| --- | --- |
| [From Business Central April 2019 (BC v14) to BC v23.1](#document-capture-setup-process-for-bc-v14-to-bc-v231) | The feature is configured in the **Document Capture Setup**. |
| [BC v23.2 and later](#document-capture-setup-process-for-bc-v232-and-later) | Document Capture will check the **Digital Voucher Entry Setup** to determine if the feature has been enabled for the type of document that's registered. |

> [!NOTE]
> For all versions of Business Central, an optional feature has been added that enables you to set up Document Capture to create digital vouchers for transactions related to [purchase allocations](@DC-41). This is optional because some organizations regard purchase allocations as purely financial records that don't necessarily need to be documented digitally.

When you enable the feature and register a purchase document, Document Capture will automatically copy all attached files into the **Incoming Documents** FactBox in the open purchase document, where they'll be listed as digital vouchers. This means that the files listed here are by default the same as the ones listed on the **General** FastTab under **Attachments**. However, there's no further link between these two sections, meaning that if you decide to delete a file in either one of them, the other section won't be automatically updated accordingly – the deleted file will still appear here.

To learn more about the setup process, see one of the sections below, depending on your version of Business Central. 

## Document Capture setup process for BC v14 to BC v23.1

To set up Document Capture to automatically create digital vouchers for older versions of Business Central (BC v14 to BC v23.1), follow these steps:

1. Search {{search}} for and select **Document Capture Setup**.
1. On the **General** FastTab, go to **Digital Vouchers**.
1. To enable Document Capture to automatically create digital vouchers from primary purchase documents (such as incoming purchase invoices), select **Create Digital Voucher from Primary Document**.
1. To enable Document Capture to automatically create digital vouchers from any additional attachments as well, select **Include attachments**.
1. If you want Document Capture to automatically create digital vouchers for [purchase allocations](@DC-41), select **Create for Purchase Allocations**.

For all documents that are registered, Document Capture will now create digital vouchers automatically according to your setup.

## Document Capture setup process for BC v23.2 and later

> [!NOTE]
> Document Capture checks the standard Business Central **Digital Voucher Entry Setup** to determine if the digital voucher feature has been enabled for the type of document that's registered. If so, Document Capture automatically transfers all Document Capture files to **Incoming Documents**.

To set up Document Capture to automatically create digital vouchers for [purchase allocations](@DC-41) for new versions of Business Central (BC v23.2 and later), follow these steps:

1. Search {{search}} for and select **Document Capture Setup**.
1. On the **General** FastTab, go to **Digital Vouchers**.
1. Select **Create for Purchase Allocations**.

For all documents that are registered, Document Capture will now create digital vouchers automatically according to your setup.

## Related information

[How to Comply with the Danish Bookkeeping Act](@DC-169)  