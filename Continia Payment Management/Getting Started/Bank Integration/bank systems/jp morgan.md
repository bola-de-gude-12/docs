---
title: JP Morgan
description: Integration with the bank system JP Morgan
date: 07-11-2024
id: PM-361
lang: en
---

# JP Morgan

With Payment Management, you can use manual communication to send bank data between JP Morgan and Microsoft Dynamics 365 Business Central. 

Refer to the general [To set up bank accounts to use manual communication](@PM-3) article for more information about setting it up. 

This article lists the file format requirements for setting up manual communication.

> [!TIP]
>
> Bank system code: 
>
> JPMORGAN (for ACH)
>
> JPM-ACCESS (for CSV)

## File formats

How to integrate your bank with Payment Management depends on the bank communication types and files your bank supports. The table below displays what is supported for manual communication with JP Morgan.  

| Bank communication | Send payments | Import status                                | Update status                                | Import payments                              | Reconcile |
| ------------------ | ------------- | -------------------------------------------- | -------------------------------------------- | -------------------------------------------- | --------- |
| Manual             | ACH or CSV    | <p style="text-align: center;">{{cross}}</p> | <p style="text-align: center;">{{cross}}</p> | <p style="text-align: center;">{{cross}}</p> | MT940     |



