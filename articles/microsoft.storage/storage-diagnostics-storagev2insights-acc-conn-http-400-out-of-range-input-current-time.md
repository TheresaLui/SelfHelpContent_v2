<properties
pageTitle="One or more parameters in the storage request was out of range"
description="One or more parameters in the storage request was out of range"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
displayOrder=""
articleId="Storagev2insights_acc_conn_HTTP_400_OutOfRangeInput_currentTime"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# One or more parameters in the storage request was out of range. 
<!--issueDescription-->
We found an **_OutOfRangeInput_** error, caused when one of the request parameter is out of range, at a much recent time **<!--$CurrentTimestamp-->[CurrentTimestamp]<!--/$CurrentTimestamp-->** that might be of interest. Unfortunately we couldn't find any requests resulting in **_OutOfRangeInput_** for the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** at **<!--$IssueTimestamp-->[IssueTimestamp]<!--/$IssueTimestamp-->**. Either the time period provided was incorrect or it's beyond the retention period of storage logs.<br><br> Sample list of requests that failed:<br>**<!--$IP_Parameter_Error_RequestUrl-->[IP_Parameter_Error_RequestUrl]<!--/$IP_Parameter_Error_RequestUrl-->**
<!--/issueDescription-->

Request parameters like api-version and date are a common cause of this error. 
   * Azure storage service version - It is a required parameter. Microsoft Azure storage services support multiple versions. To make a request against the storage services, you must specify the [storage service version](https://docs.microsoft.com/rest/api/storageservices/versioning-for-the-azure-storage-services) that you want to use for that operation, unless the request is anonymous. Refer [Previous Azure Storage service versions](https://docs.microsoft.com/rest/api/storageservices/previous-azure-storage-service-versions) for older versions of the API.
   * Date - It's a required parameter and you can specify it either in the standard HTTP/HTTPS Date header or in the x-ms-date header. Specify the date in [Coordinated Universal Time (UTC)](https://docs.microsoft.com/rest/api/storageservices/formatting-datetime-property-values) for the request. Storage service also ensures that a request is no older than 15 minutes by the time it reaches the service to prevent replay attacks. 

## **Recommended steps** 

Storage request parameters should have valid value. To resolve this issue, perform the following steps:
1. Refer below articles to specify a valid value for the request paramters found to be out of range above. 
   * [Request Headers](https://docs.microsoft.com/rest/api/storageservices/get-blob-service-properties#request-headers)
   * [Specifying Headers](https://docs.microsoft.com/rest/api/storageservices/authorize-with-shared-key#Subheading1)