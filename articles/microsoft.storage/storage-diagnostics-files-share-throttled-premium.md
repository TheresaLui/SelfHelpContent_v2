<properties
pageTitle="Azure premium file share was throttled"
description="Azure premium file share was throttled"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="kartikshah9"
ms.author="kashah"
displayOrder=""
articleId="Files_FileShareThrottled_premium"
diagnosticScenario="SuccessWithThrottling response type"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageFiles"
/>

# Azure file share was throttled

<!--issueDescription-->
An Azure file share in storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** was throttled because the IOPS (transactions) limit was reached. 
<!--/issueDescription-->

## **Recommended Steps**

* Refer to the [Azure Files scale targets](https://docs.microsoft.com/azure/storage/files/storage-files-scale-targets#file-share-and-file-scale-targets) to learn more about the scalability targets
* If the file share is a premium file share, increase the provisioned file share size to increase the IOPS limit
* Refer to the [troubleshooting Azure Files performance](https://docs.microsoft.com/azure/storage/files/storage-troubleshooting-files-performance) section for workarounds to common performance issues

