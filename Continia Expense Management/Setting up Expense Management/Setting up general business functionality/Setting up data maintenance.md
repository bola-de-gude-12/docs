---
title: Setting up Data Maintenance
date: 02-12-2024
description:
id: EM-224
lang: en
---

# Setting up Data Maintenance

Depending on where you're based, it's important to delete data in order to remain compliant with the European Union's General Data Protection Regulation (GDPR) or similar regulations. The GDPR data maintenance feature in Expense Management allows you to delete not only words and values, but also documents, document records, and any related attachments.

Before performing the data maintenance, you must specify the retention period for search data and GDPR as described below. You can either run the data maintenance manually or set up job queues to handle it automatically.

Please note that **Retention Period (Years)** and **GDPR Retention Period (Years)** specify how many closed *fiscal years* of document data is saved when the data maintenance is performed, and the minimum values are 2 and 5 respectively. This process is based on document status, meaning that it's only carried out for documents that have been posted – and the data maintenance period is calculated from the posting date of the document.

## To configure the settings for GDPR compliance

To specify the number of years GDPR-related data (that is, words and values, the documents themselves, and any related attachments) is saved before it can be deleted using data maintenance, follow these steps:

1. Choose the {{search}} icon, enter **Expense Management Setup**, and then choose the related link.
1. On the **General** FastTab, under **Data Maintenance**, go to the **GDPR Retention Period (Years)** field and specify the number of years you would like the GDPR-related data to be saved.

   > [!NOTE]
   > If a date is specified under **Purchases & Payables Setup** > **Allow Document Deletion Before**, this date is also considered when the earliest deletion date for the GDPR-related data is calculated.
   >
   > GDPR data maintenance is also related to the Secure Archive. If **Secure Archive** is enabled, the number of years specified in the **Minimum Archive Period** field also applies. 
   >
   > In this case, the setting with the longest storage period applies. For example, if **GDPR Retention Period (Years)** is set to *5 years*, the **Allow Document Deletion Before** date is set to *3 years*, and the **Minimum Archive Period** is set to *9 years*, the data is saved for *9 years* – provided that the Secure Archive is enabled.

1. To run the GDPR maintenance task from the **Expense Management Setup** page, go to **Actions** > **Functions**, and then select **Run GDPR Maintenance**.

To run data maintenance using job queues, see [Setting up Job Queues](Setting up job queues.md).


## See also

[Secure Archive](@EM-189)  