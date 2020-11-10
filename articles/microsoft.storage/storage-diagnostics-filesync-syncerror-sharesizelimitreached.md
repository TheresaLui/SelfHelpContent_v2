<properties
pageTitle="Sync error - share size limit reached"
description="Sync error - share size limit reached"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="sikoo"
ms.author="passap"
displayOrder=""
articleId="FileSync_SyncError_ShareSizeLimitReached"
diagnosticScenario="Sync error - share size limit reached"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# File Sync failed with error <!--$ErrorString-->[ErrorString]<!--/$ErrorString-->: the Azure File Share storage limit has been exceeded.

<!--issueDescription-->
Azure File Sync failed with error **<!--$ErrorString-->[ErrorString]<!--/$ErrorString-->** due to file share limit exceeded.
<!--/issueDescription-->

The [Azure File Share storage limit](https://docs.microsoft.com/azure/azure-subscription-service-limits#azure-files-limits) has been exceeded. Please follow the steps below to avoid sync failures in the future:

1. Check if there is a quota set that restricts the File Share below the [current maximum size of 5TB](https://docs.microsoft.com/azure/azure-subscription-service-limits#storage-limits). If so, increase the quota. <br>
2. Consider making each subfolder you are currently syncing a Server Endpoint in a separate Sync Group. This way each subfolder will sync to individual Azure File Shares. 


