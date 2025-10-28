---
title: Supported electronic document formats in Document Capture
date: 01-08-2025
description: Learn about the supported file formats for each country.
id: 
lang: en
---

# Supported electronic document formats
There are various options available for managing electronic documents with Continia Document Capture, depending on the type of electronic documents and files you're dealing with.

The table below lists all formats supported by Document Capture. You can search for a format and/or use one of the following filters.

* **Country** - select the desired country.
* **Delivery method** - select the desired delivery method for electronic documents:
  * [Continia Delivery Network (CDN)](@DC-53) - facilitates the exchange of files, both sending and receiving, and connects to Peppol (for Peppol BIS 3.0 and Peppol order, and related responses) or NemHandel (for OIOUBL, OIOUBL order, and related responses) in Denmark.
  * **Email** - receive electronic documents via email or file transfer, which are monitored by Document Capture.

* **Works with Continia eDocuments** - select this box to see only formats that are fully supported by Continia eDocuments, from eOrdering to eBilling.

<div
  class="table-with-filters"
  data-filters='[
    {"type": "search", "col": 1, "label": "Search for a format", "classNames": "full-width"},
    {"type": "dropdown", "col": 2, "label": "Country"},
    {"type": "checkmarkCombined", "cols": [3,4], "label": "Delivery method", "optionLabels": ["CDN", "Email"]},
    {"type": "checkmark", "col": 5, "label": "Works with Continia eDocuments"}
  ]'
>

