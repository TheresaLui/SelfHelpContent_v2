<properties
pageTitle="Static Website integration with Storage Firewall"
description="Static Website integration with Storage Firewall"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_blob_staticwebsite_firewall_integration"
diagnosticScenario="Static Website integration with Storage Firewall"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Does storage firewall work with Static Website?

<!--issueDescription-->
Storage firewall settings don't affect the public web endpoint exposed by Static Website.
<!--/issueDescription-->

## **Recommended Steps**

The storage account has a built in **[firewall](https://docs.microsoft.com/azure/storage/common/storage-network-security)** feature available, but this will not affect the public web endpoint. Even with firewall enabled the web endpoint could be publicly accessed by anyone connected to the internet. However enabling firewall restricts access to the other storage endpoints like blobs, files, dfs, table and queue.