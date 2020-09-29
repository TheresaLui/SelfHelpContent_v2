<properties
pageTitle="One or more parameters in the storage request was out of range"
description="One or more parameters in the storage request was out of range"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="Storagev2insights_acc_conn_HTTP_400_OutOfRangeInput_issueTime"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# One or more parameters in the storage request was out of range. 
<!--issueDescription-->
Some requests to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** failed, as one of the request parameters was out of range between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** and **<!--$EndTime-->[EndTime]<!--/$EndTime-->**. 

Sample list of requests that failed:
**<!--$IpParameterErrorRequestUrl-->[IpParameterErrorRequestUrl]<!--/$IpParameterErrorRequestUrl-->**
<!--/issueDescription-->

There may be more client IPs for which requests were blocked. To view the complete list, follow the steps to review the [storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging).

## **Recommended Steps** 

Storage request parameters should have valid value. 

1. Refer below articles to specify a valid value for the request parameters found to be out of range above:

   * [Request Headers](https://docs.microsoft.com/rest/api/storageservices/get-blob-service-properties#request-headers)
   * [Specifying Headers](https://docs.microsoft.com/rest/api/storageservices/authorize-with-shared-key#Subheading1)

2. Parameters like date and api-version are a common cause of the error:

   * [Azure storage service version](https://docs.microsoft.com/rest/api/storageservices/versioning-for-the-azure-storage-services) is a required parameter. Microsoft Azure storage services support multiple versions. To make a request against the storage services, you must specify the version that you want to use for that operation, unless the request is anonymous. Refer [Previous Azure Storage service versions](https://docs.microsoft.com/rest/api/storageservices/previous-azure-storage-service-versions) for older versions of the API.
   * Date is a required parameter. Specify the date in Coordinated Universal Time (UTC) for the request.
   
   
   
