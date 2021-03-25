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

# Cannot Convert to Geo Replication type with large file shares enabled

<!--issueDescription-->
Storage account **<!--$Resourcename-->[Resourcename]<!--/$Resourcename-->** cannot change to geo replication type **<!--$TargetReplicationType-->[TargetReplicationType]<!--/$TargetReplicationType-->** because it has large file shares enabled. Large file shares are currently supported only for LRS and ZRS replication types.
<!--/issueDescription-->

## **Recommended Steps**

* Create another Geo redundant storage account and manually migrate your data.

 **Recommended Documents**

* [Large file share restrictions](https://docs.microsoft.com/azure/storage/files/storage-files-how-to-create-large-file-share?tabs=azure-portal#restrictions)
* [Storage account overview](https://docs.microsoft.com/azure/storage/common/storage-account-overview)



