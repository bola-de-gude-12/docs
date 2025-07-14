---
title: System.Net.Mail.SmtpClient.Send Failed With an Error Message
date: 30-11-2023
description:
id: DO-153
lang: en
---

# System.Net.Mail.SmtpClient.Send Failed With an Error Message

## Question

System.Net.Mail.SmtpClient.Send failed with the following message:

*A call to System.Net.Mail.SmtpClient.Send failed with the following message. A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond [IP address and port number]*

What do I do?

## Answer

The error occurred because the mail server connection timed out, likely due to a restriction on the number of emails you can send per minute.

To solve the issue in a *cloud* installation, follow these steps:

1. Open **Document Output Setup**.
2. Look for **Max no. of mails per minute** in the **General** FastTab.
3. Enter **29** in this field.

To solve the issue in a *on-premises* installation, follow these steps:

1. Open **Document Output SMTP Setup**.
2. Look for **Max no. of mails per minute** in the **General** FastTab.
3. Enter **29** in this field.

This adjustment will help prevent the error in the future. By setting the connection timeout to 29, you ensure a smoother email sending process.