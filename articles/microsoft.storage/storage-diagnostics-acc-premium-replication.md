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
Storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** with **<!--$AccountType-->[AccountType]<!--/$AccountType-->** type and premium performance tier can only support LRS (Locally Redundant Storage) replication types.<br>
Azure Premium Storage accounts in Classic, General purpose v1, and General purpose v2 types do not support GRS, RA-GRS, GZRS, or RA-GZRS replication types at this time.<br>
Azure **Premium BlockBlobStorage** and **Premium FileStorage** accounts can support ZRS replication type only in [certain regions](https://docs.microsoft.com/azure/storage/common/storage-redundancy#zone-redundant-storage).
<!--/issueDescription-->

## **Recommended Documents**
* [Best practices for backup and disaster recovery of IaaS disks](https://docs.microsoft.com/azure/virtual-machines/windows/backup-and-disaster-recovery-for-azure-iaas-disks)
* [Premium Storage Features](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features)
* [Azure Storage redundancy](https://docs.microsoft.com/azure/storage/common/storage-redundancy)
