<properties
	pageTitle="Cannot access newly created account"
 	description="Cannot access newly created account"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	ms.author="passap"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32688875"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	articleId="B3F0474C-56DC-4018-9403-F5F1EBB0E534"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Cannot access newly created account

Check if your new storage account is accessible via DNS lookup by running the following command-line in your command prompt: `nslookup [myStorageAccount].blob.core.windows.net`

If the result returned a valid external name and IP address, the storage account is successfully created and is accessible through [Azure CLI](https://docs.microsoft.com/cli/azure/storage?view=azure-cli-latest), [PowerShell](https://docs.microsoft.com/powershell/module/storage/?view=win10-ps), and [Rest API](https://docs.microsoft.com/rest/api/storageservices/).   

## **Recommended Documents**

- [Azure Storage CLI](https://docs.microsoft.com/cli/azure/storage?view=azure-cli-latest)
- [Azure Storage PowerShell](https://docs.microsoft.com/powershell/module/storage/?view=win10-ps)
- [Azure Storage Rest API](https://docs.microsoft.com/rest/api/storageservices/)
- [Create Azure Storage account](https://docs.microsoft.com/azure/storage/storage-create-storage-account)<br>
- [Storage Account Replication](https://docs.microsoft.com/azure/storage/common/storage-redundancy)
