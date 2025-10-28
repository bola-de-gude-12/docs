---
title: Document Capture Setting up Data Maintenance
date: 21-01-2025
description: How to set up data maintenance for Document Capture tables
id: DC-187
lang: en
---

# Setting up Data Maintenance

When documents are processed using OCR in Continia Document Capture, a large amount of data is generated and stored over time. While this is useful to perform free-text searches in the document journal (for example, contact names on an invoice), you may not need the majority of this data. At some point, storing a lot of data can even impact the search functionality – and slow down other processes, such as importing documents and recognizing fields. Therefore, it's desirable to clear data that's no longer needed.

Depending on where you're based, it's also important to delete data in order to remain compliant with the European Union's General Data Protection Regulation (GDPR) or similar regulations. The GDPR data maintenance feature in Document Capture allows you to delete not only words and values, but also documents, document records, and any related attachments.

Before performing the data maintenance, you must specify the retention period for search data and GDPR as described below. You can either run the data maintenance manually or set up job queues to handle it automatically.

Please note that **Retention Period (Years)** and **GDPR Retention Period (Years)** specify how many closed *fiscal years* of document data is saved when the data maintenance is performed, and the minimum values are 2 and 5 respectively. This process is based on document status, meaning that it's only carried out for documents that have been posted – and the data maintenance period is calculated from the posting date of the document.

The video below outlines the most important data maintenance features:

<br>

<div style="padding:56.25% 0 0 0;position:relative;"><iframe src=https://player.vimeo.com/video/924643920?h=b599c81bb3&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479 frameborder="0" allow="autoplay; fullscreen; picture-in-picture; clipboard-write" style="position:absolute;top:0;left:0;width:100%;height:100%;" title="DC_Data maintenance_produced"></iframe></div><script src=https://player.vimeo.com/api/player.js></script>

## To configure data maintenance settings

To specify the number of years the search data is saved before it can be deleted using data maintenance, follow these steps:

1. Search ({{search}}) for and select **Document Capture Setup**.
1. On the **General** FastTab, under **Data Maintenance**, go to the **Retention Period (Years)** field and specify the number of years you would like the search data to be saved.

   > [!NOTE]
   > If a date is specified under **Purchases & Payables Setup** > **Allow Document Deletion Before**, this date is also considered when calculating the earliest deletion date for the search data. 
   >
   > In this case, the setting with the longer storage period applies. For example, if **Retention Period (Years)** is set to *2 years*, but the **Allow Document Deletion Before** date is set to *3 years*, the data is saved for *3 years*. 

1. To run the data maintenance task from the **Document Capture Setup** page, go to **Actions** > **Functions**, and then select **Run Data Maintenance**.

   >[!IMPORTANT]
   >The actual values captured in documents aren't deleted, only their captions are. This allows for the efficient use of the **Document Search** functionality across all captured data, preserving values until the document is deleted via the GDPR data maintenance feature. It also ensures minimal storage use, while maintaining search functionality for all captured information.

## To configure the settings for GDPR compliance

To specify the number of years GDPR-related data (that is, words and values, the documents itself, and any related attachments) is saved before it can be deleted using data maintenance, follow these steps:

1. Search ({{search}}) for and select **Document Capture Setup**.
1. On the **General** FastTab, under **Data Maintenance**, go to the **GDPR Retention Period (Years)** field and specify the number of years you would like the GDPR related data to be saved.

   > [!NOTE]
   > If a date is specified under **Purchases & Payables Setup** > **Allow Document Deletion Before**, this date is also considered when the earliest deletion date for the GDPR-related data is calculated.
   >
   > GDPR data maintenance is also related to the Secure Archive. If **Secure Archive** is enabled, the number of years specified in the **Minimum Archive Period** field also applies. 
   >
   > In this case, the setting with the longest storage period applies. For example, if **GDPR Retention Period (Years)** is set to *5 years*, the **Allow Document Deletion Before** date is set to *3 years*, and the **Minimum Archive Period** is set to *9 years*, the data is saved for *9 years* – provided that the Secure Archive is enabled.

1. To run the GDPR maintenance task from the **Document Capture Setup** page, go to **Actions** > **Functions**, and then select **Run GDPR Maintenance**.

To run data maintenance using job queues, see [Setting up Job Queues](Setting up job queues.md).

## Related information

[Setting up Job Queues](Setting up job queues.md)  
[Secure Archive](@DC-154) 

