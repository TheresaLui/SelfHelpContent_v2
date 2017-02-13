<properties
	pageTitle="How to create a new storage account"
	description="How to create a new storage account"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32551649"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public"
/>

# How to create a new storage account

## **Recommended steps**
1. On the Hub menu of Azure Portal, select **New -> Storage -> Storage account**.
2. Enter a name for your storage account. See [Storage account endpoints](https://docs.microsoft.com/azure/storage/storage-create-storage-account#storage-account-endpoints) for details about how the storage account name will be used to address your objects in Azure Storage.
3. Specify the deployment model to be used: **Resource Manager** or **Classic Resource Manager** is the recommended deployment model. For more information, see [Understanding Resource Manager deployment and classic deployment](https://docs.microsoft.com/azure/storage/storage-create-storage-account#storage-account-endpoints).
4. Select the type of storage account: **General purpose** or **Blob storage**. General purpose is the default.<br>
   - If **General purpose** was selected, then specify the performance tier: **Standard** or **Premium**. The default is **Standard**. For more details on standard and premium storage accounts, see [Introduction to Microsoft Azure Storage](https://docs.microsoft.com/azure/storage/storage-introduction) and [Premium Storage: High-Performance Storage for Azure Virtual Machine Workloads](https://docs.microsoft.com/azure/storage/storage-premium-storage).
   - If **Blob Storage** was selected, then specify the access tier: **Hot** or **Cool**. The default is **Hot**. See [Azure Blob Storage: Cool and Hot tiers](https://docs.microsoft.com/azure/storage/storage-blob-storage-tiers) for more details.
5. Select the replication option for the storage account: **LRS**, **GRS**, **RA-GRS**, or **ZRS**. The default is **RA-GRS**. For more details on Azure Storage replication options, see [Azure Storage replication](https://docs.microsoft.com/azure/storage/storage-redundancy).
6. Select the subscription in which you want to create the new storage account.
7. Specify a new resource group or select an existing resource group. For more information on resource groups, see [Azure Resource Manager overview](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-overview).
8. Select the geographic location for your storage account. See [Azure Regions](https://azure.microsoft.com/regions/#services) for more information about what services are available in which region.
9. Click **Create** to create the storage account.

## **Recommended documents**
- [Introduction to Microsoft Azure Storage](https://docs.microsoft.com/azure/storage/storage-introduction)<br>
- [About Azure storage accounts](https://docs.microsoft.com/azure/storage/storage-create-storage-account)<br>
- [Azure Storage Best Practices and Patterns](https://azure.microsoft.com/resources/videos/microsoft-storage-what-new-best-practices-and-patterns/)
