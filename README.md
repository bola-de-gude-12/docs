# Detailed changelog for Continia Document Capture 2026 R1 incl. CDN

{% updates format="full" %}
{% update date="2026-06-12" %}
## Document Capture 2026 R1, Service Pack 2, hotfix 1

_Release date, online: June 9, 2026_\
_Document Capture version: 28.2.1_\
_Continia Delivery Network version: 28.2.1_

|                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | ID    |
| ----------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ----- |
| Platform and technology | When a GP to Business Central cloud migration was performed in environments with Continia apps installed, the migration could fail in some cases. This occurred because Continia added entries to the **Migration Table Mapping** table without first verifying whether the migration was a GP to Business Central or a Business Central to Business Central migration. Now, Continia checks the product ID before adding custom table mappings – ensuring that GP to Business Central migrations complete successfully. | 79154 |
| eDocuments              | Previously, the DK prefix to 0184 (DK:DIGST) identifiers was automatically added when sending eDocuments, which caused deliveries to fail for participants whose registered identifier did not include the prefix. Now, when the **Recipient Type** is set to **Other** in **Continia Customer Setup**, the **Recipient ID Value** is used exactly as entered, that is, the DK prefix is no longer added automatically.                                                                                                  | 79278 |
{% endupdate %}
{% endupdates %}
