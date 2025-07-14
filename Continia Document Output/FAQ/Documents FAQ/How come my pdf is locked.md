---
title: Document Output How come my pdf is locked when I send it out
date: 06-07-2023
description: Learn how not to encrypt your PDF files. 
id: DO-100
lang: en
---

# Why is my PDF locked?

## Question

Why is my PDF locked when I send it out? In Business Central, it seems to open without prompting for a password. 


## Answer

Sending emails with unprotected PDF file attachments poses a significant vulnerability. To address this issue, you can enhance security by protecting PDF files with a password shared exclusively with the intended recipient. This can be achieved by [assigning PDF passwords for specific templates and individual customers](@DO-35).

If you prefer not to encrypt your PDF files, or if you just want to check if a PDF password is assigned, check the following:

1. Firstly, check if the email template or customer card has a password protection feature enabled:

   * Go to **Email Templates**, and select the email template. In the **General** FastTab, under **Advanced**, see whether a password has been added to the **PDF Password** field. If a password has been added, the PDF can only be opened using this password after the PDF has been sent out.
   * Open the customer card, navigate to the **Document Output** FactBox, and select the three dots next to the **Output Profile** field. In the **General** FastTab, see whether a password has been added to the **PDF Password** field. If it is, this password will be used for documents sent to this customer.

2. Additionally, ensure that your email browser (e.g., Chrome, Edge, Firefox) doesn't automatically fill in password fields. 

   

   
