---
title: Detailed Changelog for Continia Document Capture 2022 R1
date: 25-04-2024
description: Detailed Changelog for Continia Document Capture 2022 R1
lang: en
---

# Detailed Changelog for Continia Document Capture 2022 R1

This article lists all new updates, features, service packs, and hotfixes for Continia Document Capture 2022 R1.

> [!IMPORTANT]
> This version of Document Capture is no longer supported. As a consequence of this, Continia will no longer correct any errors appearing in this version, and no further service packs relating to the version will be released. For supported versions of Document Capture, see [Software Lifecycle Policy and Continia Document Capture On-Premises](@DC-13).

> [!TIP]
> As a Continia partner, you can be notified of new Document Capture versions and service packs whenever they're released. To sign up for this service, go to [this page](https://continia.zendesk.com/hc/en-us/articles/360005355079-Receive-a-notification-upon-new-Document-Capture-releases) in the Continia PartnerZone (only available to partners).

## Document Capture 2022 R1 Service Pack 7
*Release date: April 24, 2024*  
*App version: 9.7.0*  
*FOB version: 9.07*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and <br> Technology|The Continia Web Approval Portal has been updated to version 24.0.<br>  |54033|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Documents and Templates|When identifying the XML template for an electronic document, only the identification template field with the code <b>CUSTOMISATIONID</b>&nbsp;was considered. Now also the identification template field with code&nbsp;<b>VERSIONID</b>&nbsp;is considered when identifying the XML format.&nbsp; |49531|
| Documents and Templates|The following comment has been changed from: <ul><li><em>Fully matched to Purchase Order &lt;Purchase Order No.&gt;</em></li> </ul>To  <ul><li><em>The Amount Excl. VAT (&lt;<span>Amount Excl. VAT</span>&gt;) - Freight Amount (&lt;<span>Freight Amount</span>&gt;) - [Other amounts that are being subtracted ] (&lt;Amount&gt;) = &lt;Total Amount&gt; fully matched to Purchase Order &lt;Purchase Order No.&gt;.&nbsp;</em>&nbsp;</span> </li> </ul> If the template is set to <b>Auto Approve Within Variance</b> but outside tolerance, the following comment will be added: <ul><li><em>The document will not be auto-approved as the total invoice amount (&lt;Document Amount&gt;) - matched amount (&lt;Matched Amount&gt;) is outside the maximum allowed variance.</em>&nbsp; </li> </ul> |50846|
| Documents and Templates|When registering documents, and the template registration step 1 was set to<span>&nbsp;</span><b>Gen. Journal Lines</b>&nbsp;without specifying the<span>&nbsp;</span><b>Journal Template Name</b>&nbsp;or<span>&nbsp;</span><b>Journal Batch Name</b>&nbsp;on the category, the registration process would produce the following error: <ul><li><em>&quot;Imported Amount Incl. VAT does not match&quot;</em> </li> </ul>  <ul> </ul> |51671|
| Documents and Templates|<span>Optimized the document import processing time by skipping merge operations when templates are not configured to automatically combine PDF files from the same email into one Document Capture document.</span><br>  |54373|
| General Application|When <span>using the&nbsp;</span><b>Assisted Setup Guide</b><span> for&nbsp;</span>selecting what data to include in the exported configuration file, the following error could occur: <ul><li><em>The Document Storage Type field in the Document Capture Setup table cannot be changed when there are documents in the database.</em> </li> </ul> <br> |50002|

## Document Capture 2022 R1 Service Pack 6
*Release date: November 6, 2023*  
*App version: 9.6.0*  
*FOB version: 9.06*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and <br> Technology | The Continia Web Approval Portal has been updated to version 1.27.3 | 45904 |


### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|When i<span>n the Danish localization using</span>&nbsp;an amount distribution code that was not set up for the current vendor, the following error occurred: <ul><li><span><em>Std. beløbsfordelings er kun aktiveret for udvalgte leverandører.\\Leverandør <em>&lt;Standard Amount Distribution Code&gt;</em> er ikke opsat som en af de udvalgte leverandører</em>.</span> </li> </ul><font color="#171717" face="Segoe UI, SegoeUI, Segoe WP, Helvetica Neue, Helvetica, Tahoma, Arial, sans-serif">The error message has been changed to:</font>  <ul><li><font color="#171717" face="Segoe UI, SegoeUI, Segoe WP, Helvetica Neue, Helvetica, Tahoma, Arial, sans-serif"><span><em>Std. beløbsfordelingskodeskode &lt;Standard Amount Distribution Code&gt;&nbsp;er kun aktiveret for udvalgte leverandører.\\Leverandør &lt;Buy-from Vendor No.&gt; er ikke opsat som en af de udvalgte leverandører</em>.</span><br></font> </li> </ul> <font color="#171717" face="Segoe UI, SegoeUI, Segoe WP, Helvetica Neue, Helvetica, Tahoma, Arial, sans-serif"></font> |44607|
| Documents and Templates|When recognizing fields in an&nbsp;<span>XML purchase document</span> with an embedded file where the file name contained a dot character and did not have a file extension, the following error occurred: <ul><li><em>The length of the string is &lt;String Length&gt;, but it must be less or equal to 30 characters. Value: &lt;File name&gt;</em> </li> </ul>Now, MimeType (MimeCode)&nbsp;<span>will be used to identify the file type if the file type exceeds 30 characters or, for any other reason, can't be identified.</span>  |44535|
| Documents and Templates|The Approval group on templates pages <span>was sometimes shown&nbsp;</span>even though no approval workflows were enabled. |44696|
| Documents and Templates|When moving a document from&nbsp;<b>Documents (UIC) </b>to the active company and the template was set to&nbsp;<b>Register Documents Automatically</b>&nbsp;in the&nbsp;<b>Template Card</b>, the following error occurred: <ul><li><em>The following C/AL functions are limited during write transactions because one or more tables will be locked. Form.RunModal is not allowed in write transactions. Codeunit.Run is allowed in write transactions only if the return value is not used. For example, 'OK := Codeunit.Run()' is not allowed. Report.RunModal is allowed in write transactions only if 'RequestForm = FALSE'. For example, 'Report.RunModal(...,FALSE)' is allowed. XmlPort.RunModal is allowed in write transactions only if 'RequestForm = FALSE'. For example, 'XmlPort.RunModal(...,FALSE)' is allowed. Use the COMMIT function to save the changes before this call, or structure the code differently.</em> </li> </ul> |44947|
| Documents and Templates|After moving a document to another company, the preview was not shown for documents created from XML files. |45473|
| Documents and Templates|When having two XML Master templates&nbsp;with the same <b>XML Identification Template</b> and selecting <b>Recognize Fields</b> on an XML document, the following error occurred:<br><span></span> <ul><li><em>The following C/AL functions are limited during write transactions because one or more tables will be locked. Form.RunModal is not allowed in write transactions. Codeunit.Run is allowed in write transactions only if the return value is not used. For example, 'OK := Codeunit.Run()' is not allowed. Report.RunModal is allowed in write transactions only if 'RequestForm = FALSE'. For example, 'Report.RunModal(...,FALSE)' is allowed. XmlPort.RunModal is allowed in write transactions only if 'RequestForm = FALSE'. For example, 'XmlPort.RunModal(...,FALSE)' is allowed. Use the COMMIT function to save the changes before this call, or structure the code differently.</em> </li> </ul>  |45710|
| Documents and Templates|When recognizing template fields with <b>Data Type</b> set to <b>Lookup,</b>&nbsp;the<b>&nbsp;</b>following error occurred in<span>&nbsp;the&nbsp;</span><b>Document Journal</b>: <ul><li><em>The length of the string is &lt;String Length&gt;, but it must be less than or equal to 100 characters. Value: &lt;Field Value&gt;</em> </li> </ul> |45863|
| Documents and Templates|<span>The attachments were unintentionally deleted when a document was moved to the unidentified company and later moved to another company.</span> |47106|
| Document Approval|<span>When using <b>Send Status email to Approvers,</b>&nbsp;emails were not sent to shared users w<span>hen setting<span>&nbsp;</span></span><b>Forward Emails</b><b>&nbsp;</b><span>in the&nbsp;</span><b>Approval Sharing</b><span>.</span></span> |46926|
| General Application|<span>When&nbsp;</span><strong><span>Use Cloud OCR</span></strong><span>&nbsp;is false, and when using the same file path for&nbsp;</span><strong><span>PDF File Path for OCR</span></strong><span>,&nbsp;</span><strong><span>File Path for OCR-processed files</span></strong><span>, or&nbsp;</span><strong><span>XML File Path</span></strong><span>, the following error is shown:</span> <blockquote><ul><li><em>[FieldCaption] ([FilePath]) must not be equal to [FieldCaption].</em> </li> </ul> </blockquote>|44380|
| General Application|Previously, the &quot;CDC Basic&quot; Application Area could be enabled even when the Application Area feature was not in use. In this case, only Document Capture pages were visible. Now,&nbsp;<span>the &quot;CDC Basic&quot; Application Area&nbsp;</span>is only enabled if Basic Application Area is also enabled. |46182|
| General Application|<span>Expanded the progress text variable from 30 to 100 chars in the Storage Migration Status page to prevent the below error in setups with a large number of documents pending migration:</span>  <ul><li><em>The length of the string is &lt;Number&gt;, but it must be less than or equal to 30 characters. Value: &lt;Number&gt; documents are remaining.<br>Page View - Storage Migration Status has been closed.</em> </li> </ul> |46765|
| Order & Receipt Matching|When using the report &quot;Delete Invoiced Purch. Orders&quot; to batch delete orders, the following error occurred in some scenarios: <ul><li><em>The quantity (%2) that you are trying to order is lower than the quantity matched against this order. You must order at least %1 units.</em> </li> </ul> |44599|
| Platform and Technology|Fixed an issue in the Document Header fields subpage, where the cursor would return to the field having focus&nbsp;<span>(field 1)</span>&nbsp;instead of the field clicked with the mouse (field 2). This issue occurred when&nbsp; <ul><li>the value in the field having focus <span>(field 1)&nbsp;</span>was updated and </li><li>the keyboard input validation (in field 1) was triggered by clicking another field (field 2) in the list with the mouse. </li> </ul> |41837|
| Platform and Technology|<span>When opening Manual Setup in the app version of Document Capture, many duplicated records were displayed.</span> |42928|
| Purchase Documents|<span>When creating journal lines, the Source Code and Reason Code fields were not populated. Now, the<span>&nbsp;</span></span><span>Source Code field will be&nbsp;</span><span>populated from the Gen. Journal Template, and the&nbsp;</span><span>Reason Code&nbsp;</span><span>will be populated from the Gen. Journal Batch.</span> |39551|

