<properties
pageTitle="Unable to create storage account due to SRP throttling"
description="Unable to create storage account due to throttling"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_AccountCreationIssue_throttling"
diagnosticScenario="Unable to create storage account due to SRP throttling"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Unable to create storage account due to throttling

<!--issueDescription-->

Storage account <!--$ResourceName-->[ResourceName]<!--/$ResourceName--> creation failed at <!--$IssueTime-->[IssueTime]<!--/$IssueTime--> due to throttling on storage account management operations on subscription <!--$SubscriptionId-->[SubscriptionId]<!--/$SubscriptionId-->.
<!--/issueDescription-->

Please reduce [storage account management operations](https://docs.microsoft.com/rest/api/storagerp/storageaccounts) to meet [storage resource provider scale limit](https://docs.microsoft.com/azure/storage/common/storage-scalability-targets#storage-resource-provider-scale-limits) and retry storage account creation. 

## **Recommended Documents**

* [Storage resource provider scale limit](https://docs.microsoft.com/azure/storage/common/storage-scalability-targets#storage-resource-provider-scale-limits)
* [Storage account management operations](https://docs.microsoft.com/rest/api/storagerp/storageaccounts)

