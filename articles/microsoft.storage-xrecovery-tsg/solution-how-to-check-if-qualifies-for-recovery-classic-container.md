<properties
	pageTitle="How to check if qualifies for recovery attempt  Storage Account Recovery Classic ARM for the container"
	description="How to check if qualifies for recovery attempt  Storage Account Recovery Classic ARM for the container"
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
	articleId="14c55b6c-9e3c-429e-97a7-5e1fa6336c4f"
/>

# How to check if qualifies for recovery attempt  Storage Account Recovery Classic ARM for the container

<!--issueDescription-->

Please note that it is impossible to recover Data at the blob level<br>
<br>
**How to check the storage account type**<br>
<br>
Use this TSG for a request to recover storage data. As you follow through the steps in this TSG, maintain notes of each command run and output generated Should you run into any difficulties, this information will be critical to determine next steps.<br>
<br>
1. Recovery is only possible for certain types of resources and even then only if the data has not been garbage collected.<br>
2. Recovery is possible if customer re-create a Storage Account with the same name. However, it is not possible with any other resource types since the data will be overwritten.<br>
3. It can generally take anywhere from "immediately after deletion" to 14 days for the Storage service to perform garbage collection so there is no SLA or guarantee of recovery.<br>
4. Set customer expectations in your initial response itself that Azure Support will try recovery on a best effort basis but cannot guarantee recovery.<br>
5. Check if customer created a new resource with the same name (even briefly). Creating a resource with the same name reduces the chances of recovery considerably because it can trigger early clean up.<br>

<!--/issueDescription-->

## Recommended Documents

1. [Azure_Storage_TSG_Recover Storage Account](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265682/Azure_Storage_TSG_Recover-Storage-Account)
2. [Data restore scenarios for Azure Storage service](https://support.microsoft.com/en-us/help/4012226/data-restore-scenarios-for-azure-storage-service)
