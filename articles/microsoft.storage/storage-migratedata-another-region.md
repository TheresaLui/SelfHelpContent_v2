<properties
	pageTitle="Move Data to, from, or within Azure Storage"
	description="Move Data to, from, or within Azure Storage"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	ms.author="raprasad"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602700,32602736"
	resourceTags=""
	productPesIds="15629,16459"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	articleId="5d7b80ee-409f-4cce-82f8-fc2667277f52"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Move Data to, from, or within Azure Storage

## **Recommended Steps** 
Storage account cannot be migrated directly to a different region. Here is a workaround you can follow:

1. Create a new storage account in the desired region
2. Use the following tools for move the data:

 	* [Transfer data with AzCopy v10](https://docs.microsoft.com/azure/storage/common/storage-use-azcopy-v10)<br>	
	* [Transfer data with Storage Explorer](https://docs.microsoft.com/azure/vs-azure-tools-storage-manage-with-storage-explorer?tabs=windows)<br>
	* [Move Data with Azure PowerShell](https://azure.microsoft.com/documentation/articles/storage-powershell-guide-full/)<br>
	* [Move Data from Linux or OSX with Azure CLI](https://azure.microsoft.com/documentation/articles/storage-use-azcopy/)
	
 3. Once you are sure that everything is copied, you can delete the old storage account
 
Please remember that if you have applications that connects at the source Storage Account, you will need to replace the credentials for the new ones from the new storage account.

## **Recommended Documents**

- You can find what is the best data transfer solution by following [Choose an Azure solution for data transfer](https://docs.microsoft.com/azure/storage/common/storage-choose-data-transfer-solution):

	* [Data transfer for large datasets with low or no network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-low-network)<br>
	* [Data transfer for small datasets with low to moderate network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-small-dataset-low-moderate-network)<br>
	* [Data transfer for large datasets with moderate to high network bandwidth](https://docs.microsoft.com/azure/storage/common/storage-solution-large-dataset-moderate-high-network)<br>
	* [Solutions for periodic data transfer](https://docs.microsoft.com/azure/storage/common/storage-solution-periodic-data-transfer)
