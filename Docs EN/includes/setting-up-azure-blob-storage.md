Continia {param1} provides strong document file archiving capabilities with easy integration with Azure Blob Storage. To begin using Azure Blob Storage, follow the processes described here in the given order.

## To set up a storage account and container
To set up an Azure Blob Storage account and container, see [Create an Azure storage account](https://learn.microsoft.com/en-us/azure/storage/common/storage-account-create) and [Authorize access to data in Azure Storage](https://learn.microsoft.com/en-us/azure/storage/common/authorize-data-access) (Microsoft articles).

>[!IMPORTANT]
>When setting up your Azure Blob Storage account, make sure to set its **AllowBlobPublicAccess** property to **False**. This prevents a known security risk by forcing all blob data requests to be authenticated. For more information, see [Overview: Remediating anonymous read access for blob data](https://learn.microsoft.com/en-us/azure/storage/blobs/anonymous-read-access-overview) (Microsoft article).

{param1} doesn't support shared access signatures (SAS) in Azure Blob Storage, therefore you must enter a storage account access key in the **Storage Account Key** field.

## To set up {param1}
To set up the solution for Azure Blob Storage:

1. Search {{search}} for and select **{param1} Setup**.
1. Under **General** > **Document Storage Type**, click **Azure Blob Storage** to open the **Azure Blob Storage** settings group.
1. In the fields **Storage Account Name**, **Storage Account Key**, and **Blob Container Name**, enter the corresponding values from when you set up the storage account and container.