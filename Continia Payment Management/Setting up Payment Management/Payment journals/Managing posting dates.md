---
title: Managing posting dates
description: Information on how to manage the posting dates on the payment journal
date: 29-11-2021
id: PM-212
lang: en
---

# Managing posting dates

The posting dates stated on the payment lines in the Payment Journal specify when the vendor or employee payments are to be processed in the bank. The posting dates are generated based on your settings for the payment journal. For example, you can specify if the due date should be used to calculate the posting date for the generated payment lines, using the actions **Calculate Posting Date from Applies-to-Doc Due Date** and **Applies-to-Doc Due Date Offset**.

## Updating the posting date

You can specify how Payment Management should manage the posting dates in case payments can't be processed on the dates specified for the payment lines. To specify the settings for payments that are set to be posted on a bank holiday, see [Setting up Bank Holidays](@PM-7). 

In some cases, payments will not be processed by the bank in accordance with the posting date stated in the Payment Journal. If you are communicating with the bank using direct communication, a status file can be imported from the bank with the actual posting date, making it possible for Payment Management to update the posting dates on the payment journal lines in accordance with the status file received from the bank. To use this feature your bank must support posting dates in status files, and the **Allow Updating Posting Date** action must be turned on from the **Payment Management Setup** page.

