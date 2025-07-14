---
title: Editing dimensions on payments in Advanced Mode
description: Learn how to edit dimension settings using Continia Banking Advanced mode.
date: 07-05-2025
id: CB-240
lang: en
---
# Editing dimensions on payments in Advanced Mode

In Business Central, you can edit dimensions directly on the payment journal line. In [Advanced Mode](@CB-145) within Continia Banking, you have the flexibility to edit dimensions on payments, regardless of whether the payment was created manually or through the payment suggestion feature. Depending on your setup, dimensions can be modified at various stages of the process.

## To edit dimensions when using Summarize per Account
If [Summarize per Account](@CB-89) is enabled in your payment suggestion template, the batch job consolidates entries into one line per account and currency. When summarization is enabled, dimensions are applied to the combined payment. 

To edit dimensions: 
1. On the Payment Card, go to the action bar and select **Actions** > **Dimensions** to access the dimension settings.
2. From there, you can add, remove, or edit the dimensions as needed for each payment.

## To edit dimensions

If payments are handled line-by-line, you can edit the dimensions for each payment suggestion line individually:
1. Open the Payment Suggestion.
2. Navigate to the line and on the Lines action bar select **Dimensions** action to modify the dimensions applied to the summarized payment.

## To edit dimensions after journal lines have been created
After journal lines have been generated from the suggestion, you can still edit dimensions:
1. Go to the **Payment Journal**.
2. Use the action **Prepare > Edit Payment Suggestion**.
3. This opens a Payment Suggestion Card for the selected line and on the Lines action bar you can now select **Dimensions** action to modify the dimensions applied to the summarized payment.

