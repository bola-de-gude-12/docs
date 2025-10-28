Although Norway is not a member of the EU, it complies with all the EU regulations on electronic invoicing for B2G. The format of electronic invoicing is also widely accepted by the B2B sector. Furthermore, Norway plans to enhance the specifications by incorporating new document types into the electronic invoicing mandate. Norway follows the European standard for electronic invoicing and electronic documents have been widely adopted across the country.

The table below outlines the current regulatory states and future outlooks for B2G, B2B, and B2C (business-to-consumer) sectors.

<br>


| Transaction type | **Current regulatory state**                                 | **Regulatory outlook**                                       |
| ---------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| **B2G**          | Electronic invoicing has been mandatory since 2019.</br><br />{{checkmark}} *Supported by Document Capture.*<br />{{checkmark}} *Supported by Document Output.* | Plan to support eOrder and eCatalog with EHF, but no timeline has been specified yet.</br><br />{{checkmark}} *Supported by Document Capture.* |
| **B2B**          | Electronic invoicing is possible if both parties are registered with ELMA/Peppol. <br /><br />{{checkmark}} *Supported by Document Capture.*<br />{{checkmark}} *Supported by Document Output.* | No changes are expected.                                     |
| **B2C**          | No legislation is in place.                                  | No changes are expected.                                     |

## EHF and ELMA

In January 2020, the EHF (Elektronisk Handels Format) was upgraded to version 3.0, aligning with the Peppol BIS 3.0 standard and incorporating Norwegian validation rules. With this upgrade, the legacy EHF2 format became invalid. Concurrently, Norway integrated its address register, ELMA (Elektronisk mottakaadresseregister), with the Peppol eDelivery Network. Companies receiving EHF documents must be registered in both directories, typically managed by their Electronic invoicing service provider.

> [!NOTE]
>
> Occasionally, eFaktura is used for B2C invoicing, though it operates independently of ELMA/Peppol and is not supported by Continia Software.

The EHF 3.0 format is used for non-billing documents such as orders, dispatch advice, and catalogs. It doesn't include billing documents such as invoices and credit memos. For these types of documents, the Peppol BIS Billing 3.0 format is used.

When Norway adopted the Peppol BIS Billing 3.0 and EHF 3.0 standards, they also integrated the ELMA (Elektronisk mottakaadresseregister) address register with the Peppol eDelivery Network. Any Norwegian company that receives a document in the EHF format can register to receive documents from any access point. However, most Norwegian companies choose to register with ELMA. This registration process needs to be handled by the electronic invoicing service provider. Unless specified otherwise by the company, Continia automatically registers all Norwegian companies in ELMA.

>  [!NOTE]
>
>  B2B electronic invoicing is not mandatory in Norway, but it is widely adopted and used in the sector. 

<style>
  .content table tr td:nth-child(1) {
    width: 120px;
  }
  .content table tr td:nth-child(2) {
    width: 225px;
  }
  .content table tr td:nth-child(3) {
    width: 225px;
  }  
</style>