---
title: Detailed changelog for Continia Document Capture 2025 R1
date: 12-09-2025
description: The detailed changelog for Document Capture 2025 R1.
id: DC-447
lang: en
---

# Detailed changelog for Continia Document Capture 2025 R1

This article lists all new updates, features, service packs, and hotfixes for Continia Document Capture 2025 R1.

> [!TIP]
> As a Continia partner, you can be notified of new Document Capture versions and service packs whenever they're released. To sign up for this service, go to [Receive a notification upon new Document Capture releases](https://continia.zendesk.com/hc/en-us/articles/360005355079-Receive-a-notification-upon-new-Document-Capture-releases) in the Continia PartnerZone.

> [!NOTE]
> Starting with Document Capture 2025 R1, the configuration files and the Continia Web Approval Portal are no longer included in the download package for Document Capture. However, you can find links to download the Web Approval Portal and the configuration files (per localization) within the installation package. The configuration files can also be downloaded directly from Document Capture.

> [!IMPORTANT]
> Document Capture 2025 R1 supports the following versions of Microsoft Dynamics 365 Business Central: Business Central 2025 R1 (v26), Business Central 2024 R2 (v25), and Business Central 2024 R1 (v24).

## Document Capture 2025 R1, Service Pack 3, hotfix 3

*Release date, online: September 11, 2025*  
*Release date, on-premises: September 12, 2025*  
*App version: 26.3.3* 

### Bug fixes

| Functional area | Description | ID |
| --- | --- |  --- |
| Documents and Templates |This issue was solved by reverting the changes related to bug fix ID 57901, in DC 26.0.<br></br>When using brackets in the **Translation From** field in **Line Translations**, the following error was shown during field recognition:<ul><li><em>The filter &quot;&lt;Translation From field value&gt;&quot; is not valid for the Translate From field on the Data Translation table. An error occurred while interpreting the filter: Did not expect '('. For more information, see <a href="https://go.microsoft.com/fwlink/?linkid=2158058">https://go.microsoft.com/fwlink/?linkid=2158058</a>.</em> |69042|
| Documents and Templates |When a template field in a formula referenced a <b>DOCTYPE</b> template field, the value remained empty. Also, when manually updating a field, the change did not carry through to other fields where the current field was part of the formula. |69054|
| Document Approval |Shared approval entries were incorrectly sorted in the&nbsp;<b>Purchase Approval Entries</b>. |69079|

## Document Capture 2025 R1, Service Pack 3, hotfix 2

*Release date, online: August 29, 2025*  
*Release date, on-premises: September 5, 2025*  
*App version: 26.3.2* 

### Bug fixes

| Functional area | Description | ID |
| --- | --- |  --- |
| Documents and Templates |When a template field in the **Formula** referenced another template field in the **Formula**, the value sometimes remained empty unless the fields were correctly ordered on the template. Also, when manually updating a field, the change did not carry through to other fields where the current field was part of the formula.<br/><br/>Now, values are correctly captured and updated regardless of the field order on the template. |68889|

## Document Capture 2025 R1, Service Pack 3, hotfix 1

*Release date, online: August 27, 2025*  
*App version: 26.3.1*

### Bug fixes

| Functional area | Description | ID |
| --- | --- |  --- |
| Documents and Templates |When using a template field in <b>Formula</b> which refers to another template field in <b>Formula</b>, the following error was displayed during field recognition: <ul><li><em>&lt;Template field name&gt;</em>. </li></ul> |68808|

## Document Capture 2025 R1, Service Pack 3

*Release date, online: August 21, 2025*  
*Release date, on-premises: August 21, 2025*  
*App version: 26.3.0*

### New or changed functionality

| Functional area | Description | ID |
| --- | --- |  --- |
| General Application|A <b>Download </b>action has been added to the <b>Document Attachments</b> page, allowing you to download the document directly without viewing the content beforehand. If multiple records are selected, the <b>Download </b>and <b>Open </b>actions are disabled to align with standard Business Central functionality. |64599|
| eDocuments|The AdditionalItemProperty node and its child nodes Name and Value have been added to the OIOUBLINVOICE and OIOUBLCREDITMEMO eDocuments XML structures. |67958|
| eDocuments|You can now identify and connect with customers and vendors capable of receiving electronic documents more quickly and easily by using the eCandidates feature. This is possible either individually or in batches. For more information, see [Setting up customers and vendors for Continia eDocuments](@DC-180).  |68415|


### Bug fixes

