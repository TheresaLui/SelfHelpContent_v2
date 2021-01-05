<properties
pageTitle="Azure file share Directory Open Close Transactions"
description="Azure file share directory Open Close Transactions"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="kartikshah9"
ms.author="kashah"
displayOrder=""
articleId="Files_FileShareDirectoryOpenCloseTransactions"
diagnosticScenario="FileShareDirectoryOpenCloseTransactions Scenario"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
ownershipId="StorageMediaEdge_StorageFiles"
/>

# Azure file share was throttled

<!--issueDescription-->
The File Open/Close API transactions in storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** are high in proportion to the overall set of File API transactions. Validate if this pattern of high File Open/Close API transactions is applicable for your workload, as this can potentially cause latency issues.
<!--/issueDescription-->

## **Recommended Steps**

* Refer to the [Azure Files scale targets](https://docs.microsoft.com/azure/storage/files/storage-files-scale-targets#file-share-and-file-scale-targets) to learn more about the scalability targets
* Refer to the [Azure Files extensive open/close operations causing latency workaround](https://docs.microsoft.com/azure/storage/files/storage-troubleshooting-files-performance#high-latencies-for-metadata-heavy-workloads-involving-extensive-openclose-operations) to mitigate latency issues
* Refer to the [Azure Files heavy metadata workload workaround](https://docs.microsoft.com/azure/storage/files/storage-troubleshooting-files-performance#cause-2-metadatanamespace-heavy-workload) to mitigate latency issues
* If the file share is a standard file share, check if [larger file shares](https://docs.microsoft.com/azure/storage/files/storage-files-planning#onboard-to-larger-file-shares-standard-tier) are available in your region. Larger file shares support up to 10,000 IOPS per share.
