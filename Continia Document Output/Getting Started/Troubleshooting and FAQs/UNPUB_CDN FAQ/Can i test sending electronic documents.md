---
title: Can I Test Sending Electronic Documents Through the Continia Delivery Network?
date: 22-04-2024
description: Learn why you cannot send documents through CDN in a sandbox environment. 
id: DO-162
lang: en
---

# Can I Test Sending Electronic Documents Through the Continia Delivery Network?


## Question
Can I test sending electronic documents through the Continia Delivery Network?

## Answer

Due to regulations and the fact that the Continia Delivery Network is a live system, it is not permitted to send test documents. 

What you can do, though, is to post an invoice and set up your Output Profile in a way that allows you to either send the XML document as an attachment to an email, or you can download the XML file. The XML file in the email attachment/downloaded file and the XML file that would be sent through the Continia Delivery Network is, for all practical intents and purposes, the same. 

If you need to test sending out an electronic sales invoice with a specific protocol such as Peppol or OIOUBL, then you do that by modifying a codeunit.

Follow these steps: 

1. Open e-document setup 
2. Choose the protocol you want to test, for example Peppol 
3. Under the submenu Salesinvoice, remove the codeunit from salesinvoice delivery 
