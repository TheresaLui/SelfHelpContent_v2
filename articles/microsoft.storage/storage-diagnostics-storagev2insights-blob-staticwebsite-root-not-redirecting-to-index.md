<properties
pageTitle="Static Website Root not redirecting to the page set for index document"
description="Static Website Root not redirecting to the page set for index document"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_blob_staticwebsite_root_not_redirecting_to_index_document"
diagnosticScenario="Static Website Root not redirecting to the page set for index document"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Why is Root not redirecting to the page set for "index document name"?

<!--issueDescription-->
Ensure the name and extension as set in the file name on portal is the exact same of the file in the $web container including case sensitivity. For Static Website file names along with extensions are case sensitive even though served over HTTP, therefore index.html != Index.html.
<!--/issueDescription-->

