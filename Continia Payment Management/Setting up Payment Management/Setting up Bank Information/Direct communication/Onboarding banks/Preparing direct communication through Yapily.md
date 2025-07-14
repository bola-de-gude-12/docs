---
title: Preparing for Direct Communication Through Yapily
description: How to grant permissions to Yapily for different banks. 
date: 24-05-2024
id: PM-397
lang: en
---

# Preparing for Direct Communication Through Yapily

{{include "yapily-fees"}}

To integrate with your United Kingdom-based bank, Payment Management uses Yapily, a secure open banking API that offers payment services and enriched financial data. Before you can establish direct communication with your UK bank through Yapily, it is necessary to grant Yapily the required permissions. Once you granted Yapily permissions, you can set up direct communication. For more information on how to do that, refer to the steps outlined in [Onboarding Yapily with direct communication](@PM-268) article.

As each bank manages third-party access differently, the table below provides specific instructions and links for granting permissions for each bank. This information is subject to change, so when in doubt, please contact your bank for further assistance. If your bank is not listed, please refer to your bank for more information on how to grant permissions to Yapily. 

| Bank                   | Permission granting instructions                             |
| ---------------------- | ------------------------------------------------------------ |
| HSBC                   | <ol><li>Log in, open the **Permissions** tab, and in the left panel, select **Additional banking services** > **Third party provider authorisation**. </li><li>For the **Manage third party provider authorisation** row, now select the **Enquire**, **Consent**, and **Revoke** checkboxes.</li></ol> |
| Barclays               | Refer to the [How do I give my permission to a TTP](https://www.barclaycard.co.uk/business/help/making-payments/how-do-i-give-my-permission-to-a-third-party-provider-tpp-to-access-my-account) article on Barclay's website. To obtain third-party access permissions at Barclays, users need to be assigned a pre-built permission set. This permission set must be allocated and approved by the bank's system administrators. Typically, it consists of 4 or 5 different permission sets. For specific details and assistance, it is recommended to contact Barclays directly. |
| NatWest                | Download [Natwest's instructions in PDF](https://www.natwest.com/content/dam/natwest_com/Business_and_Content/PDFs/2020-05-13NWBBanklineTPPGuidesMayFinalHRV02.00.pdf). |
| Ulster Bank            | Download [Ulster Bank's instructions in PDF](https://www.ulsterbank.co.uk/content/dam/Ulster/documents/ni-region/ni-business-banking-brochures/2020-05-13UBNBanklineTPPGuidesMayFinalHRV02.00.pdf). |
| Royal Bank of Scotland | Download [Royal Bank of Scotland's instructions in PDF](https://www.rbs.co.uk/content/dam/rbs_co_uk/Business_and_Content/PDFs/2020-05-13RBSBanklineTPPGuidesMayFinalHRV02.00.pdf). |
| Virgin Money           | Refer to the [How can I consent to a Third-Party-Provider](<https://gethelp-nft.virginmoney.com/helptopic/subtopic/pagecontent/article/KA-01229/?How-can-I-consent-to-a-Third-Party-Provider-(TPP)?>) article on Virgin Money's website. |



> [!NOTE]
>
> To connect banks through Yapily, you must have Business Central version 22 or higher.

<style>

 .content table tr td:nth-child(1) {
 width: 200px;
 }
 .content table tr td:nth-child(2) {
 width: 600px;
 }
</style>

