This article lists all new features and bug fixes for each version of the Continia Delivery Network.

## Continia Delivery Network 26.01.02

*Released: June 13, 2025*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| eDocuments |Previously, incorrect taxable amounts were shown in Document Output when **Price Incl. VAT** was set to true in an OIOUBL electronic invoice. |67038|

## Continia Delivery Network 25.03.01

*Released: June 3, 2025*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application |When sending invoices as OIOUBL electronic documents, the schematron validation failed if an invoice discount was applied. The following error was shown:<ul><li><em>[F-LIB402] The taxable amount on the Invoice when currency: 'DKK', Tax Category ID: 'StandardRated' and Tax Scheme ID: '63', does not match the sum of taxable amounts from the invoice or credit note lines, after adjusting for allowances (discounts) and charges (fees). A rounding difference of up to +/- 1 is allowed...</em></li></ul>Now, documents with combinations of invoice discount % and line discount % are correctly validated and compliant. |66577|
| eDocuments |Prior to this, invalid XML files were generated when invoice lines contained negative quantities – causing the Peppol network to reject these files. |66696|

## Continia Delivery Network 26.01.01

*Released: May 28, 2025*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application |When sending invoices as OIOUBL electronic documents, the schematron validation failed if an invoice discount was applied. The following error was shown:<ul><li><em>[F-LIB402] The taxable amount on the Invoice when currency: 'DKK', Tax Category ID: 'StandardRated' and Tax Scheme ID: '63', does not match the sum of taxable amounts from the invoice or credit note lines, after adjusting for allowances (discounts) and charges (fees). A rounding difference of up to +/- 1 is allowed...</em></li></ul>Now, documents with combinations of invoice discount % and line discount % are correctly validated and compliant. |66577|
| eDocuments |Prior to this, invalid XML files were generated when invoice lines contained negative quantities – causing the Peppol network to reject these files. |66696|

## Continia Delivery Network 26.00

*Released: April 9, 2025*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|<ul><li>Lines in CII invoices/credit memos with a 0% line discount triggered a warning when validating an XML file: <em>Item net price MUST equal (Gross price - Allowance amount) when gross price is provided.</em></li><li>Comment lines containing a <b>VAT Posting Group</b> selected in the CII invoice/credit memo lines resulted in an incorrect tax category being specified in the XML files. </li><li>The <b>External Document No. </b>field now appears in the CII invoice/credit memo XML files when it has a value.</li> </ul> |64933|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|Creating a new setup for the customer and changing the Output Profile to Zugferd caused CII invoices and credit memos to use the incorrect GuidelineSpecifiedDocumentContextParameter in the XML file. |65200|

## Continia Delivery Network 25.01.03

*Released: January 24, 2025*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|When exporting electronic documents that contain comment lines in the ZUGFeRD format, the document failed validation.&nbsp; |63234|
| Country and Regional|When exporting electronic documents in the ZUGFeRD format, the validation failed when either the sender's or the receiver's identifier wasn't part of the ISO 6523 ICD list. Now, the GlobalID element is only created when the identifier is part of the ISO 6523 ICD list. |63235|
| Platform and Technology|When sending an XML document through Document Output and attaching a note with content longer than 1,024 characters, the following error was shown:<ul><li>*The Length of the string is <Length> but it must be less than or equal to 1024. Value:* <String value>.</li></ul>Now, the number of characters is not limited. |63130|

## Continia Delivery Network 25.01.02

