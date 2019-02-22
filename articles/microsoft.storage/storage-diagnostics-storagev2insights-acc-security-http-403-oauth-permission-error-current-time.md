<properties
pageTitle="Connections to storage account endpoint were blocked due to insufficient permission in the oAuth token presented"
description="Connections to storage account endpoint were blocked due to insufficient permission in the oAuth token presented"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_acc_security_http_403_oauth_permission_error_current_time"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# Connections to storage account endpoint were blocked due to insufficient permission in the oAuth token presented 
<!--issueDescription-->
We found some requests to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** that were blocked, as the permissions presented in oAuth bearer token were not sufficient for the operation performed, at a much recent time **<!--$CurrentTimestamp-->[CurrentTimestamp]<!--/$CurrentTimestamp-->** that might be of interest. Unfortunately we couldn't find oAuth token authorization failure reason for requests to **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** at **<!--$IssueTimestamp-->[IssueTimestamp]<!--/$IssueTimestamp-->**. Either the time period provided was incorrect or it's beyond the retention period of storage logs.<br><br> Sample list of requests were blocked:<br>**<!--$RequestUrl-->[RequestUrl]<!--/$RequestUrl-->**
<!--/issueDescription-->

There might be more client IPs for which requests were blocked, to get the exhaustive list you should look at [storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging).

## **Recommended steps** 

Storage requests using RBAC to authenticate should pass an oAuth token with right permisions to perform the intended operation. You can find the current permission and the required permission for the user (OID) in the failure description. 

1. Your Azure AD admin would be able to map the OID (GUID representing the user) to the the person (firstname,lastname) or virtual machine with MSI. 

2. Your account admin needs to provide the required permissions to the user  by referring the links below. 

   * [Manage access rights to Azure Blob and Queue data with RBAC](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac)
   * [Authenticate with Azure Active Directory from an application for access to blobs and queues](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-app)