| Functional area | Description | ID |
| --- | --- |  --- |
| Documents and Templates |When recognizing XML purchase documents, the comments for template fields with a formula configured were not shown in the document journal. |59237|
| Documents and Templates |When using translations for the <b>Number </b>or <b>Description </b>fields in the document card, filter expressions (e.g.: 0..9999 or freight\|delivery) were interpreted as an exact match rather than as range or multi-value filters. |67080|
| Documents and Templates |When using the <b>Move to Company</b> functionality and not having permissions to access all companies in the database, the following error was shown: <ul><li><em>Access is denied to company <b>&lt;company name&gt;</b>.</em> </li> </ul> |68400|
| Document Approval|When using the <b>Approve</b>, <b>Reject</b>, or <b>Forward </b>actions on the <b>Purchase Approval Entries</b> page, the page filters were unintentionally removed. |67544|
| Document Approval|When using the <b>Approve</b>, <b>Reject</b>, or <b>Forward </b>actions on the <b>Purchase Approval Entries </b>page, the sorting is now no longer reset.  |68465|
| General Application|The Continia Sustainability app validation process has been improved to prevent the following error from showing when using the <b>Recognize Fields </b>action: <ul><li><em>The length of the string is &lt;value&gt;, but it must be less than or equal to 20 characters.</em> </li> </ul> |68158|
| General Application|When trying to personalize the <b>Posted Sales Invoice</b> list in a company where Document Capture was not activated, the following error was shown: <ul><li><em>The Document Capture Setup does not exist. Identification fields and values: Primary Key='' &quot;</em></li> </ul> |68330|
| General Application |When copying a company in an on-premises installation and Continia eDocuments wasn't licensed, the following error message was shown: <ul><li><em>Sorry, the current permissions prevented the action. (CodeUnit 6225608 CTS-CDN Env. Cleanup Subscr. Execute: BaseApplication)</em> </li> </ul> |67696|
| Order & Receipt Matching|When conducting an order or receipt match, the <b>Difference </b>field on the <b>Invoice Matching</b> and <b>Credit Memo Matching</b> pages was not populated. |67078|
| Order & Receipt Matching|When manually matching a document to an order line, where the <b>Outstanding Qty. (Base)</b> was lower than the <b>Matched Quantity</b>, the following error was shown upon registering the document:   <ul><li><em>The quantity (&lt;Matched Quantity&gt;) that you're trying to invoice is greater than the outstanding quantity in &lt;Purchase Document&gt; &lt;Purchase Document No.&gt;. You cannot invoice more than &lt;Purchaseline.Quantity&gt; units.</em> </li> </ul> |68078|
| Platform and Technology|Previously, the Azure Blob Storage container setup validation was only performed when importing documents via the <b>Import Files</b> action tile. It is now also performed when importing individual or selected files from the <b>Display Documents </b>page. |68241|
|eDocuments|When using the **Clear** action on the **XML Structure References** page, the individual code list translations weren't removed from code list mappings. |65605|
|eDocuments|The <b>MultiplierFactorNumeric </b>node in eDocuments for the&nbsp;Document Output&nbsp;export functionality was previously formatted as an integer, which could result in invalid eDocuments. It is now correctly formatted as a decimal. |68216|
|eDocuments|If the initial network document status synchronization fails in NemHandel, the system now retries after 1 day instead of 3. |68431|
| eDocuments|When sending an order response document that included lines not of type Item, the following error could occur: <ul><li>&nbsp;<em>Item does not exist. Identification fields and values: No.=&lt;Item No.&gt;.</em> </li> </ul> |57400|
| eDocuments|When sending an eDocument where the contact name exceeded 50 characters, the following error would occur: <ul><li><em>The length of the string is &lt;Length&gt;, but it must be less than or equal to 50 characters.</em> </li> </ul> The character limit is now 100, aligning with the limit of the <b>Contact Name</b> field. |64514|
| eDocuments|When a purchase order contained comment type lines, eDocument generation could fail with the following validation error:<ul><li><em>Price Amount is mandatory for line &lt;Line No.&gt;</em> </li> </ul> |66187|
| eDocuments|The automated update of sending and receiving capabilities, configured in the&nbsp;<b>eDocument Setup, </b>would fail when trying to look up the receiving capabilities of a vendor or customer with a malformed&nbsp;identification value (e.g.: incorrect number of characters, failed modulus check). |67051|
| eDocuments|When a document was registered using a template with registration step 2 configured (e.g.: release or send for approval) and step 2 failed during execution, any attached XML files would be lost. Attachments are now retained correctly in this scenario.|67240|
| eDocuments|For the Norwegian localization, the successful eDocuments status value was incorrectly translated as <em>Mislyktes</em> (Failed), even when the document transmission was successful. |67675|
| eDocuments|The number of decimal places has been increased from 2 to 4 for the InvoiceQuantity node in OIOUBLINVOICE and the CreditedQuantity node in OIOUBLCREDITMEMO in the eDocuments XML structures. |68036|
| eDocuments|Previously, 0 (zero) taxable amounts were not included in OIOUBL orders. |68132|
| eDocuments|When trying to send an invoice response to a vendor that was set up with the PINT A-NZ electronic document format, the invoice response page would not open. |68168|
| eDocuments|Implemented functionality to add the <b>Foretaksregisteret </b>CompanyID in PEPPOL BIS 3 when the customer or supplier is located in Norway. |68648|

## Document Capture 2025 R1, Service Pack 2, hotfix 2

*Release date, online: August 06, 2025*  
*App version: 26.2.2*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Documents and Templates |When using the <b>Move to Company</b> functionality and not having permissions to access all companies in the database, the following error was shown:<ul><li><em>Access is denied to company <b>&lt;company name&gt;</b>.</em> </li> </ul> |68400|
| Order & Receipt Matching|When manually matching <span>a document<span>&nbsp;</span></span>to an order line where the <b>Outstanding Qty. (Base)</b>&nbsp;was lower than the <b>Matched Quantity</b>, the following error was shown upon registering the document:<ul><li><em>The quantity (&lt;Matched Quantity&gt;) that you're trying to invoice is greater than the outstanding quantity in &lt;Purchase Document&gt; &lt;Purchase Document No.&gt;. You cannot invoice more than &lt;Purchaseline.Quantity&gt; units.</em></li> </ul> |68078|

## Document Capture 2025 R1, Service Pack 2, hotfix 1

*Release date, online: July 21, 2025*  
*App version: 26.2.1*

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Documents and Templates |Due to an unintended change introduced in Document Capture 26.0, it was not possible to select which master template to base a new template on when importing documents from a new vendor – if more than one was available. This behavior has been reverted, so you can once again choose the desired master template. |67185|
| eDocuments |When copying a company in an on-premises installation and an unlicensed Continia eDocuments, the following error message was shown:<ul><li><em>Sorry, the current permissions prevented the action. (CodeUnit 6225608 CTS-CDN Env. Cleanup Subscr. Execute: BaseApplication).</em></li></ul> |67696|

## Document Capture 2025 R1, Service Pack 2

*Release date, online: June 25, 2025*  
*Release date, on-premises: June 25, 2025*  
*App version: 26.2.0*

### New or changed functionality

| Functional area | Description | ID |
| --- | --- |  --- |
| Documents and Templates |When deleting a vendor, any unused templates associated with that vendor will also be deleted automatically – provided that the user has the necessary permissions to delete templates. If not, only the vendor will be deleted. |50687|
| Documents and Templates |When using the <b>Move to Company</b> action in the document journal, the window for selecting the destination company and category now only shows the <b>Display Name</b> of the destination companies – and not the company name. If a company's display name is not configured, the company name is shown instead. |65052|
| Order and Receipt Matching |When using unit of measure-based purchase order/receipt matching, the <b>Invoice Matching</b> and <b>Credit Memo Matching</b> pages have been improved with the following: <ul><li>The base quantity and base unit cost values are displayed for purchase orders, purchase return orders, posted purchase receipts, posted return shipments, and document lines.</li><li>The standard quantity and unit cost fields for purchase orders, purchase return orders, posted purchase receipts, and posted return shipments can be shown or hidden using the <b>Show Qty. and Unit Cost</b> or <b>Hide Qty. and Unit Cost </b>actions.</li></ul> |64931|
| eDocuments|Line discount amounts are now automatically recognized when importing electronic orders and order changes. |65802|
| eDocuments|When processing an order response that updates an existing purchase order – and the order is in a status other than **Open** –, you are now prompted to reopen the order before continuing. Previously, you had to navigate to the order, reopen it manually, and then return to the document journal to complete the update. |66254|
| eDocuments|Previously, when updating the <b>Electronic Format</b> field in the **Continia Customer Setup** or **Continia Vendor Setup**, the <b>Send From Participation</b> field retained its value. To prevent invalid configurations, <b>Send From Participation</b> is now intentionally reset when the <b>Electronic Format</b> field is modified. |66547|
| XML Export|Added support for payment discounts in XML export when exporting electronic documents from sales invoices and service invoices. |66305|

