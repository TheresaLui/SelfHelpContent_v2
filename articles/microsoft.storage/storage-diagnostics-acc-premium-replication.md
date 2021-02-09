<properties
pageTitle="Premium storage account only supports LRS replication type"
description="Only LRS replication type is supported"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
articleId="Storagev2insights_acct_type_premium_replication"
diagnosticScenario="Premium storage account only supports LRS replication type"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Premium storage account only supports LRS replication type

<!--issueDescription-->
Storage account <!--$ResourceName-->[ResourceName]<!--/$ResourceName--> with <!--$AccountType-->[AccountType]<!--/$AccountType--> type and premium performance tier can only support locally redundant storage (LRS) replication types.<br>
At this time, Azure Premium Storage accounts (Classic, General purpose v1, and General purpose v2 types) do not support GRS, RA-GRS, GZRS, or RA-GZRS replication types.<br>
Azure **Premium BlockBlobStorage** and **Premium FileStorage** accounts support the ZRS replication type only in certain regions.
<!--/issueDescription-->

## **Recommended Documents**
* [Best practices for backup and disaster recovery of IaaS disks](https://docs.microsoft.com/azure/virtual-machines/windows/backup-and-disaster-recovery-for-azure-iaas-disks)
* [Premium storage features](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features)
* [Azure Storage redundancy](https://docs.microsoft.com/azure/storage/common/storage-redundancy)
