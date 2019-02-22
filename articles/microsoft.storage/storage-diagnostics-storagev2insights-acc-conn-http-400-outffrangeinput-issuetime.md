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
cloudEnvironments="public"
/>

# One or more parameters in the storage request was out of range. 
<!--issueDescription-->
Some requests to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** failed as one of the request parameters was out of range between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** and **<!--$EndTime-->[EndTime]<!--/$EndTime-->**. <br><br> Sample list of requests that failed:<br>**<!--$IpParameterErrorRequestUrl-->[IpParameterErrorRequestUrl]<!--/$IpParameterErrorRequestUrl-->**
<!--/issueDescription-->

## **Recommended steps** 

Storage request parameters should have valid value. To resolve this issue, perform the following steps:
1. Refer below articles to specify a valid value for the request paramters found to be out of range above. 

   * [Request Headers](https://docs.microsoft.com/rest/api/storageservices/get-blob-service-properties#request-headers)
   * [Specifying Headers](https://docs.microsoft.com/rest/api/storageservices/authorize-with-shared-key#Subheading1)

2. Parameters like date and api-version are a common cause of the error. 

   * [Azure storage service version](https://docs.microsoft.com/rest/api/storageservices/versioning-for-the-azure-storage-services) - It is a required parameter. Microsoft Azure storage services support multiple versions. To make a request against the storage services, you must specify the version that you want to use for that operation, unless the request is anonymous. Refer [Previous Azure Storage service versions](https://docs.microsoft.com/rest/api/storageservices/previous-azure-storage-service-versions) for older versions of the API.
   * Date - It's a required parameter. Specify the date in Coordinated Universal Time (UTC) for the request. 