### Bug fixes

| Functional area | Description | ID |
| --- | --- |  --- |
| Documents and Templates |Previously, attempting to open the document journal could result in the following error if security filters were applied to a customer or vendor:<br> <ul><li><em>A security filter has been applied to table &lt;Table Name&gt;. You cannot access records that are outside of this filter. Page document journal has to close.</em> </li> </ul> Now, users with security filters applied can still open the document journal and view all documents. However, limited access to vendors or customers will restrict which documents can be recognized or processed. |57402|
| Documents and Templates |Previously, applied line recognition suggestions would not reappear if they were later manually reset. Now, various suggestions to improve line recognition continue to appear as long as the document values prompt a suggestion and the suggestion has not been explicitly disabled.|59831|
| Documents and Templates |Previously, the act of registering either partially or completely matched documents could be blocked due to the following error comment: <ul><li><em>No Account has been configured for &lt;template field Amount Excl. VAT/GST/Tax&gt;.</em> </li> </ul> |60850|
| Documents and Templates |Previously, capturing a negative amount value could cause an error if the <b>Change Sign</b>option on the **Template Field Card** was enabled.  |62307|
| Documents and Templates |Previously, when recognizing FIK codes, an incorrect value could be returned if the leading characters were incorrect. Attempting to fix the value manually could sometimes cause the last eight digits to be changed incorrectly. Now, the last eight digits always match the last eight digits of the recognized series.  |63625|
| Documents and Templates |When using the <b>Create/Select Template</b> action in the document journal, it was possible to choose blocked templates. Now, you are only presented with eligible templates. |64321|
| Documents and Templates |If the currently selected template or all templates for the vendor are blocked, a new template is now created when using <b>Recognize Fields</b> in the document journal. |64385|
| Documents and Templates |Previously, it was possible to register a document that had an account type specified – but no account number – on the <b>Accounts for Amounts</b> page. |64522|
| Documents and Templates |When registering a purchase document with an invoice discount amount to the general journal or the purchase journal, the following error message was displayed: <ul><li><em>The Purchase Header does not exist. Identification fields and values: Document Type='Quote',No.=''</em> </li> </ul>An error is now displayed in the comment section before registering the document, stating that registering an invoice discount amount to a journal is not possible:<ul><li><em>The Invoice Discount Amount cannot be registered in the journal.</em> </li> </ul> |64743|
| Documents and Templates |Now, when selecting <b>Move to Company</b> in the document journal, the list of destination companies only includes companies that have Document Capture configured.  |64978|
| Documents and Templates |Previously, when using the <b>Create Vendor</b> action in the document journal, the recognized and suggested VAT number for the new vendor could in some cases be the VAT number of the receiver. Now, the VAT number field is left empty if the document value captured is the same as configured in the company information. |65562|
| Documents and Templates |The document line field was not populated during document recognition when the <b>When Value is Empty</b> setting on the template field card was set to <b>Copy value from previous line</b>, <b>Copy value from header field</b>, or <b>Copy value from line field</b>. |65830|
| Documents and Templates |The following only applies to the Swedish (SE) localization.<br><br/>One of the options in the <b>Item Charge Assignment Method</b> field on the template card was incorrectly translated to *Efter mängd*. It's now correctly translated to *Efter belopp*.  |66321|
| Documents and Templates |When the <b>Check Item Prices</b> setting was enabled in the template card to validate item sales and purchase prices, the currency code in the document header was ignored – resulting in item prices being calculated based on the local currency.  |66509|
| Documents and Templates |The template header field <b>Due Date</b> was unintentionally left empty when the currency code was not recognized and <b>LCY Code</b> in the <b>General Ledger Setup</b> was also empty. |66747|
| General Application|Previously, when executing the storage migration process, it was possible to create a job queue entry without the necessary permissions – which caused the migration to fail without notifying you. Now, you can only initiate the storage migration process if you have the required permissions. |64138|
| General Application|When the <b>Check Item Prices</b> setting was enabled in the template card to validate item sales and purchase prices, prices specified in the sales price list or purchase price list were not considered. Instead, it used the item price from the **Item Card**. |65711|
| General Application|The following only applies to the Belgian (BE) localization.<br><br/>When creating a customer or vendor using the <b>Create Customer</b> or <b>Create Vendor</b> actions, the <b>Enterprise No.</b> was not transferred accordingly. |66002|
| General Application|When a customer or a vendor was deleted, the following error could occur: <ul><li><em>Your changes cannot be saved at the moment because a record in the table ‘CDC All Record Tree Relation’ is being updated in a transaction that is executed by another session. You must wait until the other transaction is completed. This may take a while. Please try again later.</em></li> </ul> |67215|
| Order and Receipt Matching |When matching a purchase invoice to a purchase receipt and registering the document as a new invoice, attachments from the purchase order – shown in the standard Business Central FactBox – were not transferred to the created purchase invoice.  |62312|
| Order and Receipt Matching |The translations of the terms <b>Match Base Quantity </b>and <b>Match Base Unit Cost </b>have been updated on the <b>Invoice Matching </b>page for Danish, Finnish, and Norwegian (Bokmål) localizations. |65328|
| Order and Receipt Matching |When adding line translations for sales or purchase items on the document card, the <b>Base Unit of Measure</b> value from the **Item Card** was applied instead of the <b>Sales Unit of Measure</b> or <b>Purch. Unit of Measure</b>. |65647|
| Platform and Technology|Previously, when running the <b>Import Files</b> function, the following error message could occur: <ul><li><em>The length of the string is 1091, but it must be less than or equal to 1024 characters. Value: The request to Continia Online failed.<br></em><em>Http error: 502 - Message:</em>  </li> </ul> |61206|
| Purchase Documents|Using **Create**, **Cancel**, or **Create Corrective Credit Memo** on a purchase invoice that was posted directly from a purchase order caused a large number of documents to be attached to the new document. This functionality has now been rolled back to its previous behavior: no attachments are copied to the new document when performing any of these actions.  |67175|
| Documents and Templates |Previously, when moving a ZUGFeRD document to another company using the <b>Move to company</b>&nbsp;action in the document journal, any attachments to the document would be lost. |63087|
| eDocuments |A translation error in the Norwegian (NO) localization prevented the options in the <b>Value Operation</b>&nbsp;dropdown menu from appearing. |65483|
| eDocuments |Previously, it was not possible to open the <b>Outgoing Network Documents</b>&nbsp;page in solutions activated with demo credentials – such as cloud sandboxes or the demo portal. |66263|
| eDocuments|When importing a document with multiple tax specifications on the document lines – each with the same&nbsp;tax percentage,&nbsp;tax category ID,&nbsp;and&nbsp;tax scheme ID – the following error was shown: <ul><li><em>The record in &quot;VAT Specification&quot; already exists. Identification fields and values: &lt;record primary key fields&gt;</em> </li> </ul> |64022|
| eDocuments|The following adjustments have been made to the eOrder creation process:  <ul><li>The <b>/BuyerCustomerParty/EndpointID</b> node now includes the country code in the eOrder XML. </li><li>The <b>DueDate</b> node is now included in the XML to prevent a schematron validation warning. It is populated based on the purchase order <b>Due Date</b> field.</li> </ul>|65224|
| eDocuments|Previously, the item number was not exported to the <b>cac:BuyersItemIdentification</b>&nbsp;element in the OIOUBL order XML structure. Now, the item number is correctly included in the OIOUBL order lines, ensuring valid XML structure for compliance and downstream processing.|65858|
| eDocuments|Previously, a 0 (zero) VAT percentage was not applied to the eOrder and eOrder change XML eDocuments. Now, 0% VAT is correctly included where applicable. |66199|
| eDocuments|Previously, when re-registering an order after the original had been deleted, the corresponding order response could not be processed due to the missing original order ID – and the following error occurred: <ul><li><em>The Sales Header does not exist. Identification fields and values: Document Type='Order', No.=&lt;Order No.&gt;</em> </li> </ul>|66256|
| eDocuments|The&nbsp;<b>MultiplierFactorNumeric</b> XML element, which represents the discount percentage, is now included in electronic orders.   |66257|
| eDocuments|Local eDocument identification fields – such as **Enterprise No.** (BE) and **ABN** (AU) – are no longer imported into localizations where the corresponding fields are not present on the related source records. |66366|
| eDocuments| The following only applies to the Belgian (BE) localization.<br>Previously, vendor identification using the **Enterprise No.** in eBilling documents did not function as expected. This has been adjusted to improve the processing of eDocuments. |66464|
| eDocuments|It is now possible to specify IBAN payments in OIOUBL electronic invoices, which was unintentionally blocked. |66473|
| eDocuments|Added missing tooltips to several fields on the <b>eDocument Customer Setup</b> page. |66825|
| eDocuments|Allowance charges were missing in OIOUBL order lines, which could lead to incomplete or non-compliant order documents. Now, allowance charges are correctly included in the generated OIOUBL order lines.  |66970|
| XML Export|Previously, eDocuments for sales invoices and credit memos containing comment type lines could generate incorrect tax totals.&nbsp; |65765|