## Document Capture 2022 R1 Service Pack 5
*Released: May 24, 2023*  
*App version: 9.5.0*  
*FOB version: 9.05*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology|<span></span><span>Events have been added to the solution. For details, please see<span>&nbsp;</span></span><a href="https://docs.continia.com/en-us/continia-document-capture/development-and-administration/development-and-customization/event-publishers/event-publishers-900">Event Publishers for Document Capture 2022 R1 (9.00)</a>  |32025|
| Platform and Technology|The Continia Web Approval Portal has been updated to version 1.27.3 |45904|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|When i<span>n the Danish localization using</span>&nbsp;an amount distribution code that was not set up for the current vendor, the following error occurred: <ul><li><span><em>Std. beløbsfordelings er kun aktiveret for udvalgte leverandører.\\Leverandør <em>&lt;Standard Amount Distribution Code&gt;</em> er ikke opsat som en af de udvalgte leverandører.</em></li></ul> The error message has been changed to: <ul><li><em>Std. beløbsfordelingskodeskode &lt;Standard Amount Distribution Code&gt;&nbsp;er kun aktiveret for udvalgte leverandører.\\Leverandør &lt;Buy-from Vendor No.&gt; er ikke opsat som en af de udvalgte leverandører.</em></li></ul> |44607|
| Documents and Templates|When recognizing fields in an&nbsp;<span>XML purchase document</span> with an embedded file where the file name contained a dot character and did not have a file extension, the following error occurred: <ul><li><em>The length of the string is &lt;String Length&gt;, but it must be less or equal to 30 characters. Value: &lt;File name&gt;</em> </li> </ul>Now, MimeType (MimeCode)&nbsp;<span>will be used to identify the file type if the file type exceeds 30 characters or, for any other reason, can't be identified.</span>  |44535|
| Documents and Templates|The Approval group on templates pages <span>was sometimes shown&nbsp;</span>even though no approval workflows were enabled. |44696|
| Documents and Templates|When moving a document from&nbsp;<b>Documents (UIC) </b>to the active company and the template was set to&nbsp;<b>Register Documents Automatically</b>&nbsp;in the&nbsp;<b>Template Card</b>, the following error occurred: <ul><li><em>The following C/AL functions are limited during write transactions because one or more tables will be locked. Form.RunModal is not allowed in write transactions. Codeunit.Run is allowed in write transactions only if the return value is not used. For example, 'OK := Codeunit.Run()' is not allowed. Report.RunModal is allowed in write transactions only if 'RequestForm = FALSE'. For example, 'Report.RunModal(...,FALSE)' is allowed. XmlPort.RunModal is allowed in write transactions only if 'RequestForm = FALSE'. For example, 'XmlPort.RunModal(...,FALSE)' is allowed. Use the COMMIT function to save the changes before this call, or structure the code differently.</em><br> </li> </ul> |44947|
| Documents and Templates|After moving a document to another company, the preview was not shown for documents created from XML files.<br> |45473|
| Documents and Templates|When having two XML Master templates&nbsp;with the same <b>XML Identification Template</b> and selecting <b>Recognize Fields</b> on an XML document, the following error occurred:<br><span></span> <ul><li><em>The following C/AL functions are limited during write transactions because one or more tables will be locked. Form.RunModal is not allowed in write transactions. Codeunit.Run is allowed in write transactions only if the return value is not used. For example, 'OK := Codeunit.Run()' is not allowed. Report.RunModal is allowed in write transactions only if 'RequestForm = FALSE'. For example, 'Report.RunModal(...,FALSE)' is allowed. XmlPort.RunModal is allowed in write transactions only if 'RequestForm = FALSE'. For example, 'XmlPort.RunModal(...,FALSE)' is allowed. Use the COMMIT function to save the changes before this call, or structure the code differently.</em> </li> </ul>  |45710|
| Documents and Templates | When recognizing template fields with <b>Data Type</b> set to <b>Lookup,</b>&nbsp;the<b>&nbsp;</b>following error occurred in the <b>Document Journal</b>: <ul><li><em>The length of the string is &lt;String Length&gt;, but it must be less than or equal to 100 characters. Value: &lt;Field Value&gt;</em></li></ul> |45863|
| Documents and Templates|<span>The attachments were unintentionally deleted when a document was moved to the unidentified company and later moved to another company.</span><br> |47106|
| Document Approval|<span>When using <b>Send Status email to Approvers,</b>&nbsp;emails were not sent to shared users w<span>hen setting<span>&nbsp;</span></span><b>Forward Emails</b><b>&nbsp;</b><span>in the&nbsp;</span><b>Approval Sharing</b><span>.</span></span><br> |46926|
| General Application| When <strong>Use Cloud OCR</strong> is false, and when using the same file path for <strong>PDF File Path for OCR</strong>, <strong>File Path for OCR-processed files</strong>, or <strong>XML File Path</strong>, the following error is shown: <ul><li><em>[FieldCaption] ([FilePath]) must not be equal to [FieldCaption].</em></li></ul> |44380|
| General Application|Previously, the &quot;CDC Basic&quot; Application Area could be enabled even when the Application Area feature was not in use. In this case, only Document Capture pages were visible. Now,&nbsp;<span>the &quot;CDC Basic&quot; Application Area&nbsp;</span>is only enabled if Basic Application Area is also enabled. |46182|
| General Application|<span>Expanded the progress text variable from 30 to 100 chars in the Storage Migration Status page to prevent the below error in setups with a large number of documents pending migration:</span>  <ul><li><em>The length of the string is &lt;Number&gt;, but it must be less than or equal to 30 characters. Value: &lt;Number&gt; documents are remaining.<br>Page View - Storage Migration Status has been closed.</em> </li> </ul> |46765|
| Order & Receipt Matching|When using the report &quot;Delete Invoiced Purch. Orders&quot; to batch delete orders, the following error occurred in some scenarios: <ul><li><em>The quantity (%2) that you are trying to order is lower than the quantity matched against this order. You must order at least %1 units.</em></li></ul> |44599|
| Platform and Technology|Fixed an issue in the Document Header fields subpage, where the cursor would return to the field having focus&nbsp;<span>(field 1)</span>&nbsp;instead of the field clicked with the mouse (field 2). This issue occurred when&nbsp; <ul><li>the value in the field having focus <span>(field 1)&nbsp;</span>was updated and </li><li>the keyboard input validation (in field 1) was triggered by clicking another field (field 2) in the list with the mouse. </li> </ul> |41837|
| Platform and Technology|<span>When opening Manual Setup in the app version of Document Capture, many duplicated records were displayed.</span><br> |42928|
| Purchase Documents | When creating journal lines, the Source Code and Reason Code fields were not populated. Now, the Source Code field will be populated from the Gen. Journal Template, and the Reason Code will be populated from the Gen. Journal Batch. |39551|

