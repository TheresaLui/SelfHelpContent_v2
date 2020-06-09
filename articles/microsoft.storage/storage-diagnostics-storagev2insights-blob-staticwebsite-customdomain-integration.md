<properties
pageTitle="Static Website integration with Custom Domain"
description="Static Website integration with Custom Domain"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_blob_staticwebsite_custom_domain_integration"
diagnosticScenario="Static Website integration with Custom Domain"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# How to use Custom Domain with Static Website?

<!--issueDescription-->
There is no direct support for custom domains with Static Website. However, the recommended steps will help achieve the same using CDN.
<!--/issueDescription-->

## **Recommended Steps**

* Currently, the way to configure **[custom domain](https://docs.microsoft.com/azure/storage/blobs/storage-blob-static-website-custom-domain#enable-custom-domain-and-ssl)** with Static Website is to use **[Azure CDN](https://docs.microsoft.com/azure/storage/blobs/storage-https-custom-domain-cdn)**. CDN provides consistent low latencies to your website from anywhere in the world. While CDN comes at an additional cost, we have made it a compelling option with the removal of storage egress cost.
