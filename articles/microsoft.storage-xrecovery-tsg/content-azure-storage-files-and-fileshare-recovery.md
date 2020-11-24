<properties
	pageTitle="Azure Storage Files and FileShare Recovery"
	description="Azure Storage Files and FileShare Recovery"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="symondsk"
	ms.author="ksymonds"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
	articleId="49b12bc6-4ded-4e91-9386-dfb6665bc51d"
/>

# Azure Storage Files and FileShare Recovery

Azure Storage Files and FileShares are generally not recoverable. Please check if customer has fileshare snapshots. If present they can copy data out from the share snapshot using storage explorer as follows.

1. Navigate to the share using storage explorer.
2. Choose View Share Snapshots from the top ribbon
3. Double click on the preferred snapshot
4. Right click on the required file and choose to Restore Snapshot.

## Recommended Documents

1. [Azure_Storage_TSG_Recover Storage Account](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265682/Azure_Storage_TSG_Recover-Storage-Account)
2. [Data restore scenarios for Azure Storage service](https://support.microsoft.com/en-us/help/4012226/data-restore-scenarios-for-azure-storage-service)
