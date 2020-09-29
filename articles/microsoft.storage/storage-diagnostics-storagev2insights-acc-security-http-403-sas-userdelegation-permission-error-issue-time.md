<properties
pageTitle="Connections to storage account endpoint were blocked due to user delegation SAS token failures"
description="Connections to storage account endpoint were blocked due to user delegation SAS token failures"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_acc_security_http_403_userdelegation_sas_permission_error_issue_time"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Connections to storage account endpoint were blocked due to **User Delegation SAS** token failures
<!--issueDescription-->
Some requests to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** were blocked between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** and **<!--$EndTime-->[EndTime]<!--/$EndTime-->** as the __user delegation SAS__ token presented was not valid to perform the operation.

**Sample list of blocked requests with failure reason:**

<!--$SampleRequestTable-->[SampleRequestTable]<!--/$SampleRequestTable-->

<!--/issueDescription-->


**Note**: There may be more client IPs for which requests were blocked. To view the exhaustive list, review the [storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging).

## **Recommended Steps**

Storage requests using __user delegation SAS__ to authenticate should pass a valid unexpired token with right permissions to perform the intended operation.

Please look at the reason above and modify the __user delegation SAS__ token accordingly. Below are some documents that might assist you.

## **Recommended Documents**

* [SAS error codes](https://docs.microsoft.com/rest/api/storageservices/sas-error-codes)
* Create a user delegation SAS
  * [REST API](https://docs.microsoft.com/rest/api/storageservices/create-user-delegation-sas)
  * [PowerShell](https://docs.microsoft.com/azure/storage/blobs/storage-blob-user-delegation-sas-create-powershell)
  * [Azure CLI](https://docs.microsoft.com/azure/storage/blobs/storage-blob-user-delegation-sas-create-cli)
  * [.NET](https://docs.microsoft.com/azure/storage/blobs/storage-blob-user-delegation-sas-create-dotnet)
* [User delegation key](https://docs.microsoft.com/rest/api/storageservices/get-user-delegation-key#authorization)
