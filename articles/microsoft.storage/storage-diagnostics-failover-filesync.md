<properties
pageTitle="Storage account cannot failover - File Sync"
description="Storage account cannot failover - File Sync"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="Lea"
ms.author="leakkari"
displayOrder=""
articleId="Storagev2insights_Failover_FileSyncAccountCannotFailover"
diagnosticScenario="Storage account cannot failover - File Sync"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Storage account cannot failover - File Sync
<!--issueDescription-->
We detected that storage account {ResourceName} is a FileStorage/General purpose version 2 account. Azure File Sync does not support storage account failover. Storage accounts containing Azure file shares being used as cloud endpoints in Azure File Sync should not be failed over. Doing so will cause sync to stop working and may also cause unexpected data loss in the case of newly tiered files.
<!--/issueDescription-->

## **Recommended Documents**
* [How to initiate storage account failover](https://docs.microsoft.com/azure/storage/common/storage-initiate-account-failover?tabs=azure-portal#prerequisites)
* [Disaster recovery and account failover in Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance)
* [Supported Regions for GZRS and RA-GZRS accounts](https://docs.microsoft.com/azure/storage/common/storage-redundancy#geo-zone-redundant-storage)
