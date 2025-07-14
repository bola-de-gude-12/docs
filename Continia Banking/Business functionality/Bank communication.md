---
title: Bank communication and Continia Banking
description: Introduction to manual and direct banking communication.
date: 02-06-2025
id: CB-80
lang: en
---

# Bank communication in Continia Banking

Continia Banking enables you to exchange data between your bank and Microsoft Dynamics 365 Business Central using two methods: manual and direct communication.

- **Manual communication** requires you to import and export banking files yourself.
- **Direct communication** automates this process using web services, so you don’t need to handle files manually. The availability of direct communication depends on your bank’s support for this feature.

## Direct communication

Direct communication is recommended as it fully automates data exchange between Business Central and your bank. To use this feature, ensure that your Continia Banking subscription includes the Direct Communication module. Example workflow for sending payments using direct communication:

1. Create and prepare payment suggestions in the payment journal.
2. Send the payment file directly to your bank from Business Central.
3. The bank processes the payments.
4. Payment status updates (such as sent, received, paid, or rejected) are automatically imported back into the payment journal.
5. If there are errors, correct them and resend as needed. This automation also applies to importing payment, status, or statement files from the bank into Business Central.

## Direct communication through open banking providers

Continia Banking also works with open banking providers to enable direct communication between your bank and Business Central. Some banks may require extra steps, such as payment approval, when using open banking providers.

## Manual communication

Manual communication is the traditional way to exchange banking files  between Business Central and your bank. In this method, you manually  download and upload files. Example workflow for sending payments manually:

1. Create payment suggestion in the payment journal.
2. Export the payment file from Business Central and save it locally.
3. Log in to your online banking portal.
4. Upload the payment file to your bank's system.
5. Check your bank's system to confirm that payments were processed.
6. If there are errors, correct them and repeat the process.

## Cloud storage with Azure Blob Storage

If your bank uses systems outside of Business Central,  Continia Banking can integrate with Azure Blob Storage to manage and access files securely in the cloud.

To set up Azure Blob Storage, you will need:
- Storage Account Name
- Storage Account Key
- Container Name

Enter these details in Continia Banking to enable secure file management and communication. For detailed setup instructions, refer to the [Setting up Azure Blob Storage for Continia Banking](@CB-74) article.
