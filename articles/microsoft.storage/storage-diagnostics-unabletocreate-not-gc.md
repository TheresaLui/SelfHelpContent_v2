<properties
pageTitle="Unable to create storage account with the same name as deleted account"
description="Deleted storage account with the same name has not been GC"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_acc_unableToCreate_notGC"
diagnosticScenario="Account cannot be created because deleted account with the same name has not been GC"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Unable to create storage account with the same name as recently deleted account

<!--issueDescription-->
Another storage account with the name **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** was recently deleted and is blocking account creation.<!--/issueDescription--> [Storage account name must be unique](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-storage-account-name-errors#cause), so a new storage account with the same name cannot be created until after the old account has been cleaned up in the backend. This cleanup can take up to 14 days, but we have now triggered force cleanup of the deleted account when you submitted this support case which usually completes in 3 hours. You can either retry account creation with the same name after _<!--$FastGCApproxEndTime-->[FastGCApproxEndTime]<!--/$FastGCApproxEndTime--> UTC_ or create a new storage account with a different name now.


