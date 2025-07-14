---
title: Handelsbanken Global Online
description: Integration with the bank system Handelsbanken
date: 08-08-2022
id: PM-137
lang: en
---

# Handelsbanken GlobalOn-Line

With Payment Management, you can use direct or manual communication to send bank data between Handelsbanken GlobalOn-Line and Microsoft Dynamics 365 Business Central. 

This article lists the file format requirements for both communication methods. 

To learn more about how to set up direct or manual communication:

* Direct communication Handelsbanken GlobalOn-line - refer to the [Onboarding Handelsbanken GlobalOn-Line with Direct Communication](@PM-181) article.
* Manual communication Handelsbanken GlobalOn-line - refer to the general [To set up bank accounts to use manual communication](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article. 

> [!IMPORTANT]
>
> If you choose direct communication, make sure to use the bank system code: HBISO20022



## File formats

How to integrate your bank with Payment Management depends on the bank communication types and files your bank supports. The table below displays what is supported for direct and manual communication with Handelsbanken GlobalOn-Line.

| Bank communication | Send payments                | Import status                | Update status                | Import payments                                              | Reconcile                    |
| ------------------ | ---------------------------- | ---------------------------- | ---------------------------- | ------------------------------------------------------------ | ---------------------------- |
| Manual             | [PAIN.001](@PM-123#PAIN.001) | Not supported                | Not supported                | [CAMT.054C](@PM-123#CAMT.054C) [PBS Sector](@PM-123#PBS) [BG Max](@PM-123#BGMAX) [OCR-NO](@PM-123#OCR-NO) [Total IN](@PM-123#Total-IN) | [CAMT.053](@PM-123#CAMT.053) |
| Direct             | [PAIN.001](@PM-123#PAIN.001) | [PAIN.002](@PM-123#PAIN.002) | [CAMT.052](@PM-123#CAMT.052) | [CAMT.054C](@PM-123#CAMT.054C) [PBS Sector](@PM-123#PBS) [BG Max](@PM-123#BGMAX) [OCR-NO](@PM-123#OCR-NO) [Total IN](@PM-123#Total-IN) | [CAMT.053](@PM-123#CAMT.053) |



## Related information

[About direct and manual bank communication](@PM-158)

