---
title: Bank of Scotland and Payment Management
description: PM integration with the bank system Bank of Scotland
date: 26-02-2024
id: PM-284
lang: en
---

# Bank of Scotland

With Payment Management, you can use direct communication to send bank data between Bank of Scotland and Microsoft Dynamics 365 Business Central. For direct communication between your bank and Microsoft Dynamics 365 Business Central, Payment Management collaborates with Yapily, an Open Banking payment service provider. 

This article lists the file format requirements for direct communication. To learn more about how to set up communication with Bank of Scotland, refer to the [Onboarding Yapily to use Direct Communication](@PM-268) article.

> [!NOTE]
>
> Connecting banks through Yapily is only supported for Business Central version 24 or higher.

## File formats

How to integrate your bank with Payment Management depends on the bank communication types and files your bank supports. The table below displays what is supported for direct communication with Bank of Scotland.  

| Bank communication | Send payments  | Import status                                 | Update status  | Import payments                              | Reconcile      |
| ------------------ | -------------- | --------------------------------------------- | -------------- | -------------------------------------------- | -------------- |
| Direct             | Yapily Connect | {<p style="text-align: center;">{{cross}}</p> | Yapily Connect | <p style="text-align: center;">{{cross}}</p> | Yapily Connect |



## Related information

[About direct and manual bank communication](@PM-158)  
