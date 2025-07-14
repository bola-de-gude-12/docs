---
title: Setting up the Installment Module in Continia Finance
date: 17-10-2024
description: Learn how to set up scheduled payments.
id: CF-105
lang: en
---

# Setting up the Installment Module

The Installments module simplifies managing scheduled payments by creating, tracking, and managing payments spread across specific periods. You can define whether to include the document type in installment documents and [create various installment templates](@CF-102) with different maturity dates, applicable to both customers and vendors.

To set up the Installment module using the assisted setup:

1. Use the ![Search](https://docs.continia.com/images/search_small.png) icon, enter **Assisted Setup**, and select the related link.
2. In the **Continia Finance** section, select **Set up Installments**.
3. The assisted setup guide will now let you divide posted documents into multiple installments, each with their own due dates. You can easily assign an installment payment template to customers or vendors, or apply it while posting a document. Additionally, you have the option to decide how any remaining amounts will be distributed among the different installments. 

To set up the installment module:

1. Use the {{search}} icon, enter, **Installment Payments Setup**, and select the related link. 

2. On the Installment Payments Setup page, you can configure the following settings:

   | Field                                 | Description                                                  |
   | ------------------------------------- | ------------------------------------------------------------ |
   | Fill Doc. Type in Installment Entries | If enabled, the document type for each new installment entry will be the same as the original document. For example, if an invoice is divided into installments, each installment entry will also be categorized as an invoice. To use this feature, you need to specify either a document number suffix or prefix. If you choose to activate this option, please note that different outcomes may result from the postings. Therefore, we highly recommend that you coordinate with your accountant before proceeding. This option will clear the original invoice by issuing a credit note and reposting installment payment items under the invoice document type. |
   | Document No. Prefix                   | In the designated field, enter a prefix for your document number and increment it accordingly. accordingly. This is necessary only if you want to use the Fill Doc Type in the Installment Entries field and do not want to use a suffix. However, you can also add a prefix without using the document type. <br/>For instance, when posting an invoice, a prefix such as *001-* can be added to each rate. This means that the resulting document number would look like this: 001-RE-2016-0001, 002-RE-2016-0001, 003-RE-2016-0001, and 004-RE-2016-0001. Using the prefix *001-* would allow a maximum distribution of up to 999 rates. |
   | Document No. Suffix                   | Enter a suffix for the document number in the designated field. This will allow you to add up the document numbers accordingly. It is necessary to add a suffix if you want to use the **Fill Doc. Type in Installment Entries** field and do not want to use a prefix. However, you can also add a suffix without using the document type. <br />Example: Posting of invoice INV-2024-0001-1, INV-2024-0001-2, INV-2024-0001-3 |
   | Adjustment Document No. Suffix        | To improve the functionality, it is important to set up both a document number suffix and a clearing entry suffix when the Fill Doc. Type in the Installment Entries field is enabled. This feature adds a sequential suffix to the document number, which helps in better tracking and management. Without this setup, multiple reversals of installment payments are not possible. |
   | Installment Used for Residual Amount  | Specifies whether any residual amount will be automatically added to the first or last installment when an installment template is applied. The options are First position, Last position, or Blank.<br/><br/>When an installment plan template is used and the remaining amount is not zero, the system will calculate and allocate the residual amount to the specified installment. For example, if you have an invoice of €4,000 and split it into three installments, any remainder from the division will be added to either the first or last installment based on your selection. |
   | Check Due Date Order                  | Specifies how the system should handle due date validation for orders. The system can either show an error, display a warning, or ignore the issue if the due date is incorrect or out of sequence. By default, it is set to **Show Error**. |
   
3. On the action bar, select **Installment Templates** to add a template. For more information, refer to the [Adding an Installment Template](@CF-102) article. 

<style>


 .content table tr td:nth-child(1) {
 width: 230px;
 }
 .content table tr td:nth-child(2) {
 width: 570px;
 }
</style>

