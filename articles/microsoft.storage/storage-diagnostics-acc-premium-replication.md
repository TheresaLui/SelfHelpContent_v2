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
Storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**  is configured to use premium performance tier, which only supports LRS (Locally Redundant Storage) replication types. Azure Premium Storage accounts do not support ZRS, GRS, or RA-GRS replication type at this time.
<!--/issueDescription-->

## **Recommended Documents**
* [Best practices for backup and disaster recovery of IaaS disks](https://docs.microsoft.com/azure/virtual-machines/windows/backup-and-disaster-recovery-for-azure-iaas-disks)
* [Premium Storage Features](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features)
