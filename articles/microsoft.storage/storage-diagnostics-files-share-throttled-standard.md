<properties
pageTitle="Azure standard file share was throttled"
description="Azure standard file share was throttled"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="kartikshah9"
ms.author="kashah"
displayOrder=""
articleId="Files_FileShareThrottled_standard"
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
* Larger file shares support upto 10,000 IOPS per share. Please consider enabling [larger file shares](https://docs.microsoft.com/azure/storage/files/storage-files-planning#enable-standard-file-shares-to-span-up-to-100-tib) to improve performance. 
* Premium file shares support upto 100,000 IOPS per share. Please consider enabling [premium file shares](https://docs.microsoft.com/azure/storage/files/storage-how-to-create-premium-fileshare)to improve performance
* Refer to the [troubleshooting Azure Files performance](https://docs.microsoft.com/azure/storage/files/storage-troubleshooting-files-performance) section for workarounds to common performance issues
