---
title: Using the Document Capture assisted setup
date: 15-10-2025
description: How to use the Document Capture assisted setup guide.
id: DC-438
lang: en
---

# Using the Document Capture Assisted Setup

The Continia Document Capture assisted setup guide allows you to handle three different tasks in Microsoft Dynamics 365 Business Central: import a configuration, export a configuration, and set up company.

>[!NOTE]
>This assisted setup was only designed to import and export configuration, therefore it doesn’t include data such as G/L accounts, items, customers, etc.

## Importing a configuration

Importing a configuration allows you to reuse configurations that had already been set up in a different company or a different environment, such as a test environment. These configurations include templates related to document categories, eDocuments, and the Document Capture Setup.

To import a configuration:

1. Search ({{search}}) for and select **Set Up Document Capture**.
1. In the **Action** dropdown menu, click **Import Configuration**.
1. In the **Import from** dropdown menu, select the source of the configuration. If you select **File**, you need to add the file that contains the configuration under **File Name**.
1. If the correct localization isn't automatically set, select the three dots by the **Localization** field and select the correct localization. This is only required when importing from online.
1. Select or clear the checkboxes by each configuration to include them or exclude from the import. When you're done, click **Next**.
1. When the process is completed, click **Finish** to close the popup.

## Exporting a configuration

Exporting a configuration allows you to reuse configurations set up in the current company. These configurations include templates related to document categories, eDocuments, and the Document Capture Setup.

To export a configuration:

1. Search ({{search}}) for and select **Set Up Document Capture**.
2. In the **Action** dropdown menu, click **Export Configuration**.
3. Select or clear the checkboxes by each configuration to include them or exclude from the export. When you're done, click **Next**.
4. The configuration file is generated and automatically downloaded. Click **Finish** to close the popup.

## Setting up a company

Setting up a company ensures that Document Capture has the basic configuration to handle most tasks. This includes master templates and identification templates.

To set up a company:

1. Search ({{search}}) for and select **Set Up Document Capture**.
2. In the **Action** dropdown menu, click **Set up Company**.
3. If the correct localization isn't automatically set, click the three dots by the **Localization** field and select the correct localization.
4. When the process is completed, click **Finish** to close the popup.
