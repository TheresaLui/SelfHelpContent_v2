<properties
pageTitle="Premium storage account only supports one service type"
description="Premium storage account only supports one service type"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_acct_type_premium"
diagnosticScenario="Premium storage account only supports one service type"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>

# <!--$ResourceKind-->[ResourceKind]<!--/$ResourceKind--> storage account only supports <!--$SupportedServices-->[SupportedServices]<!--/$SupportedServices-->

<!--issueDescription-->
Storage account **<!--$DestinationResourceName-->[DestinationResourceName]<!--/$DestinationResourceName-->** is a **<!--$ResourceKind-->[ResourceKind]<!--/$ResourceKind-->** account which only supports <!--$SupportedServices-->[SupportedServices]<!--/$SupportedServices-->. Only **<!--$SupportedData-->[SupportedData]<!--/$SupportedData-->** data can be migrated from **<!--$SourceResourceName-->[SourceResourceName]<!--/$SourceResourceName-->** to **<!--$DestinationResourceName-->[DestinationResourceName]<!--/$DestinationResourceName-->**.

Please create:
1. [File Storage account](https://azure.microsoft.com/blog/premium-files-pushes-azure-files-limits-by-100x/) for premium files data
2. [Block Blob account]( https://azure.microsoft.com/blog/introducing-azure-premium-blob-storage-limited-public-preview/) for premium block and append blob data
3. [General-purpose v2 account](https://docs.microsoft.com/azure/storage/common/storage-account-overview#general-purpose-v2-accounts) for premium disk and page-blob data
<!--/issueDescription-->