## Document Capture 2022 R1 Service Pack 4
*Released: January 27, 2023*  
*App version: 9.4.0*  
*FOB version: 9.04*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Documents and Templates|<span>A new field, <span>Split XML Documents Automatically, has been</span>&nbsp;added to the Document Category card.&nbsp;</span><span>When populating the&nbsp;</span><span>Split XML Documents Automatically&nbsp;</span><span>field, XML documents are automatically split during import.</span> |41895|
| Documents and Templates | The following comment is now configurable: <ul><li>This document may contain pages that belong to another Source ID. </li></ul> |43142|
| General Application|Added validation code to the EWS Client Secret field on the CDC Document Category table to&nbsp;<span>prevent common input mistakes.</span> |42452|
| General Application | When security filters were applied on the Purchase Header table to restrict the view on Purchase Orders, the following error occurred when opening the Assign to Me page: <ul><li><em> A security filter has been applied to table Purchase Header. You cannot access records that are outside of this filter. </em></li></ul> |43357|
| Platform and Technology| Events have been added to the solution. For details, please see <a href="https://docs.continia.com/en-us/continia-document-capture/development-and-administration/development-and-customization/event-publishers/event-publishers-900">Event Publishers for Document Capture 2022 R1 (9.00)</a> |32025|
| Platform and Technology|The Continia Web Approval Portal has been updated to version 1.26.1 |43356|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional| Corrected the following German's welcome mail texts when exporting users to Continia Online: <ul><li><em>&quot;Sie wurden als Benutzer für Continia Online&quot; is changed to &quot;Sie wurden als Benutzer für Continia Online <b>eingerichtet</b>.&quot;</em> </li><li><em>&quot;Ihr Konto wurde bereits aktiviert und Sie können auf Continia Online unter &lt;URL&gt;&quot; is changed to &quot;Ihr Konto wurde bereits aktiviert und Sie können auf Continia Online unter &lt;URL&gt; <b>zugreifen</b>.&quot;</em></li></ul> |38320|
| Documents and Templates|When a document is registered and&nbsp;re-opened, d<span>ocument validation has been added<span>&nbsp;</span></span>to ensure that the auto-match process is correctly triggered again. |24415|
| Documents and Templates|<span>During document registration,&nbsp;</span>Unit Cost, Line Discount %, Line Discount Amount, and Line Amount were re-calculated on the purchase line when the Unit of Measure Code on the document line was different from the Base Unit of Measure on the Item Card or Resource Card pages. |26491|
| Documents and Templates| When selecting the Accounts for Amounts action for a document without a template assigned, the list contained all existing posting setups for all templates in the database. <br><br> The Accounts for Amounts action is now disabled when a document does not have a template assigned yet. |30471|
| Documents and Templates| A new field Prioritize Cr. Memo as Doctype has been added to the Template Card. <br><br> The document type is by default determined by the topmost caption found in the PDF. <br><br> When Prioritize Cr. Memo as Doctype is set to true, the document is classified as a credit memo when a credit memo caption is found even though the PDF might have words written higher up that otherwise would identify it as an invoice. |34639|
| Documents and Templates|When creating a new template field, special characters are preserved for the following template fields: <ul><li>Dimension fields. </li><li>PAYMENT-ID field. The field is available in all localizations in XML templates&nbsp;<span>OIOUBL,&nbsp;</span><span>OIOXML,</span><span>&nbsp;and&nbsp;<span>KØB-DK (Danish localization only).</span></span> </li> </ul> |39552|
| Documents and Templates|<span>When an identification field contained multiple words (e.g. Vendor Name = &quot;My Supplier&quot;), the right template was not found in some situations.</span> |39594|
| Documents and Templates|Attachments were wrongly deleted when documents were moved to the&nbsp;<span>unidentified company.</span> |40371|
| Documents and Templates|Changing the Purchase File Display Name in the Document Capture Setup page had no effect when displaying attachments in the Documents factbox on the Vendor Card and Vendor List pages.<br>|40372|
| Documents and Templates|<span>The feature that copies an existing vendor template from a different company is no longer case-sensitive for the vendor name field. Note that the user must have access (permission), and<span>&nbsp;</span></span><span>Document Capture must be</span><span>&nbsp;activated in the companies involved.</span><br> |40675|
| Documents and Templates|The unidentified company (UIC) feature has been improved with the following changes: <ul><li> Use Unidentified Company Documents in Document Capture Setup can't be disabled if the field Doc. with Unidentified Company on a document category is configured to 'Import as UIC Document'. </li><li> If Use Unidentified Company Documents in Document Capture Setup is turned off and you activate Auto Move to Company on the Document Category, you are asked whether you would like to activate the Use Unidentified Companys Documents. </li><li> When enabling Auto Move to Company on the Document Category, the option Doc. with Unidentified Company becomes editable. </li><li> When disabling Auto Move to Company on the Document Category Card, the option Doc. with Unidentified Company is automatically set to 'Import in active Company'. </li><li>The tooltips regarding UIC in Document Capture Setup, Document Category Card, and Document Journal pages have been revised. </li></ul> |40846|
| Documents and Templates| When using the Recognize Fields action and recognizing lines, and having a line field with a long field code, the following error occurred in some situations: <ul><li><em>The length of the string is &lt;Lenght of field&gt;, but it must be less than or equal to 20 characters. Value: &lt;Template Field Code value&gt;</em></li></ul> |40971|
| Documents and Templates| When registering a document and Continia Payment Management was installed, the following error could occur: <ul><li><em>Field CPM Preferred Bank Account Code (6216183) of table Purchase Header (38) is obsolete, reason: Field name is too long.</em></li></ul> |42272|
| Documents and Templates|In table&nbsp;6086017 - CDC Msg. Center Setup Template, the fields listed below have been made not editable. <ul><li>Field&nbsp;7&nbsp; - Information Allowed </li><li>Field&nbsp;<span>8&nbsp; - Warning Allowed</span> </li><li><span>Field 9 - Error Allowed</span> </li> </ul>  |42308|
| Documents and Templates|The Max. Variance Amount Allowed (LCY)&nbsp;<span>field<span>&nbsp;</span></span>on the Template Card was incorrectly updated when updating on the master template. |42341|
| Documents and Templates|When registering a document with document lines where the text in the No. field had more than 50 characters, the following error occurred: <ul><li><em>The length of the string is &lt;string length&gt;, but it must be less than or equal to 50 characters. Value: &lt;No. field value&gt;</em><br> </li> </ul> |42358|
| Documents and Templates| In some situations, the document comment shown below could be displayed multiple times in the document comment section. <ul><li><em>WARNING: Amount Incl. VAT ([Amount Incl. VAT]) does not match the rounded amount ([Rounded Amount Incl. VAT]) calculated using Invoice Rounding Precision and Invoice Rounding Type configured for [Currency Code].</em></li></ul> |42952|
| Documents and Templates| When adding a vendor with a name longer than 50 characters to Excluded Sources on the Document Category, the following error occurred: <ul><li><em>The length of the string is &lt;Text length&gt;, but it must be less than or equal to 50 characters. Value: &lt;Vendor Name&gt;.</em></li></ul>  |42995|
| Documents and Templates|<span>Line recognition without captions has been improved.&nbsp;</span> <span>Before, document lines without header captions were not recognized across similar documents.&nbsp;</span><span>Now, the lines are recognized when the line columns are in the same position within the vertical and horizontal margins in the document.</span> |43083|
| Documents and Templates|<span>When recognizing lines and capturing Discount Percentage, Discount Amount is now calculated using the same formula as in the standard application.&nbsp;</span> |43247|
| Documents and Templates|When looking up using the <span>Template List&nbsp;</span><span>page,&nbsp;</span>search texts for the current template were not shown. |43471|
| Documents and Templates|Corrected a spelling mistake on the Category card. The field caption &quot;TIFF Image Colour Mode&quot; was changed to&nbsp;<span>&quot;TIFF Image Color Mode&quot;.</span> |43522|
| Documents and Templates|<span>When using &quot;Copy Template&quot; to create a new master or identification template, the Source Record No. and Source Record Name&nbsp;</span><span>fields<span>&nbsp;are now&nbsp;</span></span><span>empty on the new template.</span> |43526|
| Documents and Templates|When creating a template using the &quot;Create/Select Template...&quot; action, the fixed value or formula field for lookup fields was not transferred to the created template. |43931|
| Document Approval|The handling of number filters in Advanced Approval Groups has been i<span>mproved</span>.<br> |42579|
| General Application|The Export Attachments&nbsp;<span>report<span>&nbsp;</span></span>did not include any additional files even when the Export Related Documents option was populated.<br> |34791|
| General Application|<span>As the XML Attachments document category <span>(XMLATTACH)<span>&nbsp;</span></span>is only to be used for automatically saving the files embedded in an XML Document, this category is now filtered out from all the Drag and Drop Categories pages.&nbsp;</span><br> |41233|
| General Application|When importing an XML document with description lines exceeding 250 characters, the following error occurred:&nbsp; <ul><li><em>The length of the string is &lt;string length&gt;, but it must be less than or equal to 250 characters. Value: &lt;description&gt;</em> </li> </ul> |41492|
| General Application| When scrolling horizontally through matching lines, the table headers did not follow the table columns and instead remained in their original position. |41698|
| General Application|Captions were missing on page 138 - Posted Purchase Invoice page for multiple localizations. |42019|
| General Application | When renaming a record in a table where the primary key was Time, BigInteger, or DateTime, the following error occurred: <ul><li><em> Field Type '&lt;Field Type&gt;' not supported as a key value. </em></li></ul> |42899|
| General Application|<span>It is no longer possible to create empty files&nbsp;<span>using New button<span>&nbsp;</span></span>in the Document Files Factbox. This change only a<span>pplies to Business Central 14 (April 2019).</span></span> |43384|
| Order & Receipt Matching|In the Invoice Matching page when splitting a line on a purchase order, Status is now set to Open, in order to avoid following error: <ul><li><em><span>Status must be equal to 'Open' in Purchase Header: Document Type=&lt;Document Type&gt;, No.=&lt;Document No.&gt;. Current value is '&lt;Current Status&gt;'.</span></em> </li> </ul> |21769|
| Platform and Technology|The Document Nos. is now validated for characters that either the file system or Azure Blob Storage does not support. This validation occurs when setting the document number series and when importing documents. |39545|
| Platform and Technology|Closing the Document Card, using the ESC key, would sometimes close both the Document Card and the underlying Document List, thus returning focus to the role center. |41271|
| Platform and Technology|<span>It is no longer possible to add empty files using the drag-and-drop functionality in the Document Files Factbox.</span><br> |42372|
| Purchase Documents|Payment Reference is now updated on Danish FIK 75. |38424|
| Purchase Documents| When capturing a valid IBAN more than 30 characters long into the Vendor Bank Account No. header field, the following error comment was added to the document. <ul><li><em> Vendor Bank Account No. is not correct. </em></li></ul> |44418|

