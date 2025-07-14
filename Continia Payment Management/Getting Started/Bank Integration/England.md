---
title: United Kingdom and Payment Management
description: Supported banks in the United Kingdom
date: 24-03-2025
id: PM-102
lang: en
---
# United Kingdom

{{include "pm-bank-information-country-introduction" "United Kingdom"}}

<br>

> [!TIP]
>
> We are continuously adding support for new banks. If your preferred bank is not listed, please contact us to learn more about the possibilities.

| Bank | Manual communication | Direct communication |
| --- | :-: | :-: |
| [Allied Irish Banks](@PM-277) | {{cross}} | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| [Barclays](@PM-222) | {{checkmark}} | {{checkmark}} |
| [Coutts and Company](@PM-279) | {{cross}} | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| [Danske Bank](@PM-118) | {{checkmark}} | {{checkmark}} |
| [DNB](@PM-122) | {{checkmark}} | {{checkmark}} |
| [HSBC](@PM-285) | {{checkmark}} | {{checkmark}} |
| [JP Morgan](@PM-361) | {{checkmark}} | {{cross}} |
| [Lloyds Business](@PM-286) | {{cross}} | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| [Natwest](@PM-287) | {{checkmark}} | {{checkmark}} |
| [Nordea (Corporate Netbank)](@PM-140) | {{checkmark}} | {{cross}} |
| [Royal Bank of Scotland](@PM-349) | {{checkmark}} | {{checkmark}} |
| [Revolut](@PM-291) | {{cross}} | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| [Santander UK](@PM-292) | {{cross}} | {{checkmark}} |
| [SEB (ISO format)](@PM-130) | {{checkmark}} | {{cross}} |
| [Ulster Bank](@PM-293) | {{checkmark}} | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |
| [Virgin Money (includes Clydesdale, B-bank, Yorkshire)](@PM-294) | {{cross}} | ({{checkmark}}<a href="#footnote-1"><sup>1</sup></a>) |


<small style>
<div class="footnotes">
 <hr />
 <ol>
 <li id="footnote-1">Direct communication with this bank via Yapily is currently in beta. If you encounter any issues, please reach out to Continia Support for assistance.</li>
 </ol>
</div>
</small>


## Yapily 

To enable direct communication between your bank and Microsoft Dynamics 365 Business Central, [Payment Management has partnered with Yapily](@PM-268), which is an Open Banking payment service provider used by many banks in the United Kingdom. Yapily Payments provides a secure open banking payments infrastructure that enables account-to-account payments at scale.

> [!NOTE]
>
> Connecting banks through Yapily is only supported for Business Central version 24 or higher.

{{include "yapily-fees"}}