## Document Capture 2025 R1, Service Pack 1, hotfix 2

*Release date, online: May 30, 2025*  
*App version: 26.1.2*

### Bug fixes

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| Purchase Documents      | When attempting to cancel a posted purchase invoice, the following error could occur:<ul><li><em>App Document Capture is not activated.</em></li></ul> | 66573 |
| Documents and Templates | When importing documents using a job queue, the following error could occur:<ul><li><em>Microsoft Dynamics 365 Business Central Server attempted to issue a client callback to show a selection menu: (Table 6085579 CDC Template). Client callbacks are not supported on Microsoft Dynamics 365 Business Central Server.</em></li></ul> | 66824 |

## Document Capture 2025 R1, Service Pack 1, hotfix 1

*Release date, online: May 27, 2025*  
*App version: 26.1.1*

### Bug fixes

| Functional area    | Description                                                  | ID    |
| ------------------ | ------------------------------------------------------------ | ----- |
| Purchase Documents | When attempting to register a purchase order, the following error could appear:<ul><li><em>The length of the string is xx, but it must be less than or equal to 80 characters. Value: \<text\>: \<Document No.\> Order No.: \<Order No.\></em></li></ul> | 64497 |

## Document Capture 2025 R1, Service Pack 1

*Release date, online: May 14, 2025*  
*Release date, on-premises: May 14, 2025*  
*App version: 26.1.0*

### New or changed functionality

| Functional area | Description                                                  | ID    |
| --------------- | ------------------------------------------------------------ | ----- |
| eDocuments      | The&nbsp;<b>Network Profile</b>&nbsp;field on the<b>&nbsp;XML Structure Setup</b>&nbsp;page has been replaced by the <b>Supported by Network Profiles</b>&nbsp;field, which opens the updated <b>Network Profiles</b>&nbsp;page. This page allows you to tweak the prioritization of network profiles, and ensures that the top profile in the list is automatically selected.<br/><br/>Additionally, wildcard profile matching has been implemented to support scenarios where the recipient’s exact profile identifier is unknown. This ensures that the correct profile (wildcard or exact) is selected when sending documents in the PINT format (e.g.: PINT A-NZ). | 64224 |
| eDocuments      | Support for the PINT and PINT A-NZ Billing BIS formats has been added. The PINT A-NZ specification becomes mandatory for eInvoicing in Australia and New Zealand on 15 May 2025, replacing the A-NZ Peppol BIS 3.0 format – which is no longer supported.<br/> <br/>For more information, see [Understanding PINT and PINT A-NZ for eInvoicing in Australia and New Zealand](@DC-463). | 62709 |
| XML Export      | The following improvements have been added to the ZUGFeRD format: <br/>Lines in CII invoices/credit memos with a 0% line discount no longer trigger the following warning when validating an XML file:<ul><li><em>Item net price MUST equal (Gross price - Allowance amount) when gross price is provided.</em> </li></ul>Comment lines containing a VAT posting group selected in the CII invoice/credit memo lines no longer result in an incorrect tax category being specified in the XML files.<br/><br/>The <b>External Document No. </b>field now appears in the CII invoice/credit memo XML files when it contains a value. | 64933 |


### Bug fixes

