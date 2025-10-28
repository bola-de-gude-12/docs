---
title: Detailed changelog for Continia Document Capture 2025 R2
date: 27-10-2025
description: The detailed changelog for Document Capture 2025 R2.
id: DC-389
lang: en
---

# Detailed changelog for Continia Document Capture 2025 R2

This article lists all new updates, features, service packs, and hotfixes for Continia Document Capture 2025 R2.

> [!TIP]
> As a Continia partner, you can be notified of new Document Capture versions and service packs when they're released. To sign up for this service, go to [Receive a notification upon new Document Capture releases](https://continia.zendesk.com/hc/en-us/articles/360005355079-Receive-a-notification-upon-new-Document-Capture-releases) in the Continia PartnerZone (only available to partners).

> [!NOTE]
> The changelog for Document Capture also includes the release notes for the [Continia Delivery Network](@DC-53) (CDN).
>
> When new versions of both apps are released together, the release notes for the CDN are listed along the release notes for that Document Capture release. When a new version of the CDN is released separately, its release notes are listed by themselves – and you must update the CDN app discretely.

> [!IMPORTANT]
> Document Capture 2025 R2 supports the following version of Microsoft Dynamics 365 Business Central: Business Central 2025 R2 (v27).

## Document Capture 2025 R2, hotfix 1

*Release date, online: October 20, 2025*  
*App version: 27.0.1* 

### Bug fixes

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| Documents and Templates | When a template field using a formula referenced another template field with a fixed-value formula, the result sometimes remained empty. | 69910 |
| General Application     | When certain Continia email scenarios were assigned to an email account, the upgrade to Document Capture version 27 would fail due to the following error: <ul><li><em>The record in table Email Scenario already exists. Identification fields and values: Scenario='Document Capture Assigned Documents'</em></li> </ul> | 70585 |

## Document Capture 2025 R2

*Pre-release date, online: September 17, 2025*  
*Release date, online: October 1, 2025*  
*Release date, on-premises: October 8, 2025*  
*App version: 27.0.0* 

### New or changed functionality