| **Format** | **Country** | **CDN delivery** | **Email delivery** | Continia eDocuments | **Comments** |
| :-: | :-: | :-: | :-: | :-: | :-- |
| Peppol BIS 3.0 | Australia | {{checkmark}} | {{cross}} | {{checkmark}} | Starting with Document Capture 2023 R2 Service Pack 2, customers in Australia can connect directly to the Peppol eDelivery Network. For more information, see <a href="/continia-document-capture/getting-started/importing-electronic-documents/electronic-invoicing-in-australia">Managing electronic documents in Australia</a>. |
| A-NZ Peppol BIS 3.0 | Australia | {{checkmark}} | {{cross}} | ? | A-NZ Peppol BIS 3.0 is an Australian/New Zealand Peppol extension that contains additional rules. |
| PINT A-NZ | Australia | {{checkmark}} | {{cross}} | {{checkmark}} | PINT A-NZ is a more standardized and internationally aligned format. Since 15 May, 2025, the A-NZ Peppol BIS 3.0 extensions are no longer supported – and all e-invoicing must use the PINT A-NZ specification. |
| UBL | Australia | {{cross}} | {{checkmark}} | {{cross}} | - |
| Peppol BIS 3.0 | Austria | {{checkmark}} | {{cross}} | {{checkmark}} | One of multiple country standards being adopted by businesses and public entities. |
| ebInterface | Austria | {{cross}} | {{checkmark}} | {{cross}} | - |
| UBL | Austria | {{cross}} | {{checkmark}} | {{cross}} | - |
| Peppol BIS 3.0 | Belgium | {{checkmark}} | {{cross}} | {{checkmark}} | Country standard supported by all public government entities and in the process of being adopted by businesses. |
| UBL | Belgium | {{cross}} | {{checkmark}} | {{cross}} | - |
| UBL | Canada | {{cross}} | {{checkmark}} | {{cross}} | No country standard, but custom formats can be configured. |
| Peppol BIS 3.0 | Denmark | {{checkmark}} | {{cross}} | {{checkmark}} | Peppol is a country standard supported by all public entities and in the process of being adopted by businesses. |
| UBL | Denmark | {{cross}} | {{checkmark}} | {{cross}} | - |
| OIOUBL | Denmark | {{checkmark}} | {{cross}} | {{checkmark}} | With the introduction of the Danish Bookkeeping Act (Act No. 700 of 24 May 2022), all Danish organizations must be registered with NemHandel and be able to send and receive electronic invoices and credit memos in the Danish OIOUBL format via the NemHandel network.<br></br>The OIOUBL format is supported as of Document Capture 2022 R1 Service Pack 1 (v9.01) and Continia Delivery Network v3.01. For older versions, documents must be delivered via email instead. |
| OIOUTS | Denmark | {{checkmark}} | {{cross}} | {{checkmark}} | The OIOUTS format is supported as of Document Capture 2023 R1 (v11) and Continia Delivery Network v5.00. For older versions, documents must be delivered via email instead. |
| OIOXML | Denmark | {{cross}} | {{checkmark}} | {{cross}} | The OIOXML format was replaced by the OIOUBL format. Documents of this type can only be delivered via email. |
| Peppol BIS 3.0 | Finland | {{checkmark}} | {{cross}} | {{checkmark}} | - |
| Finvoice | Finland | {{cross}} | {{checkmark}} | {{cross}} | Partly being adopted by businesses and public government entities.<br><br>TEAPPSXML is currently not supported, but may be in the future. |
| UBL | Finland | {{cross}} | {{checkmark}} | {{cross}} | - |
| Peppol BIS 3.0 | France | {{checkmark}} | {{cross}} | {{checkmark}} | Partly being adopted by businesses and public government entities. |
| UBL | France | {{cross}} | {{checkmark}} | {{cross}} | - |
| Peppol BIS 3.0 | Germany | {{checkmark}} | {{cross}} | {{checkmark}} | Country standard supported by all public government entities and in the process of being adopted by businesses. |
| XRechnung 2.0 and later | Germany | ? | ? | ? | XRechnung is a German Peppol extension that contains additional rules. |
| ZUGFeRD Profile XInvoice | Germany | {{cross}} | {{checkmark}} | {{cross}} | ZUGFeRD Profile XInvoice as XML (XInvoice CII). |
| ZUGFeRD 2.1.1 | Germany | {{cross}} | {{checkmark}} | {{cross}} | ZUGFeRD 2.1.1 (extended, as PDF/A-3 with integrated XML or as XML only). |
| ZUGFeRD 2.0 | Germany | {{cross}} | {{checkmark}} | {{cross}} | ZUGFeRD 2.0 (extended, as PDF/A-3 with integrated XML or as XML only). |
| ZUGFeRD 1.0 | Germany | {{cross}} | {{checkmark}} | {{cross}} | ZUGFeRD 1.0 (Continia no longer provides the required templates by default, though they're available on request). |
| UBL | Germany | {{cross}} | {{checkmark}} | {{cross}} | - |
| Peppol BIS 3.0 | Iceland | {{checkmark}} | {{cross}} | {{checkmark}} | - |
| Peppol BIS 3.0 | Ireland | {{checkmark}} | {{cross}} | {{checkmark}} | Ireland has decided to use Peppol as a document delivery method, but this isn't enforced at the moment. |
| UBL | Ireland | {{cross}} | {{checkmark}} | {{cross}} | - |
| Peppol BIS 3.0 | Netherlands | {{checkmark}} | {{cross}} | {{checkmark}} | Starting with Document Capture 2023 R2 Service Pack 2, customers in the Netherlands are able to connect directly to the Peppol eDelivery Network. For more information, see <a href="/continia-document-capture/getting-started/importing-electronic-documents/electronic-invoicing-in-the-netherlands">Managing electronic documents in the Netherlands</a>. |
| SimplerInvoicing | Netherlands | {{cross}} | {{cross}} | {{cross}} | SimplerInvoicing is a Dutch, B2B implementation of the Universal Business Language (UBL) standards known as SI-UBL. Support for this format is scheduled for September. |
| UBL | Netherlands | {{cross}} | {{checkmark}} | {{cross}} | - |
| Peppol BIS 3.0 | New Zealand | {{checkmark}} | {{cross}} | {{checkmark}} | Starting with Document Capture 2023 R2 Service Pack 2, customers in New Zealand can connect directly to the Peppol eDelivery Network. For more information, see <a href="/continia-document-capture/getting-started/importing-electronic-documents/electronic-invoicing-in-new-zealand">Managing electronic documents in New Zealand</a>. |
| A-NZ Peppol BIS 3.0                                          | New Zealand | {{checkmark}} | {{cross}} | {{checkmark}} | A-NZ Peppol BIS 3.0 is an Australian/New Zealand Peppol extension that contains additional rules. |
| PINT A-NZ | New Zealand | {{checkmark}} | {{cross}} | {{checkmark}} | PINT A-NZ is a more standardized and internationally aligned format. Since 15 May, 2025, the A-NZ Peppol BIS 3.0 extensions are no longer supported – and all e-invoicing must use the PINT A-NZ specification. |
| UBL | New Zealand | {{cross}} | {{checkmark}} | {{cross}} | - |
| Peppol BIS 3.0 | Norway | {{checkmark}} | {{cross}} | {{checkmark}} | Country standard supported by all public entities and most businesses. |
| EHF 3.0 | Norway | {{checkmark}} | {{cross}} | {{checkmark}} | Peppol BIS 3.0 is sometimes also referred to as EHF 3.0. |
| EHF 2.0 | Norway | {{cross}} | {{checkmark}} | {{cross}} | - |
| UBL | Norway | {{cross}} | {{checkmark}} | {{cross}} | - |
| Peppol BIS 3.0 | Poland | {{checkmark}} | {{cross}} | {{checkmark}} | Country standard supported by all public entities and in the process of being adopted by businesses. |
| UBL | Poland | {{cross}} | {{checkmark}} | {{cross}} | - |
| Peppol BIS 3.0 | Portugal | {{checkmark}} | {{cross}} | {{checkmark}} | Country standard supported by all public government entities and in the process of being adopted by businesses. |
| UBL CIUS-PT | Portugal | {{cross}} | {{checkmark}} | {{cross}} | - |
| CEFACT CIUS-PT2 | Portugal | {{cross}} | {{checkmark}} | {{cross}} | - |
| FacturaE | Spain | {{cross}} | {{checkmark}} | {{cross}} | Country standard being adopted by businesses and public authorities. |
| Peppol BIS 3.0 | Sweden | {{checkmark}} | {{cross}} | {{checkmark}} | Peppol is the new country standard, supported by all public government entities and in the process of being adopted by businesses. |
| Svefaktura 1.0 | Sweden | {{cross}} | {{checkmark}} | {{cross}} | - |
| UBL | Sweden | {{cross}} | {{checkmark}} | {{cross}} | - |
| Peppol BIS 3.0 | United Kingdom | {{checkmark}} | {{cross}} | {{checkmark}} | There's currently no standard, but the NHS has implemented Peppol BIS 3.0. |
| UBL | United Kingdom | {{cross}} | {{checkmark}} | {{cross}} | - |
| Custom | United States | {{cross}} | {{checkmark}} | {{cross}} | There's no country-wide standard, but custom formats can be configured. |
| Peppol BIS 3.0 | Other countries | {{checkmark}} | {{cross}} | {{checkmark}} | Standard Peppol invoicing format. |
| UBL | Other countries | {{cross}} | {{checkmark}} | {{cross}} | - |


## See also

[Setting up the Continia Delivery Network](@DC-75)