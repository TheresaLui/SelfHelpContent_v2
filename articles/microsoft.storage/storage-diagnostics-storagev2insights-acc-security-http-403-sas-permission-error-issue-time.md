<properties
pageTitle="Connections to storage account endpoint were blocked due to SAS token failures"
description="Connections to storage account endpoint were blocked due to SAS token failures"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_acc_security_http_403_sas_permission_error_issue_time"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Connections to storage account endpoint were blocked due to SAS token failures
<!--issueDescription-->
Some requests to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** were blocked between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** and **<!--$EndTime-->[EndTime]<!--/$EndTime-->** as the SAS token presented was not valid to perform the operation. 

**Sample list of blocked requests with failure reason:**

<!--$SampleRequestTable-->[SampleRequestTable]<!--/$SampleRequestTable-->

<!--/issueDescription-->


**Note**: There may be more client IPs for which requests were blocked. To view the exhaustive list, review the [storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging).

## **Recommended Steps**

Storage requests using SAS to authenticate should pass a valid unexpired token with right permissions to perform the intended operation.

Please look at the reason above and modify the SAS token accordingly. Below are some documents that might assist you.

## **Recommended Documents** 

* [SAS error codes](https://docs.microsoft.com/rest/api/storageservices/sas-error-codes)
* [Create an account SAS](https://docs.microsoft.com/rest/api/storageservices/create-account-sas)
* [Create a service SAS](https://docs.microsoft.com/rest/api/storageservices/create-service-sas)

