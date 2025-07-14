---
title: Importing PSP payments
date: 23-11-2022
description: Describes how to import payments from a third-party service provider
id: PM-299
lang: en
---

# Importing PSP payments

Payment Management lets you import payments from payment service providers (PSPs) using different [PSP agreements](@PM-298) to set up the bank account and the import rules. This way, you can easily import data from third-party service providers such as marketplaces and payment services and don't have to enter the data for each payment manually.

>  [!IMPORTANT]
>
> Only users with the CPM365 ADMIN, SUPER, or CPM PSP IMPORT permission set can create PSP agreements and import PSP files.



To import payments from payment service providers:

1.	Use the ![Search for page or report](/images/search_small.png) icon, and search for **Cash Receipt Journals**, then select the related link. Alternatively, from the top action bar, select **Cash Management** > **Cash Receipt Journal**. 
2.	To ensure third-party payments are allowed for the journal, navigate to the **Batch Name field** and select the three dots.
3.	On the **General Journal Batches** dialog, navigate to the **Payment Service Provider Journal** column. This column must be selected for PSP payments to be possible.
4.	Open the relevant journal, and select **Import Payments**. If you have not set up an [agreement for the PSP](@PM-298), you will be prompted to do so. 

5.	On the **Import Payments** dialog, in the **PSP Agreement** field, you can select the PSP agreement that you want to import payments for. By default, the PSP agreement is filled in. Optionally, you can add a manual document number and specify that you want the account lines to be created per posting date. Select **Ok**.
6.	You are now prompted to select the file for import. Continia converts the file and sends the data to Continia online, making it possible to import the data to the Cash Receipt Journal in Microsoft Dynamics 365 Business Central.

> [!TIP]
>
> For an overview of the total amount for different customers, bank accounts, currency codes, and G/L accounts, you can use the statistics page. On the action bar, select **Actions** > **Journal Statistics** to open it.



 

## Related information

[Adding a Payment Service Provider Agreement](@PM-298)

[Payment Service Providers](@PM-300)