| Functional area         | Description                                                  | ID    |
| ----------------------- | ------------------------------------------------------------ | ----- |
| Documents and Templates | Previously, when using the <b>Change Category</b> action for an XML documents in the document journal, the following error could occur:<ul><li><em>File Type must be equal to 'OCR' in Document: &lt;Document No.&gt; Current value is 'XML'.</em> </li></ul> Additionally, if the assigned category is incorrect, an error comment is now shown: <ul><li><em>The assigned document category does not support this document. Please use the 'Change Category' action to move it to the &lt;Document Category Code&gt; category.</em></li></ul> | 65717 |
| eDocuments              | Previously, importing OIOUBL electronic documents that included line discounts could result in an incorrect unit price being captured. | 63275 |
| eDocuments              | When sending an order confirmation in the OIOUBL format where the <b>Ship-To Country/Region Code</b> was empty, the following error could occur: <ul><li><em>The Country/Region does not exist. Identification fields and values: Code=''</em></li></ul> | 64231 |
| eDocuments              | Previously, when moving an unregistered eDocument to another company, an error could occur. | 64686 |
| eDocuments              | When sending an electronic Peppol document for a posted invoice containing lines with a quantity of 0, the following error was shown:<ul><li><em>Attempted to divide by zero.</em> </li></ul> | 64881 |
| eDocuments              | Previously, when exporting an OIOUBL XML document, a source document line with a unit of measure different from the base unit and a quantity per unit of measure other than 1 resulted in incorrect values in the XML file. The invoice line price amount was inaccurate, and the base quantity was set to the quantity per unit of measure.<br/><br/>Now, the base quantity is correctly set to 1, and the price amount reflects the price of a single item in the line. | 64977 |
| eDocuments              | When importing OIOUBL invoice or credit memo responses, the following error could occur: <ul><li><em>There is no Template within the filter.&nbsp;</em><em>Filters: Category Code: PURCHASE, Type: Master, Data Type: XML, XML Identification Template: EBILLINGRESP-ID</em> </li> </ul> | 65445 |
| eDocuments              | Previously, the SenderParty EndpointID&nbsp;and ReceiverParty EndpointID nodes in the Peppol BIS3 and OIOUBL XML structures were incorrectly&nbsp;mapped, resulting in invalid eDocuments. | 65446 |
| eDocuments              | The price amount node in the PINT and Peppol formats was limited to two decimal places. This limit has now been extended to support up to ten decimal places. | 65703 |
| General Application     | Previously, the sending of NemHandel eDocuments was considered successful if no negative receipt was received within 48 hours, even when no delivery confirmation was available.<br/><br/>Now, both positive and negative receipts can be received for outgoing NemHandel eDocuments, allowing for more accurate tracking of delivery status. | 65596 |
| General Application     | When opening the <b>Outgoing Network Documents</b> page, the following error could occur: <ul><li><em>Current permissions prevented the action.(CodeUnit 6225510 CTS-CDN eDocument Table Mgt. Execute: Continia Delivery Network) </em> </li> </ul>This only applies to on-premises installations. | 66285 |
| XML Export              | Previously, creating a Document Output setup for a customer and changing the output profile to ZUGFeRD could cause CII invoices and credit memos to use the incorrect GuidelineSpecifiedDocumentContextParameter in the XML file. | 65200 |
| XML Export              | When sending a Peppol document based on an invoice where&nbsp;<b>Price Incl. VAT</b>&nbsp;was set to true, the resulting document could in some cases include the invoice line price amount with VAT included – instead of excluding VAT as expected. | 65235 |
| XML Export              | When creating ZUGFeRD eDocuments, the following error could occur in some cases:<ul><li><em>The following fields must be of the same type:<br/>    Field: \<from field name\> <-- \<to field name\><br/>    Table: \<from table name\> <-- \<to table name\><br/>    Type: \<from data type\> <-- \<to data type\></em></li></ul> | 65816 |

## Document Capture 2025 R1, hotfix 5

*Release date, online: May 9, 2025*  
*Release date, on-premises: May 9, 2025*  
*App version: 26.0.5*

### Bug fixes

| Functional area | Description | ID |
| --- | --- |  --- |
| Documents and Templates |When using the **Select/Create Template** action in the document journal, the choice of which master template to use when creating a vendor template had unintentionally been disabled. |65855|

## Document Capture 2025 R1, hotfix 4

*Release date, online: May 2, 2025*  
*App version: 26.0.4*

### Bug fixes

| Functional area | Description | ID |
| --- | --- |  --- |
| General Application |On-premises customers could, in certain scenarios, see the following error when upgrading Document Capture:<ul><li><em>Could not upgrade the extension 'Continia Document Capture' by 'Continia Software' from version '\<from version no\>' to '\<to version no\>' for tenant '\<tenant ID\>' and company '\<company name\>' due to the following error: 'Sorry, the current permissions prevented the action. (Codeunit 6086228 CTS-CDN License Mgt. Execute: Continia Document Capture)'.</em></li></ul> |66135|
| General Application |When importing documents, the following error would occur due to a change introduced in Document Capture 26.0:<ul><li><em>The following C/AL functions are limited during write transactions because one or more tables will be locked.<br><br> Form.RunModal is not allowed in write transactions.<br/><br/> Codeunit.Run is allowed in write transactions only if the return value is not used. For example, 'OK := Codeunit.Run()' is not allowed.<br/><br/> Report.RunModal is allowed in write transactions only if 'RequestForm = FALSE'. For example, 'Report.RunModal(...,FALSE)' is allowed.<br/><br/> XmlPort.RunModal is allowed in write transactions only if 'RequestForm = FALSE'. For example, 'XmlPort.RunModal(...,FALSE)' is allowed.<br/><br/> Use the COMMIT function to save the changes before this call, or structure the code differently.</em></li></ul>This change has been revised, and will be reintroduced later when the code is restructured. |66128|

## Document Capture 2025 R1, hotfix 3

*Release date, online: April 28, 2025*  
*App version: 26.0.3*

### Bug fixes

| Functional area | Description | ID |
| --- | --- |  --- |
| Documents and Templates |When using the **Select/CreateTemplate** action in the document journal, the choice of which master template to use when creating a vendor template had unintentionally been disabled. |65855|
| Documents and Templates |Trying to change the value in the <b>No.</b> field on a purchase line for a document that was pending approval, while the <b>Can Edit Posting Lines</b> setting was enabled in the **Continia User Setup**, resulted in the following error: <ul><li><em>Status must be equal to 'Open' &nbsp;in Purchase Header: Document Type=&lt;Document Type&gt;, No.=&lt;Document No.&gt;. Current value is 'Pending Approval'.</em> </li> </ul> |65861|
| Purchase Documents |Previously, attachments copied using&nbsp;the&nbsp;<b>Correct</b>,&nbsp;<b>Cancel</b>,<b>&nbsp;</b>or&nbsp;<b>Create Corrective Credit Memo</b>&nbsp;actions on a posted purchase invoice could not be opened from the newly created purchase document. |65702|

