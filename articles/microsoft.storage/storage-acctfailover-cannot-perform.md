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

## **Recommended Steps**
Customer-managed account failover feature is currently unavailable due to a service issue that impacts access to the storage account after failover. We are working with priority to address the issue, validate and deploy the fix. We apologize for the inconvenience this has caused.

If you have an immediate need to perform account failover for disaster recovery of your production workload, please submit a support ticket with details on your failover scenario. We will work with you to perform the failover from the service backend. For all other non-critical scenarios, we recommend waiting for the customer-managed failover feature to be enabled again. Alternatively you can backup your data to a second storage account in your target region by performing another write operation. 


## **Recommended Documents**

- [Check that the storage account is in the supported region](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance#about-the-preview)<br>
- [Make sure you have registered for Preview](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance#about-the-preview)<br>
- [Make sure the account is enabled for GRS, RA-GRS](https://docs.microsoft.com/azure/storage/common/storage-initiate-account-failover#prerequisites)<br>
- [Verify that Data was replicated to secondary region by checking the LastSyncTime](https://docs.microsoft.com/azure/storage/common/storage-initiate-account-failover#important-implications-of-account-failover)
