Use the Continia Banking/Finance Data Migration tool to transfer data from OPplus to Continia Banking and Continia Finance in Microsoft Dynamics 365 Business Central. 

> [!IMPORTANT]
>
> Content in this article is maintained continuously and some steps may require additional attention depending on your setup. Review all instructions carefully before starting the migration process.

The migration tool provides a guided and structured approach to moving financial data. When migration is complete:

* OPplus is automatically deactivated.
* Continia Banking and Continia Finance are activated as needed. 

## Prerequisites

Before you start migration, make sure the following requirements are met:

* **OPplus version** - make sure you are using OPplus version 26.0.0 or higher.
* **Payment Import Registers** - verify that all OPplus payment import registers have been posted.
* **Payment Proposals** - confirm that all OPplus Payment Proposals have been posted.
* **Journals** - post or delete all open journals before migration. 
* **Admin access** - make sure you have administrative access and permissions to install the relevant apps.

Additionally, install these apps in your environment before migration:

- **Continia Banking**
- **Continia Banking Migration OPplus**

## Run the migration tool

To start the migration tool:

1. Search ({{search}}) for and select **Continia Banking/Finance Data Migration Setup**. 
2. The wizard will guide you through the following steps:
   * **Pre-validation** - before initiating the migration, the tool runs a pre-validation check on existing OPplus data to detect and resolve any potential issues. 
   * **Migration to Continia Finance** - after pre-validation, the tool migrates data to Continia Finance. This step updates financial records and ensures that all financial data is accurately transferred. The Finance Upgrade must be completed before migrating to Continia Banking. The tool includes a verification step to confirm this before proceeding.
   * **Migration to Continia Banking** - the final step involves migrating banking data to Continia Banking. This ensures that all banking transactions and related data are transferred.

## Next steps

* The OPP permission sets weren’t migrated. Assign the [Continia Banking permission sets](@CB-59) to users. 