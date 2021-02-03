<properties
pageTitle="Classic account cannot failover"
description="Classic account cannot failover"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="Sijia"
ms.author="siz"
displayOrder=""
articleId="Storagev2insights_Failover_ClassicAccountCannotFailover"
diagnosticScenario="Classic account cannot failover"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Classic account cannot failover

<!--issueDescription-->
Account Failover does not support classic storage accounts. Account failover is available for general-purpose v1, general-purpose v2, and Blob storage account types with Azure Resource Manager deployments. For storage accounts that are configured for RA-GRS and GRS, failover is supported for all public regions but is not available in sovereign or national clouds at this time. For storage accounts that are configured for GZRS and RA-GZRS, failover is supported only in certain regions.
<!--/issueDescription-->

## **Recommended Documents**

* [Disaster recovery and account failover in Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance)
* [Supported Regions for GZRS and RA-GZRS accounts](https://docs.microsoft.com/azure/storage/common/storage-redundancy#geo-zone-redundant-storage)
