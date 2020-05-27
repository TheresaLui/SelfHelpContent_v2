<properties
pageTitle="Storage Account was throttled due to a scalability limit being exceeded"
description="Storage Account was throttled due to a scalability limit being exceeded"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="AngshumanNayakMSFT"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_ingress_egress_iops_throttling_aa"
diagnosticScenario="Storage IOPS overlimit"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="storage"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** was throttled due to a scalability limit being exceeded
<!--issueDescription-->
**<!--$AADescription-->[AADescription]<!--/$AADescription-->**
<!--/issueDescription-->

Refer [Azure Storage Scalability and Performance Targets](https://docs.microsoft.com/azure/storage/common/storage-scalability-targets) to know more about the various scalability targets. We recommended that you configure [storage analytics](https://docs.microsoft.com/azure/storage/common/storage-analytics) to monitor your storage account. This will help you to track your application's increased transaction or bandwidth usage and enable you to take corrective steps to prevent similar issues in the future. For further information, please refer [monitoring, diagnostics and troubleshooting guide for Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentThrottlingError).

