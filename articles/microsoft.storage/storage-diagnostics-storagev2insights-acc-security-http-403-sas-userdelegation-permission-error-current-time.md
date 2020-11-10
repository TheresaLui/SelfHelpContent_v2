<properties
pageTitle="Connections to storage account endpoint were blocked due to user delegation SAS token failures"
description="Connections to storage account endpoint were blocked due to user delegation SAS token failures"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_acc_security_http_403_userdelegation_sas_permission_error_current_time"
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

No __user delegation SAS__ token auth failures were found for **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** around the issue time **<!--$IssueTimestamp-->[IssueTimestamp]<!--/$IssueTimestamp-->**.

It's possible that there were no __user delegation SAS__ auth failures during the time provided or it's beyond the retention period of storage logs. If the time period was not correct, please rerun the insight with the correct time.<br> However, some __user delegation SAS token__ auth failures were found for the current time **<!--$CurrentTimestamp-->[CurrentTimestamp]<!--/$CurrentTimestamp-->** that might be of interest.

**Sample list of blocked requests with failure reason**

<!--$SampleRequestTable-->[SampleRequestTable]<!--/$SampleRequestTable-->

<!--/issueDescription-->

**Note**: There may be additional client IPs for which requests were blocked. To get the exhaustive list, review the [storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging).

## **Recommended Steps**

Storage requests using __user delegation SAS__ to authenticate should pass a valid, unexpired token with right permissions to perform the intended operation.

Please look at the reason above and modify the SAS token accordingly.

## **Recommended Documents**

* [SAS error codes](https://docs.microsoft.com/rest/api/storageservices/sas-error-codes)
* Create a user delegation SAS:

  * [REST API](https://docs.microsoft.com/rest/api/storageservices/create-user-delegation-sas)
  * [PowerShell](https://docs.microsoft.com/azure/storage/blobs/storage-blob-user-delegation-sas-create-powershell)
  * [Azure CLI](https://docs.microsoft.com/azure/storage/blobs/storage-blob-user-delegation-sas-create-cli)
  * [.NET](https://docs.microsoft.com/azure/storage/blobs/storage-blob-user-delegation-sas-create-dotnet)

* [User delegation key](https://docs.microsoft.com/rest/api/storageservices/get-user-delegation-key#authorization)
