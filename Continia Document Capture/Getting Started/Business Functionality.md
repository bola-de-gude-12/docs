---
title: Business functionality in Document Capture
date: 14-07-2025
id: DC-49
lang: en
description: >-
  Detailed information on the functionality included in the latest version of
  Document Capture.
---

# Business functionality

As an end-to-end solution for importing, processing, registering, approving, and archiving PDF or electronic invoices and other business documents, Continia Document Capture offers considerable benefits to a wide range of businesses. It can streamline processes and reduce data-entry costs for companies in sectors as diverse as finance, healthcare, manufacturing, transportation, and so on.

Built on a modular basis, Document Capture can be customized to suit your particular business needs. Each of the modules that it’s divided into represents an area of functionality. You can choose to add any modules you want using the initial setup guide, which is accessed straight from your Role Center in Microsoft Dynamics 365 Business Central.

> \[!IMPORTANT] Not all features are available in all versions of Document Capture. To see features available per version of Document Capture, refer to [Comparison of features by Document Capture version](../../Continia%20Document%20Capture/Getting%20Started/@DC-46/).

Below is a description of each of the modules, along with an overview of their respective features.

## Essential

The mandatory Essential module allows you to import purchase invoices and credit memos into Business Central. The imported files can be scanned documents, PDF files processed using optical character recognition (OCR), or XML files – which you can import and process in various ways and formats, such as Peppol and XRechnung, via the Continia Delivery Network (CDN).

The module enables you to recognize document header fields using OCR, and to map the recognized data to the actual location of the textual content in the documents. This one-time mapping can then be used to automate the process for all future documents received from the same vendor.

