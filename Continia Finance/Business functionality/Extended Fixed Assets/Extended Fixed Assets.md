---
title: Extended Fixed Assets in Continia Finance
date: 08-10-2024
description: Learn about the settings of the Extended Fixed Assets module.
id: CF-09
lang: en
---

# Setting up the Extended Fixed Assets Module

Continia Finance brings enhanced functionality to the Fixed Asset module, allowing more effective management of your long-term, revenue-generating assets like buildings, vehicles, and machinery.

This module automates value adjustments by altering depreciation rates, offers asset template utilization during asset acquisition, and enables separate posting of acquisition costs or sales for precise financial tracking.

## Set up the Extended Fixed Assets module using the assisted setup

1. Choose the {{search}} icon, enter **Assisted Setup**, and select the related link.
2. In the **Continia Finance** section, select **Set up Ext. Fixed Assets**.
3. The wizard lets you manage your assets by quantity, as well as distinguish between sale and scrapping when disposing of them. Additionally, partial disposals can be booked efficiently in the module – with the system handling all required transactions in a single step. To create fixed assets, you can add templates. 

## Set up Extended Fixed Assets

1. Choose the {{search}} icon, enter **Extended Fixed Asset Setup**, and select the related link.

2. On the **General** FastTab, you find various settings that can be applied:

   | Field                                                        | Description                                                  |
   | ------------------------------------------------------------ | ------------------------------------------------------------ |
   | Fixed Asset Template Nos.                                    | Select a number series for the fixed asset templates.        |
   | Use Rounding Book Value in Periodic Depreciation             | Enable this to round the book value for depreciation postings. The depreciation amounts ensure a rounded book value for periodic depreciation and postings generated when **Depreciation until FA Date** is activated. This is considered during the first depreciation posting. |
   | Clear FA No. when Reverse Transaction                        | If enabled, the system generates a reversal entry for transaction reversals – instead of creating a negative acquisition entry, which could lead to accounting discrepancies. |
   | Print Alternating Shading                                    | When you activate alternating shading, it shades alternate lines in a subtle grey, significantly improving the legibility and focus on individual lines. |
   | Colored Hyperlinks in Reports                                | If enabled, the master data records are underlined in distinct colors – serving as interactive links to their corresponding reports. |
   | Set VAT for Correction Disposal or Acquisition               | If enabled, the original posting groups are included in the journal when a sale is reversed. |
   | Insert Customer or Vendor for Correction Disposal or Acquisition | If enabled, the system automatically generates a line item for the offset account (customer) when a sale is reversed. |
   | Set Error Entry No. in Credit Memo                           | Specifies whether to assign an error entry number when processing a credit memo. If enabled, the system logs the reversal with an error entry number – ensuring that the reversal of the asset sale is tracked accurately. |
   | Use Duplication List                                         | Indicates that if the type is Fixed Asset, the details on the line are posted to all specified depreciation books for the assets |
   | Post Copies Automatically                                    | Enables automatic posting of parallel entries for additional depreciation books. In international companies, for example, depreciation may need to be posted according to both local regulations and the parent company's requirements – making it possible to use multiple depreciation books. |
   | Automatically Post Duplicates to the G/L integrated Depreciation Book | When activated, acquisition and sale transactions are also posted to other depreciation books integrated with financial accounting. |
   | Do not use FA Allocations                                    | If enabled, the dimension distribution from the asset card isn't applied. This is useful, for example, when you want to include the distribution in imputed depreciation – but exclude it from financial accounting depreciation. |

3. On the **Acquisitions** FastTab, you can use the following settings:

   | Field                                                        | Description                                                  |
   | ------------------------------------------------------------ | ------------------------------------------------------------ |
   | Pmt. Discount on Acquisition Costs                           | If enabled, the system deducts payment discounts from fixed asset acquisition values during invoice payment. If there are multiple fixed assets or mixed items in the invoice, the discount is distributed accordingly. If you reverse the invoice application, the Fixed Assets area's cost corrections, including acquisition and depreciation, are reversed too.<br/><br/>Note that using the **Unapply** function does not affect the system's automatic depreciation posting on the payment date. However, any depreciation posted between invoice payment and asset acquisition is corrected accordingly. |
   | Depr. until FA Posting Date                                  | If enabled, the corresponding field in the journal line or the purchase document is activated for additional acquisition postings. This means a depreciation posting is performed on the asset acquisition date. <br />This feature is only activated for further acquisitions if the depreciation posting has occurred. If no prior depreciation posting exists, it is unnecessary because the next depreciation run writes off the entire acquisition cost from the starting date of regular depreciation. |
   | Depr. Acquisition Cost                                       | Indicates whether the additional acquisition cost recorded on this line has been depreciated in relation to the depreciation that has already been applied to the fixed asset at the time of posting. Fixed asset acquisition costs include the purchase price and any additional expenses necessary to acquire the asset and prepare it for its intended use, such as delivery and handling charges, installation costs, and legal fees.<br/><br/>For example, if a fixed asset is activated on 15 January and a second invoice related to the acquisition cost is received in March, the depreciation acquisition cost field can be used to retroactively align the depreciation start date with the original activation date of 15 January. This adjustment applies only to costs incurred within the same year. Therefore, if the fixed asset was activated in November and the next invoice is received in January of the following year, the new acquisition cost doesn't retroactively apply to the November activation. |
   | Check Depr. Date of Previous Month for Corr. Acquisition Costs | This setting prevents a subsequent acquisition posting if no depreciation was recorded in the previous month. If enabled, users receive a note or error message prompting them to complete the previous month's depreciation run before proceeding with the acquisition posting to ensure accurate depreciation calculations. If the subsequent acquisition occurs in a new fiscal year and no depreciation has been recorded by the end of the prior year, the system issues an error message instead of a note.<br/><br/>For example, if a fixed asset (such as an electric car) was activated in January, and an additional component (like a supplemental battery pack) is purchased in November, the system checks if depreciation has been recorded for the previous month. If depreciation has not been booked and this field is enabled, the system generates an error indicating that depreciation must be posted before proceeding with the acquisition. |
   | Revise Depreciation Date for Correct Acquisition Costs       | This setting prevents a subsequent acquisition posting if depreciation has already been recorded with a later date. When enabled, an error message notifies the user that the depreciation posting must be reversed before the acquisition can be processed. This ensures that the correct depreciation amounts are calculated for each month.<br/><br/>For example, if depreciation for March has already been posted, and an invoice for the same fixed asset is received after the depreciation has been booked, the system generates an error upon attempting to post the acquisition. Depending on the legislation in your country, possible actions include either deleting the March depreciation for the fixed asset or postponing the acquisition posting to April. |
   | Copy Line Descr. to G/L Entry and FA Entry                   | Indicates that the description from document lines of type Fixed Asset is automatically transferred to the corresponding entries in the general ledger (G/L) and fixed asset ledger. If enabled, the line description is consistent across both ledgers. |

4. On the **Disposal** FastTab, you can set the following options:

   | Field                                        | Description                                                  |
   | -------------------------------------------- | ------------------------------------------------------------ |
   | Depreciation until FA is Posted for Disposal | If enabled, the system automatically sets the creation date as the depreciation date for sales postings. |
   | Reclassification of Journal Template         | Specifies the reclassification journal template utilized for processing partial disposals. |
   | Reclassification of Journal Batch            | Indicates the reclassification journal batch designated for posting partial disposals. |
   
   

<style>

 .content table tr td:nth-child(1) {
 width: 80px;
 }
 .content table tr td:nth-child(2) {
 width: 520px;
 }
</style>
