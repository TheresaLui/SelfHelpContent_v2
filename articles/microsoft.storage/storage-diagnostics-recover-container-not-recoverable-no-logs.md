<properties
pageTitle="Cannot find deletion logs for deleted blob container(s)"
description="Cannot find deletion logs for deleted blob container(s)"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_blobContainer_recovery_cannot_noLog"
diagnosticScenario="Storage Blob Container(s) is not recoverable since no deletion log was found"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Unable to recover Blob Container
<!--issueDescription-->
Microsoft Azure sincerely apologizes that we are unable to recover deleted blob container(s).
<!--/issueDescription-->

### Blob container(s) does not exist
The following blob container(s) in storage account _**<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**_ are not recoverable because we cannot find deletion log for them between **<!--$LogSearchStartTime-->[LogSearchStartTime]<!--/$LogSearchStartTime-->** and **<!--$LogSearchEndTime-->[LogSearchEndTime]<!--/$LogSearchEndTime-->**. Any container(s) that was deleted at an earlier time are also not recoverable. As part of our [data privacy guarantee](https://www.microsoft.com/TrustCenter/Privacy/default.aspx), we ensure that data deleted by our customer is eventually overwritten. These blob container(s) and all their contents were cleaned up after deletion and is no longer recoverable by Azure:<br>

<!--$DeletionInfo_ContainersNotExist-->[DeletionInfo_ContainersNotExist]<!--/$DeletionInfo_ContainersNotExist-->


### Active blob container(s) exist
The following blob container(s) already exist in storage account _**<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**_ which means that they were either not deleted or has been recreated with the same name. It is not possible for us to recover a container with the same name as another container in the  storage account:<br>

<!--$DeletionInfo_ContainersActive-->[DeletionInfo_ContainersActive]<!--/$DeletionInfo_ContainersActive-->

Please follow our [best practices for protecting your data](https://docs.microsoft.com/azure/storage/common/storage-disaster-recovery-guidance?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#best-practices-for-protecting-your-data) to ensure that accidentally deleted content can be recovered in the future.
