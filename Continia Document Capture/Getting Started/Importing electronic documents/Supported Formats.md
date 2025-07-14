---
title: Supported electronic document formats in Document Capture
date: 13-05-2025
description: Learn about the supported file formats for each country.
id: DC-55
lang: en
---

# Supported electronic document formats
There are various options available for managing electronic documents with Continia Document Capture, depending on the type of electronic documents and files you're dealing with: 

* **CDN** - the [Continia Delivery Network (CDN)](@DC-53) facilitates the exchange of files, both sending and receiving, and connects to Peppol or NemHandel in Denmark supporting the following electronic document formats:
  * **Peppol** - Peppol BIS 3.0 and Peppol order, and related responses.
  * **NemHandel** - OIOUBL (*Offentlig* Information Online Universal Business Language) and OIOUBL order, and related responses in Denmark.

* **Email** - you can receive electronic documents via email, which are monitored by Document Capture.

The table below displays a list of supported formats for each country when receiving files via email.



| **Country** | **Format** | **Delivery** | **Comments** |
| --- | --- | --- | --- |
| Australia | A-NZ Peppol BIS 3.0,<br>Peppol BIS 3.0,<br>PINT A-NZ,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN<a href="#footnote-1"><sup>1</sup></a>, email/file | Country standard being adopted by businesses and public authorities.<br><br>A-NZ Peppol BIS 3.0 is an Australian/New Zealand Peppol extension that contains additional rules.<br><br>PINT A-NZ is a more standardized and internationally aligned format. Since 15 May, 2025, the A-NZ Peppol BIS 3.0 extensions are no longer supported – and all eInvoicing must use the PINT A-NZ specification. |
| Austria | Peppol BIS 3.0,<br>ebInterface<a href="#footnote-2"><sup>2</sup></a> ,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN, email/file | One of multiple country standards being adopted by businesses and public entities. |
| Belgium | Peppol BIS 3.0,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN, email/file | Country standard supported by all public government entities and in the process of being adopted by businesses. |
| Canada | UBL<a href="#footnote-2"><sup>2</sup></a> | Email/file | No country standard, but custom formats can be configured. |
| Denmark | Peppol BIS 3.0,<br>UBL<a href="#footnote-2"><sup>2</sup></a>,<br>OIOUBL<a href="#footnote-3"><sup>3</sup></a>, <br>OIOUTS<a href="#footnote-4"><sup>4</sup></a>, <br>OIOXML<a href="#footnote-5"><sup>5</sup></a> | CDN, email/file | Peppol is a country standard supported by all public entities and in the process of being adopted by businesses.<br><br>With the introduction of the Danish Bookkeeping Act (Act No.700 of 24 May 2022), all Danish organizations must be registered with NemHandel and be able to send and receive electronic invoices and credit memos in the Danish OIOUBL format via the NemHandel network. |
| Finland | Finvoice<a href="#footnote-2"><sup>2</sup></a>, <br>Peppol BIS 3.0,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN, email/file | Partly being adopted by businesses and public government entities.<br><br>TEAPPSXML is currently not supported, but may be in the future. |
| France | Peppol BIS 3.0,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN, email/file | Partly being adopted  by businesses and public government entities. |
| Germany | XRechnung 2.0 and later,<br>Peppol BIS 3.0,<br>ZUGFeRD Profile XInvoice<a href="#footnote-2"><sup>2</sup></a> ,<br>ZUGFeRD 2.1.1, <br>ZUGFeRD 2.0, <br>ZUGFeRD 1.0<a href="#footnote-2"><sup>2</sup></a>,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN, email/file | Country standard supported by all public government entities and in the process of being adopted by businesses.<br><br>XRechnung is a German Peppol extension that contains additional rules.<br><br>For ZUGFeRD, the following formats are currently supported (only email/file transfer): <ul><li>ZUGFeRD 1.0 (Continia no longer provides the required templates by default, though they're available on request.)</li><li>ZUGFeRD 2.0 (extended, as PDF/A-3 with integrated XML or as XML only)</li><li>ZUGFeRD 2.1.1 (extended, as PDF/A-3 with integrated XML or as XML only)</li><li>ZUGFeRD Profile XInvoice as XML (XInvoice CII)</li></ul> The ZUGFeRD format complies with the EU directive as of version 2.0. |
| Ireland | Peppol BIS 3.0,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN, email/file | Ireland has decided to use Peppol as a document delivery method, but this isn't enforced at the moment. |
| Netherlands | Peppol BIS 3.0,<br>SimplerInvoicing,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN<a href="#footnote-6"><sup>6</sup></a>, email/file | Country standard being adopted by businesses and public authorities.<br><br>SimplerInvoicing is a Dutch, B2B implementation of the UBL (Universal Business Language) standards, known as SI-UBL. |
| New Zealand | A-NZ Peppol BIS 3.0,<br>Peppol BIS 3.0,<br>PINT A-NZ,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN<a href="#footnote-1"><sup>1</sup></a>, email/file | Country standard being adopted by businesses and public authorities.<br><br>A-NZ Peppol BIS 3.0 is an Australian/New Zealand Peppol extension that contains additional rules.<br/><br/>PINT A-NZ is a more standardized and internationally aligned format. Since 15 May, 2025, the A-NZ Peppol BIS 3.0 extensions are no longer supported – and all eInvoicing must use the PINT A-NZ specification. |
| Norway | Peppol BIS 3.0,<br>EHF 3.0,<br>EHF 2.0<a href="#footnote-2"><sup>2</sup></a>, <br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN, email/file | Country standard supported by all public entities and most businesses.<br><br>Peppol BIS 3.0 is sometimes also referred to as EHF 3.0. |
| Poland | Peppol BIS 3.0,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN, email/file | Country standard supported by all public entities and in the process of being adopted by businesses. |
| Portugal | Peppol BIS 3.0,<br />UBL CIUS-PT<a href="#footnote-2"><sup>2</sup></a>, <br />CEFACT CIUS-PT2<a href="#footnote-2"><sup>2</sup></a> | CDN, email/file | Country standard supported by all public government entities and in the process of being adopted by businesses. |
| Spain | FacturaE<a href="#footnote-2"><sup>2</sup></a> | Email/file | Country standard being adopted by businesses and public authorities. |
| Sweden | Peppol BIS 3.0,<br>Svefaktura 1.0<a href="#footnote-2"><sup>2</sup></a> ,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN, email/file | Peppol is the new country standard supported by all public government entities and in the process of being adopted by businesses. |
| United Kingdom | Peppol BIS 3.0,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN, email/file | There's currently no standard, but the NHS has implemented Peppol BIS 3. |
| United States | Custom | Email/file | There's no country-wide standard, but custom formats can be configured. |
| Other countries | Peppol BIS 3.0,<br>UBL<a href="#footnote-2"><sup>2</sup></a> | CDN, email/file | Standard Peppol invoicing format. |

<small style>

<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">Starting with Document Capture 2023 R2 Service Pack 2, customers in Australia and New Zealand can connect directly to the Peppol eDelivery Network. For more information, see <a href="/continia-document-capture/getting-started/importing-electronic-documents/electronic-invoicing-in-australia">Managing electronic documents in Australia</a> and <a href="/continia-document-capture/getting-started/importing-electronic-documents/electronic-invoicing-in-new-zealand">Managing electronic documents in New Zealand</a>. </li>
    <li id="footnote-2">This format isn't supported by the Continia Delivery Network.</li>
    <li id="footnote-3">The OIOUBL format is supported as of Document Capture 2022 R1 Service Pack 1 (v9.01) and Continia Delivery Network v3.01. For older versions, documents must be delivered via email/file instead.</li>
    <li id="footnote-4"> The OIOUTS format is supported as of Document Capture 2023 R1 (v11) and Continia Delivery Network v5.00. For older versions, documents must be delivered via email/file instead.
    <li id="footnote-5">The OIOXML format was replaced by the OIOUBL format. Documents of this type can only be delivered via email/file.</li>    
    <li id="footnote-6">Starting with Document Capture 2023 R2 Service Pack 2, customers in the Netherlands are able to connect directly to the Peppol eDelivery Network. For more information, see <a href="/continia-document-capture/getting-started/importing-electronic-documents/electronic-invoicing-in-the-netherlands">Managing electronic documents in the Netherlands</a>. </li>    
  </ol>
</div>


</small>

## Related information

[Setting up the Continia Delivery Network](@DC-75)