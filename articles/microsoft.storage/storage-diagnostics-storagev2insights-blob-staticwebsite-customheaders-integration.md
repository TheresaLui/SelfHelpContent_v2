<properties
pageTitle="Static Website integration with custom headers"
description="Static Website integration with custom headers"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_blob_staticwebsite_custom_headers_integration"
diagnosticScenario="Static Website integration with custom headers"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# How to add Custom Headers and rules with Static Website?

<!--issueDescription-->
There is no direct support for custom headers with Static Website. However, the below steps will help achieve the same using CDN.
<!--/issueDescription-->

## **Recommended Steps**

Currently the way to configure Host header with Static Website is to use **[Azure CDN - Verizon Premium](https://docs.microsoft.com/azure/cdn/cdn-verizon-premium-rules-engine)** on top of Azure Blob, using the Rules engine and accessing the CDN end point. 

Please provide us your feedback **[here](https://feedback.azure.com/forums/217298-storage/suggestions/34959124-allow-adding-headers-to-static-website-hosting-in)**.