| Functional area | Description | ID |
| --- | --- |  --- |
| Documents and Templates |When deleting a vendor, any unused templates associated with that vendor are also deleted automatically – provided the user has the necessary permissions to delete templates. If not, only the vendor is deleted. |50687|
| Documents and Templates |To improve flexibility when registering sales documents, the following document error comment has been made configurable: <ul><li><em>&lt;External Document No.&gt; already exists (on Sales Header, &lt;Document Type&gt; = &lt;Order No.&gt;) </em></li> </ul>  |63888|
| Documents and Templates |When a template field is set to the <b>Lookup</b> data type, the <b>Translate To</b> field on the <b>Template Field Card</b> also functions as a lookup field now. This allows you to select values dynamically, rather than entering them manually. To enable this functionality, lookup values must be configured for both the source table and source field of the template field.  |64315|
| Documents and Templates |When using the <b>Move To Company</b> action in document journal, the window for selecting the destination company and category only shows the <b>Display Name</b> of the destination companies now - not the company name. However, if a company's display name is not configured, the company name is populated instead. |65052|
| Documents and Templates |Support for capturing Business Central Sustainability activity values and calculating them from emission values has been added to the document journal and document card. |67922|
| Document Approval|Previously, when updating the <b>Number</b> field in a purchase document line via the Web Approval Portal to a fixed asset account, the existing values for <b>Quantity</b>, <b>Price</b>, and <b>Amount</b> were removed. These values are now retained. |56809|
| General Application|A <b>Download</b> action has been added to the <b>Document Attachments</b> page, allowing you to download the document directly without viewing the content beforehand. If multiple records are selected, the <b>Download</b> and <b>Open</b> actions are disabled to align with standard Business Central functionality. |64599|
| General Application| The following changes have been applied to the Document Capture permissions sets:<ul><li>CDC-ALL has been renamed to CDC Basic.</li><li>CDC-SUPER has been renamed to CDC Admin.</li></ul>The renamed permission sets will be updated automatically during the upgrade. For more information about permission sets, see [Document Capture permissions](@DC-140). |68497|
| General Application | The field handling of <b>Buyer Reference</b> and <b>Order Reference</b>&nbsp;in Document Output (DO) and Continia Delivery Network (CDN) has been reworked for the PEPPOL BIS 3, OIOUBL, and XRechnung formats.<br></br>Current field mapping: <ul><li>&lt;BuyerReference&gt; ? <b>Your Reference</b> </li><li>&lt;OrderReference&gt;&lt;ID&gt; ? <b>External Document No.</b> </li><li>&lt;OrderReference&gt;&lt;SalesOrderID&gt; ? <b>Order No.</b> </li> </ul> Validation behavior:<ul><li>PEPPOL BIS 3 - the pre-posting validation now requires either <b>Your Reference</b> or <b>External Document No.</b> An error is shown if both are missing, in line with Peppol XML requirements. </li><li>OIOUBL - the pre-posting validation has been removed, as these elements are not mandatory in the format. </li><li>XRechnung - the pre-posting validation has been removed. However, &lt;BuyerReference&gt; is mandatory. The value is taken from <b>Your Reference</b>. If this field is empty, a default placeholder value <b>NA</b>&nbsp;(i.e.: not answered) is inserted. </li> </ul> |60261|
| Order & Receipt Matching | When using unit of measure-based purchase order/receipt matching, the <b>Invoice Matching</b> and <b>Credit Memo Matching</b> pages have been improved with the following: <ul><li>The base quantity and base unit cost values are displayed for purchase orders, purchase return orders, posted purchase receipts, posted return shipments, and document lines.</li><li>The standard quantity and unit cost fields for purchase orders, purchase return orders, posted purchase receipts, and posted return shipments can be shown or hidden by using the <b>Show Qty. and Unit Cost</b> or <b>Hide Qty. and Unit Cost</b> actions.</li></ul> |64931|
| Platform and Technology | The **Continia Users** and **Continia User Setup** tables have been refactored and moved to Continia Business Foundation app. <br/><br/>Functionality specific to users has also been moved to separate apps:<ul><li>The **Approval Setup** has been moved to the app Continia Approvals.</li><li>The **Web Portal Setup** has been moved to the Continia Online Connector app.</li></ul>For more information, see [Important notice about refactoring in Document Capture and Expense Management](https://continia.zendesk.com/hc/en-us/articles/27530051601810-Important-notice-about-refactoring-in-Document-Capture-and-Expense-Management) (only available to partners). |69889|
| Platform and Technology|With the release of Document Capture 2025 R2 (27.00), support is only provided for Business Central 2025 release wave 2 (BC v27). This was previously announced in the pre-release newsletters. |54588|
| Purchase Documents|To prevent the manual handling of invoices related to VAT rounding differences, a new field - <b>Allow automatic update of VAT amount</b> - has been added to the <b>General Ledger Setup</b> page. This setting enables automatic updates of VAT amounts when registering purchase documents.<br></br> When <b>Allow automatic update of VAT amount</b> is enabled, the assigned VAT amount is automatically adjusted to match the imported VAT amount - provided that the difference between the purchase document’s <b>Assigned Amount Incl. VAT</b> and <b>Imported Amount Incl. VAT</b> is within the <b>Maximum Allowed Difference Incl. VAT</b> defined in the general ledger setup.<br></br> This setting is enabled by default for new installations of Document Capture. For existing users upgrading to this version, the setting is disabled by default and can be enabled manually if this behavior is desired.    |63726|
| Purchase Documents|Capture of item tracking information at the line level has been added to the Purchase category for PDF invoices. This functionality currently only applies to invoice creation without order or receipt matching.<br></br>Tracking capture is enabled by adding by adding one or more of the following line fields to the template: <b>Lot No.</b>, <b>Serial No.</b>, or <b>Package No.</b> To ensure that tracking information is parsed to the purchase invoice line, at least one of these fields must contain a value.<br></br> The line fields <b>Expiration Date</b> and <b>Warranty Date</b> have also been added. If present, values from these fields are parsed along with the tracking information. |64510|
| eDocuments|The <b>Network Profile</b> field on the <b>XML Structure Setup</b> page has been replaced by a new field: <b>Supported by Network Profiles</b>. Selecting this field opens the updated <b>Network Profiles </b>page, where the prioritization of profiles can be adjusted. The top profile in the list is now automatically selected during document sending.<br></br>Additionally, wildcard profile matching has been introduced to support cases where the recipient’s exact profile identifier is unknown. This ensures the correct profile – either a wildcard match or an exact match – is selected when sending documents in the PINT format (e.g.: PINT A-NZ). |64224|
| eDocuments|Line discount amounts are now automatically recognized when importing electronic orders and order changes. |65802|
| eDocuments|When processing an order response that updates an existing purchase order – and the order is in a status other than **Open** – you're now prompted to reopen the order before continuing. Previously, you had to navigate to the order, reopen it manually, and then return to the document journal to complete the update. |66254|
| eDocuments|Previously, when updating the <b>Electronic Format</b> field in **Continia Customer Setup** or **Continia Vendor Setup**, the <b>Send From Participation</b> field retained its value. Now, <b>Send From Participation</b> is intentionally reset when the <b>Electronic Format</b> field is modified to prevent invalid configurations. |66547|
| eDocuments|The AdditionalItemProperty node and its child nodes **Name** and **Value** have been added to the OIOUBLINVOICE and OIOUBLCREDITMEMO eDocuments XML structures. |67958|
| eDocuments|Added a new setting to the <b>Continia eDocuments Setup</b> page: <b>Attach PDF to eDocuments</b>. When enabled, a PDF version of the document is automatically generated and embedded into the XML file. |68101|
| eDocuments|You can now identify and connect with customers and vendors capable of receiving electronic documents more quickly and easily by using the eCandidates feature. This is possible either individually or in batches. |68415|

### Bug fixes

All relevant bug fixes released in service packs and hotfixes up to Service Pack 3, hotfix 3 for Document Capture 2025 R1 (26.00) are also included in Document Capture 2025 R2 (27.00). The description of these bug fixes is not repeated on this page.

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| General Application | When sending invoices as OIOUBL electronic documents, the schematron validation failed if an invoice discount was applied. The following error was shown: <ul><li><em>[F-LIB402] The taxable amount on the Invoice when currency: 'DKK', Tax Category ID: 'StandardRated' and Tax Scheme ID: '63', does not match the sum of taxable amounts from the invoice or credit note lines, after adjusting for allowances (discounts) and charges (fees). A rounding difference of up to +/- 1 is allowed...</em> </li> </ul>Now, documents with combinations of invoice discount % and line discount % are compliant and correctly validated. | 66577 |
| Documents and Templates | The error message displayed when using the <b>Move to Company</b> action without selecting a destination category has been updated for clarity. | 64346 |
| Documents and Templates | Previously, when recognizing an XML document where a template field's XML path contained unsupported characters, Business Central could return an error that caused the page to close unexpectedly. | 65747 |
| Documents and Templates | Due to a change introduced in Document Capture 26.0, the following error could occur when importing documents:<ul><li><em>The following C/AL functions are limited during write transactions because one or more tables will be locked. Form.RunModal is not allowed in write transactions. Codeunit.Run is allowed in write transactions only if the return value is not used. For example, 'OK := Codeunit.Run()' is not allowed. Report.RunModal is allowed in write transactions only if 'RequestForm = FALSE'. For example, 'Report.RunModal(...,FALSE)' is allowed. XmlPort.RunModal is allowed in write transactions only if 'RequestForm = FALSE'. For example, 'XmlPort.RunModal(...,FALSE)' is allowed. Use the COMMIT function to save the changes before this call, or structure the code differently.</em></li></ul> This change has been rolled back and will be reintroduced at a later stage, once the necessary code restructuring has been completed. | 66128 |
| Documents and Templates | The value in the template line field <b>Discount %</b> is now included when using the <b>Create Line on Purchase Order</b> function on the <b>Invoice Matching</b> page. The value is only transferred if the <b>Discount Amount</b> line field is zero. | 66890 |
| Purchase Documents      | When registering different purchase documents (e.g.: invoices and credit memos) that had been assigned the same number during posting, attachments from both documents were incorrectly shown together. | 66059 |
| Purchase Documents      | For easier lookup of the registered document details, a <b>Document Card</b> action has been added to the action group <b>Order</b> on the <b>Sales Order</b> page. | 66235 |
| eDocuments|The <b>Send Electronic Confirmation</b> action has been added to the posted <b>Purchase Invoice</b> page.  |55909|
| eDocuments|During document import, values from the XML <b>Note</b> element were not populated on the document when mapped to a field. |67905|
| eDocuments|In some cases, when sending an eDocument through the Peppol network, the actual delivery date would not be exported – which could cause issues when sending to a receiver that needed that information. Now, the actual delivery date are always exported. |68372|