---
title: Setting up custom payment service providers
date: 09-07-2025
description: Learn how to set up a custom PSP integration using Continia's transaction ports and PSP agreements.
id: CB-255
lang: en
---

# Setting up custom payment service providers

Continia Banking includes preconfigured support for several well-known payment service providers (PSPs) such as PayPal, Klarna, and Adyen. If you're working with a PSP that isn't supported by default, you can configure Continia Banking to manually import payment files from that provider. This article guides you through the process of setting up a custom PSP integration using Continia's transaction ports and PSP agreements.

## Step 1: Analyze the payment file

Start by reviewing the PSP’s file structure. For example, identify:

- Delimiters (e.g., comma, semicolon)
- Column headers (e.g., Amount, Date, Reference)
- Data formats (e.g., date format, decimal separator)

For more information, see the [To analyze the file](@CB-134#to-analyze-the-file) section in the *Introducing transaction ports* article. 

## Step 2: Set up a transaction port

Create a transaction port to define how the fields in your file map to Business Central.

- Define the column structure and field separators.
- Map each column to a relevant Business Central field (e.g., transaction amount, account number, payment text).

For more information, see the [Setting up transaction ports](@CB-124) article.

## Step 3: Add the Payment Service Provider

Before you can configure payment file imports for a custom PSP, you need to add the provider to Continia Banking. This involves creating a new entry with basic details such as the code, description, and transaction port. 

Add your Payment Service Provider:

1. Search ({{search}}) for and select **Payment Service Providers**.
2. On the action bar, select **New**.
3. Enter the **Code**, **Description**, and **Transaction Port**.


## Step 4: Create a PSP agreement

Link the custom transaction port to a **PSP agreement**. This allows you to:
- Assign G/L accounts for fees, shipping costs, or commissions.
- Group and organize payment data from the specific PSP.

For more information, see the [Setting up a payment service provider](@CB-181) article.

## Step 5: Import the payment file

Once set up:
- Go to the **Cash Receipt Journal**.
- Select the appropriate PSP agreement.
- Import the file and apply transactions.

For more information, see the [Importing PSP payments](@CB-209) article