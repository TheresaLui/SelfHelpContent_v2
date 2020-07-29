<properties
	pageTitle="How to check if qualifies for recovery attempt  Storage Account Recovery Classic ARM"
	description="How to check if qualifies for recovery attempt  Storage Account Recovery Classic ARM"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="4d45b552-c63a-49f9-8583-4fe9aacf976d"
/>

# How to check if qualifies for recovery attempt  Storage Account Recovery Classic ARM

1. Ensure storage account does not exist currently. 
2. Account name should not have been reused. 
3. Customer should NOT recreate a storage account with the same name. 
4. In some cases, recreating a storage account with the same name will cause the original storage account data to be cleaned up early making it unrecoverable. 
5. If already recreated, they will need to delete the recreated account before we start.

## Recommended Documents

1. [Azure_Storage_TSG_Recover Storage Account](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265682/Azure_Storage_TSG_Recover-Storage-Account)
2. [Data restore scenarios for Azure Storage service](https://support.microsoft.com/en-us/help/4012226/data-restore-scenarios-for-azure-storage-service)