## Document Capture 2025 R1, hotfix 2*

*Release date, online: April 9, 2025*  
*App version: 26.0.2*

### New or changed functionality

| Functional area | Description | ID |
| --- | --- |  --- |
| eDocuments |When sending an electronic Peppol document for a posted invoice containing lines with a quantity of 0, the following error was shown: <ul><li><em>Attempted to divide by zero.</em></li></ul> |64881|
| eDocuments |The following error was shown when running the Document Capture assisted setup: <ul><li><em>Sorry, the current permissions prevented the action. (TableData 6086242 CTS-CDN eDoc. Payment Means eDocuments Payment Means Insert: Continia Document Capture).</em></li></ul> |65470|

\* The preview version of Document Capture 2025 R1 was released as 26.0.0, and the first official version was released as 26.0.1. Hence there's no hotfix 1.

## Document Capture 2025 R1

*Pre-release date, online: March 21, 2025*  
*Release date, online: April 1, 2025*  
*Release date, on-premises: April 9, 2025*  
*App version: 26.0.1*

### New or changed functionality

| Functional area | Description | ID |
| --- | --- |  --- |
| Country and Regional|The following only applies&nbsp;to the CH (Swiss) localization. <br><br/>When creating a vendor bank account from a QR code, the following fields are automatically populated from the bank directory: <ul><li>Name </li><li>Address </li><li>Address 2 </li><li>City </li><li>Post Code </li><li>SWIFT Code </li> </ul> |59483|
| Documents and Templates | To align with Business Central standards, the template field <b>Account Type </b>has been renamed to <b>Type</b>, and <b>No.</b> has been renamed to <b>No.</b> <br>These changes apply to the following pages: <ul><li>Document Journal </li><li>Document Card </li><li>Accounts for Amounts </li><li>Assigned Amount Lines </li> </ul> Additionally, the field <b>Ask to set Default Account No. </b>on the template has been renamed to <b>Ask to set Default No.</b> |47816|
| Documents and Templates |When selecting the <b>Move To Company</b> action in the document journal, you can now choose both the destination company and the destination category. This allows you to move documents to a different company and category in one step. |49658|
| Documents and Templates |The <b>Item Charge Assignment</b> field on the template card is now only displayed when either of the template match invoice/credit memo options is set to match against receipt or return shipment lines. |52054|
| Documents and Templates |Using the <b>Create Lines</b> action to create the first allocation line on the <b>Purchase Allocations </b>page could result in allocation lines with an incorrect document type. To prevent this, the <b>Create Line </b>action is now only enabled if at least one allocation line has already been created. |53361|
| Documents and Templates |When selecting the <b>Run GDPR Maintenance</b> action in <b>Document Capture Setup </b>to delete old documents, the associated document log entries are also removed. |54731|
| Documents and Templates |To help identify the destination company when moving documents between companies, the <b>Display Name</b> field has been added to the <b>Move to Company</b>&nbsp;page. This field is available through page customization.  |56703|
| Documents and Templates |Validation of&nbsp;Continia Sustainability&nbsp;template&nbsp;header and line&nbsp;fields has been added to the document journal and&nbsp;document card pages. Any validation notifications relating to the sustainability fields are displayed as configurable comments in the <b>Comments</b> section. |57494|
| Documents and Templates |The <b>Change Category</b> action in the document journal now allows you to move a document to any category. Previously, you could only move documents between categories with the same Source Record Table ID. |59661|
| Documents and Templates |When changing a document's category by adding the <b>Document Category Code</b> column to&nbsp;the document journal and updating its value, the recognize fields functionality is now automatically activated in the destination category. |59665|
| Documents and Templates |When recognizing document lines using AI, it is now possible to override the AI’s suggested values for the following line fields: <ul><li>Number </li><li>Description </li><li>Quantity </li><li>Unit Cost </li><li>Line Amount </li> </ul>You can manually capture values either by using the field caption or by selecting a different value directly from the document. |60606|
| Documents and Templates |In&nbsp;<b>Accounts for Amounts</b>, the sustainability fields are only editable when&nbsp;<b>Type</b> is G/L Account or Item.  |62103|
| Documents and Templates |Previously, opening a PDF file would automatically trigger a download to your computer. Now, PDFs open directly in the Business Central client using the new Business Central 2025 R1 standard feature: <b>Preview PDF attachments directly in the web client</b>. This allows you to view documents instantly, while still having the option to download them when needed.  |64353|
| Document Approval|To prevent approval blockages in the Web Approval Portal, enabling one of the following Continia approval workflows in the Document Capture Setup automatically creates an approval user group with the code **ALL**, but only if a group with the same name doesn’t already exist. The group includes all assigning and approval permissions on all types and dimensions.<ul><li>Purchase invoice</li><li>Purchase credit memo</li><li>Purchase order approval</li><li>Purchase return order</li></ul> |45868|
| Document Approval|The settings&nbsp;<b>Enable Order Approval</b> and <b>Enable Return Order Approval</b> have been added to the <b>Purchase&nbsp;</b><b>Approval Setup </b>assisted&nbsp;guide. |49612|
| Document Approval|Added the&nbsp;<b>Document Date </b>field to the <b>Purchase&nbsp;</b><b>Approvals Entries </b>page. |53311|
| General Application|When selecting the<b> Perform Document Check</b> action in the document control log, the filter is now automatically set to show only failed lines – if any are identified.|55040|
| General Application|Read-links have been added to Continia Document Capture entries on the Business Central&nbsp;<b>Assisted Setup</b> page, providing direct access to the related&nbsp;Continia Docs article. |60550|
| Order and Receipt Matching |It's now possible to match purchase invoices and credit memos to purchase orders/receipts or return orders that contain lines with the same line amount, even if they have different units of measure and, as a result, different unit costs. For further details, see [Setting up order and receipt matching](@DC-60). |27261|
| Order and Receipt Matching |To clarify the potential impact on <b>Quantity to Receive </b>for unreceived order lines, the message shown when registering a matched purchase invoice to a purchase order that has already been matched has been extended. |63587|
| Purchase Documents|When using the&nbsp;<b>Correct</b>, <b>Cancel</b>,<b>&nbsp;</b>or <b>Create Corrective Credit Memo</b>&nbsp;actions on a posted purchase invoice, any attachment on the posted invoice is now copied to the document created in the cancel/correct process. The files are copied as drag-and-drop attachments.  |58765|
| Platform and Technology |Document Capture's custom FactBox pane resizing implementation, when running on Business Central 26.0 and above, has been deprecated in favor of Microsoft's latest native implementation.<br><br/>Note that Microsoft's implementation limits the FactBox pane width to a maximum of 50% of the screen, whereas Document Capture's previous implementation allowed for wider expansion. |64858|
| eDocuments |The new Payment Means feature provides you with more flexibility when configuring and using payment means in electronic invoices and credit memos.<br/><br/>For more information, see [Using payment means in eDocuments](@DC-450). |62706|
| eDocuments |You can now use the <b>Create</b> <b>Vendor </b>and <b>Create Customer </b>guides when working with XML/eDocuments received via the Continia Delivery Network. |40795|
| eDocuments|From the <b>Outgoing Network Documents </b>page, you can now send copies of previously sent documents. This feature is available for eDocuments with the status <b>Successful</b> – and only for electronic document formats that support the **Copy Indicator** node. Currently, only the OIOUBL format supports it.<br><br/>When using the <b>Resend </b>action, an eDocument record is created in the Continia Delivery Network, and the document copy is sent automatically. Additionally, a new <b>Copy </b>column has been added to the <b>Outgoing Network Documents </b>page to indicate that the sent eDocument is a copy.|55339|
| eDocuments|The <b>Document Receipts</b> FactBox has been added to the <b>eDocument Overview</b> page.<br><br/>A new field, <b>Document Receipt Status</b>, has been added to the following pages. This field displays the document's latest receipt status, allowing you to track its receipt state directly from the eDocument card. <ul><li><b>eBilling Outgoing Document Card</b> </li><li><b>eBilling Response</b> </li><li><b>eOrder Document</b> </li><li><b>eOrder Response</b> </li> </ul> |56152|
| eDocuments|The following only applies&nbsp;to the DK (Danish) localization. <br/><br>In the newer versions of Business Central, a notification could appear on the Role Center informing you that the company hasn't been registered in the NemHandel network – even if a participation was previously approved through Continia. To remove the notification, open the&nbsp;<b>Continia Delivery Network Participations</b>&nbsp;page containing the approved NemHandel participation. |56617|
| eDocuments|The <b>Skip </b>action has been added to the **Import eDocument Configurations** step in the <b>Set Up Continia eDocuments </b>assisted guide. This action allows the setup to continue without importing a configuration. If this step is skipped and the setup has not been completed previously, the following error is shown: <ul><li><em>The setup has failed. Please, restart the wizard and do not skip the configuration import.</em></li> </ul> |60368|
| eDocuments|The <b>Set Up eDocuments </b>assisted guide has been added to the standard Business Central <b>Assisted Setup </b>list. |60369|
| eDocuments|The following only applies to the BE (Belgian) localization.<br/><br/>The eDocuments source identification by enterprise number has been added to the following Document Capture templates.<br/><br/>    EORDERCANCEL-ID (eOrder Cancellation - Ident.)<br/>    EORDERCHANGE-ID (eOrder Change - Identification)<br/>    EORDER-ID (eOrder - Identification)<br/>    EBILLING-ID (eBilling - Identification)<br/>    EORDERRESP-ID (eOrder - Identification)<br/>    EBILLINGRESP-ID (eInvoice Resp - Identification)  |60665|
| eDocuments|Prior to this, utility statement (UTS) documents failed to be related to the corresponding invoice when the invoice was received using eDocuments. |60906|
| eDocuments|Previously, when sending a Peppol invoice through the Continia Delivery Network while using the standard payment discount functionality in Business Central, the generated electronic document did not reflect the discounts. Now, the discount amounts are correctly applied in the electronic document. |61175|
| eDocuments|It's now possible to set all participations within a company to test mode. To make use of this feature, go to the <b>Continia eDocuments Setup</b> page and enable the <b>Test Mode</b> option. When enabling test mode in a company, the following applies:<ul><li>All communication through the Continia Deliver Network is suspended – no documents are received, and no documents are sent. </li><li>All supported business documents can be resent – regardless of their existing status. Both eDocuments (i.e.: eBilling, eOrder, and eResponse) and related network documents are recreated and marked with the status Test. </li><li>When a company is copied, all existing participations are put in test mode. This goes for companies created within the tenant using the copy functions on the&nbsp;<b>Companies</b> page or when SaaS environments are copied from the Admin Center.</li> </ul> |61704|
| eDocuments|The field **Handle Incoming eBilling Docs** has been added to the **Continia eDocuments Setup** page. This field specifies whether incoming electronic documents of type invoice or credit memo should be processed using the eDocuments feature. |61800|
| eDocuments|To support&nbsp;A-NZ Peppol BIS3 in&nbsp;Australia and New Zealand,&nbsp;two new XML structures have been added: <ul><li><b>ANZPEPPOLBIS3CRMEMO </b>-&nbsp;A-NZ Peppol BIS3 Credit Memo</li><li><b>ANZPEPPOLBIS3INV </b>-&nbsp;A-NZ Peppol BIS3 Invoice </li> </ul> |62091|
| eDocuments|The <b>XML Structure View</b> page layout has been restructured to improve the user experience: <ul><li>Fields which should not be edited (such as <b>Sequence</b>)<b>&nbsp;</b>have been moved to the FactBox as information.&nbsp; </li><li>Fields which are edited less often (such as <b>Line Node</b> and <b>Business Term</b>)&nbsp;have been moved to the FactBox. These can be modified with the use of the new action <b>Modify Details</b>, under the <b>Actions</b> group. </li> </ul>|62923|
| eDocuments|Disabled network profiles and participation ID types are now hidden, and cannot be selected or used for sending eDocuments. This ensures only active metadata is used, improving data integrity and compliance.  |63748|

