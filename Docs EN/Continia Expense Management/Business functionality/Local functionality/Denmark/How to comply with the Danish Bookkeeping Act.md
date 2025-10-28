---
title: How to Comply with the Danish Bookkeeping Act
date: 24-05-2024
description:  
id: EM-227
lang: en
---

# How to Comply with the Danish Bookkeeping Act

> [!NOTE]
> This is the English version of the article. You can find the Danish version here: [Sådan kan du overholde bogføringsloven](@EM-228).

> [!IMPORTANT]
> Support for the Danish Bookkeeping Act has been fully implemented in Expense Management and Document Capture as of version 12.02.

## Business Central online or on-premises

The Danish Bookkeeping Act (Act No.700 of 24 May 2022) requires Danish organizations to use digital bookkeeping systems. A digital bookkeeping system can be a standard system that the IT service provider chooses to register with and have approved by the Danish Business Authority (Erhvervsstyrelsen), or it can be an unregistered digital bookkeeping system whose compliance with the Act is ensured by the organization itself.

### Business Central online

Microsoft has registered **Microsoft Dynamics 365 Business Central online** with the Danish Business Authority and had it approved as a standard digital bookkeeping system. Any organization looking to further optimize their administration is free to use Continia Document Capture, Continia Expense Management, Continia Document Output, and Continia Payment Management in addition to the registered system without this affecting the Danish Business Authority's approval.

You can find more details here: [Compliance with the bookkeeping act in Denmark](https://learn.microsoft.com/en-us/dynamics365/business-central/localfunctionality/denmark/compliance-denmark#main-requirements----15-no-2) (Microsoft article).

### Business Central on-premises (local installation)

**Microsoft Dynamics 365 Business Central on-premises** is also a digital bookkeeping system, but this has *not* been registered with and approved by the Danish Business Authority. This means that organizations that use this system are themselves responsible for ensuring that the system is used in a way that complies with the Act.

In terms of bookkeeping functionality, the latest version of Business Central on-premises is the same system as the online version,<a href="#footnote-1"><sup>1</sup></a> meaning that all requirements relating to its bookkeeping features will be met. For the on-premises version, just as with the online version, any organization looking to further optimize their administration is free to use Document Capture, Expense Management, Document Output, and Payment Management in addition to Business Central.

<small style>

<div class="footnotes">
  <hr />
  <ol>
    <li id="footnote-1">Certain features may require the installation of program add-ons (apps) or activation using Feature Management.</li>        
  </ol>
</div>
</small>

## Best practice for storing digital documents

The Danish Bookkeeping Act requires Danish companies to digitally store documents related to purchases and sales. With Document Capture and Expense Management, each individual organization can choose the particular storage method that suits them best.

> [!NOTE]
> Document Capture, Expense Management, and Document Output can all be set up to require that documents must be stored when sales and purchase transactions are posted. Continia's solutions thereby enable organizations to ensure compliance with the Bookkeeping Act's requirement of digital document storage.

### Business Central online

For Danish organizations using Business Central online, Microsoft stipulates that purchase documents must be stored in the **Incoming Documents** table as of July 1, 2024. This is straightforward with Document Capture and Expense Management, as they automatically copy all purchase documents to this table. Consequently, organizations that use these solutions won't notice this new requirement.

If an organization stores purchase documents that have been registered using Document Capture or Expense Management in the Business Central database, the documents will appear in the database twice. This method is a convenient and simple, but for some organizations it may take up a disproportionately large amount of database space, as the documents are stored in both Continia's tables and Microsoft's **Incoming Documents** table. Such organizations can choose to store their purchase documents from Document Capture and Expense Management using Azure Blob Storage instead. For more information, see [Setting up Azure Blob Storage](@EM-230).

### Business Central on-premises

Organizations that use Business Central on-premises can choose to store their digital purchase documents using any of the following methods:

* In Continia's tables in the Business Central database
* Using Azure Blob Storage
* Locally on the organization's own server

Each individual organization can also choose to have Document Capture and Expense Management automatically copy all purchase documents to the Business Central **Incoming Documents** table. This may be useful if the organization currently stores purchase documents using Azure Blob Storage or locally on the organization's server, as the documents will then be covered by the security of the database and the backup routines that have been set up for this.

> [!IMPORTANT]
> Organizations that use locally installed versions of Business Central must ensure that bookkeeping transactions and digital documents are fully backed up automatically at least once a week. Such backups must be stored on a server in an EU or EEA country by a non-affiliated company that's presumed to meet recognized standards for IT security.

## Continia's solutions and the Bookkeeping Act

The Danish Bookkeeping Act requires organizations to use systems that support the automation of their administrative processes. This is the very purpose of Document Capture, Expense Management, Document Output, and Payment Management. The use of Continia's solutions also makes it easier for your organization to meet the following requirements of the Bookkeeping Act:

* Continuous and accurate registration of transactions
* Digital storage of purchase and sales documents
* Securing of audit trails
* Sending and receiving of electronic invoices
* Reconciliation of the organization's bank accounts

Continia's solutions are built inside Business Central and don't affect the basic functionality of the digital bookkeeping system or the storage of data. Having consulted the Danish Business Authority, Continia can confirm that all Continia solutions can be used together with Business Central online with no consequence for its status as a registered standard digital bookkeeping system.