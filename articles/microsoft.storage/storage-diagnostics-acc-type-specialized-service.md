<properties
pageTitle="Specialized storage account only supports one service type"
description="Specialized storage account only supports one service type"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_acct_type_specialized_service"
diagnosticScenario="Specialized storage account only supports one service type"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Upgrade scenario not supported for storage account type

<!--issueDescription-->
Storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** is a **<!--$ResourceKind-->[ResourceKind]<!--/$ResourceKind-->** account which only supports <!--$SupportedServices-->[SupportedServices]<!--/$SupportedServices-->.
<!--/issueDescription-->

## **Recommended Steps**

To use other storage services, please create:

1. [File Storage account](https://azure.microsoft.com/blog/premium-files-pushes-azure-files-limits-by-100x/) for premium files data
2. [Block Blob account]( https://azure.microsoft.com/blog/introducing-azure-premium-blob-storage-limited-public-preview/) for premium block and append blob data
3. [General-purpose v2 premium account](https://docs.microsoft.com/azure/storage/common/storage-account-overview#general-purpose-v2-accounts) for premium disk and page-blob data
4. [General-purpose v2 standard account](https://docs.microsoft.com/azure/storage/common/storage-account-overview#general-purpose-v2-accounts) for all standard storage services