*Released: January 21, 2025*  
### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|When sending an issued reminder electronically, with a customer ledger entry line with an amount equal to zero, the electronic document failed network validation. The field <b>Remaining Amount</b>&nbsp;is now also included in the electronic OIOUBL Reminders. |62453|
| Country and Regional|When exporting electronic documents in the ZUGFeRD format, the document failed validation. The validation errors were related to:&nbsp; <ul><li>Document amounts and their formatting </li><li>Wrong namespace URL used for the QualifiedDataType namespace </li> </ul>To better control the identification of ZUGFeRD and XRechnung documents, two fields have been added to the&nbsp;<b>CDN Customer Setup </b>page:<ul><li>**CII Process ID** - defines the version of the ZUGFeRD format for the&nbsp;<b>Business Process Specified Document Context Parameter </b>node.</li><li>**XRechnung ID** - defines the version of the XRechnung format for the&nbsp;<b>Customization ID</b> node.</li> </ul>When exporting electronic documents in the ZUGFeRD or XRechnung formats, the latest version of the format will be used&nbsp; (urn:cen.eu:en16931:2017#compliant#urn:xeinkauf.de:kosit:xrechnung_3.0).  |62693|
| eDocuments|<span>Switching from demo credentials to production credentials and running the Continia Delivery Network onboarding could result in duplicate metadata records being created.</span> |61905|
| eDocuments|Enabled export of billing reference in Peppol credit memos. The value exported is 'Applies To Document No.', from the **Sales Credit Memo** header. If that value is empty, the default value 'N/A' is applied. |62577|
| eDocuments|When recognizing an order change as an eDocument in Document Capture, the following error was shown: <ul><li><em>There is no eOrder Header within the filter.&nbsp;<span>Filters: eDocument Status: Registered, Created: &lt;&lt;Created Date Time&gt;.</span></em>  </li> </ul> |62715|
| General Application|When sending an OIOUBL electronic invoice or credit memo using Document Output, the document failed network validation and the following error was shown: <ul><li><em>[F-LIB381] Invalid VAT TaxAmount - When TaxCategory/ID are 'StandardRated' and TaxableAmount &gt; 0 (&lt;TaxableAmountValue&gt;) TaxAmount can't be '(0.00)' unless calculated vat '(&lt;TaxAmountValue&gt;)' are less then 0.005</em> </li> </ul> |62732|
| General Application|A permission issue would, in certain cases, return the following error: <ul><li>*The current permissions prevented the action. (TableData 6225620 CTS-CDN Part. Prof. Rel. Delete: Continia Delivery Network)*</li> </ul> |62783|

## Continia Delivery Network 25.01.01

*Released: December 19, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| eDocuments|<span>When manually importing a Document Capture configuration file, the following error would appear in certain scenarios</span>: <ul><li><em>The Continia eDocuments Setup does not exist. Identification fields and values: Primary Key-''</em> </li></ul> |62226|
| General Application|When sending an OIOUBL document, the following error occurred: <ul><li><em><span>There is no Network Profile within the filter.&nbsp;</span><span>Filters: CDN GUID: &lt;CDN Guid Value&gt;</span></em></li> </ul>. |62120|

## Continia Delivery Network 25.00.02

*Released: October 31, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
|eDocuments|When sending a sales invoice as a Peppol or OIOUBL electronic document, the endpoint ID for both the customer and the vendor wasn't formatted according to the electronic format requirement. For electronic documents sent via NemHandel that failed validation, this issue prevented proper mapping of the validation error receipt – causing the document to be marked as 'Sent successfully', even though it wasn't actually delivered. |61027|
| eDocuments|When sending a Peppol sales invoice with a negative line quantity or price, the validation failed. |60360|
| eDocuments|When sending a sales invoice as a Peppol or OIOUBL electronic document, any empty fields of type GUID were exported in the XML document. This caused the eDocuments to fail validation. |61144|

## Continia Delivery Network 25.00.01
*Released: October 10, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|When exporting a Peppol document with only a GLN for the delivery information, the document failed validation.&nbsp; |60393|

## Continia Delivery Network 25.00
*Released: October 1, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|For the New Zealand localization, the company identifier was taken from the field&nbsp;11620&nbsp;ABN and not from the field with number 90&nbsp;GLN.&nbsp; |58005|
| General Application|When exporting a Peppol XML document, the allowance charge node wasn't created when the line discount amount was less than 0. |57836|

## Continia Delivery Network 24.02.01
*Released: September 17, 2024* 

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|When exporting a Peppol document from a Danish company, the payment means information was wrongly created, causing the document to fail validation. |59509|

## Continia Delivery Network 24.02
*Released: August 30, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | Id |
| --- | --- |  --- |
| Country and Regional|Fixed the following issues in OIOUBL Order: <ul><li>Updated UBL version from 2.01 to 2.1 </li><li>Ensured that&nbsp; &quot;Contact ID&quot; is populated in the BuyerCustomerParty class. </li><li>Corrected an issue that that in some cases could populate the Amount field with the VAT Amount. </li> </ul> |57394|
| Country and Regional|For the New Zealand localization, the company identifier was taken from the field&nbsp;11620&nbsp;ABN and not from the field with number 90&nbsp;GLN.&nbsp; |58005|
| General Application|<span>When an eOrder response document is used to relay an item substitution from the selling party to the buying party, the substituted Item No. did not propagate correctly to the purchase document at the buying party.</span> |56149|
| General Application|When exporting an Peppol XML document the allowance charge node was not created when <b>Line Discount Amount</b> was less than 0. |57836|

## Continia Delivery Network 24.01.07
*Released: August 7, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
|eDocuments|Prior to this fix, the following error was thrown when receiving a posted sales invoice or<span> </span>a purchase order with varying VAT percentages on different lines (e.g.: 25% and 10%) through the Continia Delivery Network: <ul><li><span>*The record in table VAT Sub Total already exists. Identification fields and values: Header Table No.=<eDocument Header Table No.>Header Type=<eDocument  Header Type>,Document No.=<eDocument No.>,Document Line No.=<eDocument Line No..>,VAT Category Id=<VAT Category ID>*</span></ul></li> |58107|
| General Application |Prior to this fix, an error was thrown when trying to export an XRechnung document in a sandbox environment. |58023|

## Continia Delivery Network 24.01.06
*Released: July 30, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
|eDocuments|<span>When sending an eDocument where the type of the line was **G/L Account**, no unit of measure was used on the eDocument line. This caused the eDocument to not pass the validation. |58006|
| Country and Regional|For the New Zealand localization, the company identifier was taken from the field 11620 ABN and not from the field with number 90 GLN. |58005|
| eDocuments|The default value set on the XML structure entry was not used for the eDocument lines. |57399|
| eDocuments|When an incoming eDocument contained a field with a date older than or equal to 01-01-1753, the following error occurred: <ul><li><em>Cannot write the value 01-01-1753 to the field [Field Name] in the table [Table name] because the value is either too long or the content is invalid.</em></li></ul>In such cases, the date will not be processed. |58013|

## Continia Delivery Network 24.01.05
*Released: July 12, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| eDocuments|When exporting an XML document with an additional document attached, users might encounter the following error: <ul><li><em>The length of the string is &lt;length&gt;, but it must be less than or equal to 30 characters. Value: &lt;Field value&gt;</em></li></ul> |57634|
| eDocuments|<span>The validation rule for the identifier type 0208 BE:EN </span><span>has been updated. The new validation rule is: </span><code>[0-1]{1}[0-9]{9}</code><span>.</span><br> |57702|
| eDocuments|When selecting multiple documents to send through eDocuments, the following error occurred: <ul><li><em>Error Message: (</em>Contents of the first XML<em>)</em></li></ul> |57915|

## Continia Delivery Network 24.01.04
*Released: July 3, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| eDocuments|When importing an electronic document containing a mix of namespace declarations, an error occured when reading the content of the document causing the Bussiness Central client to crash. |57389|
| eDocuments|The value of the legal company ID was not trimmed according to the validation rules of the electronic document.&nbsp; |57396|
| eDocuments|When trying to send an electronic invoice that contained a comment line with a description longer than 50 characters, the following error occured: <ul><li><em>The length of the string is [lenght of Comment Line Description], but it must be less than or equal to 50 characters. Value: [Comment Line Description]</em></li></ul> |57397|

## Continia Delivery Network 24.01.03
*Released: June 26, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| eDocuments | Recognizing fields in an electronic document that contained document lines with InvoicedQuantity = 0 would produce the following error message: <ul><li><em>Attempted to divide by zero</em> </li> </ul> |57282|

## Continia Delivery Network 24.01.02
*Released: June 13, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|When exporting an invoice or a credit memo as an XRechnung document, XRechnung version 3.0 will be used. |54595|

## Continia Delivery Network 24.01.01
*Released: June 4, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|When onboarding a new company with the network identifier &quot;NL:KVK&quot; to the Continia Delivery Network, the following validation error occured: <ul><li><em>The Identifier Type ID of the participation is invalid (Rule: '[0-9]{17}').</em></li></ul> |56769|

## Continia Delivery Network 24.01
*Released: May 28, 2024*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Introducing a new field in Customer Setup &quot;<b>Use Document Information for CustomerParty</b>&quot;.<br> When exporting a document, you now have the option to retrieve the Customer party details directly from the document rather than Customer. | 56588 |


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| Country and Regional | When exporting electronic documents the VAT identifier of any party was taken from the VAT Registration No. field or any localized fields based on the localization of the Business Central. Now, this will be based on the country code of the party.&nbsp; | 53451 |
| General Application | When exporting a Sales Invoice as an XRechnung document, the XRechnung version 3.0 will be used.&nbsp; | 54595 |
| General Application | Several enhancements have been implemented for Peppol Payment Means functionality.&nbsp;&nbsp; <ul><li>PaymentID Availability: </li><ul><li>Previously restricted to KID and FIK. </li> </ul><li>PlusGiro will be set as payment method under the following conditions. </li><ul><li>Country/Region Code is 'SE' and &quot;Plus Giro No.&quot; has a value. </li> </ul><li>Bank Information Export is now based on the presence of Bank Account No. </li><ul><li>If Bank Account No. has a value. Bank Account and Bank Branch No. will be exported. </li><li>If Bank Account No. does not have a value. SWIFT/BIC and IBAN will be exported if present. </li> </ul> </ul> | 54780 |
| General Application | When opening the <b>Outgoing Network Documents</b>&nbsp;page, the following error could occur: <ul><li><em>The record in table Network Document already exists. Identification fields and values: System ID=<em><span><em>&lt;Field Value&gt;</em></span></em></em> </li> </ul> | 55683 |

## Continia Delivery Network 24.00.01
*Released: May 1, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | The network identifier fields on the Customer Setup page were disabled and no values were shown. | 54404 |

## Continia Delivery Network 24.00
*Released: April 2, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | When exporting an OIOUBL Service Invoice and Credit Memo the following error occurred for text lines:<br><ul><li><em>No. must have a value in Service Invoice Line: [Document No], [Line No.]. It cannot be zero or empty.</em> </li> </ul> | 53952 |

## Continia Delivery Network 6.02
*Released: March 7, 2024*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | Added support for onboarding companies, sending and receiving electronic documents throught the PEPPOL eDelivery Network via Continia Delivery Network for the following countries:&nbsp;<span>Netherlands, Australia, New Zeeland.&nbsp;</span> When the localization of the Business Central is set to Netherlands,&nbsp;<span>Australia</span><span>&nbsp;or&nbsp;</span><span>New Zeeland</span> all company information and documents will be stored in a separate datacenter according to the local regulations.&nbsp; | 53318 |

## Continia Delivery Network 6.01.03
*Released: February 12, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | A delivery codeunit for reminders has been created in order to support sending reminders through the Continia Delivery Network. | 53281 |

## Continia Delivery Network 6.01.02
*Released: February 1, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | <span>A&nbsp;rounding error could occur on XML node LineExtensionAmount w</span>hen exporting a document with <b>Prices Incl. VAT </b>set to true.&nbsp; | 52601 |
| General Application | When opening the <b>CDN Customer Setup Page</b>&nbsp;without a VAT Registration No.&nbsp;the following error occurred: <ul><li><span><em>The value of COPYSTR parameter 2 is outside of the permitted range. The current value is: -1. The permitted range is: from 1 to 2.147.483.647.</em></span> </li> </ul> | 52933 |

## Continia Delivery Network 6.01.01
*Released: January 20, 2024*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| General Application | When trying to send an reminder the following error occurred:<br><ul><li><span><em>There is no Network Profile in the filter.<br></em></span><em><br></em> <em>Filters: Network: nemhandel, ProcessIdentifier: Procurement-BilSim-1.0, DocumentIdentifier: urn:oasis:names:specification:ubl:schema:xsd:Reminder-2::Reminder##OIOUBL-2.02::2.0, CDN GUID: &lt;&gt;{00000000-0000-0000-0000-000000000000}</em> <em><span></span></em> </li> </ul> | 52403 |

## Continia Delivery Network 6.01
*Released: December 15, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- | --- |
| | The Action &quot;Open Source Document&quot; on <b>Outgoing Network Documents</b>&nbsp;now supports Service Invoices and Credit Memos. | 51678 |
| General Application                                       | When exporting an PEPPOL,OIOUBL or XRechnung electronic documents and the document line had the&nbsp;<b>Type</b>&nbsp;G/L Account, cbc:Description node will not be created. | 50216 |
| General Application                                       | <span>When exporting an OIOUBL Service Invoice/Credit Memo the following error occurred, when having the same extension fields with the same ID and different type:</span> <ul><li><span><em>The following fields must have the same type:&nbsp;<br></em></span><em>Field: &lt;Sales Line Field Name&gt; &lt;-- &lt;Service Invoice Line Field Name&gt;&nbsp;<br></em><em>Table: Sales Line &lt;-- Service Invoice Line&nbsp;<br></em><em>Type: &lt;Field Type&gt; &lt;-- &lt;Field Type&gt;.</em> </li> </ul> | 51462 |

## Continia Delivery Network 6.00, hotfix 2
*Released: November 20, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|When trying to create an Electronic Document, the following error could occur:&nbsp; <ul><li><em><span>There is no Output profile within the filter.</span><br><span>Filters: Profile Code: '', E-Document Setup Code: &lt;&gt;''</span></em> </li> </ul> |51206|

## Continia Delivery Network 6.00, hotfix 1
*Released: November 9, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|When exporting an OIOUBL document with a text line, a item line with standard VAT and a item line without VAT the following error occurred: <ul><li><span><em>Specifying the same TaxSubtotal.TaxCategory.ID in one TaxTotal class is not allowed</em></span> </li> </ul> |50849|
| General Application|In some cases, when sending an electronic document<span>, the following error could occur</span>:&nbsp; <ul><li><em>The Continia Delivery Network Subnetwork does not exist. Identification fields and values: Network Name=''</em> </li> </ul> |50892|
| General Application|When creating an XRechnung document in the Continia Demo Portal, the following error could occur:&nbsp; <ul><li><span><em>There is no Network Profile within the filter.</em></span> <em>Filters: Network Name: <em>&lt;Network&gt;</em>, Process Identifier: <em><em>&lt;Process Identifier&gt;</em></em>, Document Identifier: <em><em><em>&lt;<em>Document Identifier</em>&gt;</em></em></em></em>  </li> </ul> |50950|

## Continia Delivery Network 6.00
*Released: October 2, 2023*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|When exporting an OIOUBL document, the AccountCustomerParty/cac:Contact node will be populated with contact information from the following fields, listed in order of priority: <ol><li><em>Contact on Invoice.</em> </li><li><em>Customer Primary Contact.</em> </li><li><em>Salescode on Document.</em> </li><li><em>Customer Salescode.</em> </li> </ol> |46473|
| General Application|The codeunits exporting the XRechnung documents were using an extended version of the XRechnung version. Now the codeunits use the latest version of the simple XRechnung version 2.3.&nbsp; Furthermore, the code will automatically find and use the latest version of the XRechnung that best matches the document receiver and the Continia Delivery Network participation. Therefore we recommend adding all the different versions of the XRechnung format to the existing participation.&nbsp; In the cases where a match is not found, the following error will be thrown: <ul><li><em>&quot;The customer does not support receiving the version of the current profile (&lt;Profile description&gt;). For best results add all versions of the profile to your participation, the system will automatically use the latest version.&quot;</em> </li> </ul> |41716|
| General Application|When exporting an OIOUBL XML document the following error occurred if the bank account number exceeded 10 characters. <ul><li><span><em>PaymentMeansCode = 42, &nbsp;Account ID must be no more than 10 characters</em></span> </li> </ul> &nbsp;The PayeeFinancialAccount/cbc:ID node will only contain numbers and will not exceed 10 characters in length. |42808|
| General Application|Outgoing Network Documents cues has been added to the <b>Document Output Rolecenter. |42897|
| General Application|When the Continia Delivery Network Customer Setup record is being inserted, if the field&nbsp;<b>Use GLN in Electronic Document</b>&nbsp;from the standard Microsoft OIOUBL extension is set to true then&nbsp;<b>Receiver Type</b>&nbsp;is set to GLN and <b>Use GLN for Party and Legal Identification</b> is set to true. |43079|
| General Application|When exporting an OIOUBL document the maximum allowed decimals have been set to follow the schematron rules for OIOUBL. |46745|
| General Application|When selecting the<em> </em>ZugFerd <b>Outputprofile </b>on D<b>ocument Output Customer Setup List</b> the<b> Cross Industry Invoice Version</b> is set to <em>ZUGFeRD/Factur-X</em> |49139|
| General Application|Output profiles ZUGFeRD, OIOUBL, PEPPOL and XRECHNUNG are now prepared to support more document types, than the ones possible to send in the specific format. This means that the profile can generate the XML where possible, and send emails for the remaining template types. There should be no need for further configuration than adding the Output profile to the <b>Document Output Customer List.&nbsp;  |49140|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|<span>New field </span><b>Enabled</b><span>&nbsp;on Participation ID Type.&nbsp;</span><span>Network Profiles and Participation ID Types with&nbsp;</span><b>Enabled&nbsp;</b><span>= TRUE will now be hidden all across Continia Delivery Network.</span>  |31671|
| General Application|When exporting an OIOUBL XML Document <span>using IBAN as the PaymentMeans&nbsp;</span>the&nbsp;<span>FinancialInstitution node was not created.</span><span></span> |43162|
| General Application|All validation codeunits have been updated to follow the latest XML ruleset in order to reduce the risk of non-compliant XML documents. |43773|
| General Application|When sending more than 100 documents at a time, while opening the <b>Outgoing Network Documents </b>page, only the status of the first 100 documents was updated.&nbsp; |44530|
| General Application|When exporting an OIOUBL document, the following validation error occurred if a line had no&nbsp;<span>Unit of Measure Code</span>. <ul><li><em>Line '&lt;Line No.&gt;' with lineExtensionAmount (&lt;Line Amount&gt;) must equal (Price.PriceAmount (0) / Price.BaseQuantity (1) ) * Quantity (&lt;Quantity&gt;) +/- 1.00 (Quantity unitCode and Price.BaseQuantity unitCode are equal</em> </li> </ul> |46040|
| General Application|<span>In some cases, a document received from Continia Delivery Network was created twice, this was causing the document to always be present in the Documents for Import even though the document was already imported.&nbsp;<span>Additionally, when importing documents, only the first document imported would be marked as processed by Document Capture.&nbsp;</span></span> |46297|
| General Application|When running the Continia Delivery Network onboarding wizard, if the Country/Region Code exceeds 4 characters the following message will be displayed and the&nbsp;<span>Country/Region Code will copy the first 4 characters.</span> <ul><li><em>The value for &lt;Country/Region Code&gt; must be stated in the &lt;ISO code&gt; format with a maximum length of &lt;4&gt;.</em> </li> </ul> |46342|
| General Application|When registering for a participation for Nemhandel, without a mandatory profile, the following error was thrown. <ul><li><em>The &lt;Network Profile Description&gt; Network Profile is mandatory for the registration in the PEPPOL Network.</em><br> </li> </ul>This has been changed to&nbsp;  <ul><li><em>The <em>&lt;Network<em><span>&nbsp;</span>Profile</em>&nbsp;Description&gt;</em> Network Profile is mandatory for the registration in the NemHandel Network.</em> </li> </ul> |46746|
| General Application|<span></span> When activating <b>Use GLN from document</b> on the <b>CDN Customer Setup</b> page, the field <b>GLN</b> from the document is now used when exporting the invoice as the recipient of the document. This field is part of the standard Business Central OIOUBL extension app, and will only be used when the extension is installed.&nbsp; |47003|
| General Application|The export of an OIOUBL document was not taking into consideration the Profile ID specified <span>for the customer&nbsp;</span>in the field&nbsp;<b>OIOUBL Process ID</b>&nbsp;on the page&nbsp;<b>CDN Customer Setup. |47380|
| General Application|When exporting an XML Document a blank line was exported if line <b>Type</b> was comment, <b>Number</b>&nbsp;had a value but <b>Description</b> was blank. |47395|
| General Application|When exporting an OIOUBL document, the following error occurred if <b>Sell-to Contact Name</b>, exceeded 20 characters.<br><ul><li><em>The length of the string is &lt;string length&gt;, but it must be less than or equal to 20 characters. Value: &lt;Sell-to Contact No.&gt;</em> </li> </ul>|47630|
| General Application|When exporting an PEPPOL document, if the document was with <b>Prices Incl. VAT.&nbsp;</b>The <b>Line Discount Amount</b>&nbsp;was rounded which could result in the following validation error: <ul><li><em>Invoice line net amount MUST equal (Invoiced quantity * (Item net price/item price base quantity) + Sum of invoice line charge amount - sum of invoice line allowance amount</em> </li> </ul> |47966|
| General Application|When exporting PEPPOL or XRechnung electronic documents, where the <b><span>Bill-to</span>&nbsp;Customer</b> was different from the <span><b>Sell-to Customer</b>, the information in the <b>Accounting Customer Party</b> section was filled in with the <b>Sell-to Customer</b>, and a new <b>Payee Party</b> section was created for the <b>Bill-to Customer</b> information.&nbsp;</span> <span>This was against the PEPPOL and XRechnung rules, as the <b>Payee Party</b> section should contain information about the Payment Receiver.</span> <span><br></span> <span>A new field <b>Use Sell-to Customer</b> is created on the <b>CDN Customer Setup</b> page, which can be used to force the use of <b>Sell-to Customer</b> information in the <b>Accounting Customer Party</b>. The field is hidden by default.&nbsp;</span> |48078|
| General Application|When exporting an XML document, the following error occurred: <ul><li><em></em><em><span>There is no Output profile within the filter.&nbsp;</span></em><em>Filters: Profile Code: ''</em>  </li> </ul> |48127|
| General Application|<span>After creating a test system as a copy of the production system having Continia Delivery Network participations</span>, when pressing on any of the tiles or the <b>Import files</b> action on the <b>Document Capture rolle center</b>, <span>the following error occurred</span>: <ul><li><em><span lang=DA>The SSL connection could not be established, see|49530|

## Continia Delivery Network 5.02, hotfix 1
*Released: September 18, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional |When sending a PEPPOL document from or to a company with a SIRET number&nbsp;<span>defined</span>, this will now be used for the Party Identification node.&nbsp; |49463|
| General Application|<span>After creating a test system as a copy of the production system having Continia Delivery Network participations</span>, when pressing on any of the tiles or the <b>Import files</b> action on the <b>Document Capture rolle center</b>, <span>the following error occurred</span>: <ul><li><em><span lang=DA>The SSL connection could not be established, see|49530|

## Continia Delivery Network 5.02
*Released: August 28, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|When exporting an XML Document a blank line was exported if line <b>Type</b> was comment, <b>Number</b> had a value but <b>Description</b> was blank. |47395|
| General Application|When exporting an OIOUBL document, the following error occurred if <b>Sell-to Contact Name</b>, exceeded 20 characters.<br><ul><li><em>The length of the string is &lt;string length&gt;, but it must be less than or equal to 20 characters. Value: &lt;Sell-to Contact No.&gt;</em> </li> </ul>|47630|
| General Application|When exporting an PEPPOL document, if the document was with <b>Prices Incl. VAT.&nbsp;</b>The <b>Line Discount Amount</b>&nbsp;was rounded which could result in the following validation error: <ul><li><em>Invoice line net amount MUST equal (Invoiced quantity * (Item net price/item price base quantity) + Sum of invoice line charge amount - sum of invoice line allowance amount</em><br> </li> </ul> |47966|
| General Application | When exporting PEPPOL or XRechnung electronic documents, where the <b>Bill-to Customer</b> was different from the <b>Sell-to Customer</b>, the information in the <b>Accounting Customer Party</b> section was filled in with the <b>Sell-to Customer</b>, and a new <b>Payee Party</b> section was created for the <b>Bill-to Customer</b> information. This was against the PEPPOL and XRechnung rules, as the <b>Payee Party</b> section should contain information about the Payment Receiver. <br><br> A new field <b>Use Sell-to Customer</b> is created on the <b>CDN Customer Setup</b> page, which can be used to force the use of <b>Sell-to Customer</b> information in the <b>Accounting Customer Party</b>. The field is hidden by default. |48078|
| General Application|When exporting an XML document, the following error occurred: <ul><li><em></em><em><span>There is no Output profile within the filter.&nbsp;</span></em><em>Filters: Profile Code: ''</em>  </li> </ul> |48127|

## Continia Delivery Network 5.01.04
*Released: August 15, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application | During the export of electronic PEPPOL or XRechnung documents where <b>Bill-to Customer</b> was different from <b>Sell-to Customer</b>, the information in the <b>Accounting Customer Party</b> section was filled with the <b>Sell-to Customer</b> data, and a new <b>Payee Party</b> section was created for the <b>Bill-to Customer</b> information. This was against PEPPOL and XRechnung rules, as the <b>Payee Party</b> section should contain information about the payment receiver. |48843|

## Continia Delivery Network 5.01.03
*Released: July 17, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application | When an XML document was exported, the following error occurred: <ul><li><em>There is no Output profile within the filter. Filters: Profile Code: ''</em></li></ul> |48127|

## Continia Delivery Network 5.01.02
*Released: June 29, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application | When a PEPPOL document was exported, if the document was with <b>Prices Incl. VAT</b>, the <b>Line Discount Amount</b> was rounded, which could result in the following validation error: <ul><li><em>Invoice line net amount MUST equal (Invoiced quantity \* (Item net price/item price base quantity) + Sum of invoice line charge amount - sum of invoice line allowance amount.</em></li></ul> |47966|

## Continia Delivery Network 5.01.01
*Released: June 9, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|When exporting an OIOUBL document, the following error occurred if <b>Sell-to Contact Name</b> exceeded 20 characters.<br><ul><li><em>The length of the string is &lt;string length&gt;, but it must be less than or equal to 20 characters. Value: &lt;Sell-to Contact No.&gt;</em> </li> </ul>|47630|


## Continia Delivery Network 5.01
*Released: June 2, 2023*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|When exporting an OIOUBL document, the AccountCustomerParty/cac:Contact node will be populated with contact information from the following fields, listed in order of priority: <ol><li><em>Contact on Invoice.</em> </li><li><em>Customer Primary Contact.</em> </li><li><em>Salescode on Document.</em> </li><li><em>Customer Salescode.</em> </li> </ol> |46473|
| General Application|When exporting an OIOUBL XML document the following error occurred if the bank account number exceeded 10 characters. <ul><li><span><em>PaymentMeansCode = 42, &nbsp;Account ID must be no more than 10 characters</em></span> </li> </ul> &nbsp;The PayeeFinancialAccount/cbc:ID node will only contain numbers and will not exceed 10 characters in length. |42808|
| General Application|When the Continia Delivery Network Customer Setup record is being inserted, if the field&nbsp;<b>Use GLN in Electronic Document</b>&nbsp;from the standard Microsoft OIOUBL extension is set to true then&nbsp;<b>Receiver Type</b>&nbsp;is set to GLN and <b>Use GLN for Party and Legal Identification</b> is set to true. |43079|
| General Application|When exporting an OIOUBL document the maximum allowed decimals have been set to follow the schematron rules for OIOUBL. |46745|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|When exporting an OIOUBL XML Document using IBAN as the PaymentMeans the FinancialInstitution node was not created. |43162|
| General Application|All validation codeunits have been updated to follow the latest XML ruleset in order to reduce the risk of non-compliant XML documents. |43773|
| General Application|When sending more than 100 documents at a time, while opening the <b>Outgoing Network Documents </b>page, only the status of the first 100 documents was updated.&nbsp; |44530|
| General Application|When exporting an OIOUBL document, the following validation error occurred if a line had no Unit of Measure Code. <ul><li><em>Line '&lt;Line No.&gt;' with lineExtensionAmount (&lt;Line Amount&gt;) must equal (Price.PriceAmount (0) / Price.BaseQuantity (1) ) * Quantity (&lt;Quantity&gt;) +/- 1.00 (Quantity unitCode and Price.BaseQuantity unitCode are equal</em> </li> </ul> |46040|
| General Application|<span>In some cases, a document received from Continia Delivery Network was created twice, this was causing the document to always be present in the Documents for Import even though the document was already imported.&nbsp;<span>Additionally, when importing documents, only the first document imported would be marked as processed by Document Capture.&nbsp;</span></span> |46297|
| General Application|When running the Continia Delivery Network onboarding wizard, if the Country/Region Code exceeds 4 characters the following message will be displayed and the Country/Region Code will copy the first 4 characters. <ul><li><em>The value for &lt;Country/Region Code&gt; must be stated in the &lt;ISO code&gt; format with a maximum length of &lt;4&gt;.</em> </li> </ul> |46342|
| General Application|When registering for a participation for Nemhandel, without a mandatory profile, the following error was thrown. <ul><li><em>The &lt;Network Profile Description&gt; Network Profile is mandatory for the registration in the PEPPOL Network.</em></li> </ul>This has been changed to <ul><li><em>The &lt;Network Profile Description&gt; Network Profile is mandatory for the registration in the NemHandel Network.</em></li></ul> |46746|
| General Application|<span></span> When activating <b>Use GLN from document</b> on the <b>CDN Customer Setup</b> page, the field <b>GLN</b> from the document is now used when exporting the invoice as the recipient of the document. This field is part of the standard Business Central OIOUBL extension app, and will only be used when the extension is installed.&nbsp; <br>|47003|
| General Application|The export of an OIOUBL document was not taking into consideration the Profile ID specified <span>for the customer&nbsp;</span>in the field&nbsp;<b>OIOUBL Process ID</b>&nbsp;on the page&nbsp;<b>CDN Customer Setup.</b> |47380|

## Continia Delivery Network 5.00.01
*Released: May 22, 2023*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application | The export of an OIOUBL document was not taking into consideration the profile ID specified for the customer in the field **OIOUBL Process ID** on the page **CDN Customer Setup**. | 47380 |

## Continia Delivery Network 5.00
*Released: April 1, 2023*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|On the Network Documents list, a new action, <span>Mark as Processed,</span>&nbsp;has been added. When running the function, the network document will be set to unprocessed and can be imported again into the document journal. |28156|
| General Application|For OIOUBL Documents export codeunits have been added for Service Invoice and Service Credit Memos. |32878|
| General Application|Added support for exporting of ZUGFeRD Electronic documents.&nbsp; |32888|
| General Application| In the &quot;CDN Customer Setup Card&quot; a new boolean field &quot;PEPPOL use GLN for Party and Legal identification&quot; has been added. Enabling this field will prioritize using GLN instead of VAT Registration No. for Customer Party Identification and Customer Party Legal Identification nodes. |34627|
| General Application|When exporting an OIOUBL document. Payment Means Due Date will now be populated with the due date from the invoice. |40202|
| General Application|When exporting an OIOUBL document, the profile will change depending on how the receiver is registered.&nbsp; If the receiver is registered with the profiles Procurement-BilSim and NES5, the <span>Procurement-</span>BilSim profile will be chosen. If the receiver is only registered with the NES5 profile, this profile will be chosen. |42453|
| General Application|New field on CDN Customer Setup &lt;<em>Use GLN from document</em>&gt;.&nbsp; This makes it possible for Danish localizations to use &lt;<em>EAN</em>&gt; on the document as receiver endpoint ID. |42724|
| General Application| Events have been added to the solution. For details, please see [Event Publishers for Continia Delivery Network 5.00](@DO-80) |42861|
| General Application|Improved user experience of the CDN Customer Setup Page.&nbsp; <ul><li>Added groups for the different formats OIOUBL, PEPPOL and CII. </li><li>All fields that are specific to an XML format have been moved to the relevant group.&nbsp; </li> </ul> |43201|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
||When exporting a PEPPOL document the Belgian enterprise number was not stated in the correct format.&nbsp; |38857|
| General Application|When setting up the participation for an E-Document Setup, you can now only select participations with a minimum of a Network Profile with the Direction Outbound or Both.&nbsp; <br> <br> |31529|
| General Application|When onboarding a participation, it's now possible to register in the PEPPOL network and the NemHandel network at the same time. |39996|
| General Application|<span>The following Event Publisher in Codeunit&nbsp;6086271&nbsp;CTS-CDN OIOUBL Export Inv.&nbsp;has been marked as obsolete as the XmlDoc parameter is not a VAR parameter:</span><ul><li><span>OnBeforeCreateHeaderNotes</span> </li> </ul><span>This will be replaced by the following Event Publisher:</span><ul><li><span>OnBeforeSetHeaderNotes</span> </li> </ul><br> |40920|
| General Application|<span>Continia Delivery Network now supports the new &quot;Item Reference&quot; table introduced as a feature in Business Central 2020 Release Wave 2.</span><br> |41710|
| General Application|It was posible to create an oboarding with a network profile having the Profile Direction as Both, even though Document Capture was not installed. Now the following error is thrown:&nbsp; <ul><li><em>You do not have access to Document Capture. Profile direction cannot be Inbound or Both.</em><br> </li> </ul> |41889|
| General Application|<span>When exporting an OIOUBL document, the validation of the document failed because two or more Tax Categories with the same VAT percentage were present.&nbsp;</span> <br> |41922|
| General Application|<span>When exporting an OIOUBL document, the validation of the document was failing because the&nbsp;</span><span>InstructionID node was&nbsp;</span><span>exported without a value.</span> <br> |42018|
| General Application|When exporting an XML document text lines with spaces in the description will be skipped. |42632|
| General Application|When trying to create an OIOUBL Electronic document in a Sandbox environment, the following error occurred: <br> <ul><li><em><span>There is no Network Profile within the filter.</span><br></em> <em><br></em> <em>Filters: Network Name: nemhandel, Process Identifier: Procurement-BilSim-1.0, Document Identifier: urn:oasis:names:specification:ubl:schema:xsd:Invoice-2::Invoice##OIOUBL-2.02::2.0</em>  </li> </ul> |42809|
| General Application|The Output Profiles for reminders were not created when running the&nbsp;Document Output Setup Wizard. |43480|
| General Application|<span>When exporting an OIOUBL Document where the &lt;Qty. per Unit of Measure&gt; on the line had a value between 0 and 1, for example, 0.2, the PriceAmount node was not calculated correctly.</span> |43496|
| General Application|In the CDN Customer Setup page, the Sender ID and in the E-Document Setup page, the Receiver ID value will now be filled with information from localized fields, for example, Enterprise No. for Belgium. |43768|
| General Application|When exporting an OIOUBL Credit Memo and using the following event&nbsp;OnBeforeSkipDocumentLine, the FromCodeunit parameter had the wrong value&nbsp;6086240&nbsp;(&quot;<span>CTS-CDN PEPPOL BIS3 Inv.&quot;).</span> This has been corrected to&nbsp;6086272&nbsp;(&quot;CTS-CDN OIOUBL Export Cr.&quot;). |44664|
| General Application|For Sender and Receiver with Swedish the country-specific prefix 'SE' and the suffix '01' are now removed when exporting a PEPPOL document.&nbsp; |45514|
| General Application|When exporting an OIOUBL document, the node&nbsp;<span>DocumentTypeCode was not added inside the&nbsp;<span>AdditionalDocumentReference element.</span></span> |45752|
| General Application|When exporting a PEPPOL, XRechung or OIOUBL document, item line nodes will be populated with Item Attributes, if the item contains any Item Attributes. The following nodes will be created <ul><li>AdditionalItemProperty/cbc:Name will include <em>Item Attribute [Name]</em>.<br> </li><li>AdditionalItemProperty/cbc:Value will include <em>Item Attribute [Value]</em>.<br> </li> </ul> |45862|
| General Application|ZUGFERD Output profiles were created with the value &quot;PDF and XML (e-doc)&quot; in the field E-mail, this has been corrected to the value &quot;PDF&quot;. |45867|
| General Application|When exporting an OIOUBL Document the order in which the data in the&nbsp;<span>Contact section under<span>&nbsp;</span></span>AccountingCustomerParty is being exported has been changed to the following priority: <span><ol><li><em>Customer Primary Contact</em> </li><li><em>Customer Contact</em> </li><li><em>Customer Salesperson Code</em> </li><li><em>Salesperson on Document</em> </li> </ol></span> |45875|

## Continia Delivery Network 4.03
*Released: March 27, 2023*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|<span>Events have been added to the solution. For details, please see [Event Publishers for Continia Delivery Network 2022 R2 (4.00)](@DO-38) |43354|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|In the CDN Customer Setup page, the Sender ID and in the E-Document Setup page, the Receiver ID value will now be filled with information from localized fields, for example, Enterprise No. for Belgium. |43768|
| General Application|When exporting an OIOUBL Credit Memo and using the following event&nbsp;OnBeforeSkipDocumentLine, the FromCodeunit parameter had the wrong value&nbsp;6086240&nbsp;(&quot;<span>CTS-CDN PEPPOL BIS3 Inv.&quot;).</span> This has been corrected to&nbsp;6086272&nbsp;(&quot;CTS-CDN OIOUBL Export Cr.&quot;). |44664|

## Continia Delivery Network 4.02
*Released: January 2, 2023*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|Added support for exporting of ZUGFeRD Electronic documents.&nbsp; |32888|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|The Output Profile for reminders was not created when running the&nbsp;Document Output Setup Wizard. |43480|
| General Application|<span>When exporting an OIOUBL Document where the &lt;Qty. per Unit of Measure&gt; on the line had a value between 0 and 1, for example, 0.2, the PriceAmount node was not calculated correctly.</span> |43496|

## Continia Delivery Network 4.01
*Released: December 12, 2022*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|On the Network Documents list, a new action, <span>Mark as Processed,</span>&nbsp;has been added. When running the function, the network document will be set to unprocessed and can be imported again into the document journal. |28156|
| General Application|<font color="#171717" face="Segoe UI, SegoeUI, Segoe WP, Helvetica Neue, Helvetica, Tahoma, Arial, sans-serif">In the &quot;CDN Customer Setup Card&quot; a new boolean field &quot;PEPPOL use GLN for Party and Legal identification&quot; has been added. Enabling this field will prioritize using GLN instead of VAT Registration No. for Customer Party Identification and Customer Party Legal Identification nodes.</font> |34627|
| General Application|When exporting an OIOUBL document. Payment Means Due Date will now be populated with the due date from the invoice. |40202|
| General Application|When exporting an OIOUBL document, the profile will change depending on how the receiver is registered.&nbsp; If the receiver is registered with the profiles Procurement-BilSim and NES5, the <span>Procurement-</span>BilSim profile will be chosen. If the receiver is only registered with the NES5 profile, this profile will be chosen. |42453|
| General Application|<span>Events have been added to the solution. For details, please see [Event Publishers for Continia Delivery Network 2022 R2 (4.00)](@DO-38) |42861|


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
||When exporting a PEPPOL document the Belgian enterprise number was not stated in the correct format.&nbsp; |38857|
| General Application|When setting up the participation for an E-Document Setup, you can now only select participations with a minimum of a Network Profile with the Direction Outbound or Both.&nbsp; <br> <br> |31529|
| General Application|When onboarding a participation, it's now possible to register in the PEPPOL network and the NemHandel network at the same time. |39996|
| General Application|<span>The following Event Publisher in Codeunit&nbsp;6086271&nbsp;CTS-CDN OIOUBL Export Inv.&nbsp;has been marked as obsolete as the XmlDoc parameter is not a VAR parameter:</span><ul><li><span>OnBeforeCreateHeaderNotes</span> </li> </ul><span>This will be replaced by the following Event Publisher:</span><ul><li><span>OnBeforeSetHeaderNotes</span> </li> </ul><br> |40920|
| General Application|<span>Continia Delivery Network now supports the new &quot;Item Reference&quot; table introduced as a feature in Business Central 2020 Release Wave 2.</span><br> |41710|
| General Application|Automatic generation of output profiles, for OIOUBL, were wrongly generated with the description &quot;PEPPOL&quot;. This description has been changed to OIOUBL. |41834|
| General Application|It was posible to create an oboarding with a network profile having the Profile Direction as Both, even though Document Capture was not installed. Now the following error is thrown:&nbsp; <ul><li><em>You do not have access to Document Capture. Profile direction cannot be Inbound or Both.</em><br> </li> </ul> |41889|
| General Application|<span>When exporting an OIOUBL document, the validation of the document failed because two or more Tax Categories with the same VAT percentage were present.&nbsp;</span> <br> |41922|
| General Application|<span>When exporting an OIOUBL document, the validation of the document was failing because the&nbsp;</span><span>InstructionID node was&nbsp;</span><span>exported without a value.</span> <br> |42018|
| General Application|When exporting an XML document text lines with spaces in the description will be skipped. |42632|
| General Application|When trying to create an OIOUBL Electronic document in a Sandbox environment, the following error occurred: <br> <ul><li><em><span>There is no Network Profile within the filter.</span><br></em> <em><br></em> <em>Filters: Network Name: nemhandel, Process Identifier: Procurement-BilSim-1.0, Document Identifier: urn:oasis:names:specification:ubl:schema:xsd:Invoice-2::Invoice##OIOUBL-2.02::2.0</em>  </li> </ul> |42809|

## Continia Delivery Network 4.00
*Released: October 1, 2022*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| General Application                                       | Support added for exporting documents in the A-NZ PEPPOL BIS 3 format.&nbsp; | 31752 |
| General Application                                       | <span>New events have been added to the solution. Find them in the article [Event Publishers for Continia Delivery Network 2022 R2 (4.00)](@DO-38). | 32149 |
| General Application                                       | It is now possible to export OIOUBL reminders.               | 32880 |
| General Application                                       | <span>Support added for exporting documents in the </span><span>Netherlands&nbsp;</span><span>PEPPOL BIS 3 format.&nbsp;</span><br> | 32884 |
| General Application                                       | <span>When sending an OIOUBL document via NemHandel network, the validation of the document failed because ContactID is mandatory for OIOUBL documents.</span>&nbsp;The code now populates the ContactID with the Salesperson Code from the Invoice/Credit Memo.&nbsp; | 34768 |
| General Application                                       | When sending an OIOUBL document to a receiver with a GLN identifier, the document was failing the validation with the following error messages:&nbsp; <em><br></em> <em>&quot;<span>[F-LIB196] schemeID = DK:SE, CompanyID must be a valid SE number (like 'DK12345678', value found: '1234567890123')</span>&quot;</em> <em><br></em> <em><span>&quot;[F-LIB190] schemeID = DK:CVR, CompanyID must be a valid CVR number (like 'DK12345678', value found: '<em><span>1234567890123</span></em>')&quot;</span><br></em> | 34770 |
| General Application                                       | The following events have been removed from the solution: <br> Codeunit&nbsp;6086240&nbsp;CTS-CDN PEPPOL BIS3 Inv. <ul><li>OnBeforeSetBuyerReference </li><li>OnBeforePaymentMeans </li> </ul>Codeunit&nbsp;6086241&nbsp;CTS-CDN PEPPOL BIS3 Cr.M.  <ul><li>OnBeforeSetBuyerReference </li><li>OnBeforePaymentMeans </li> </ul> <span>Codeunit&nbsp;</span><span>6086242&nbsp;CTS-CDN PEPPOL BIS3 Sv. Inv.</span><br> <span><ul><li>OnBeforeSetBuyerReference </li><li>OnBeforePaymentMeans </li> </ul></span> <span><span>Codeunit&nbsp;</span><span>6086243&nbsp;</span><span><span>CTS-CDN XRechnung 2 Inv.</span></span><br></span> <span><span><span><ul><li>OnBeforeSetBuyerReference </li><li>OnBeforePaymentMeans </li> </ul></span></span></span> <span><span><span>Codeunit&nbsp;</span><span>6086244&nbsp;CTS-CDN XRechnung 2 Cr.Memo</span><br></span></span> <span><span><span><ul><li>OnBeforeSetBuyerReference </li><li>OnBeforePaymentMeans </li> </ul></span></span></span> <span><span><span><span>Codeunit&nbsp;</span><span>6086245&nbsp;<span>CTS-CDN XRechnung 2 Sv. Inv.</span></span><br></span></span></span> <span><span><span><span><span><ul><li>OnBeforeSetBuyerReference </li><li>OnBeforePaymentMeans </li> </ul></span></span></span></span></span> <span><span><span><span><span>Codeunit&nbsp;</span><span>6086246&nbsp;</span><span><span>CTS-CDN XRechnung 2 Sv.Cr.Memo</span></span><br></span></span></span></span> <span><span><span><span><span><span><ul><li>OnBeforeSetBuyerReference </li><li>OnBeforePaymentMeans </li> </ul></span></span></span></span></span></span> <span><span><span><span><span><span>Codeunit&nbsp;</span><span>6086247&nbsp;</span><span>CTS-CDN PEPPOL BIS3 Sv. Cr.M.</span><br></span></span></span></span></span> <span><span><span><span><span><span><ul><li>OnBeforeSetBuyerReference </li><li>OnBeforePaymentMeans </li> </ul></span></span></span></span></span></span> <span><span>Codeunit&nbsp;</span><span>6086271&nbsp;</span><span>CTS-CDN OIOUBL Export Inv.</span><br></span> <ul><li><span><span>OnBeforePaymentMeans<br></span></span> </li> </ul> <span><span><span>Codeunit&nbsp;</span><span>6086272&nbsp;</span><span>CTS-CDN OIOUBL Export Cr.</span><br></span></span> <ul><li><span><span><span>OnBeforePaymentMeans</span></span></span> </li> </ul> | 41228 |


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
|                                                           | For PEPPOL Service Invoice and Service Credit Memo cbc:BuyerReference is now populated in the following order: <ol><li>&lt;Your Reference&gt; </li><li>&lt;No.&gt; </li> </ol> | 32052 |
|                                                           | When exporting an OIOUBL Credit Memo the text lines had 0 in CreditedQuantity. | 34368 |
| General Application                                       | For PEPPOL documents, when Bill-To Customer is different from Sell-To Customer the PayeeParty Node will now be added. | 31062 |
| General Application                                       | When exporting an OIOUBL document having a line with 0 in quantity the following error occurred:&nbsp; <ul><li><span><em>Attempted to divide by zero.</em></span> </li> </ul>  <br> | 31359 |
| General Application                                       | <span>Added a new action to Incoming Document List page - &quot;</span><span>Set Document to Processed&quot;</span><span>. This action allows the user to mark a document as Processed, preventing the document to be imported again.&nbsp;&nbsp;</span> | 31511 |
| General Application                                       | <span>It is now possible to further customise the export of electronic documents by pressing the Additional setup action from the Continia Delivery Network subpart in the Document Output Customer Setup page.</span> <span>On this page you can choose a custom ProfileID to be used when sending the document in the Continia Delivery Network (for example NES5 for OIOUBL).</span> <span><br></span> | 31854 |
| General Application                                       | When exporting a PEPPOL document from a Swedish sender company, the value at the XML path &quot;Invoice/AccountingSupplierParty/PartyTaxScheme/CompanyID&quot; was not formatted according to the PEPPOL validation rules.&nbsp;&nbsp; | 31855 |
| General Application                                       | <span>When exporting PEPPOL or XRechnung, documents following only the following type of lines are not exported:</span><br> <ul><li>Empty lines: Line No. = &quot;&quot; , Description = &quot;&quot;<br> </li><li>Sub Invoice Lines: Type &lt;&gt; &quot;&quot;, Quantity = 0 </li> </ul> | 31871 |
| General Application                                       | When sending a PEPPOL or XRechnung Service Invoice or Credit Memo the following transferfields error occured: <ul><li><em>The following fields must have the same type:<br></em><em><br>Field: [FieldName] &lt;-- [FiledName]<br></em><em>Table: [TableName] &lt;-- [TableName]<br></em><em>Type: [FieldType] &lt;-- [FieldType]</em> </li> </ul>  <ul> </ul>  <br> | 31919 |
| General Application                                       | When exporting OIOUBL documents the Delivery nodes DeliveryActualDeliveryDate and DeliveryActualDeliveryTime are renamed: From <ul><li>DeliveryActualDeliveryDate </li><li>DeliveryActualDeliveryTime </li> </ul>To <ul><li>ActualDeliveryDate <br> </li><li>ActualDeliveryTime<br> </li> </ul> | 32876 |
| General Application                                       | When exporting OIOUBL documents the following error occurred: <ul><li><em>The Salesperson/Purchaser does not exist. Identification fields and values: Code=&lt;<font color="#171717" face="Segoe UI, SegoeUI, Segoe WP, Helvetica Neue, Helvetica, Tahoma, Arial, sans-serif">Salesperson/Purchaser Code&gt;</font></em> </li> </ul> | 34743 |
| General Application                                       | <span>When exporting PEPPOL or XRechnung documents, Delivery node will not be exported if the required values are not present.&nbsp;</span><br> | 34809 |
| General Application                                       | When exporting an OIOUBL Document, the EndpointID for VAT No. did not contain the prefix DK.&nbsp; | 38466 |
| General Application                                       | When exporting OIOUBL or PEPPOL documents, empty lines with a space in description will be skipped when exporting. | 39644 |
| General Application                                       | When exporting OIOUBL documents, it's now possible to use the&nbsp;OnSetPaymentMeans Event Publisher to specify the FIK payment details. | 39680 |
| General Application                                       | <span>When exporting OIOUBL &amp; PEPPOL documents the following error occurred in some situations:</span><ul><li><em>The length of the string is &lt;string lenght&gt;, but cannot exceed 50 characters. Value: &lt;<span>string</span>&gt;</em> </li> </ul><br> | 40565 |
| General Application                                       | <span>When exporting an PEPPOL document where either the customer or supplier was Belgian the following validation error occured:</span><br> <ul><li><em>Belgian enterprise number MUST be stated in the correct format.</em> </li> </ul> | 41371 |
| General Application                                       | When exporting OIOUBL documents, the validation for PartyIdentification was failing, when customers VAT number did not have a value. | 41543 |

## Continia Delivery Network 3.01
*Released: April 1, 2022*  

### New or changed features

</br>

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| General Application                                       | <span>Events have been added to the solution. For details, refer to [Event Publishers for Continia Delivery Network 2022 R1 (3.00)](@DO-15) on Continia Docs. | 32149 |

</br>

### Bug fixes

</br>

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
|                                                           | For PEPPOL Service Invoice and Service Credit Memo cbc:BuyerReference is now populated in the following order <ol><li>&lt;Your Reference&gt; </li><li>&lt;No.&gt; </li> </ol> | 32052 |
| General Application                                       | When exporting an OIOUBL document with a line with 0 in quantity the following error occurred:&nbsp; <ul><li><span><em>Attempted to divide by zero.</em></span> </li> </ul> | 31359 |
| General Application                                       | <span>Added a new action to Incoming Document List page - &quot;</span><span>Set Document to Processed&quot;</span><span>. This actions allows the user to mark a document as Processed, preventing the document to be imported again.&nbsp;&nbsp;</span> | 31511 |
| General Application                                       | When exporting a PEPPOL document from a Swedish sender company, the value at the XML path &quot;Invoice/AccountingSupplierParty/PartyTaxScheme/CompanyID&quot; was not formatted according to the PEPPOL validation rules.&nbsp;&nbsp; | 31855 |
| General Application                                       | <span>When exporting PEPPOL or XRechnung, documents following only the following type of lines are not exported:</span><br> <ul><li>Empty lines: Line No. = &quot;&quot; , Description = &quot;&quot;<br> </li><li>Sub Invoice Lines: Type &lt;&gt; &quot;&quot;, Quantity = 0 </li> </ul> | 31871 |
| General Application                                       | When sending a PEPPOL or XRechnung Service Invoice or Credit Memo the following transferfields error occured. <ul><li><em>The following fields must have the same type:<br></em><em><br>Field: [FieldName] &lt;-- [FiledName]<br></em><em>Table: [TableName] &lt;-- [TableName]<br></em><em>Type: [FieldType] &lt;-- [FieldType]</em> </li> </ul>  <ul> </ul> | 31919 |
| General Application                                       | When opening the Customer Setup page, if the E-Document Setup Code was not the same as Output Profile Code, t<span>he following error occurred</span>:&nbsp; <ul><li><em>Customer Setup: There is no E-Document Setup within the filter.<br><em>Filters: Code: &lt;Output Profile Code&gt;</em></em> </li> </ul> | 31995 |

## Continia Delivery Network 2.03
*Released: February 4, 2022*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description                                                  | ID    |
| --------------------------------------------------------- | ------------------------------------------------------------ | ----- |
| General Application                                       | <span>When sending a PEPPOL document with positive quantity and negative line amount, or the opposite, the validation was failing.&nbsp;</span> | 30191 |
| General Application                                       | <span>When sending a PEPPOL document with 0 quantity, the validation was failing.&nbsp;</span><br> | 30390 |
| General Application                                       | <span>When sending a PEPPOL document with an item which contained an GTIN number the validation was failing.&nbsp;</span> | 30501 |
| General Application                                       | Added support for exporting OIOUBL electronic documents.&nbsp; | 30562 |
| General Application                                       | <span>When sending a PEPPOL document with a VAT Posting Group or Bus. Posting Group longer than 10 characters, the following error occurred:</span><span><br> <ul><li><em>The length of the string is &lt;Actual Length&gt;, but it must be less than or equal to &lt;Max Length&gt; characters. Value: &lt;VAT Posting Group Code&gt;</em> </li> </ul> </span> | 30762 |
| General Application                                       | When sending a PEPPOL Invoice where the total&nbsp;<span>invoice</span><span>&nbsp;</span><span>amount is 0, the validation of the PEPPOL document was failing because the PayableAmount element was not created.</span> | 30953 |
| Platform and Technology                                   | <span>Events have been added to the solution. For details, please see [Event Publishers for Continia Delivery Network 2021 R2 (2.00)](@DO-13) | 30840 |


## Continia Delivery Network 2.02
*Released: November 30, 2021*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|Empty lines (Lines with no Type, Description nor Quantity) are now skipped by default when exporting a PEPPOL or XRechnung electronic document.&nbsp; The following event&nbsp;OnBeforeSkipDocumentLine in Codeunit 6086234 &quot;CTS-CDN Export Mgt.&quot; was introduced so that this logic can be further customised. |26208|
| General Application|When trying to onboard a participation in Continia Delivery Network only for sending PEPPOL or XRechnung documents, the Onboarding wizard will indicate that the participation already exists in the PEPPOL network, even though is it only required to be registered in the PEPPOL network when receiving documents.&nbsp;&nbsp; |28581|
| General Application|Improved the pages Network Documents and Outgoing Network Documents.&nbsp; <ul> </ul> <br> |28833|
| General Application|External Document No. and Order No. will now be set inside OrderReference on all PEPPOL exports. <br> Event publisher created with handle pattern for all PEPPOL export codeunits. <ul><li>OnBeforeSetOrderReference</li> </ul> |29470|
| General Application|When finding the customer or company identifier based on the localization of the Continia Delivery Network, the system was not taking in consideration the country of the customer or company. |29548|
| General Application|When running the Document Output wizard, the following error was thrown:<ul><li><em>&quot;<span>The field Template of table Output profile contains a value (SALESINVOICE) that cannot be found in the related table (E-Mail Template Header).</span>&quot;</em></li></ul> |29579|
| General Application|Removed check on Ship-To information on Credit Memos and Return Orders for XRechnung Exports. |29620|
| General Application|The validation of XRechnung documents failed because of a missing Line Feed at the end of the Payment Terms description. |29702|
| General Application|The amount in the path&nbsp;Invoice/InvoiceLine/Price/PriceAmount was rounded. This is not a requirement for PEPPOL documents.&nbsp; |29729|
| Platform and Technology|Obsolete Publisher Function for all CDN Exports. <ul><li><span>OnBeforeSetBuyerReference</span></li></ul> New Publisher Function for all CDN Exports. <ul><li>OnBeforeCreateBuyerReference</li></ul> |29508|

## Continia Delivery Network 2.01
*Released: October 4, 2021*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology|The following events are added to the solution:<br><span><br>OnBeforeValidate</span>&nbsp;<ul><li>Codeunit&nbsp;6086251 CTS-CDN PEPPOL Chk. Sales Inv.</li><li>Codeunit 6086252&nbsp;CTS-CDN PEPPOL Chk. Sales Cr.M</li><li>Codeunit 6086254&nbsp;CTS-CDN XRech2 Chk. Sales Inv</li><li>Codeunit 6086255&nbsp;CTS-CDN XRech2 Chk. Sales Cr.M</li><li>Codeunit 6086259&nbsp;CTS-CDN XRech2 Chk. Sv. Inv.</li><li>Codeunit 6086260&nbsp;CTS-CDN XRech2 Chk. Sv. Cr.M</li><li>Codeunit 6086260&nbsp;CTS-CDN XRech2 Chk. Sv. Cr.M</li><li>Codeunit 6086267&nbsp;CTS-CDN PEPPOL Chk. Serv. Inv.</li><li>Codeunit 6086268&nbsp;CTS-CDN PEPPOL Chk. Serv. Cr.M</li></ul>OnAfterValidate<ul><li>Codeunit&nbsp;6086251&nbsp;CTS-CDN PEPPOL Chk. Sales Inv.</li><li>Codeunit 6086252&nbsp;CTS-CDN PEPPOL Chk. Sales Cr.M</li><li>Codeunit 6086267&nbsp;CTS-CDN PEPPOL Chk. Serv. Inv.</li><li>Codeunit 6086268&nbsp;CTS-CDN PEPPOL Chk. Serv. Cr.M</li></ul>|24692|
| Platform and Technology|<span>The following event is added to the solution:<br><br>OnAfterGetReceiverInfo<ul><li>Codeunit 6086234 CTS-CDN Export Mgt.</li></ul>This event can be used to change the Receiver ID type and value.&nbsp;</span>|27940|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application|In some cases when sending an electronic document via Continia Delivery Network the following error was thrown:&nbsp;<ul><li><em>&quot;<span>Unable to convert from Microsoft.Dynamics.Nav.Runtime.NavXmlNode to Microsoft.Dynamics.Nav.Runtime.NavXmlElement.</span>&quot;</em></li></ul>|27171|
| General Application|When running the system first with DEMO credentials, 4 temporary Network Profiles are created.&nbsp;After changing to Production Credentials, when sending an electronic document the following error was thrown:&nbsp;<br><ul><li><em>&quot;You are trying to send a network document to customer &lt;Customer No.&gt;, but you have not registered for this type of documents.<br></em><em>Your participation: &lt;Participation Display Name&gt;<br></em><em>Profile: &lt;Network Profile&gt;&quot;</em></li></ul>|27436|
| General Application|When not choosing to create the Output Profiles for Service documents in the Document Output Setup Wizard, the following error was thrown&nbsp;<ul><li><span><em>&quot;The field Template of table Output profile contains a value (SERVINVOICE) that cannot be found in the related table (E-Mail Template Header).&quot;</em></span></li></ul>|27727|
| General Application|When sending an electronic document where the Receiver Identifier was empty on the Customer Setup, the following was thrown:&nbsp;<ul><li><em>&quot;The Continia Delivery Network API returned the following system error: Error Code <span>gateway_error - Unhandled error (SupportId: <span>00000000-0000-0000-0000-000000000000</span>)</span>&quot;</em></li></ul>|27808|
| General Application|<span></span>When choosing the VAT option in Receiver Type on Customer Setup page, the Receiver ID Type was empty.<br>When choosing the VAT option in Sender Type on E-Document Setup page, the Sender ID Type was empty. &nbsp;<br><span></span>|27822|
| General Application|When creating a PEPPOL document from a sales document without a Salesperson on, the following error occurred:&nbsp;<ul><li><em>&quot;The Salesperson/Purchaser does not exist. Identification fields and values: Code=''&quot;</em>&nbsp;</li></ul>|27929|
| General Application|When using Dynamics NAV 2015 version, the Continia Delivery Network Onboarding Wizard was not showing any instructional text.|28084|







<style>
.content table tr td:nth-child(1) {
width: 100px;
}
.content table tr td:nth-child(2) {
width: 500px;
}
.content table tr td:nth-child(3) {
width: 30px;
}
</style>