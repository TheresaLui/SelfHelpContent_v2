<properties
pageTitle="ADLS Gen 2 account cannot failover"
description="ADLS Gen 2 account cannot failover"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="Lea"
ms.author="leakkari"
displayOrder=""
articleId="Storagev2insights_Failover_ADLSGen2AccountCannotFailover"
diagnosticScenario="ADLS Gen2 account cannot failover"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# ADLS Gen2 Storage Account Failover

<!--issueDescription-->
Storage account {ResourceName} cannot failover because ADLS Gen2 storage accounts (accounts that have hierarchical namespace enabled) are not supported at this time. Account failover is available for general-purpose v1, general-purpose v2, and Blob storage account types with Azure Resource Manager deployments.
<!--/issueDescription-->

## **Recommended Documents**
* [How to initiate storage account failover](https://docs.microsoft.com/azure/storage/common/storage-initiate-account-failover?tabs=azure-portal#prerequisites)
* [Disaster recovery and account failover in Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance)
* [Supported Regions for GZRS and RA-GZRS accounts](https://docs.microsoft.com/azure/storage/common/storage-redundancy#geo-zone-redundant-storage)
