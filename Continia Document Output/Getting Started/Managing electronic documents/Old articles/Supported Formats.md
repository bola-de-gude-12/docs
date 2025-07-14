---
title: Supported E-Invoice Formats per Country
date: 17-11-2023
description:  
id: 
lang: en
---

# Supported E-Invoice Formats per Country
The following table lists the e-invoice formats for each country, indicates whether the format can be transmitted to the PEPPOL eDelivery Network through Continia Delivery Network, and whether there are any other formats supported by Document Output (outgoing) or Document Capture (ingoing). 

> [!NOTE]
>
> PEPPOL is the infrastructure for transferring e-documents, and PEPPOL BIS (Business Interoperability Specifications) is the default format for documents sent through the infrastructure. 

| Country                           | E-invoice Format                     | Invoice Format Compatible with CDN | Other supported invoice Formats | Description                                                  |
| --------------------------------- | ------------------------------------ | ---------------------------------- | ------------------------------- | ------------------------------------------------------------ |
| [Australia](Australia.md)         | PEPPOL BIS3                          | {{checkmark}}                      |                                 | PEPPOL BIS3 is the official e-invoice format in Australia.   |
| [Austria](Austria.md)             | PEPPOL BIS3                          | {{checkmark}}                      |                                 | All Austrian suppliers to the Austrian federal government must use e-invoices according to the Austrian ICT Consolidation Act. |
| [Belgium](Belgium.md)             | PEPPOL BIS3                          | {{checkmark}}                      | FACTUR-X                        | All Belgian companies are registered as PEPPOL receivers in the BOSA registry. However, it is important to note that they can be re-routed through the Continia Delivery Network if necessary. <br />FACTUR-X: A PDF-A standard with an embedded cross-industry XML format. FACTUR-X invoices must be sent via email to ensure proper transmission and receipt. |
| [Denmark](Denmark.md)             | PEPPOL BIS3<br />OIOUBL (UBL2.1)     | {{checkmark}}<br />{{checkmark}}   |                                 | Traditionally, the NemHandel network transmits OIOUBL in Denmark. <br />This can be onboarded separately in Continia Delivery Network, enabling support of both document types in one solution.<br />OIOUTS: This is a Cross Industry format used mainly by the supply chain and telecom industry. It can only be attached to an OIOUBL invoice and sent internally to companies connected to the Danish NemHandel Network. Document Output can connect to the NemHandel network through Delivery Network, but Document Output can’t create the OIOUTS specification XML. |
| [Finland](Finland.md)             | PEPPOL BIS3                          | {{checkmark}}                      |                                 | There are currently three distinct electronic invoicing standards used in Finland. However, Document Output exclusively supports the PEPPOL format. To receive the PEPPOL XML files through Document Output, the recipient must also be connected to a PEPPOL Access Point.<br/><br/>While other electronic invoicing formats are available, such as Finvoice and TEAPPSXML, these formats are incompatible with Document Output. As a result, files in these formats cannot be processed or managed through the Delivery Network. |
| [France](France.md)               | PEPPOL BIS3                          | {{checkmark}}                      | FACTUR-X                        | Currently, France has no legal requirement for using PEPPOL. However, it is important to highlight that the relevant stakeholders are actively working on initiatives to implement PEPPOL in France.<br />FACTUR-X: A PDF-A standard with an embedded cross-industry XML format. FACTUR-X invoices must be sent via email to ensure proper transmission and receipt. |
| [Germany](Germany.md)             | PEPPOL BIS3<br />XRechnung           | {{checkmark}}                      | ZUGFeRD                         | ZUGFeRD: A PDF-A standard with an embedded cross-industry XML format. ZUGFeRD invoices must be sent via email to ensure proper transmission and receipt. |
| [Ireland](Ireland.md)             | PEPPOL BIS3                          | {{checkmark}}                      |                                 | Ireland has decided to use PEPPOL as a document delivery method, but this isn't enforced at the moment. |
| [Luxemburg](Luxembourg.md)        | PEPPOL BIS3                          | {{checkmark}}                      |                                 | Peppol BIS3 is the official e-invoicing format for both B2G invoicing and B2B invoicing in Luxembourg. |
| [Netherlands](Netherlands.md)     | PEPPOL BIS3                          | {{checkmark}}                      |                                 | PEPPOL BIS3 is the official e-invoicing format in the Netherlands. |
| [New Zealand](New Zealand.md)     | PEPPOL BIS3                          | {{checkmark}}                      |                                 | PEPPOL BIS3 is the official e-invoicing format in New Zealand. |
| [Norway](Norway.md)               | PEPPOL BIS3<br />(EHF 3.0)           | {{checkmark}}                      |                                 | EHF is the Norwegian adaptation of the PEPPOL standard. In Norway, B2B and B2G transactions must use the EHF format for electronic invoicing. When registering in PEPPOL, it is necessary to update the ELMA network, which Continia efficiently handles during the registration process for the Delivery Network.<br/><br/>Please note that the legacy EHF 2.0 formats are no longer in use and are considered obsolete. Additionally, Norway has an eFaktura XML format specifically designed for B2C customer invoicing. However, it is important to know that Document Output does not support this format. |
| [Poland](Poland.md)               | PEPPOL BIS3                          | {{checkmark}}                      |                                 | Accepted by B2G and in process for B2B.                      |
| [Sweden](Sweden.md)               | B2G: PEPPOL BIS 3.0 – Svefaktura 2.0 | {{checkmark}}                      |                                 | The country standard for B2G transactions is also being formally adopted for B2B. Previously, the legacy format was known as SveFaktura 1.0. However, it is important to note that Document Output does not support this format. |
| [United Kingdom](England.md)      | PEPPOL BIS3                          | {{checkmark}}                      |                                 | While the UK does not have a mandatory requirement for Peppol, it is worth mentioning that the National Health Service (NHS) has proactively implemented the capability to receive Peppol files. |
| [United States](United States.md) | PEPPOL BIS3                          | {{checkmark}}                      |                                 | Although PEPPOL is not a mandatory requirement in the United States, an increasing number of companies are recognizing the benefits and adopting the Peppol format. |
| Other countries                   | PEPPOL BIS3                          | {{checkmark}}                      |                                 | Even in countries without specific regulations regarding Peppol, companies can still send Peppol BIS3 billing to recipients connected to a Peppol Access Point.  As of 2023, the prevailing standard format remains Peppol BIS3 billing; however, it is important to note that the Peppol PINT variant will soon replace this. |



## Supported document types by format

The table below provides you with an overview of the document types that are supported by each e-invoice format mentioned in the above table.

| Format      | Document types                                               |
| ----------- | ------------------------------------------------------------ |
| PEPPOL BIS3 | <li>Sales invoice</li><li>Sales credit memo</li><li>Service invoice</li><li>Service credit memo</li> |
| XRechnung   | <li>Sales invoice</li><li>Sales credit memo</li><li>Service invoice</li><li>Service credit memo</li> |
| ZUGFeRD     | <li>Sales invoice</li><li>Sales credit memo</li><li>Service invoice</li><li>Service credit memo</li> |
| OIOUBL      | <li>Sales invoice</li><li>Sales credit memo</li><li>Service invoice</li><li>Service credit memo</li><li>Reminder</li> |

