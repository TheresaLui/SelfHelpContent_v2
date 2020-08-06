<properties
pageTitle="Static Website common causes for http 404 error"
description="Static Website common causes for http 404 error"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_blob_staticwebsite_common_causes_for_404_error"
diagnosticScenario="Static Website common causes for http 404 error"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Why am I getting 404 from Static Website?

<!--issueDescription-->
Please see the Recommended Steps to resolve HTTP 404 errors with Static Website.
<!--/issueDescription-->

## **Recommended Steps**

Some of the common causes of getting an HTTP 404 error are as below:

- Use a web endpoint such as *https://myaccount.z5.web.core.windows.net/index.html* instead of a blob endpoint like *https://myaccount.blob.core.windows.net/$web/index.html*. You can find the actual endpoint on the Azure portal.
- For Static Website file names along with extensions are case sensitive even though served over HTTP, therefore index.html != Index.html
- CDN endpoint might take time to provision. Please wait 90 mins after you provisioned new CDN for the propagation to happen.
