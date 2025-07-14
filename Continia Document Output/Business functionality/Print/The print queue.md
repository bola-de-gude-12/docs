---
title: The Print Queue
date: 01-12-2022
description:
id: DO-51
lang: en
---

# The Print Queue

The Print Queue provides the ability to print, along with Document Output Service, which is otherwise not possible using a cloud-based solution. 

The Print Queue can be compared to a print queue on an locally installed printer, and in Document Output, The Print Queue displays all documents picked up by the Output Profiles  **Print** and **Email and Print** that havn't been printed yet. 

You can also configure directly on an email template if emails sent using this template will be printed, meaning sent to the Print Queue for printing. You do this by opening an email template, and in the **General FastTab**, in the **On Email (SMTP)** field, you select either **Print** or **Email and Print**. If you can't see the **On Email (SMTP)** field, then select **Show more** in the upper right-hand corner.

The Print Queue also helps you troubleshoot problems if any print job fails and the entry remains in the queue.

Documents forwarded to the Print Queue are printed immediately, so there's no need to create a job queue to run the Print Queue automatically.

Email jobs attached to a specific document type will initially send all documents to the Document Queue, and documents that aren't set to be sent as emails are forwarded to the Print Queue or the Outgoing Network Documents queue, depending on the Output Profile on the documents.

>  [!NOTE]
>  The Print Queue should print all documents in the queue automatically. If the queue contains documents that aren't printed, it's very likely that there's a problem with the printer, such as empty paper trays or toner cartridges, or the printer is offline.
