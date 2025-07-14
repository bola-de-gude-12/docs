---
title: Matching documents using a job queue in Document Capture
date: 16-06-2025
id: DC-479
description:  
lang: en
---

# Matching documents using a job queue

Automatic matching is occasionally blocked or hindered by other business processes. For example, a delayed delivery of goods can make it impossible for Continia Document Capture to automatically match an invoice against a goods receipt if the goods receipt doesn't yet exist when the invoice is received by your accounts payable department. In such cases, running the so-called "batch match" job queue is convenient, as it will attempt to carry out the automatic matching repeatedly at regular intervals. In the above example, the job queue would ensure that once the goods had finally arrived, the invoice would be matched against its corresponding goods receipt.

To run this job queue, you'll need to run codeunit 6086022 **CDC Batch Match Documents**. For more information on how to set up the job queue, see [Setting up job queues](/Continia Document Capture/Setting up Document Capture/Setting up general business functionality/Setting up job queues.md).
