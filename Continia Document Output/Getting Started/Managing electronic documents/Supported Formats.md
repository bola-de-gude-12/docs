---
title: Supported Electronic Document Formats in Document Output
date: 03-05-2024
description: Learn more about the supported file formats for each country.
id: DO-57
lang: en
---

# Supported Electronic Document Formats
There are various options available for sending electronic documents with Continia Document Output, depending on the type of electronic documents and files you're dealing with: 

* **Through CDN** - the [Continia Delivery Network (CDN)](@DC-53) facilitates sending files and connects to Peppol or NemHandel in Denmark supporting the following electronic document formats:
  * **Peppol** - Peppol BIS 3.0 and Peppol order, and related responses.
  * **NemHandel** - OIOUBL and OIOUBL order, and related responses in Denmark.

* **Through email** - you can send electronic documents via email, which are monitored by Document Output.

The table below displays a list of supported formats for each country when sending files. 



| **Country** | **Format** | **Delivery** | **Comments** |
| --- | --- | --- | --- |
| [Australia](@DO-171) | PEPPOL BIS3 | CDN, email/file | PEPPOL BIS3 is the official e-invoice format in Australia. |
| [Austria](@DO-172) | PEPPOL BIS3 | CDN, email/file | All Austrian suppliers to the Austrian federal government must use e-invoices according to the Austrian ICT Consolidation Act. |
| [Belgium](@DO-173) | PEPPOL BIS3 | CDN, email/file | All Belgian companies are registered as PEPPOL receivers in the BOSA registry. However, it is important to note that they can be re-routed through the Continia Delivery Network if necessary. <br />Also supported is FACTUR-X: A PDF-A standard with an embedded cross-industry XML format. FACTUR-X invoices must be sent via email to ensure proper transmission and receipt. |
| [Canada](@DO-174) | UBL<a href="#footnote-1"><sup>1</sup></a> | Email/file | No country standard, but custom formats can be configured. |
| [Denmark](@DO-175) | PEPPOL BIS3<br />OIOUBL (UBL2.1) | CDN, email/file | Traditionally, the NemHandel network transmits OIOUBL in Denmark. <br />This can be onboarded separately in Continia Delivery Network, enabling support of both document types in one solution.<br />OIOUTS: This is a Cross Industry format used mainly by the supply chain and telecom industry. It can only be attached to an OIOUBL invoice and sent internally to companies connected to the Danish NemHandel Network. Document Output can connect to the NemHandel network through Delivery Network, but Document Output can’t create the OIOUTS specification XML. |
| [Finland](@DO-176) | PEPPOL BIS3 | CDN, email/file | There are currently three distinct electronic invoicing standards used in Finland. However, Document Output exclusively supports the PEPPOL format. To receive the PEPPOL XML files through Document Output, the recipient must also be connected to a PEPPOL Access Point.<br/><br/>While other electronic invoicing formats are available, such as Finvoice and TEAPPSXML, these formats are incompatible with Document Output. As a result, files in these formats cannot be processed or managed through the Delivery Network. |
| [France](@DO-177) | PEPPOL BIS3 | CDN, email/file | Currently, France has no legal requirement for using PEPPOL. However, it is important to highlight that the relevant stakeholders are actively working on initiatives to implement PEPPOL in France.<br />Also supported is FACTUR-X: A PDF-A standard with an embedded cross-industry XML format. FACTUR-X invoices must be sent via email to ensure proper transmission and receipt. |
| [Germany](@DO-178) | PEPPOL BIS3<br />XRechnung | CDN, email/file | Also supported is ZUGFeRD: A PDF-A standard with an embedded cross-industry XML format. ZUGFeRD invoices must be sent via email to ensure proper transmission and receipt. |
| [Ireland](@DO-179) | PEPPOL BIS3 | CDN, email/file | Ireland has decided to use PEPPOL as a document delivery method, but this isn't enforced at the moment. |
| [Netherlands](@DO-186) | PEPPOL BIS3 | CDN, email/file | PEPPOL BIS3 is the official e-invoicing format in the Netherlands. |
| [New Zealand](@DO-180) | PEPPOL BIS3 | CDN, email/file | PEPPOL BIS3 is the official e-invoicing format in New Zealand. |
| [Norway](@DO-181) | PEPPOL BIS3<br />(EHF 3.0) | CDN, email/file | EHF is the Norwegian adaptation of the PEPPOL standard. In Norway, B2B and B2G transactions must use the EHF format for electronic invoicing. When registering in PEPPOL, it is necessary to update the ELMA network, which Continia efficiently handles during the registration process for the Delivery Network.<br/><br/>Please note that the legacy EHF 2.0 formats are no longer in use and are considered obsolete. Additionally, Norway has an eFaktura XML format specifically designed for B2C customer invoicing. However, it is important to know that Document Output does not support this format. |
| [Poland](@DO-182) | PEPPOL BIS3 | CDN, email/file | Accepted by B2G and in process for B2B. |
| [Portugal](@DO-183) | UBL CIUS-PT<a href="#footnote-1"><sup>1</sup></a> <br />CEFACT CIUS-PT2<a href="#footnote-1"><sup>1</sup></a> | CDN, email/file | Country standard supported by all public government entities and in the process of being adopted by businesses. |
| [Spain](@DO-184) | FacturaE<a href="#footnote-1"><sup>1</sup></a> | Email/file | Country standard being adopted by businesses and public authorities. |
| [Sweden](@DO-185) | B2G: PEPPOL BIS 3.0 | CDN, email/file | The country standard for B2G transactions is also being formally adopted for B2B. Previously, the legacy format was known as SveFaktura 1.0. However, it is important to note that Document Output does not support this format. |
| [United Kingdom](@DO-187) | PEPPOL BIS3 | CDN, email/file | While the UK does not have a mandatory requirement for Peppol, it is worth mentioning that the National Health Service (NHS) has proactively implemented the capability to receive Peppol files. |
| [United States](@DO-188) | PEPPOL BIS3 | Email/file | Although PEPPOL is not a mandatory requirement in the United States, an increasing number of companies are recognizing the benefits and adopting the Peppol format. |
| Other countries | PEPPOL BIS3 | CDN, email/file | Even in countries without specific regulations regarding Peppol, companies can still send Peppol BIS3 billing to recipients connected to a Peppol Access Point.  As of 2023, the prevailing standard format remains Peppol BIS3 billing; however, it is important to note that the Peppol PINT variant will soon replace this. |

<small style>

<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">This format isn't supported by Document Output.</li>  
  </ol>
</div>



</small>

## Supported document types by format

The table below provides you with an overview of the document types that are supported by each e-invoice format mentioned in the above table.

| Format      | Document types                                               |
| ----------- | ------------------------------------------------------------ |
| PEPPOL BIS3 | <li>Sales invoice</li><li>Sales credit memo</li><li>Service invoice</li><li>Service credit memo</li> |
| XRechnung   | <li>Sales invoice</li><li>Sales credit memo</li><li>Service invoice</li><li>Service credit memo</li> |
| ZUGFeRD     | <li>Sales invoice</li><li>Sales credit memo</li><li>Service invoice</li><li>Service credit memo</li> |
| OIOUBL      | <li>Sales invoice</li><li>Sales credit memo</li><li>Service invoice</li><li>Service credit memo</li><li>Reminder</li> |