### Bug fixes

All relevant bug fixes released in service packs and hotfixes up to Service Pack 2, hotfix 1, for Document Capture 2024 R2 (25.00) are also included in Document Capture 2025 R1 (26.00). The description of these bug fixes is not repeated on this page.

>[!NOTE]
>The bug fix with ID 57901 has been reverted in DC 26.3.3. This bug will be readdressed with a different approach in a later service pack. For more information, see [Document Capture 2025 R1, Service Pack 3, hotfix 3](#document-capture-2025-r1-service-pack-3-hotfix-3).

| Functional area | Description | ID |
| --- | --- |  --- |
| Country and Regional|Previously, when creating a vendor from a PDF, recognized country codes with more than two characters would block the vendor creation. |58737|
| Country and Regional|Previously, the&nbsp;<b>VAT Bus. Post. Group</b>&nbsp;column on the&nbsp;<b>Accounts for Amounts</b>&nbsp;page was incorrectly translated in the Swedish localization to<b> Moms produktbokföringsmall</b>. It's now correctly translated to <b>Moms rörelsebokföringsmall</b>.  |62311|
| Country and Regional |A missing English localization has been added for the <b>Delete Blanks</b> field&nbsp;on the&nbsp;<b>Template Field Card</b> page. |64951|
| Documents and Templates |Captions have been removed for the template template line field <b>Order No.</b> as lines fields are only recognized through manual marking. Therefore, the captions serve no purpose. |45900|
| Documents and Templates |When importing multiple files, a field recognition failure in one document prevented subsequent documents from being recognized. |48432|
| Documents and Templates |When using the drop shipment feature on a purchase order line, attempting to update the order quantity from the Purchase Order category would result in the following error:<ul><li><em>Quantity on line <Line No.> cannot be updated. The line is linked to purchase order line <Purchase Order Line No.>, which is associated with sales order <Sales Order No.>.</em></li></ul> |54332|
| Documents and Templates |When reopening a registered document in the Contact category, the created interaction log entry remained on the contact – which could result in the document being registered multiple times. This issue occurred because the reopen codeunit was missing from the category card. A new codeunit has been added to ensure that previously registered data is cleared when reopening the document, preventing duplicate registrations. |57119|
| Documents and Templates |When capturing a value containing an operator character (such as \| or &amp;), the following error could sometimes occur due to incorrect handling of line translation values:&nbsp; <ul><li><em>The filter &quot;...&quot; is not valid for the Translate From field on the Data Translation table. The right side of '\|' operators cannot be empty.</em> </li> </ul> |57901|
| Documents and Templates |Previously, capturing a value that contained certain special characters (such as \\) would result in an &quot;Unrecognized escape sequence&quot; error. This has been adjusted for the following characters: \, +, [, ], {, }, ?, (, ), *. |58452|
| Documents and Templates |Previously, entering a negative value in the header field <b>Type </b>(née **Account Type**)<b>&nbsp;</b>would result in the following error:&nbsp; <ul><li><em>The SELECTSTR comma-string ,G/L Account,Item,Resource,Fixed Asset,Charge (Item),,Amount Distribution Code,Purchase Contract,Allocation Account does not contain a value for index -49999.</em> <em>Page Document Journal has to close.</em> </li> </ul>Now, entering an invalid value clears the field – leaving it empty.  |59880|
| Documents and Templates |Previously, registering a sales document with the same external document number as an existing sales order was not possible, as the registration was blocked by an error comment. To align with Business Central standards, it is now possible to register sales orders with duplicate external document numbers. The comment still appears in the document journal, but it will no longer block registration. |61451|
| Documents and Templates |In certain cases, when recognizing purchase document lines that spanned across multiple pages, values from the last line were not captured. |62183|
| Documents and Templates |Previously, if two or more master templates existed and none were set as default, the following error message appeared when attempting to create a template via the dialog that opens after selecting <b>Recognize Fields</b>: <ul><li><em>An error occurred and the transaction is stopped. Contact your administrator or partner for further assistance.</em> </li> </ul> Now, when selecting the <b>Create New </b>action, the first available template is used if no default master template has been configured. |62339|
| Documents and Templates |The template field rule for Belgian VAT registration numbers in the default setup has been updated from <b>(BE)?0[0-9]{9}</b>&nbsp;to <b>(BE)?[0-9]{10}</b> to ensure a correct identification, as the Belgian VAT numbers can begin with 0 or 1. |64540|
| Document Approval|Spaces have been adjusted in a warning comment related to matching the total amount of purchase receipts.  |53544|
| Document Approval|When using the&nbsp;<b>Send Approval Request</b> action for an open purchase document and no workflow was found, the following misleading error was shown: <ul><li><em>The approval request cannot be sent because the invoice is already pending approval or released.</em> </li> </ul>For open purchase documents, the error message has been updated to:  <ul><li><em>The approval request cannot be sent because no suitable workflow could be found.</em></li> </ul> |55657|
| Document Approval|The following caption and tooltip have been updated on the <b>Document Capture Setup / Continia Web Approval</b> page to better reflect the related functionality: <ul><li>Amounts in LCY =&gt; Total amount in LCY </li><li>Specifies whether to show the amounts on documents in local currency if the document is in a foreign currency. =&gt; Specifies whether to show the total amount on documents in local currency if the document is in a foreign currency. </li> </ul>|61523|
| Document Approval|The following page captions have been updated to use &quot;<b>- Document Capture</b>&quot;&nbsp;instead of &quot;<b>(DC)</b>&quot;: <ul><li><b>Approval Sharing - Document Capture</b> </li><li><b>General Posting Setup - Document Capture</b> </li><li><b>Vendor Posting Groups - Document Capture</b> </li> </ul> This change standardizes the naming convention to improve clarity and consistency. |63549|
| General Application|In certain cases, the&nbsp;<b>Stop Line Recognition</b>&nbsp;setting on the&nbsp;<b>Template Field Card</b>&nbsp;was ignored when capturing purchase document lines using the manual line recognition method. As a result, document lines following the totals were unintentionally captured. |61536|
| General Application |When using the **Create Vendor** guide, it is now possible to clear the **Country Code** and **Currency Code** fields. |64546|
| Purchase Contracts|The option <b>Purchase</b> <b>Contracts </b>has been removed from the <b>Translate to Type </b>field on the <b>Line Translations </b>page because it wasn't a valid option. The **No.** action should be used instead. |54088|
| Purchase Contracts|Previously, when registering a purchase invoice with a purchase contract selected as the account type – and the <b>Auto Approve Within Variance </b>setting on the contract was set to <b>No</b> – the invoice could still be automatically released and approved, if other required conditions were met. |63447|
| Purchase Documents|The misspelling of <b>registrering</b> has been adjusted to <b>registering</b> in several warning comments.|59557|
| Purchase Documents|If a default remit-to code has been configured on the vendor level, the <b>Remit-To Code</b> field on the purchase invoice is now automatically set when registering a document. |62426|
| eDocuments |The template line field <b>No.</b>&nbsp;has been set to not required on the <b>eOrder Response</b> master template. |62437|