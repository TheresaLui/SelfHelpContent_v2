<properties
pageTitle="Cannot change account to geo redudancy type"
description="Cannot change account to geo redudancy type due to large file shares enabled"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="leakkari"
ms.author="leakkari"
displayOrder=""
articleId="Storagev2insights_acct_cannot_change_replication_largefilesharesenabled"
diagnosticScenario="Cannot change account to geo redudancy type"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_AccountManagement"
/>

# Migrate to ZRS within a region

<!--issueDescription-->
Storage account **{ResourceName}** cannot change to geo replication type **{TargetReplicationType}** because it has large file shares enabled. Large file shares is currently only supported for LRS and ZRS replication types, please see [Restrictions](https://docs.microsoft.com/azure/storage/files/storage-files-how-to-create-large-file-share?tabs=azure-portal#restrictions).
<!--/issueDescription-->

## **Recommended Steps**

* Create another Geo redundant storage account and manually migrate your data.
* [Storage account overview](https://docs.microsoft.com/en-us/azure/storage/common/storage-account-overview)