> \[!NOTE] The Essential module only includes data capture at the header level, and only for purchase invoices and credit memos. To recognize fields at the line level and process other types of business documents, upgrade to the [Advanced Capture module](../../continia-document-capture/getting-started/business-functionality/#advanced-capture).

With the Essential module, you get access to the following key features:

| Feature                                                                                                                                                                                                                                                         |     Included    |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------: |
| View and verify images inside Business Central                                                                                                                                                                                                                  | \{{checkmark\}} |
| Drag and drop attachments from and to any record                                                                                                                                                                                                                | \{{checkmark\}} |
| Recognize and process purchase invoices and credit memos                                                                                                                                                                                                        | \{{checkmark\}} |
| Add any custom field to be recognized, and dynamically transfer recognized values to purchase documents                                                                                                                                                         | \{{checkmark\}} |
| Recognize multiple amounts (e.g.: total cost amount plus total freight amount)                                                                                                                                                                                  | \{{checkmark\}} |
| Recognize multiple VAT/tax amounts and assign these to different G/L accounts                                                                                                                                                                                   | \{{checkmark\}} |
| Use fixed values for any field                                                                                                                                                                                                                                  | \{{checkmark\}} |
| Easily change the area of recognition on scanned documents                                                                                                                                                                                                      | \{{checkmark\}} |
| Configure rules for fields, ensuring that the correct values are recognized (e.g.: specific format, positive amount only, etc.)                                                                                                                                 | \{{checkmark\}} |
| Vendor-specific settings and templates for recognition and validation                                                                                                                                                                                           | \{{checkmark\}} |
| Caption suggestions for master template fields, including the ability to ignore such suggestions                                                                                                                                                                | \{{checkmark\}} |
| Assisted setup guide for the creation of template fields                                                                                                                                                                                                        | \{{checkmark\}} |
| Configure whether amounts are including or excluding VAT/tax                                                                                                                                                                                                    | \{{checkmark\}} |
| Manual splitting of PDF files inside Business Central (e.g.: multiple invoices in one PDF file)                                                                                                                                                                 | \{{checkmark\}} |
| Document analysis and capture built directly into Business Central, allowing for app customization                                                                                                                                                              | \{{checkmark\}} |
| Safe digital archive with free-text search capabilities                                                                                                                                                                                                         | \{{checkmark\}} |
| Automated checking of bank accounts, VAT numbers, and phone numbers to avoid fraud                                                                                                                                                                              | \{{checkmark\}} |
| Capture QR codes and extract data within them                                                                                                                                                                                                                   | \{{checkmark\}} |
| Register documents directly to general journal lines, using a vendor, a bank, or a G/L account as the balancing account                                                                                                                                         | \{{checkmark\}} |
| View documents in payment journals                                                                                                                                                                                                                              | \{{checkmark\}} |
| Document viewer availability on the **Vendor Ledger Entries** page                                                                                                                                                                                              | \{{checkmark\}} |
| Amount distribution codes for determining how amounts are allocated to accounts and dimensions when purchase lines are created                                                                                                                                  | \{{checkmark\}} |
| Ability to configure comment types and have documents automatically assigned to specific users in case of errors                                                                                                                                                | \{{checkmark\}} |
| Notification of remaining pages in OCR licenses                                                                                                                                                                                                                 | \{{checkmark\}} |
| Automatic vendor and field recognition when documents are moved to other companies                                                                                                                                                                              | \{{checkmark\}} |
| Automatic deactivation of Continia solutions when companies are copied                                                                                                                                                                                          | \{{checkmark\}} |
| Option to display the original sender email in **Ready to Import** when using Cloud OCR, rather than the address of an intermediary inbox or similar                                                                                                            | \{{checkmark\}} |
| Notifications for admins about open, unregistered documents                                                                                                                                                                                                     | \{{checkmark\}} |
| Support for **WORKDATE** and **TODAY** in template field formulas, enabling you to have specific dates automatically inserted for all documents using the relevant template                                                                                     | \{{checkmark\}} |
| Secure Archive, an archive that automatically and securely stores your digital bookkeeping documents in their original form                                                                                                                                     | \{{checkmark\}} |
| Continia Hub, a central in-app assistance hub designed for convenience and user feedback                                                                                                                                                                        | \{{checkmark\}} |
| Support for the QR-Bill Management app by Microsoft                                                                                                                                                                                                             | \{{checkmark\}} |
| Document control log, providing a central overview of documents requiring special attention due to file checksum issues or post-approval changes                                                                                                                | \{{checkmark\}} |
| Support for multi-entity management (MEM) by Binary Stream Software                                                                                                                                                                                             | \{{checkmark\}} |
| Automated cleanup processes to delete captured words, generated values, and entire records based on document status and age – ensuring GDPR compliance and maintenance of privacy and data integrity                                                            | \{{checkmark\}} |
| Continia eDocuments: proprietary functionality that enables you to manage and exchange eBilling and eOrdering documents (XML) directly from Business Central, send documents automatically, check the eDocument capabilities of customers and vendors, and more | \{{checkmark\}} |
| Continia Delivery Network: a service that integrates with the Peppol eDelivery Network and the NemHandel network, enabling you to send and receive electronic documents in Business Central                                                                     | \{{checkmark\}} |
| Support for invoice discounts and allocation accounts                                                                                                                                                                                                           | \{{checkmark\}} |
| Take payment days into account when calculating due dates in Spain                                                                                                                                                                                              | \{{checkmark\}} |
| Receive warnings regarding invoices that have already been paid and registered via Continia Expense Management                                                                                                                                                  | \{{checkmark\}} |
| Handle payment means in Continia eDocuments                                                                                                                                                                                                                     | \{{checkmark\}} |

## Advanced Capture

The Advanced Capture module enables you to import and OCR-process other types of business documents than purchase invoices and credit memos, including custom documents. It also allows you to capture both header- and line-level data, and to split business documents automatically during import – if necessary. The module is particularly relevant if you need to import complex documents, high volumes of documents, or documents from multiple different vendors.

The Advanced Capture module includes the following key features:

| Feature                                                                                                                                                                                            |     Included    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------: |
| Recognize unlimited types of documents (e.g.: sales orders, purchase receipts, employee-related documents, shipping notes, etc.) and customize fields to be recognized in these document types     | \{{checkmark\}} |
| Line recognition, including: AI-enhanced line capture; combining AI with manual capture; capturing lines spanning multiple rows; relative line capture; and capturing field captions at line level | \{{checkmark\}} |
| Item reference for line translation                                                                                                                                                                | \{{checkmark\}} |
| Automatic splitting of PDF files inside Business Central, based, for example, on barcode or invoice number                                                                                         | \{{checkmark\}} |
| Automatic moving of documents to the right company, based on company identification texts                                                                                                          | \{{checkmark\}} |
| Automatic checking of line item prices                                                                                                                                                             | \{{checkmark\}} |
| Support for prepayments, including advance letters in the Czech Republic                                                                                                                           | \{{checkmark\}} |
| Dedicated category for creating and updating purchase orders                                                                                                                                       | \{{checkmark\}} |
| Support for assignment of item charges during document registration                                                                                                                                | \{{checkmark\}} |
| Document viewer availability on the **General Ledger Entries** and **General Journals** pages                                                                                                      | \{{checkmark\}} |
| Change the imported amount of a purchase document from the general and purchase journals                                                                                                           | \{{checkmark\}} |
| Update purchase orders based on delivery notes to automate the receiving process                                                                                                                   | \{{checkmark\}} |

## Order Matching

Order Matching makes it possible for you to match incoming business documents like purchase invoices and credit memos with other related documents, such as purchase orders, return orders, or return shipments. The documents are basically compared to ensure that there’s consistency between them: if the documents match (for example, in terms of price or number of items), they can be processed and approved automatically – whereas if they don’t, the relevant discrepancies must be handled. You can manually configure the levels of tolerance for such discrepancies.

With the Order Matching module, you get the following key features:

| Feature                                                                                                            |     Included    |
| ------------------------------------------------------------------------------------------------------------------ | :-------------: |
| Built-in image viewer as part of the matching process                                                              | \{{checkmark\}} |
| Manual matching to purchase receipts and return shipments                                                          | \{{checkmark\}} |
| Matching to unposted purchase orders and unposted return orders                                                    | \{{checkmark\}} |
| Automatic matching to purchase orders, receipts, return orders, and return shipments                               | \{{checkmark\}} |
| Matching based on vendor shipment number and vendor order number                                                   | \{{checkmark\}} |
| Configurable and automatic line-by-line matching[<sup>1</sup>](<Business Functionality.md#footnote-1.1>)           | \{{checkmark\}} |
| Automated, rule-defined tolerance of differences between order and invoice amounts – as well as subsequent posting | \{{checkmark\}} |
| Copy header dimensions from order to invoice automatically                                                         | \{{checkmark\}} |
| Update existing purchase order or return order, instead of creating invoice or credit memo                         | \{{checkmark\}} |
| Support for serial and lot numbers in the matching process                                                         | \{{checkmark\}} |
| Support for package tracking in order and receipt matching                                                         | \{{checkmark\}} |
| Application of tolerance amounts/percentages at line level                                                         | \{{checkmark\}} |
| Add missing order lines for matching purposes                                                                      | \{{checkmark\}} |
| Automatic matching via job queues                                                                                  | \{{checkmark\}} |
| Match purchase invoices with units of measure that differ from the related purchase order                          | \{{checkmark\}} |

\


***

1. Note that this feature also requires the Advanced Capture module to be installed.

## Document Approval

With Document Approval, you get a full approval workflow that allows you to approve business documents, assign approvers, and set approval limits. You can force the approval of documents, put them on hold, or have them approved automatically. It’s also possible to forward documents and delegate approvals if, for example, you’re out of office for a period of time.

The Document Approval module gives you access to the following key features:

| Feature                                                                                                                                                                          |     Included    |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :-------------: |
| Enhancement of a range of common workflow and approval scenarios not supported by standard Business Central                                                                      | \{{checkmark\}} |
| Built-in image viewer as part of the approval process                                                                                                                            | \{{checkmark\}} |
| Automatic approval and posting within predefined limits                                                                                                                          | \{{checkmark\}} |
| Send out a combined email with all invoices for approval                                                                                                                         | \{{checkmark\}} |
| Support for approval sharing when out-of-office is on (e.g.: for holiday, leave, etc.)                                                                                           | \{{checkmark\}} |
| Approval sharing that allows one or multiple people to manage approvals for others                                                                                               | \{{checkmark\}} |
| Forward invoices and credit memos for approval to a specific person                                                                                                              | \{{checkmark\}} |
| Support for four-eyes approval (i.e.: a minimum of two users checking all invoices)                                                                                              | \{{checkmark\}} |
| Dimension and amount validation during approval                                                                                                                                  | \{{checkmark\}} |
| Amount validation on posting to check posted amounts against actual document amounts                                                                                             | \{{checkmark\}} |
| Request predefined reason codes when invoice or credit memo is put on hold or rejected                                                                                           | \{{checkmark\}} |
| Pre-post purchases to G/L before documents are approved                                                                                                                          | \{{checkmark\}} |
| Approval flows that allow for document approval based on preconfigured approvers                                                                                                 | \{{checkmark\}} |
| Advanced approval that allows for document approval based on dimension codes                                                                                                     | \{{checkmark\}} |
| Free online hosting with Continia Software[<sup>1</sup>](<Business Functionality.md#footnote-2.1>)                                                                               | \{{checkmark\}} |
| Direct connection to Business Central using web services (full data consistency)[<sup>1</sup>](<Business Functionality.md#footnote-2.1>)                                         | \{{checkmark\}} |
| An intuitive UI for users to approve purchase invoices, credit memos, and other business documents[<sup>1</sup>](<Business Functionality.md#footnote-2.1>)                       | \{{checkmark\}} |
| Functionality that enables users to easily change lines, approve and reject documents, put documents on hold, forward documents to other users, and add attachments and comments | \{{checkmark\}} |
| Configurable account and dimension limitations to simplify selections[<sup>1</sup>](<Business Functionality.md#footnote-2.1>)                                                    | \{{checkmark\}} |
| Have approvals carried out by Business Central limited users                                                                                                                     | \{{checkmark\}} |
| Searchable, safe archive[<sup>1</sup>](<Business Functionality.md#footnote-2.1>)                                                                                                 | \{{checkmark\}} |
| Easy use of predefined templates to automatically create lines in invoices and credit memos                                                                                      | \{{checkmark\}} |
| Approval of purchase orders and return orders using Continia's approval workflow functionality, including the Continia Web Approval Portal                                       | \{{checkmark\}} |
| User-specific list of approvers when forwarding approval requests                                                                                                                | \{{checkmark\}} |
| Ability to prevent approvers from changing the on-hold status of documents for approval                                                                                          | \{{checkmark\}} |
| Option to allow both types of approval-sharing users to receive notifications                                                                                                    | \{{checkmark\}} |
| Put a document on hold and approve it at the same time                                                                                                                           | \{{checkmark\}} |
| Sort by due date and approval due date on the **Purchase Approval Entries** page                                                                                                 | \{{checkmark\}} |
| Approve documents across different companies on the Web Approval Portal                                                                                                          | \{{checkmark\}} |

\


***

1. Note that you also need the Web Approval Portal to use this feature.

## Purchase Contracts

The Purchase Contracts module makes it easy for you to manage your purchase contracts and have them reviewed regularly to ensure timely action. It provides you with an overview of your contracts and subscriptions, streamlines the contract review process, and enables you to have purchase documents approved automatically upon registration – if their amounts relate to contract amounts within a specified variance.

With the Purchase Contracts module, you get access to the following key features:

| Feature                                                                                                                              |     Included    |
| ------------------------------------------------------------------------------------------------------------------------------------ | :-------------: |
| Centralized management and storage of all purchase contracts, subscriptions, and other recurring costs                               | \{{checkmark\}} |
| Create contracts with all relevant information, such as vendor, pricing, contract start and end dates, and detailed contract lines   | \{{checkmark\}} |
| Comprehensive archive containing all contract-related documents and files from the contract card                                     | \{{checkmark\}} |
| Ability to create contracts directly from a recurring invoice                                                                        | \{{checkmark\}} |
| Auto-filling of contract details when invoices are processed in the document journal                                                 | \{{checkmark\}} |
| A straightforward and structured periodic review process, ensuring that you only pay for what you need                               | \{{checkmark\}} |
| Option to have the review process started automatically at regular intervals based on company policies                               | \{{checkmark\}} |
| Ability to review all contracts before the beginning of a new fiscal year                                                            | \{{checkmark\}} |
| Overview of contracts that need to be sent for approval                                                                              | \{{checkmark\}} |
| Email notifications to contract approvers when contracts are due for approval                                                        | \{{checkmark\}} |
| An intuitive user interface that makes it easy to approve contracts from Business Central or the Web Approval Portal                 | \{{checkmark\}} |
| Functionality that enables contract approvers to easily change lines, approve and cancel contracts, and add attachments and comments | \{{checkmark\}} |
| Automatic approval of recurring invoices within allowed tolerances, based on approved contracts                                      | \{{checkmark\}} |
| Purchase contract intelligence, a system that suggests contract creation based on patterns detected in recurring invoices            | \{{checkmark\}} |

## Related information

[Release plan](../../Continia%20Document%20Capture/Getting%20Started/@DC-56/)\
[Feature management](../../Continia%20Document%20Capture/Getting%20Started/@DC-455/)
