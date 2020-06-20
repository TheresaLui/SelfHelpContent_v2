<properties
	pageTitle="Azure Account Failover Cannot Perform"
	description="Azure Account Failover Cannot Perform"
	infoBubbleText=""
	service="microsoft.storage"
	resource="storageaccounts"
	authors="Sijia"
	ms.author="siz"
	displayOrder=""
	articleId="cea80e58-c969-4e77-a04d-c6de1bfb4399"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32631234"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# Azure Account Failover Cannot Perform
## **Recommended Action**
Customer-managed account failover feature is currently unavailable due to a service bug that may impact access to the storage account after failover. We are working with priority to fix the problem, validate and deploy the fix. We apologize for the inconvenience this has caused.

## **Recommended Documents**

- [Check that the storage account is in the supported region](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance#about-the-preview)<br>
- [Make sure you have registered for Preview](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance#about-the-preview)<br>
- [Make sure the account is enabled for GRS, RA-GRS](https://docs.microsoft.com/azure/storage/common/storage-initiate-account-failover#prerequisites)<br>
- [Verify that Data was replicated to secondary region by checking the LastSyncTime](https://docs.microsoft.com/azure/storage/common/storage-initiate-account-failover#important-implications-of-account-failover)
