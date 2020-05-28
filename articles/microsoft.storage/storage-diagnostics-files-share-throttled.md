<properties
pageTitle="Azure file share was throttled"
description="Azure file share was throttled"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="jeffpatt24"
ms.author="jeffpatt"
displayOrder=""
articleId="Files_FileShareThrottled"
diagnosticScenario="SuccessWithThrottling response type"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure file share was throttled

<!--issueDescription-->
An Azure file share in storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** was throttled because the IOPS (transactions) limit was reached. 
<!--/issueDescription-->

## **Recommended Steps**

* Refer to the [Azure Files scale targets](https://docs.microsoft.com/azure/storage/files/storage-files-scale-targets#file-share-and-file-scale-targets) to learn more about the scalability targets
* If the file share is a standard file share, check if [larger file shares](https://docs.microsoft.com/azure/storage/files/storage-files-planning#onboard-to-larger-file-shares-standard-tier) is available in your region. Larger file shares support up to 10,000 IOPS per share.
* If the file share is a premium file share, increase the provisioned file share size to increase the IOPS limit
* To learn more, see the [provisioned shares](https://docs.microsoft.com/azure/storage/files/storage-files-planning#provisioned-shares) section in the Azure Files planning guide
