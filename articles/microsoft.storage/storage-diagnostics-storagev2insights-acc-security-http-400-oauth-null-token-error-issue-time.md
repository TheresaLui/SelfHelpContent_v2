<properties
pageTitle="Connections to storage account endpoint were blocked due to Null oAuth token"
description="Connections to storage account endpoint were blocked due to Null oAuth token"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_acc_security_http_400_oauth_null_token_error_issue_time"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# One or more parameters in the storage request was out of range. 
<!--issueDescription-->
Some connections to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** were blocked between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** and **<!--$EndTime-->[EndTime]<!--/$EndTime-->** as they had a Null oAuth bearer token. <br><br> Sample list of requests were blocked<br>**<!--$RequestUrl-->[RequestUrl]<!--/$RequestUrl-->**
<!--/issueDescription-->

Storage requests using RBAC to authenticate should pass a valid oAuth token with right permisions to perform the intended operation.

## **Recommended steps** 
Find the current permission and the required permission for the user (OID) in the failure description above. 

1. Your Azure AD admin would be able to map the OID (GUID representing the user) to the the person (firstname,lastname) or virtual machine with MSI. 
2. Your account admin needs to provide the required permissions to the user  by referring the links below. 

   * [Manage access rights to Azure Blob and Queue data with RBAC](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac)
   * [Authenticate with Azure Active Directory from an application for access to blobs and queues](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-app)