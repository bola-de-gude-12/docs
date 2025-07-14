---
title: Nordea US
description: Integration with the bank system Nordea US
date: 28-11-2023
id: PM-358
lang: en
---

# Nordea US

With Payment Management, you can use manual communication to send bank data between Nordea US and Microsoft Dynamics 365 Business Central. 

This article lists the file format requirements for the manual communication method. To learn more about how to set up manual communication for Nordea US, refer to the [Setting up bank accounts](@PM-3#to-set-up-bank-accounts-to-use-manual-communication) article.

> [!TIP]
>
> Bank system code: NACHA



## File formats

How you can integrate your bank with Payment Management depends on the types of bank communication and files your bank supports. The table below displays what is supported for manual communication with Nordea US.  


| Bank communication | Send payments| Import status | Update status | Import payments| Reconcile|
| --- | --- | --- | --- | --- | --- |
| Manual | NACHA | Not supported | Not supported | Not supported | MT940/BAI |



## To connect to Nordea US 

To connect with Nordea US, several manual setup steps are required to configure the Nacha ACH and BAI formats.

To set up the Nacha ACH and BAI format for Nordea US manually: 

1. Use the {{search}} icon, enter **Bank System**, and select the related link.
2. Select **New**. 
3. In the **Code** field, enter NDEA-NACHA. 
4. Open the NDEA-NACHA Bank System card, and on the action bar, select **Import Setup** > **From Continia Online**.  
5. Use the {{search}} icon, enter **Banks**, and select the related link.
6. Select **New**. 
7. On the Banks page, enter the following information:
   * **Name**: NORDEAUS
   * **Manual**: NDEA-NACHA 
   * **Payment Export**: Manual 
   * **Account Statement Import**: Manual 
   * **Bank Account Statement File Format**: BAI 
8. Use the {{search}} icon, enter **Bank Accounts**, and select the related link.
9. Open the bank account card and set up the following field: 
   * **Bank Code**: NORDEAUS 

Payments can now be exported in Nacha ACH format, and account statements can be imported in BAI format for specific bank accounts.

 

