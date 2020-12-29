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
The File Open/Close API transactions in storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** are high in proportion to the overall set of File API transactions. Please validate if this pattern of high File Open/Close API transactions is applicable for your workload as this could be be potentially the root cause for latency issues.
<!--/issueDescription-->

## **Recommended Steps**

* Refer to the [Azure Files scale targets](https://docs.microsoft.com/azure/storage/files/storage-files-scale-targets#file-share-and-file-scale-targets) to learn more about the scalability targets