## Document Capture 2022 R1 Service Pack 3
*Released: October 31, 2022*  
*App version: 9.3.0.0*  
*FOB version: 9.03.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Documents and Templates| All templates, including master and identification templates, are stored in the same table and are using the same pages. Only a few of the fields on the pages are relevant for i<span>dentification templates.&nbsp;</span> All fields and actions not relevant for identification templates are now hidden/disabled.  |14803|
| Documents and Templates|<span>Added support for line translation for the sales category using the GTIN field on the Item.</span><br> |24082|
| Documents and Templates|For the Danish localization (DK), the following three new template fields have been added to the PEPPOL3 template to support FIK numbers. <ul><li>Vendor No. </li><li>PaymentID&nbsp; </li><li>FIK </li> </ul> |32731|
| Documents and Templates|The following comments have been made <span>configurable</span>: <ul><li><em>Vendor Bank Account No. is not correct.</em> </li><li><em><span>VAT Registration No</span>. is not correct.</em> </li> </ul>  |34866|
| Documents and Templates|<p><span lang=EN-US>The performance of the Recognize Fields function has been optimized.</span><span lang=EN-US></span> </p> |34907|
| Documents and Templates|<span>The performance <span>when searching for templates</span>&nbsp;has been<span>&nbsp;</span></span><span>optimized.</span> |35065|
| Documents and Templates| The data caption on the Template Field Card has been changed to show the field name only. For example, Amount Excl. VAT. <br><br> Previously the following was shown at the top of the Template Field Card page: Template number, Type, Code, and Field name. |39185|
| Documents and Templates|The Comment field has been added to page 6085600 - CDC Document List With Image and page 6086074 - CDC Delegated Documents List. |40280|
| Document Approval|<span>The &quot;Error email&quot;<span>&nbsp;</span></span><span>field&nbsp;</span><span>has been removed from the Document Capture Setup / Purchase Approval page. When sending the approval or reminder email notification, a message containing a list of the users with an invalid email address is displayed instead.</span><br> |32015|
| General Application|<span>When translating No. and Description, the system has been changed to prioritize exact values over values containing the asterisk (\*) symbol.<br></span><br> With the following configuration for the No. field,<br> <ul><li>\*FREIGHT\* -&gt; G/L Account 1000 </li><li>EXPRESS FREIGHT\|NORMAL FREIGHT -&gt; G/L Account 2000 </li> </ul> &quot;Express Freight&quot; will now be translated to G/L Account 2000 as the row without the asterisk (\*) symbol is prioritized.<br> <br> Support has also been added for enclosing search terms in single quotes (') when the value includes characters that are reserved for use in Business Central filter-notation (i.e. the characters &nbsp;( ) \| &lt; &gt; = .. ? &amp;). It is, however, not possible to wrap the asterisk (\*) and the Ignore case-sensitivity operator (@).<br> <br> The priority order is:<br> <ol><li>Item field GTIN </li><li>Number exact match </li><li>Number exact match with filter characters (e.g. 'AiP&amp;12' or 'TM&gt;Y') </li><li>Number filters (e.g. 100..109 or Freight\|Delivery) </li><li>Number filter using &quot;\*&quot; (e.g. 10\* or \*freight) </li><li>Item Reference table </li><li>Item Vendor table </li><li>Item table - field &quot;Vendor Item No.&quot; </li><li>Item No. field from Item table (template setting &quot;Use Vendor/Customer Item Nos.“) </li><li>Number &quot;\*&quot; translation only </li><li>Description exact match </li><li>Description exact match with filter characters (e.g. 'Anderson &amp; co.') </li><li>Description filters (e.g. Apple iMac\|Apple iPhone) </li><li>Description filters using &quot;\*&quot; (e.g. Apple\*) </li><li><span>Description &quot;\*&quot; translation only</span> </li> </ol>   |32564|
| General Application|<span>When recognizing sales document lines where either Unit Cost, Quantity, or Line Amount is not recognized, the missing field is now <span>automatically&nbsp;</span>calculated.&nbsp;</span><span>Previously, only Quantity was <span>automatically&nbsp;</span>calculated. <br><br> Recognizing two of the three fields and if all five fields (including the Line Discount Amount and Line Discount Percentage fields) have a blank value in Formula, the missing field is automatically calculated as specified below:<br> <ul><li>Line Amount = Quantity \* Unit Cost - DiscAmount </li><li>Unit Cost = (Line Amount + DiscAmount) / Quantity </li><li>Quantity = (Line Amount + DiscAmount) / Unit Cost </li> </ul> If DiscAmount is zero after capture (either not captured or captured as zero), and Line Discount % is not zero, DiscAmount is calculated as follows: <br> <ul><li>DiscAmount = Line Amount \* Line Discount % / 100 </li> </ul> When one of the three fields is calculated, an error, warning, or information comment is inserted in the comment section, depending on the comment setup.<br> <br> A new integration event has been added: OnBeforeAdjustMissingFields(VAR Document : Record “CDC Document”;VAR Handled : Boolean)<br> <br> <span>If customers wish to disable the auto-calculation of the three values, you create an event subscriber that changes the handled value to TRUE.</span><br> |34610|
| General Application| When changing one of the fields relevant for OCR processing, the following notification is shown in RTC: <ul><li><em>The OCR configuration file will be exported when pressing OK or refresh.<br></em> </li> </ul>And in Web Client the following notification is shown:<br> <ul><li><em><span>The OCR configuration file will be exported when closing or refreshing this page</span>.</em> </li> </ul>  <ul> </ul> |39184|
| Order & Receipt Matching| The “Use tracking by package number in reservation and tracking system” feature is now supported in order and receipt matching (only for matching purchase receipt lines and return shipment lines). |24488|
| Order & Receipt Matching|The Special&nbsp;<span>Sales Order No. field is now available on the Purch. Invoice Match Subpage.</span> |39228|
| Platform and Technology | Events have been added to the solution. For details, please see [Event Publishers for Document Capture 2022 R1 (9.00)](https://docs.continia.com/en-us/continia-document-capture/development-and-administration/development-and-customization/event-publishers/event-publishers-900). |32025|
| Platform and Technology|<p><span lang=EN-US>The performance of the Find Entries (<span>Navigate)</span>&nbsp;function has been optimized.</span> </p> |34909|
| Platform and Technology|<span>The Continia Web Approval Portal has been updated to version 1.25.2</span><br> |41509|
| Purchase Documents|<span>The performance<span>&nbsp;</span><span>during the&nbsp;<span>approval of documents</span></span>&nbsp;has been<span>&nbsp;</span></span><span>optimized&nbsp;<span>in<span>&nbsp;</span></span><span>Business Central<span>&nbsp;</span></span><span>2020 release wave 2 (BC17)</span><span><span>&nbsp;</span>and newer versions.</span></span> |38945|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|<span>The Enable Standard Notification field caption on the Document Capture Setup page was wrongly translated in several languages.</span><br> |38872|
| Country and Regional|<span>Captions were missing on page 55 -<span>&nbsp;</span></span><span>Purch. Invoice Subform<span>&nbsp;</span></span><span>for many localisations.</span>|40310|
| Documents and Templates|When registering a document while applying an<span><span>&nbsp;</span>amount distribution code on negative amounts</span>, the following error occurred: <ul><li><em>There is no Standard Amount Distribution Line within the filter. Filters: Amount Distribution Code: [Amount Distribution Code], Unit Cost: &lt;&gt;0</em> </li> </ul> Now, it is possible to use amount distribution codes on negative amounts. |21762|
| Documents and Templates|When batch registering documents from the GLDOC category, none of the documents were registered. |27400|
| Documents and Templates|When registering a document and when Registration Step 1 was set to Create Journal Lines and Registration Step 2 was set to Post, the following error occurred. <ul><li><em><span>The journal 'Journal Template Name'= 'XXX', 'Journal Batch Name' = 'YYY' is not empty. Please delete or post the existing journal lines before registering a new document</span><span>.</span></em> </li> </ul> |31340|
| Documents and Templates|When selecting Create Journal Lines for either Invoice Reg. Step 1 or Credit Memo Reg. Step 1, the Matching and Approval groups and the corresponding matching options for invoices and credit memos disappeared.&nbsp; |34498|
| Documents and Templates|The configuration file now defaults table no. to 80 for the Journal Template field in the Purchase category. |34511|
| Documents and Templates|<span>In the Portuguese configuration file, rules and captions changed to the following for the<span>&nbsp;DOCTYPE&nbsp;<span>field on&nbsp;</span></span><span>master templates</span>:</span><br> <ul><li><span>&quot;F&quot; for invoice</span> </li><li><span>&quot;N&quot; for credit memos</span> </li> </ul> |38421|
| Documents and Templates|When importing the first document from the Document Categories lookup from the Document Journal page, all the actions were disabled until the Document Journal page was reopened.&nbsp;&nbsp; |38493|
| Documents and Templates| When Registration Step 1 was set to Create Journal Lines, and Registration Step 2 was set to Post, Registration Step 2 was not executed. |38495|
| Documents and Templates|When pressing the &quot;Add Template Field&quot; action in the <span>Document Journal</span>, focus is now placed on&nbsp;<span>the first field on the Template Field List. Previously, focus was placed&nbsp;</span><span>on the last field in the list.</span> |38592|
| Documents and Templates|The Order/Return Order field always showed false on the Assigned Documents page.<br> |38682|
| Documents and Templates|When opening attachments on the Document Journal or Document Card page for registered documents, the following error occurred: <ul><li><em>The Document does not exist. Identification fields and values: No.=&lt;Document No.&gt;</em></li></ul> |38737|
| Documents and Templates|<span>In some situations, the Move Up and Move Down actions on the Template Fields subpage did not work.</span> |38959|
| Documents and Templates|When using a field translation with stars (\*) at both the beginning and the end of the translation, the word was not translated correctly. |38978|
| Documents and Templates|The <span>Delete after Download field was wrongly hidden after selecting an EWS protocol on Document Category Card.</span> |39102|
| Documents and Templates|When recognizing document lines, the template No. field is mandatory. <br><br> The error message shown in the Document Journal&nbsp;<span>when running the&nbsp;</span><span>Recognize Fields function and when&nbsp;<span>the No. field is missing&nbsp;</span></span></span></span><span>has been changed to the following message:</span> <ul><li><em><em><em><span>When recognizing lines, y</span><span>ou must include the line field &lt;Field Name&gt; in the template.</span></em></em></em> </li> </ul> |39240|
| Documents and Templates|The copy template action was disabled on identification templates. Now it is enabled. |39325|
| Documents and Templates|<span>For master template fields with Data Type Lookup, the predefined value in the formula field is now populated when a template is created from the master template.</span><br> |39397|
| Documents and Templates|<span>For the German localization, n</span><span>o stylesheet was shown when opening an XRechnung CII&nbsp;document.</span> |40286|
| Documents and Templates|<span>For the German localization,<span>&nbsp;t</span></span>he <span>XRechnung CII<span>&nbsp;<span>XML<span>&nbsp;</span></span></span></span>master template did not recognize the document type correctly. |40297|
| <s>Documents and Templates</s> |<s>Attachments were wrongly deleted when documents were moved to the&nbsp;<span>unidentified company.</s></s><a href="#footnote-2.1"><sup>1</sup></a></span> | <s>40371</s>|
| Documents and Templates|The Default field is now hidden on templates of type Master and Identification. |40798|
| Documents and Templates|<span>When importing a Svefaktura, embedded files did not get created as attachments.</span><br> |40810|
| Documents and Templates|<span>The document header fields were not shown when opening the Document Journal <span>page in&nbsp;</span></span><span><span>Business Central 2020 release wave 2 (BC v17)</span></span><span>.</span> |41945|
| Document Approval| When exporting users now, the system only sends welcome emails to Continia users configured in a company if Welcome Emails in Continia Web Portals is set to Automatic for the relevant company. Before, the system only used the Welcome Emails setting from the company wherefrom the Export Users function was run. |21311|
| Document Approval|When setting a date or boolean filter on advanced approval groups, the following error occurred: <ul><li><em>It is not possible to set [Value] to [Data type].</em><br> </li> </ul> Now, it is possible to filter with dates and booleans.<br>  |34602|
| Document Approval| When posting a document with approval comments where the comment length was greater than 80 characters, the following error occurred: <ul><li><em>The length of the string is &lt;text length&gt;, but it must be less than or equal to 80 characters. Value: &lt;Comment&gt;.</em></li></ul> |38719|
| Document Approval|When cancelling an approval request for a purchase header with a posted allocation, the allocation was not recreated when the purchase header was again sent for approval. |39188|
| Document Approval|The performance has been optimized when running the CDC Purch. Approval Entries page. |41956|
| General Application| <p><span lang=en-DK>When the <span>Azure Storage account name wasn't in lower cases, importing or moving files was impossible.&nbsp;</span></span><span>The Azure Storage account name is, therefore, now|29570|
| General Application|When multiple users imported documents simultaneously, some files could be empty, and the same document could be imported more than once. To prevent this, only one instance of the document import process can be running now.<span></span> |31076|
| General Application|<span>When activating both Use Cloud OCR and Export OCR Configuration Files in the Document Capture Assisted Setup Guide, it was not possible to deactivate Export OCR Configuration Files until Use Cloud OCR was deactivated.</span><br> |38507|
| General Application|The value in the following fields has been masked: <ul><li>The EWS Client Secret field on page&nbsp;6085578 - CDC Document Category Card </li><li><span>The </span><span>AAD Application Key field</span><span>&nbsp;on p</span>age 6192775 - CDC Continia Web Portal Card </li> </ul> |38741|
| General Application|When exporting configurations through the Document Capture Assisted Setup Guide, decimal values were converted to integers (e.g., 22,5 was converted to 225).&nbsp; |38812|
| General Application|When sending status emails, the following error occurred in some situations: <ul><li><em>You do not have the following permissions on the TableData <span>CDC App. Reminder E-Mail Setup</span>: Read.</em> </li> </ul> |41037|
| General Application| Allow Force Registration was not copied to other companies when you, in the User Setup by Company in the Continia User page, granted the user access to another company. <br><br> Export User is now hidden in the Continia Users List page when the web approval portal is not configured in any company. |41724|
| Order & Receipt Matching|<span>The following only applied to Business Central 2019 release wave 2 (BC15) and later versions.<br></span>  <span><br></span> <span>When adding the &quot;Line Discount % (Invoice)&quot; field to the&nbsp;</span><span>Order Lines subpage on the Invoice Matching page, a wrong field caption was shown in personalization mode.&nbsp;</span> |38780|
| Order & Receipt Matching|An error message was shown when performing a manual match and typing in a negative Direct Unit Cost (Invoice)&nbsp;or negative Direct Unit Cost (Cr. Memo). <br><br> The following message was shown if the document was matched to a receipt or an order: <ul><li><em>Direct Unit Cost (Invoice) must be positive.</em> </li> </ul>And&nbsp;<span>the following message was shown if the document was matched to a </span>return shipment or return order: <ul><li><em>Direct Unit Cost (Cr. Memo) must be positive.</em> </li> </ul>Now, there is no limit when manually changing Direct Unit Cost values.<br>   |39210|
| Order & Receipt Matching|<span>When Invoice Reg. Step 1 was set to Match &amp; Update Order or Credit Memo Reg. Step 1 was set to Match &amp; Update Return Order, it was possible to register the document without any warning message.<br></span><br> Now, the following warning message is shown, when registering an invoice without matching:<br> <ul><li><em>Invoice Reg. Step 1 has been set up to Match &amp; Update Order, but no lines were matched. Do you want to continue the registration?</em> </li> </ul> And, the following warning message is shown, when trying the register a credit memo without matching:<br> <ul><li><span><em>Credit Memo Reg. Step 1 has been set up to Match &amp; Update Return Order, but no lines were matched. Do you want to continue the registration?</em></span> </li> </ul>|39334|
| Platform and Technology|The action button for files in the Documents factbox became invisible when files had long names.<br> |38387|
| Platform and Technology|When the template field code was more than 15 characters long, the following error occurred during field recognition:<br><ul><li><em>The length of the string is &lt;Lenght of field&gt;, but it must be less than or equal to 20 characters. Value: &lt;'TemplateField.Code'&gt;</em> </li> </ul>  |39544|
| Purchase Documents|When the Purchase File Display Name field in Document Capture Setup was set to Posted Document No. + Vendor Document No. or Unposted Document No., the setting was only used in the factboxes<span>&nbsp;on posted document pages. The functionality has now been extended to other pages, such as the Vendor card and Vendor List page.</span> <br> |32229|
| Purchase Documents|During registration of a document, the&nbsp;<span>Purchaser Translation page is shown if no purchaser can be found. The page only had an OK button.&nbsp;</span><span>It was, therefore, not possible to close the page and thereby stop the registration process.</span> |39079|
| Purchase Documents|For the <span>Netherland&nbsp;</span>localization when After Step 1 was set to codeunit 6085715 (CDC Purch. Doc. - After Step 1) and Invoice Reg. Step 1 was set to Create Journal Lines on the Template Card page, the following error occurred: <ul><li><em><span>The following error occurred when performing Codeunit ID: After Step 1 on invoice &lt;Invoice No.&gt;:<br></span></em><em><br>The Purchase Header does not exist. Identification fields and values: Document Type='Invoice',No.='&lt;Invoice No.&gt;'<br><em><br>Any subsequent steps will have to be performed manually.</em><br></em> </li> </ul>     |39273|
| Purchase Documents|The Pay-to Name field in the CDC Purch. Allocation Header table has been extended from 50 to 100 characters. |41575|

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-2.1">Unfortunately, this feature wasn't included in this release as previously announced but will become available in a future release instead.</li>
  </ol>
</div>
</small>

## Document Capture 2022 R1 Service Pack 2
*Released: June 17, 2022*  
*App version: 9.2.0.0*  
*FOB version: 9.02.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| <s>Documents and Templates</s>|<s>The data caption on the template field card has been changed to the field name.</s><a href="#footnote-1"><sup>1</sup></a> |<s>32266</s>|
| Documents and Templates|The possibility to delete or import multiple files has been added to the Document List page. |32847|
| Documents and Templates|The performance during document import has been <span>optimized.</span> |35089|
| Document Approval|We have added&nbsp;<span>the&nbsp;</span><span>Document Card and Match Lines actions&nbsp;</span>to the Assigned To Me page. |28013|
| General Application|The “Out of Office Setup” page has been added to the Document Capture menu, and it is now possible to find the page using the build-in Business Central search function. |23492|
| General Application|<span>The OCR configuration file is now exported when changing relevant fields and using on-prem OCR, including&nbsp;<span>modifying the <span>Process PDF files with XML files&nbsp;</span>field</span>.</span> <span>Previously <span>the OCR configuration file was only automatically exported when using cloud OCR.</span></span> |28627|
| General Application| In the web client, it is not possible to set the size of the document view factbox. To work around this, we had previously created a page (6086077 - CDC User Property List2) that an administrator can use to set the size for the relevant users by changing ”Add-In Min Width”. <br><br> We have now added the &quot;Document View Width&quot; field (previously named ”Add-In Min Width”) to the Continia User Setup list and card. <br><br> We suggest you start with 750 or higher in &quot;Document View Width&quot; field if the size of the document view factbox is too small. |30245|
| General Application|<span>When changing the Company Code, the following message was previously shown:</span> <ul><li><span><em>When you change Company Code you must:&nbsp;</em></span> </li> </ul> <blockquote><blockquote><span><em>- Reactivate Document Capture</em></span> </blockquote><blockquote><span><em>- Export OCR Configuration Files</em></span> <span><em><br></em></span> </blockquote></blockquote><span>&nbsp;Now the message shown is:</span> <ul><li><span><em>When you change Company Code you must:</em></span> </li> </ul> <blockquote><blockquote><span><em>- Export OCR Configuration Files</em></span> <span><em><br></em></span> </blockquote></blockquote><span>&nbsp;Since there is no need to reactivate Document Capture.</span> |31997|
| General Application|<p><span>	In Business Central 2021 release wave 1 (BC18),&nbsp;<span>email scenarios are now supported for the following processes:</span><br></span> </p><ul><li><span>Document Capture Approval Status Email - Used when sending the approval status email.</span> </li><li><span>Continia Welcome Email - Used when sending the welcome emails to Continia users.</span> </li><li><span>Document Capture Assigned Documents - Used when sending assigned notifications.</span> </li><li><span>Document Capture Status Email To Reviewers - Used when sending status emails to reviewers.</span> </li> </ul>|32182|
| General Application|<span>When running the Document Capture Setup Wizard and selecting a localization, the list of available localizations is now sorted ascending by name.</span><br>|32708|
| General Application|The NAV Login Type field on the Continia User list is now editable to support scenarios where the default value must be changed. |32740|
| General Application|When opening the Payment Journal, the following error occurred: <span><em><ul><li><span>The Document Capture Setup does not exist. Identification fields and values: Primary Key=''</span> </li> </ul> </em></span> |34590|
| Platform and Technology| Events have been added to the solution. For details, please see <a href="/continia-document-capture/development-and-administration/development-and-customization/event-publishers/event-publishers-900">Event Publishers for Document Capture 2022 R1 (9.00)</a> |32025|
| Platform and Technology| When using Document Capture pages with client add-ins in some situations, the following &quot;Reduced functionality&quot; warning was shown <ul><li><em>The &lt;Add-in name&gt; control add-in might not run as you expect it to. The functionality has been reduced to ensure your productivity. Contact the add-in vendor for more information. </em></li></ul> |32790|

<small style>
<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">Unfortunately, this feature wasn't included in this release as previously announced, but it will be available in all releases from DC 10.00 and onwards.</li>
  </ol>
</div>
</small>

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|Missing translations have been added to the Document Search page. |34595|
| Documents and Templates|Fixed an issue where the F2 function key did not behave as expected when working with the document header fields in the Document Journal. |21693|
| Documents and Templates|<span>The Delete button on the Split and Merge Documents page was enabled, even though the &quot;Allow Deleting Documents&quot; option was not activated on the Document Category page.&nbsp; </span>|27408|
| Documents and Templates|<span>Added support for Translate to Type =<span>&nbsp;</span><span>Resource<span>&nbsp;</span></span>on the Accounts for Amounts and Purchase Line Translation page.</span> <br> |30343|
| Documents and Templates|<span><span>The setting &quot;Change Sign&quot; on template fields did not change the sign as expected in some situations.</span></span> |30347|
| Documents and Templates|<span>The 'Stop Recognition' field is now hidden when the template type is Line or when Allow Line Recognition is not activated.</span><br> |30823|
| Documents and Templates|<span>On a template with &quot;Prices Incl. VAT&quot; set to yes, the &quot;Validate VAT Calculation&quot; field did not work as intended.</span><br> |31411|
| Documents and Templates|The KID field is now copied to the created purchase header during document registration.<br> |31841|
| Documents and Templates| Calculations did not work when a template field code contained a space or certain special characters.<br>Therefore, it is now being prevented that template field codes include a space or the following special characters:&nbsp;(/\*-+()\|&lt;&gt;%^&amp;=.?$#@'&quot;).<br>  |31969|
| Documents and Templates|<span></span> <span>When trying to register a document where the Document Type <span>field<span>&nbsp;</span></span>had not been added to the document template, the following error occurred: <br><ul><li><span><em>The Template Field does not exist. Identification fields and values: Template No.=&lt;template no&gt;,Type='Header',Code='DOCTYPE'</em></span> </li> </ul> |32410|
| Documents and Templates|In some situations for the NL localization when registering a document with VAT Amount, the following error occurred: <ul><li><em>Doc. Amount VAT&nbsp;must not be more than VAT Amount.</em> </li> </ul> |32427|
| Documents and Templates|Configuring &quot;Invoice Step 1&quot; or &quot;Credit Memo Step 1&quot; on a template to <span>&quot;Create Journal&quot;&nbsp;</span>caused both document types to be registered to a general journal. |32647|
| Documents and Templates|<span>A line translation was not found when the Vendor Item No. on the item was not uppercase.</span><br>|32721|
| Documents and Templates|Tooltips have been added to the following fields on the document category card; <ul><li>Journal Template, </li><li>Journal Template Name </li><li>Journal Batch Name. </li> </ul> |34509|
| Documents and Templates|When using lookup in the Journal Template field on the Document Category page, only template tables are now shown. |34510|
| Documents and Templates|The Show Document After Register field on the Template was ignored when registering documents to journals. Now, the relevant journal is opened when&nbsp;<span>Show Document After Register is populated.</span> |34514|
| Documents and Templates|<span>When using an amount rounding precision <span>different<span>&nbsp;from the&nbsp;</span></span>invoice rounding precision defined in General Ledger Setup and recognizing lines, the following error occurred in some situations:</span><br>  <ul><li><em>The sum of all lines ([Sum of Line Amounts]) does not reconcile to the total amount ([Amount Ex. VAT]).</em> </li> </ul>  |34575|
| Documents and Templates|When registering a document and Field in Purchase Header or Field in Line Table was blank, the following error occurred in some situations: <ul><li><em>The supplied field number '\<FieldID\>' cannot be found in the '\<TableID\>' table</em></li></ul> The error occurred if Field in Purchase Header or Field in Line Table contained a field number that did not exist. In this situation, Field in Purchase Header or Field in Line Table was showing a blank value. <br><br> Now, the field ID is shown when Field in Purchase Header or Field in Line Table contains a field number that does not exist. |34615|
| Documents and Templates|When recognising fields from the Document Journal, the following error occurred in some situations: <ul><li>The length of the string is &lt;string lenght&gt;, but cannot exceed 20 characters. Value: &lt;<span>string</span>&gt; </li> </ul> |34694|
| Documents and Templates|To limit the number of external calls when showing the scanned images on the Document Journal, we now only check for HTML files on a document if the file type is XML. |34713|
| Documents and Templates|When opening the standard Payment Journal. The following error occurred in some situations: <ul><li><span><em>The Document already exists. I</em></span><em>dentification fields and values:&nbsp;</em><em>No.=&lt;No.&gt;</em> </li> </ul> |38557|
| Document Approval|A wrong advanced approval group could be used if the purchase header filters contained the range operator &quot;..&quot;. |30591|
| Document Approval|The advanced approval groups link was wrongly opening the Approval Sharing page instead of the Advanced Approval Groups page.<br> |30908|
| Document Approval|Now approvers can see their own documents in the Document Archive Search (page 6085792) even when the Continia Web Approval Portal is not in use.<br> |32367|
| Document Approval|When importing the configuration file, header and line dimensions on the&nbsp;<span>Document Capture Setup-&gt; Continia Web Approval card was populated wrongly with dimension value from a Cronus company.</span> |32854|
| Document Approval|<span>When assigning users to an approval flow immediately after creating the approval flow and without leaving the line and using drilldown in No. of Approvers, the Approval Amount Limit field was not editable.</span><br>  |34793|
| Document Approval|<span>When approving an invoice under the following conditions</span> <ul><li><span>as a <span>4-eye amount approver (when &quot;4-eyes Approval&quot; was equal to &quot;Required - both with full amounts limits&quot; in Document Capture Setup)</span></span> </li><li><span>using approval sharing and using the&nbsp;<span>owner's approval permissions (the user did not have authority to approve the amount on the invoice using their own rights</span></span> </li> </ul> the following error occurred:</span> <ul><li><span><em>This invoice requires 4-eyes approval of the full amount. You must approve and forward it to a second approver who can approve the full amount.</em></span> </li> </ul> |38465|
| General Application|When deleting a Continia User Setup record, the related record from the standard User Setup table was also deleted if the standard Business Central fields not shown on the <span>Continia User Setup page were empty. <br><br> The record from the standard User Setup table</span>&nbsp;is now only deleted if fields added by extensions also are empty. |28070|
| General Application|When using the Force Register function on a document where the GL Account No. had been specified, the registered invoice had no lines. |30224|
| General Application|<span>When uploading a file&nbsp;<span>using drag and drop, a 0 kb file was created if the&nbsp;<span lang=DE>Max Upload Size of the service tier configured under Client Services was exceeded.</span></span></span> <span>Users are now getting the following error instead when adding a file using drag and drop if the file size is too large.<br><ul><li><span><em>The file that you are trying to use is too large.</em></span> </li> </ul></span> |30900|
| General Application|<span>The &quot;Document Search&quot; function returned different results when searching for more than one word and when changing the order of the words. The search has been corrected, and the process now works as an AND search in all scenarios when searching for more than one word.</span> |31025|
| General Application|The wrong translation was used when registering a sales document if the number field was blank. The code has now been aligned with the corresponding code for purchase documents. |31296|
| General Application|<span>When using Business Central online, the&nbsp;</span><span>Document Capture Activities part is only visible if Document Capture is activated.</span> |32014|
| General Application|When accessing the template field card, the fields Type and Code are now only visible when creating a new template. <br> |32265|
| General Application|The notification email sent concerning &quot;Documents assigned to me&quot; now includes a link to the relevant page in BC. |32425|
| General Application|The Contracts menu point was shown in the Continia Web Approval Portal even though the Contracts and Subscriptions feature was not activated.&nbsp;&nbsp; |32616|
| General Application|<span>Captions have been updated.</span> |34370|
| General Application| When clicking on the document line on the Payment Journal page, the following error occurred in some situations:<ul><li><em>The Document does not exist. Identification fields and values: No.=''</em></li></ul> |34701|
| General Application|When renaming a Salesperson/Purchaser to a value with more than 10 characters, the following error occurred: <ul><li><em>Cannot write the value &lt;Code&gt; to the Purchaser Code in table CDC Purch. Cont. Hdr. Arch. because the value is either too long or the content is invalid.</em> </li> </ul> |34797|
| General Application|When opening the Approvers list from the Approval Flows page, the following error occurred even when the length of the Approval Flow Code was less than or equal to 10 characters. <ul><li><em>The length of the string is 12, but it must be less than or equal to 10 characters. Value: '&lt;Approval Flow Code&gt;'</em> </li> </ul> |38475|
| Platform and Technology|<span>When trying to upgrade to Document Capture 9.01 (app version) in a Spanish localization, the following error occurred:<br><ul><li><span><em>The upgrade of an extension in the context of the company &lt;Companyname&gt; has failed.</em></span> </li> </ul>The error only occurred when&nbsp;<span>using Azure Blob Storage in a company containing documents where the company was not activated,</span> </span> |34398|
| Platform and Technology|In some situations, shortcut keys did not work in the Document Journal and the Document Card. <br> This occurred when the page's&nbsp;<span>control add-ins (Capture UI and Document Header Fields) had focus.</span> |34648|
| Purchase Documents|Document Capture fields were shown on page 51 even when Document Capture was not activated. |32441|
| Purchase Documents|When registering a DC document using the option &quot;Match and Update Order&quot;, the resulting posted purchase invoice/credit memo did not show the correct number of attached documents. |32754|
| Purchase Documents|Unit of Measure Code was sometimes set to [Blank] on the purchase invoice line after registering a document. This resulted in the f<span>ollowing error during purchase invoice posting:</span> <ul><li><em>The Resource Unit of Measure does not exist. Identification fields and values: Resource No.=&lt;Resource No.&gt;,Code=''</em><br> </li> </ul> |35157|

## Document Capture 2022 R1 Service Pack 1, hotfix 6
*Released: May 17, 2022*  
*App version: 9.1.0.6*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application | When renaming a Salesperson/Purchaser to a value with more than 10 characters, the following error occurred: <ul><li><em>Cannot write the value \<Code\> to the Purchaser Code in table CDC Purch. Cont. Hdr. Arch. because the value is either too long or the content is invalid.</em></li></ul> | 34797 |

## Document Capture 2022 R1 Service Pack 1, hotfix 5
*Released: May 11, 2022*  
*App version: 9.1.0.5*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Documents and Templates | When using a different Amount- and Invoice rounding precision (defined in General Ledger Setup) and recognizing lines, the system could in some case present the following error: <ul><li><em>The sum of all lines ([Sum of Line Amounts]) does not reconcile to the total amount ([Amount Ex. VAT]).</em></li></ul> | 34575 |

## Document Capture 2022 R1 Service Pack 1, hotfix 4
*Released: May 5, 2022*  
*App version: 9.1.0.4*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| General Application | When opening Payment Journal, the following error occurred: <ul><li><em>The Document Capture Setup does not exist. Identification fields and values: Primary Key=''</em></li></ul> | 34590 |

## Document Capture 2022 R1 Service Pack 1, hotfix 3
*Released: May 2, 2022*  
*App version: 9.1.0.3*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | When trying to upgrade to Document Capture 9.01 app version in a Spanish localization, the following error occurred: <ul><li><em>The upgrade of an extension in the context of the company \<Companyname\> has failed.</em></li></ul> The error only occurred when using Azure Blob Storage, in a company containing documents where the company was not activated. | 34398 |


## Document Capture 2022 R1 Service Pack 1, hotfix 2
*Released: April 8, 2022*  
*App version: 9.1.0.2*  
*FOB version: 9.01.02*  

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Platform and Technology | The Continia Web Approval Portal has been updated to version 1.24.1 | 32639 |


## Document Capture 2022 R1 Service Pack 1, hotfix 1
*Released: April 1, 2022*  
*App version: 9.1.0.1*  

Only released in Business Central online.

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Documents and Templates | When trying to register a document, where the field Document Type had not been added to the document template, the following error occurred: <ul><li><em>"The Template Field does not exist. Identification fields and values: Template No.=\<template no\>,Type='Header',Code='DOCTYPE'"</em></li></ul> |

## Document Capture 2022 R1 Service Pack 1
*Released: April 1, 2022*  
*App version: 9.1.0.0*  
*FOB version: 9.01.00*  

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|<span>The Portuguese localization is now supported.</span><br><br><span>Continia Core and Continia Delivery Network Object captions have not been translated in this release.</span> <span>The translations will be included in a future service pack.</span> <span><br></span>   |28562|
| Country and Regional|<span>The Polish configuration file has now been updated.<span>&nbsp;</span></span><span>Category names and captions have been updated to Polish in the new version</span><span>.</span> |32412|
| Documents and Templates|The template field Prices Incl. VAT field is now hidden on master templates.&nbsp; |14624|
| Documents and Templates|The &quot;Change Sign&quot; field has been added to the Template Field Card page.<br> |30348|
| Documents and Templates|<span>For the Belgian and French localizations, the configuration file has been updated.&nbsp;</span>Caption Mandatory has been set to true for most p<span>urchase header&nbsp;</span><span>template fields.</span> <br><br> The following purchase header template fields still have Caption Mandatory = False: <ol><li><span>DOCTYPE -&nbsp;[I]nvoice / [C]r. Memo</span> </li><li><span>GLACCOUNTNO -&nbsp;G/L Account No.</span> </li><li><span>CURRCODE -&nbsp;Currency Code</span> </li><li><span>POSTINGDESC -&nbsp;Posting Description</span> </li> </ol> |31925|
| General Application|The sorting of the comments on the Document Card was not the same as the sorting on the Document List:&nbsp;This has been changed, so the comments on the Document Card are now sorted the same way as on the Document List.&nbsp;<br> |14670|
| General Application|Added the Navigate/Find Entries button on the Document Search page.&nbsp; |30447|
| Platform and Technology|<span><span>On the Continia Web Portal List and </span><span>Continia Web Portal Card, a new action, Create Web Portal Setup has been added. When running the function, the Windows Web Service URL and Database Web Service URL<span>&nbsp;is</span></span><span>&nbsp;</span><span>automatically filled in with suggested values based on the active Dynamics 365 Business Central service tier connection (available for NAV 2013 R2 and newer versions).</span></span>  |31796|
| Platform and Technology| Events have been added to the solution. For details, please see <a href="/continia-document-capture/development-and-administration/development-and-customization/event-publishers/event-publishers-900">Event Publishers for Document Capture 2022 R1 (9.00)</a> |32025|
| Platform and Technology|The Continia Web Approval Portal has been updated to version 1.24.0.<br> |32311|
| Platform and Technology| With Document Capture 2022 R1 service pack 1 (9.01), we have released Document Capture for Microsoft Dynamics 365 Business Central 2022 release wave 1 (BC20). <br><br> Document Capture 2022 R1 service pack 1 (9.01) in Business Central online will not be available for Microsoft Dynamics 365 Business Central 2021 release wave 2 (BC19). You will only be able to use Document Capture 2022 R1 service pack 1 (9.01) in Business Central online when you have upgraded to Microsoft Dynamics 365 Business Central 2022 release wave 1 (BC20). |32415|
| Purchase Documents|When validating the bank account information, we now check against: <ul><li>IBAN </li><li>Bank Branch + Bank Account No. </li><li><span>Bank Account No. + Bank Branch</span> </li> </ul> |28278|

### Bug fixes

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|<span><span>An error comment is created when the same external document number is used more than once. However, in the&nbsp;</span><span>Spanish localization, Business Central can be configured to allow the same&nbsp;<span>external document number to be used several times by populating the&nbsp;<span>&quot;Same Ext. Doc. No. in Diff. FY.&quot; field in&nbsp;<span>Purchases &amp; Payables<span>&nbsp;Setup.&nbsp;</span></span></span></span></span><span>This is now supported in the&nbsp;<span>Spanish localization.</span></span></span> |31437|
| Country and Regional|<span>When we released DC9.00, we forgot to write the following in the changelog:</span><br> <br> In the<span><span><span><span>&nbsp;</span>United States, captions on many screens wrongly displayed VAT instead of TAX. We have created a new app,&nbsp;<span>Document Capture (US), to correct this issue. This app must be installed to show the correct captions.</span></span></span></span> <br><br> <span><b>The following applies when using Document Capture in Business Central online.</b><br></span> <span>When installing Document Capture for the first time in the&nbsp;</span><span>United States,&nbsp;the new&nbsp;Document Capture (US) app&nbsp;must be installed to get the correct captions.</span><br> <span><span><span><br></span></span></span> <span><span><span><span>If Document Capture is already being used, the new&nbsp;</span><span>Document Capture (US) app<span>&nbsp;</span><span>must also be installed from AppSource to get the correct captions.</span></span></span></span></span> <span><span><span><span><span><br><br></span></span></span></span></span> <span><span><span><span><span><b>The following applies when using Document Capture on-premises.</b><br></span></span></span></span></span> <span><span><span><span><span>Install or upgrade Document Capture as you normally do, and the correct app will be installed.</span></span></span></span></span> <br> |31856|
| Country and Regional|Many&nbsp;ambiguous translations have been corrected for the Finnish localization. |32277|
| Documents and Templates|<span>When drilling down into &quot;Pending OCR&quot; or &quot;Ready to import&quot; on the <span>Document Capture Role Center</span>, the document list is now shown when there <span>only<span>&nbsp;</span></span>are documents in one category.</span> |23487|
| Documents and Templates|<span>The validation of the FIK number was not correct. For example, when the FIK number started with 71, 73, or 75, the system wrongly only accepted vendor numbers beginning with 7, 8, or 9.</span> |31615|
| Documents and Templates|Captioned changed for &quot;Doc Date&quot; to &quot;Doc. Date&quot; in all master template for English localizations. The master template is located under Department -&gt; Document Capture -&gt; Document Journal -&gt; Templates -&gt; Master template (view) |31718|
| Documents and Templates|<span>The &quot;First Table Line Has Caption&quot; field has been moved into the Line Recognition group on the Template Card page.&nbsp;</span> |32056|
| Documents and Templates|<span>While registering a sales document and if there was a difference between the imported and assigned amounts, the created sales document was not rolled back and the <span>DC Document&nbsp;</span><span>status stayed</span></span><span><span>&nbsp;open.</span></span> |32064|
| General Application|If the Document Capture Setup page was opened <span>in Business Central cloud&nbsp;</span>before the setup wizard had been run, the Document Storage Type field was set to File Storage, and Cloud OCR was not activated. |23951|
| General Application|When identifying a template with more than two search texts, the &quot;Identified By&quot; in the Document Journal field was blank. |25471|
| General Application|The Attachment action has been disabled when no documents are shown on the Document Journal page. |25502|
| General Application|When having activated only the Essential module, the following error occurred when recognizing lines on a template: <ul><li><em>This function requires the following module to be activated: Continia Document Capture, Advanced Capture.</em> </li> </ul>|29496|
| General Application|<span>On the Document Search page, tooltips have been updated, and actions have been moved and renamed.</span><br> |30497|
| General Application|<span>When filtering on the <span>Get Order Lines</span> page (opened from the Invoice page), the following error occurred if no purchase lines existed within the applied filter:</span><br> <ul><li><em>Purchase Line: There is no Purchase Line within the filter. <br><br> Filters: Document Type: &lt;<em>Document Type&gt;</em>, Document No.: &lt;Document No.&gt;, Outstanding Quantity: &lt;<em>Outstanding Quantity</em>&gt;, Pay-to Vendor No.: &lt;<em>Pay-to Vendor No.&gt;</em>, Currency Code: &lt;<em>Currency Code&gt;</em></li></ul> |30662|
| General Application|The Storage Migration Wizard has been renamed to&nbsp;<span>Storage Migration&nbsp;</span>Assisted Setup Guide. |31664|
| General Application|The following error occurred when a document was reopened, or a purchase line was deleted: <ul><li><em>You do not have the following permissions on CodeUnit CDC Relation Mgt.: Execute.</em> </li> </ul> |31766|
| General Application|<span>Emails with multiple attachments were deleted when deleting a DC document from the email and using Azure Blob Storage.<br> </span>|31828|
| General Application|<span>The File Factbox on the Payment Journal did not show all relevant documents in some situations.</span><br> |31877|
| Platform and Technology|<span>When changing email protocol to EWS on the Document Category Card, the related EWS fields were not shown. You had to reopen the page to get the fields shown.</span><br> |31991|

## Document Capture 2022 R1
*Released: March 1, 2022*  
*App version: 9.0.0.0*  
*FOB version: 9.00.00*  

### New or changed functionality (missed)

The below new functionality in Document Capture 2022 R1 (9.00) was originally not included in the changelog for Document Capture 2022 R1.

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|<span>The Faroe Islands localization is now supported in Business Central online.<br></span>|27920|
| Country and Regional|The Greenland localization is now supported in Business Central online.<br>|28192|
| Documents and Templates|On page 6085600&nbsp;- CDC Document List With Image, the following actions are now hidden if no XML documents exist or when using Document Capture without access to the&nbsp;<span>XML import module</span>. <ul><li>Styled XML </li><li>XML Viewer </li><li>XML File </li> </ul> |27110|
| Documents and Templates|Added support for the ZUGFeRD Version 1 format.&nbsp; |29535|
| Documents and Templates|The PEPPOL3 XML template now supports the Australia-New Zealand extension of the PEPPOL format -&nbsp;<span>A-NZ</span> PEPPOL. |29903|
| Documents and Templates|On the split and merge page, it is now possible to show the original filename of the document shown. The field is hidden by <span>default</span>. |29993|
| Document Approval|<span>Added support for Type = <span>Resource<span>&nbsp;</span></span>on purchase lines in the Continia Web Approval Portal.&nbsp;</span><span>This is supported under the following conditions:</span><ul><li><span><span>Business Central 2020 wave 1</span>&nbsp;(BC16) or newer versions, and</span></li><li><span>Document Capture 7.00 SP3 or newer versions, and</span></li><li><span>Continia Web Approval Portal version 1.19.0 or newer versions</span></li></ul>|24827|
| Document Approval|We have optimized the performance when showing approvers on the Purchase Invoice and Purchase Credit Memo pages. |28967|
| General Application|When exporting vendor document attachments using the Export Attachments report, all attachment types&nbsp;<span>within the filters applied</span>&nbsp;were exported. It is now possible to limit the export to PDF, XML, or all file types. When XML is selected, the styled HTML file is also included in the export.<span></span> |27456|
| General Application|In Business Central 2021 release wave 2 (BC19), the &quot;Item Reference No.&quot; field is now shown on the &quot;CDC Purch. Inv. Archive Subf.&quot; and &quot;CDC Purch Cr. Memo Arc Subform&quot; pages instead of the &quot;Cross-Reference No.&quot; field.|27783|
| General Application| <p><span>A new page showing files related to payments has been developed. The page can be added to the Payment Journal and will show the related posted purchase invoices.</span> </p><p> </p><p><span>The new page is Page 6085663 - CDC Purchase Journal File FB.</span> </p><p> </p><p><span>When adding the page as a factbox, the following filters must be set.</span> </p><ul><li><em><span>Find Documents Using=CONST(Document Reference)</span></em> </li><li><em><span>Source Table No. Filter=FILTER(81)</span></em> </li><li><em><span>Source Subtype Filter=FIELD(Applies-to Doc. Type)</span></em> </li><li><em><span>Source No. Filter=FIELD(Applies-to Doc. No.)</span></em> </li><li><em><span>User ID=FIELD(Applies-to ID)</span></em> </li> </ul> |28130|
| General Application|To optimize the performance when running Business Central, we are now caching if a user is a Team Member. |29227|
| General Application|<span></span>We have optimized the performance in CDC Log Mgt. when determining if records should be checked for modifications. &nbsp;<span></span> |29229|
| General Application|When registering a sales order, the following error occurred in some situations: <ul><li><span>The Sales Line already exists.<br>Identification fields and values:<br>Document Type=&lt;<span>Document Type</span>&gt;,Document No.=&lt;<span>Document No.</span>&gt;,Line No.=<span>&lt;<span>Line No.</span>&gt;</span></span> </li> </ul>  |29768|
| Platform and Technology|We have updated the ABBYY Installer to contain a newer version of ABBYY (12.5.6.12).<br>The full changelog of the ABBYY version can be read here:<a href="https://www.abbyy.com/finereader-engine-downloads/windows/">https://www.abbyy.com/finereader-engine-downloads/windows/</a><br><br>As we have only changed the ABBYY component, we have not changed the version number of the installed Continia Document Capture for NAV - Service (x64). the version number is still 8.00.|27260|
| Platform and Technology|When getting the error message about missing server components, the message has been changed. The following has been added to the error message: &quot;Remember to restart the service tier after installing the components.&quot;&nbsp; <ul><li><em>Server components for Document Capture are not installed.<br></em><em>Server components should be placed in the folder:<br></em><em><br>&lt;add-in path&gt;<br></em><em><br>Remember to restart the service tier after installing the components.</em> </li> </ul>  |27887|
| Platform and Technology|Procedure BreakDownPaymentId in Codeunit 6085738 &quot;CDC Is Valid Payment-Id (DK)&quot; is now external. |28578|
| Platform and Technology|The following Event Publisher in Codeunit&nbsp;6085576 CDC Capture Management is obsolete as the Word parameter is not a VAR parameter: <ul><li><span>OnBeforeUpdateFieldValue</span> </li> </ul>  This will be replaced by the following Event Publisher: <ul><li><span>OnBeforeUpdateFieldValueCapture</span> </li> </ul> |29420|

### New or changed functionality

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Country and Regional|	The Finnish localization is now supported. |28563|
| Country and Regional|<span>The<span>&nbsp;Polish&nbsp;</span></span><span>localization is now supported.</span> <span>Unfortunately, it was not possible to complete the Polish configuration file in time for the release, Therefore, the&nbsp;<span>configuration file</span>&nbsp;i<span>n the <span>Polish<span>&nbsp;</span></span>product package is a copy of the W1 configuration file. When the Polish configuration file is ready, it will be available for download from online when running the Document Capture Assisted Setup Guide.</span></span> |28564|
| Documents and Templates|<span>The following document error message</span><ul><li><span><em>No. &lt;No.&gt; on line &lt;Line No.&gt; must be translated.</em></span> </li> </ul> <span>has been changed to</span> <ul><li><span><em>Line &lt;Line No.&gt; must be translated. Please add a translation of No. &lt;No.&gt; or Description &lt;Description&gt;</em><span></span></span> </li> </ul><span>When an XML document line contained a unit of measure code that could not be translated into a unit of measure code configured in Business Central, the line was not recognized. This has been changed so that the line is now recognized, and the following document error message is created:</span> <ul><li><em>Unit of Measure is not correct on line &lt;Line No.&gt;.</em> </li> </ul>  <p> </p>  |14771|
| Documents and Templates|<p><span lang=EN-GB></span> </p><span>The registration of purchase documents has been extended to include registration directly to a general journal. The capture of both total amounts and line details are supported.<br></span><br> The functionality is enabled on a template level thus enabling the possibility to register some vendors as documents and others directly to a general journal.<br> <br> <span>Registration with match against receipts or orders is not supported.</span><br><p><span lang=EN-GB></span> </p>|22684|
| Documents and Templates|The following 13 messages are now configurable: <ul><li><span>[Date 1]  greater than today on credit note.</span> </li><li>Different date formats used on fields. </li><li>Due Date = Invoice Date </li><li>The XML Document contains [discounts and charges] elements that are not created as Fields for this Template. Please use Add Template Field to add them. </li><li>You must specify G/L Account No. when Fill-out LCY is activated in Document Capture Setup. </li><li>You must specify G/L Account No. </li><li>No valid exchange rate exists for currency '[Currency Code 1]' on the [Date 1]. </li><li>Prices Including VAT on Order [Order No. 1] is Yes. The value must equal the setting on template [Template No. 1], which is No. </li><li>Blocked cannot be 'All' on Vendor [Vendor 1] </li><li>[Our Order No.] = '[Order No.]' exists but Warehouse Receive is required. </li><li>Order No. = '&lt;Order No.&gt;' exists but no open receipts exists (Warehouse Receive is required). </li><li>[Our Order No.] = '[Order No.]' exists but is fully received and invoiced. </li><li>[Our Order No.] = '[Order No.]' exists but is fully received. </li> </ul> |27522|
| Documents and Templates|During registration of a purchase document, a series of dialogs have been consolidated into a single page that allows the user to select the correct purchaser if none could be determined based on information from the document. |28590|
| Document Approval|<span>Additional functionality has been built into the approval flows.<br></span>Two new fields, “Selection Method” on the approval flow and “Approval Amount Limit” on the individual approvers configured on the approval flow, have been added.<br> Depending on the configuration of these fields, different subsets of the approvers will be used when approving a document with an approval flow code applied.<br> <br> The new option field “Selection Method” on the approval flow configures as follows:<br> <ul><li>“All”: An approval entry for each approver in the flow is created. This is the default value and equals the functionality found in previous versions of Document Capture. </li><li><span>“First Qualified”: Will select the first, single approver of the flow that has a value in “Approval Amount Limit” that equals or exceeds the total value of the purchase document submitted for approval.</span><br> </li><li><span>“All to first qualified”: Will select all approvers of the flow starting with the approver having the lowest value in “Approval Amount Limit” up to, and including, the first qualified approver (see definition of qualified approver in the selection method “First Qualified”).</span><br> </li><li><span>“Initial and first qualified”: Will select the approver with the lowest value in “Approval Amount Limit” and then the first qualified approver.</span><br> </li> </ul>  |14562|
| Document Approval|<span><span>On the Purchase Approval Entries page, y</span>ou now have direct access to the attachments for the purchase document.</span> |21591|
| Document Approval|A new boolean field, &quot;<span>Enable Standard Notification</span>&quot;, has been added to the Document Capture Setup/Purchase Approval page. The field controls the Business Central standard workflow notifications. This feature is available in&nbsp;<span>Business Central 2021 release wave 2 (BC19) and newer versions.</span> <span><br></span> <span><span>The new field &quot;<span>Enable Standard Notification</span>&quot; in Document Capture Setup<span>/Purchase Approval</span> works as follows:</span></span><b>&nbsp;</b><br><ul><li><span>False: A</span><span>ll standard notifications for workflow codes starting with &quot;DC-&quot; are suppressed.&nbsp;<span>This is the default value. As a result, only Document Capture email notifications are sent to the approvers.</span></span><br> </li><li><span>True: Standard notifications&nbsp;</span><span>for workflow codes starting with &quot;DC-&quot; are enabled. This&nbsp;<span>equals the functionality found in previous versions of Document Capture, where standard Business Central workflow notifications are sent to the approvers.</span></span><br> </li> </ul> |22564|
| Document Approval|<span>A threshold value on 4-eyes approval has been implemented. <span>If a purchase document has a total value below the specified value, then 4-eye approval is suspended on that document.&nbsp;</span>The value is specified in Document Capture Setup -&gt; Purchase Approval in the new field &quot;4-eye Threshold Amount (LCY)&quot;.</span><br> |22682|
| Document Approval|On Advanced Approval Groups, the option caption <span>&quot;</span><span>Invoice Full Amount&quot;<span>&nbsp;</span></span>for the <span>&quot;Four Eyes Approval&quot; field&nbsp;</span>has been changed <span>to &quot;</span><span>Invoice Full Amount and Dimension&quot;.</span> |27348|
| General Application|The page with Continia Web Approval Portal settings has been removed from the Document Capture Setup wizard.&nbsp; |14786|
| General Application|<span>In multiple captions, we have replaced &quot;NAV&quot; with &quot;BC&quot;.</span><br> |14793|
| General Application|When exporting the configuration using the Document Capture Setup Wizard, it is now possible to include the purchase reason codes.<br> |17682|
| General Application|<span><span>In the app-based versions (BC15, BC16, BC17, BC18, and BC19), access to the document files has been added to the following pages:</span><br></span> <span><span><br></span></span> <span><span><span>Through the page field &quot;Attachments&quot;<br></span><ul><li>Sales Credit Memo (card) </li><li>Sales Order (card) </li><li>Posted Sales Invoice (card) </li><li>Posted Sales Credit Memo (card) </li> </ul> <br> Through the factbox &quot;Documents&quot; (hidden by default)<br> <ul><li>Jobs (list) </li><li>Job (card) </li><li>Sales Credit Memo (list) </li><li>Sales Orders (list) </li><li>Posted Sales Invoices (list) </li><li>Posted Sales Shipment (card) </li><li>Posted Sales Shipments (list) </li><li><span><span><span>Posted Sales Credit Memos (list)</span></span></span> </li> </ul> </span></span> |19715|
| General Application|<span>In Business Central 2020 release wave 2 (BC17) and newer versions, Navigate was renamed to Find Entries. N<span>avigate in Document Capture is now renamed to Find Entries in <span>Business Central<span>&nbsp;</span></span><span>2020 release wave 2 (BC17)</span><span><span>&nbsp;</span>and newer versions</span>.</span></span><br> |21584|
| General Application|A new storage migration wizard has been developed. The wizard is used to move files from one storage setup to another. |24226|
| General Application|A new option field&nbsp;<span>&quot;Purchase File Display Name&quot;<span>&nbsp;</span></span>has been added to the Document Capture Setup page. The field controls how the document file name is displayed in the Document Capture drag and drop FactBox on posted documents. <br> Available options are: <ul><li>Posted Document No. </li><li>Posted Document No. + Vendor Document No. </li><li>Unposted Document No. </li> </ul> |26739|
| General Application|<span>Teaching tips have been added to the following pages.</span> <span><ul><li><span>Document Category</span> </li><li>Template Card </li><li>Purchase Line Translations </li><li>Posting Setup (Accounts for Amounts) </li><li>Standard Amount Distribution Code </li><li>Document Card </li><li>Invoice Matching </li><li>Split and Merge Documents </li><li><span>Purchase Allocation</span> </li> </ul></span> |27495|
| General Application|A link to the Continia Company Setup page has been added to the Document Capture Setup page. |29017|
| Platform and Technology|<span><b>With the release of Document Capture 2022 R1 (9.00), we only support Business Central 2019 Spring (BC14) and newer versions.</b><br></span><br> <span>Even though we are not supporting Business Central October 2018 (BC13) and older versions in Document Capture 2022 R1 (9.00), we are still supporting the old NAV/Business Central versions in future service packs released for Document Capture 2021 R2 (8.00).</span><br> |27541|
| Platform and Technology|<span>The Continia Web Approval Portal has been updated to version 1.23.0.</span><br> |31352|
| Purchase Documents|<span>In the app-based versions (BC15, BC16, BC17, BC18, and BC19), the &quot;Document Files factbox&quot; has been added to the following pages.&nbsp;</span> <ul><li>Posted Purchase Invoices </li><li>Posted Purchase Credit Memos </li> </ul>  <span>The factbox is shown by default.</span><br> |26762|

### Bug fixes
All relevant bugfixes released in service pack 1 to service pack 2, hotfix 3 for Document Capture 2021 R2 (8.00), service pack 1 to 3 for Document Capture 2021 R1 (7.00), and service pack 1 to 4 for Document Capture 2020 R2 (6.50) are also included in Document Capture 2022 R1 (9.00). The description of these bugfixes is not repeated on this page.

<br>

| <span style="white-space: nowrap;">Functional area</span> | Description | ID |
| --- | --- |  --- |
| Documents and Templates|It is now only possible to have one default vendor template.&nbsp;<span>Setting a vendor template to default will remove the default setting from other vendor templates.</span> |29961|
| Documents and Templates|Fixed an issue where it was not possible to recognise any fields on a document after performing split and merge. |30352|
| Documents and Templates|The ID template for PDF invoices (EINKAUF-ID) in the CH localization configuration file has been updated with rules to better identify &quot;VAT Registration No.&quot; on imported invoices. |30508|
| Documents and Templates|The &quot;Assign To User&quot; action on the &quot;Assigned to me&quot; page was not populated with all available users in specific configurations. |30919|
| Documents and Templates|Multiple look-up's in rules could lead to unintentional modification of the rules on the master template. |30934|
| Documents and Templates|Added additional identification rules for the XRECHNUNG-ID XML identification template to support the latest version of the XRechnung format.&nbsp;&nbsp; |31339|
| Documents and Templates|When capturing an XML document with an embedded file where the base64 text included spaces, the attachment file was not created. PEPPOL URI attachments were not saved as an attachment. The new template field URI Attachments will now handle these types of attachments.&nbsp;&nbsp; |31458|
| Documents and Templates|When running Document Capture in Busniess Central Online and using the functions Split and Merge, Rotate and Move Up/Down you sometimes recive the error: <span><br></span><ul><li><em>C:\<span>azagent\</span><span>A1</span><span>\_work</span><span>\27</span><span>\s</span><span>\Continia.Common.Imaging</span><span>\PdfTool.cs..ctor - LoadFromStream caused an error. Status: GenericError, Page: 0.</span></em> </li> </ul>  |31514|
| Document Approval|In some situations, the company name was not encoded correctly in the link to the Business Central client when sending out approval e-mails. |30240|
| Document Approval|When a user with&nbsp;<span>NAV Login Type &quot;No NAV Login&quot; or Database&nbsp;</span>tried to log in on the Continia Web Approval Portal, the following error occurred if the user had been exported without WebService Key: <ul><li><em>Web Service Access Key must not be empty for User &lt;User ID&gt; when NAV Login Type is Database for Continia User &lt;User ID&gt;.</em> </li> </ul><span>Now, the following error is shown when such a user is exported to the Continia Web Approval Portal:</span>  <ul><li><span><em>Web Service Access Key must not be empty for User &lt;User ID&gt; when NAV Login Type is Database.</em></span> </li> </ul> |30509|
| Document Approval|<span>We have fixed an issue where the number of documents was not correct in the Approval Portal.</span><br> |31573|
| General Application|The&nbsp;CDC-APPROVE permission set had execute permission to all tables, pages, and codeunits. These permissions have now been removed as the DC permission set must be used together with the standard permission sets, and these already have the execute permissions. |29308|
| General Application|The icon used for the Create Web Services function on Continia Web Portal List has been changed to the icon used for the same function on other pages in Document Capture. |29400|
| Order & Receipt Matching|<span>When matching against a receipt or return shipments line for a G/L Account or Charge Item, the following error occurred in NAV3.70 to BC14</span><span>:</span> <ul><li><em>Quantity per unit of measure must be defined</em> </li> </ul>  |28944|
| Order & Receipt Matching|When handling documents with an order number filter containing more than 20 characters, the following error occurred: <ul><li><span><em>The length of the string is &lt;Order number filter length&gt;, but it must be less than or equal to 20 characters. Value: &lt;Ordernumber Filter<em>&gt;</em></em></span> </li> </ul> <br> |30236|
| Order & Receipt Matching|<span>When capturing lines and matching against order numbers with the matching option &quot;Always&quot;, no filter would be applied </span><span>on the order number&nbsp;</span><span>if the captured order no was blank.</span><br> |30695|
| Platform and Technology|Configuring line capture was not possible <span>in BC15 and BC16<span>&nbsp;</span></span>as the capture add-an did not respond to mouse clicks.&nbsp; |30645|
| Platform and Technology|The Handle variable was not reset when subscribing to events in the function CaptureDocument in the &quot;CDC Capture Engine&quot; codeunit. If Handled was set to true in one of the <span>preceding<span>&nbsp;events, the subsequent&nbsp;<span><span>events were not executed.</span></span></span></span> |30731|
