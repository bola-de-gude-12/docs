---
title: QR-Bill Management App Integration
date: 30-01-2025
description:  
id: DC-217
lang: en
---

# QR-Bill Management App Integration

> [!IMPORTANT]
> This article only applies to Microsoft Dynamics 365 Business Central 2023 release wave 1 (BC v22) and later.

If you've installed the QR-Bill Management app developed by Microsoft for the Swiss market, Continia Document Capture can integrate with it by copying the content of any identified QR code directly into the app. Whenever a purchase document with a valid QR code is imported into Document Capture, the QR code is automatically identified and read by Document Capture, and the captured QR data is then transferred to the QR-Bill Management app when you register the document.

The following fields on the **QR-Bill** FastTab are automatically populated with the captured data upon document registration:

* **IBAN/QR-IBAN**
* **Currency**
* **Billing Information**
* **Amount**
* **Unstructured Message**

Payment references contained within captured QR codes are also automatically transferred to the relevant field in Microsoft Dynamics 365 Business Central. To find this for a registered invoice, open the invoice, go to the **Invoice Details** FastTab, and locate the **Payment Reference** field.

In addition to the above, Document Capture also carries out other QR-related actions when you register a document with a QR code:

* It uses the IBAN detected in the QR code to identify the vendor who sent the document.
* It validates that the captured document amount is equal to the amount of the QR code.
* When creating a vendor bank account from a QR code, the following fields are automatically populated from the bank directory:
  * **Name**
  * **Address**
  * **Address 2**
  * **City**
  * **Post Code**
  * **SWIFT Code**

> [!IMPORTANT]
> The automatic population of vendor-related fields requires an updated bank directory. To get the latest clearing numbers:
> 1. Download the TXT file from the [Download Bankenstamm](https://www.six-group.com/de/products-services/banking-services/interbank-clearing/online-services/download-bank-master.html) page of the SIX website. Next, go to Business Central.
> 2. Choose the {{search}} icon, enter **Bank Directory**, and then choose the related link.
> 3. On the **Bank Directory** page, select **Import Bank Directory**. Then, select the TXT file downloaded in step 1.