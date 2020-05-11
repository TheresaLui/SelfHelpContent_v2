<properties
pageTitle="Storage Account was throttled due to single partition limit being exceeded"
description="Storage Account was throttled due to single partition limit being exceeded"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="AngshumanNayakMSFT"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_single_partition_limit_exceeded_throttling"
diagnosticScenario="Storage IOPS overlimit"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="storage"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** was throttled due to single partition limit being exceeded
<!--issueDescription-->

The partition overload was caused by the access pattern of the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**<!--/issueDescription--> and we recommend that you follow the [partition naming convention](https://docs.microsoft.com/azure/storage/common/storage-performance-checklist#subheading47) to reduce the frequency of partition split. Partition split can result in storage operation failures and increased latency.

We also recommended that you configure [storage analytics](https://docs.microsoft.com/azure/storage/common/storage-analytics) to monitor your storage account. This will help you to track your application's access pattern and enable you to take corrective steps to prevent similar issues in the future. For further information, please refer [monitoring, diagnostics, and troubleshooting guide for Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentThrottlingError).


