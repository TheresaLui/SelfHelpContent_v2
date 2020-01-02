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
cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
/>

# Why am I getting 404 from Static Website?

<!--issueDescription-->
Some of the common causes of getting an HTTP 404 error are as below
- Use the web endpoint like https://myaccount.z5.web.core.windows.net/index.html endpoint instead of the blob endpoint https://myaccount.blob.core.windows.net/$web/index.html . </br> You can find the actual endpoint on the Azure portal.</br>
- For Static Website file names along with extensions are case sensitive even though served over HTTP, therefore index.html != Index.html.
- CDN endpoint might take time to provision. Please wait till 90 mins after you provisioned new CDN for the propagation to happen.
<!--/issueDescription-->
