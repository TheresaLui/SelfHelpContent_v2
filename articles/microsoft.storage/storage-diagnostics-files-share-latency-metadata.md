<properties
pageTitle="Azure file share high latency due to heavy metadata operations"
description="Azure file share high latency due to heavy metadata operations"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="kartikshah9"
ms.author="kashah"
displayOrder=""
articleId="StorageFileMetadataWorkloadInsight_heavymetadata"
diagnosticScenario="FileShare high latency due to heavy metadata"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageFiles"
/>

# Azure file share is facing high latency issues

<!--issueDescription-->
An Azure file share in storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** is facing high latency low throughput issues due to heavy metadata workload. 
<!--/issueDescription-->

## **Recommended Steps**

* Refer to the [Azure Files scale targets](https://docs.microsoft.com/azure/storage/files/storage-files-scale-targets#file-share-and-file-scale-targets) to learn more about the scalability targets
* Refer to the [Azure Files heavy meatadata workload workaround](https://docs.microsoft.com/azure/storage/files/storage-troubleshooting-files-performance#cause-2-metadatanamespace-heavy-workload) to mitigate latency issues
* If the file share is a standard file share, check if [larger file shares](https://docs.microsoft.com/azure/storage/files/storage-files-planning#onboard-to-larger-file-shares-standard-tier) is available in your region. Larger file shares support up to 10,000 IOPS per share.
