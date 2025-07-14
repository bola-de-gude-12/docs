---
title: Adding a Payment Service Provider
date: 23-11-2022
description: Describes how to set up a PSP.
id: PM-298
lang: en
---

# Adding a Payment Service Provider

Payment Management supports file imports from third-party Payment Service Providers (PSPs) such as eCommerce marketplaces (e.g., Amazon and bol.com) and payment services (e.g., Paypal and Klarna). You can [import the customer payment files](@PM-299) directly from the PSP into the cash receipt journal.     

Payment Management comes with preset PSPs for which you can add agreements. PSP agreements help you distinguish between different payment streams for a PSP. For example, if for the same PSP, other bank accounts or G/L accounts for posting fees apply. 

> [!TIP]
>
> We are continuously working on adding support for new payment service providers. If your preferred PSP is not listed, please get in touch with us to learn more about the possibilities.



The following information is available for every PSP:

| **Field**      | **Description**                                              |
| -------------- | ------------------------------------------------------------ |
| Code           | Specifies the code that identifies the payment service provider. |
| Description    | Description of the payment service provider.                 |
| File Format    | Displays the appropriate file format that is imported. The options are XML, Excel, and Text. |
| PSP Agreements | Displays the number of PSP agreements the payment service provider has. Select to view PSP agreements or to add one. |

> [!NOTE]
>
> You must set up at least one PSP agreement to import files from a PSP.



## To set up the External Payment Reference

Before adding a PSP agreement, you must apply a few general settings related to the External Payment Reference field in the Payment Management setup. This field is added to sales documents and customer ledger entries and is used to find the unique PSP entry references to apply for payments or refunds during the import.

> [!IMPORTANT]
>
> Only users with the CPM365 ADMIN, SUPER, or CPM PSP IMPORT permission set can create PSP agreements and import PSP files.



To apply External Payment Reference field settings to prepare to add a PSP agreement:

1. Use the ![Search for a page or report](/images/search_small.png) icon, search for **Payment Management Setup**, and select the related link.

2. Navigate to the FastTab **Payment Receipt Import**, and enter information for the following fields:

   * **Update External Payment Reference** - select what field to use as the reference number on sales documents. You can choose from the following options: **Using Custom Field**, **Using Your Reference**, **Using External Document No.** 
   * **Custom External Payment Reference Field Name** - If you selected **Using Custom Field** in the Update External Payment Reference field, select the appropriate field from the Sales Header table.

   Payment Management now prompts you to update External Payment Reference in not posted sales documents and open the customer ledger entries. 

   

   

## To add a PSP Agreement

PSP agreements help you distinguish between the different payment streams for a PSP. For example, if for the same PSP, other bank accounts, or different G/L accounts for posting fees apply. 

To set up a PSP agreement for a payment service provider:

1. Use the ![Search for page or report](/images/search_small.png) icon, search for PSP Agreement Setup, and select the related link. 
2. On the **PSP Agreement** page, select a new line and enter information for the following fields, and then select **Next**:

| **Field**                | **Description**                                              | Required field                           |
| ------------------------ | ------------------------------------------------------------ | ---------------------------------------- |
| Name                     | Enter a name for the PSP agreement.                          | Yes                                      |
| Payment Service Provider | Select the PSP code to connect the PSP agreement to the correct payment service provider. | Yes                                      |
| Bank Account No.         | Select the bank account number to use as the Balancing Bank Account in Cash Receipt Journal lines. | Yes                                      |
| Default Customer No.     | Specify the customer number that is used for not applied journal lines. | No                                       |
| Default Currency Code    | Specify the currency code that should be applied if no currency code is set in the file. | No<a href="#footnote-1"><sup>1</sup></a> |
| Merge Fees               | Select the Merge Fees checkbox if you want to merge lines with the same fees and same posting date. This is convenient if you don't need to view all the lines in detail. Additional benefit is improved performance as merging the fees can lead to faster import. <br />You must clear the Merge Fees checkbox if you want to apply invoice dimensions to the fees, as these won't work if Merge Fees is active. | No                                       |

<small style>

<div class="footnotes">

 <hr />

 <ol>

 <li id="footnote-1">Some PSP settlement files don't have a currency indication. In that case, the Default Currency Code field is mandatory and will be used to determine the currency.</li>

 </ol>

</div>

</small>



3. Continia adds default rules for fees and other charges in the PSP Agreement Rule Template for every PSP. This way, fees, and additional costs can be easily separated. The following fields apply:

| **Field**                        | Description                                                  |
| -------------------------------- | ------------------------------------------------------------ |
| Account Type                     | Select the account type you want to apply the rule to. For example, *G/L account*. |
| Account No.                      | Specifies the account no. that the application rule applies to. Required field. |
| Search Text                      | Specifies the text to search for to identify a match in the journal lines. For example, *shipping costs*. |
| Search Principle                 | Specifies how the search is applied. The options are **Exact**, **From Left**, **From Right**, and **Within**. For example, select Within if you know the PSP positions the commission correction someplace in the description. |
| Search in Description            | Select if you want to apply search to the description field of the payment line. For example, if you know the PSP adds the commission correction to the payment description. |
| Search in Additional Information | Select if you want to apply search to the additional information of the cash receipt journal line. |

You have the following options:
* To apply all default rules: enter an Account No. for all the rules. 

* To deselect some of the rules, navigate to the Search in the Description column and deselect the rule(s) you don't want to use. Make sure to enter an Account No. for all the rules. 

  > [!NOTE]
  >
  > The PSP Agreement Rule template for every PSP is intended to cover all invoice fields you may want to separate. You can set up a custom rule if the field you require is not represented in the rule template.

4. Select **Finish** to complete the setup or **Next** to return to the PSP Agreement page to add another agreement.

> [!TIP]
>
> Optionally, for every PSP Agreement, you can set dimensions used in every journal line. This way, you can group posted PSP entries for analysis and reporting purposes. To add dimensions for the PSP agreement: on the PSP Agreement Setup page, on the action bar, select **Manage** > **Dimensions**.



## Related information

[Importing PSP payments](@PM-299)

[Payment Service Providers](@PM-300)



