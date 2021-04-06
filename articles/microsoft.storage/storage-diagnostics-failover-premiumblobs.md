<properties
pageTitle="Cannot failover due to existing premium block blobs"
description="Cannot failover due to existing premium block blobs"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="Lea"
ms.author="leakkari"
displayOrder=""
articleId="Storagev2insights_Failover_PremiumBlockBlobsCannotFailover"
diagnosticScenario="ADLS Gen2 account cannot failover"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Storage account containing premium block blobs

<!--issueDescription-->
Storage account {ResourceName} cannot failover because it contains premium block blobs. Premium block blobs do not currently support geo-redundancy.
<!--/issueDescription-->

## **Recommended Documents**
* [How to initiate storage account failover](https://docs.microsoft.com/azure/storage/common/storage-initiate-account-failover?tabs=azure-portal#prerequisites)
* [Disaster recovery and account failover in Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance)
* [Supported Regions for GZRS and RA-GZRS accounts](https://docs.microsoft.com/azure/storage/common/storage-redundancy#geo-zone-redundant-storage)
