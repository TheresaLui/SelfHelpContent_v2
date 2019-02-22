<properties
pageTitle="Connections to storage account endpoint were blocked due to insufficient permission in the oAuth token presented"
description="Connections to storage account endpoint were blocked due to insufficient permission in the oAuth token presented"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_acc_security_http_403_oauth_permission_error_issue_time"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# One or more parameters in the storage request was out of range. 
<!--issueDescription-->
Some requests to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** were blocked as the permissions presented in oAuth bearer token were not sufficient for the operation performed between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** and **<!--$EndTime-->[EndTime]<!--/$EndTime-->**.<br><br> Sample list of requests were blocked:<br>**<!--$RequestUrl-->[RequestUrl]<!--/$RequestUrl-->**
<!--/issueDescription-->

## **Recommended steps** 

Storage requests using RBAC to authenticate should pass an oAuth token with right permisions to perform the intended operation. You can find the current permission and the required permission for the user (OID) in the failure description. 

1. Your Azure AD admin would be able to map the OID (GUID representing the user) to either of the following. 

    * The person (firstname,lastname) 
    * The virtual machine with MSI 

2. Your account admin needs to provide the required permissions to the user  by referring the links below. 

   * [Manage access rights to Azure Blob and Queue data with RBAC](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac)
   * [Authenticate with Azure Active Directory from an application for access to blobs and queues](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-app)