---
title: Document Queue
date: 08-04-2024
description:  
id: DO-72
lang: en
---

# Document Queue
The Document Queue is a list of documents that are ready to be sent using Document Output. When an item is listed in the Document Queue you can see the Business Central document it originates from and, if needed, go directly to the source record for more information. It's also possible to see the email template that will be used with each item on the list. 

The Document Queue list will only display documents that are ready to be emailed. If documents are marked with the Document Output profile **Print**, the document is automatically forwarded to the **Print Queue**, or the **Outgoing Network Documents** if the Output Profile is configured for XML files.

The pre-configured email job queue is configured to automatically dispatch all entries in the Document Queue list. The job queue entry running Object ID 6175283 is automatically configured to run email jobs every minute as default.

If it's not enabled, all documents that are ready to be sent will remain in the **Document Queue** to be manually dispatched.
<br>
<br>
<iframe src="https://player.vimeo.com/video/893357464?h=2ea0d9b615&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" width="560" height="315" frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" title="DO Learn_3a Send with the Document Queue"></iframe>

This video is part of the course [Get started using Document Output](https://learn.continia.com/get-started-using-document-output) on Continia Learn.