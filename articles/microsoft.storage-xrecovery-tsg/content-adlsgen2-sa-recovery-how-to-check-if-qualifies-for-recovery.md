<properties
	pageTitle="ADLS Gen 2 How to check if qualifies for recovery attempt  Storage Account Recovery Classic ARM"
	description="How to check if qualifies for recovery attempt  Storage Account Recovery Classic ARM"
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
	articleId="0dcee7bf-ec58-41c4-9e77-b1e43d3d5717"
/>

# ADLS Gen 2 How to check if qualifies for recovery attempt  Storage Account Recovery Classic / ARM

<br>


## ANNOUNCEMENT : **C**ustomer-controlled **S**torage **A**ccount **R**ecovery  [(CSAR)]((https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/407376/Azure-Storage-Customer-controlled-Storage-Account-Recovery-(CSAR))) is now live in the Portal 



<br>
<br>


1. Ensure storage account does not exist currently. 
2. Account name should not have been reused. 
3. Customer should NOT recreate a storage account with the same name. 
4. In some cases, recreating a storage account with the same name will cause the original storage account data to be cleaned up early making it unrecoverable. 
5. If the customer has already re-created the account, they will need to delete it first before recovery can be attempted
6. Storage account was deleted less than 14 days ago.

## Recommended Documents


1. [Azure_Storage_TSG_Recover Storage Account](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265682/Azure_Storage_TSG_Recover-Storage-Account)
2. [Data restore scenarios for Azure Storage service](https://support.microsoft.com/en-us/help/4012226/data-restore-scenarios-for-azure-storage-service)


