---
title: Migrating OPplus data to Continia Banking
description: Migrating OPplus data to Continia Banking
date: 03-04-2025
id: CB-233
lang: en
---

# Migrating OPplus data to Continia Banking

Continia provides a migration tool to ensure an easy and safe transfer of your OPplus data to Continia Banking and Continia Finance.

The Continia Banking/Finance Data Migration Setup helps customers seamlessly migrate their data from OPplus to Continia Banking and Continia Finance within Microsoft Dynamics 365 Business Central. This tool offers a structured approach to migrating financial data, ensuring a seamless switch between the two systems.

Once the migration is complete, OPplus is deactivated, and Continia Banking and Continia Finance are activated automatically.

## The migration process

To start the migration tool:

* Search ({{search}}) for and select **Continia Banking/Finance Data Migration Setup**. The wizard will guide you through the following steps:
  * **Pre-validation** - before initiating the migration, the tool runs a pre-validation check on existing OPplus data to detect and resolve any potential issues. 
  * **Migration to Continia Finance** - after pre-validation, the tool migrates data to Continia Finance. This step updates financial records and ensures that all financial data is accurately transferred. The Finance Upgrade must be completed before migrating to Continia Banking. The tool includes a verification step to confirm this before proceeding.
  * **Migration to Continia Banking** - the final step involves migrating banking data to Continia Banking. This ensures that all banking transactions and related data are seamlessly transitioned.

## Prerequisites

Before migrating OPplus data into Continia Banking and Continia Finance, make sure the following prerequisites are met:
* **OPplus version** - make sure you are using OPplus version 26.0.0 or higher.
* **Payment Import Registers** - verify that all OPplus payment import registers have been posted.
* **Payment Proposals** - confirm that all OPplus Payment Proposals have been posted.
* **Journals** - we recommend to post or delete all open journals before migration. 
* **Admin access** - make sure you have administrative access and permissions to install the relevant apps.