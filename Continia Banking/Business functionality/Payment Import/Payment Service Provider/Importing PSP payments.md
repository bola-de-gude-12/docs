---
title: Importing PSP payments in Continia Banking
date: 02-04-2025
description: Describes how to import payments from a third-party service provider in Continia Banking.
id: CB-209
lang: en
---

# Importing PSP payments

Continia Banking lets you import payments from payment service providers (PSPs) using different [PSP agreements](@CB-181) to set up the bank account and the import rules. This way, you can easily import data from third-party service providers such as marketplaces and payment services and don't have to enter the data for each payment manually.

>  [!IMPORTANT]
>
> Only users with the CTS-CB ADMIN, CTS-CBCP ADMIN, and CTS-PP ADMIN permission set can create PSP agreements and import PSP files.

To set up a cash receipt journal for PSP payments:

1. Search ({{search}}) for and select **Cash Receipt Journals**.
2. Navigate to the **Batch Name** field and click the three dots to open the **General Journal Batches** page.
3. Locate the journal that you want to use for importing, then enable **Payment Service Provider Journal**. If you have not set up an [agreement for the PSP](@CB-181), you will be prompted to do so. 
4. On the action bar, select **Home** > **Import (Existing) PSP Payments**.
5. On the **Import Payments** dialog, in the **PSP Agreement** field, select the PSP agreement that you want to import payments for. By default, the PSP agreement is filled in. Optionally, you can add a manual document number and specify that you want a balance account line to be created per posting date. Select **Ok** to continue.
6. You are now prompted to select the file for import. Continia converts the file and sends the data to [Continia Transaction Ports](@CB-134), making it possible to import the data to the Cash Receipt Journal.

> [!TIP]
>
> For an overview of the total amount for different customers, bank accounts, currency codes, and G/L accounts, on the action bar, select **Actions** > **Journal Statistics** to open the statistics page.

## Related information

[Adding a Payment Service Provider Agreement](@CB-181)   
[Payment Service Providers](@CB-128)



