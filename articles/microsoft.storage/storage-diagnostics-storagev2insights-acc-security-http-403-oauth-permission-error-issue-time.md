<properties
pageTitle="Connections to storage account endpoint were blocked due to insufficient permission in the oAuth token presented"
description="Connections to storage account endpoint were blocked due to insufficient permission in the oAuth token presented"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_acc_security_http_403_oauth_permission_error_issue_time"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Connections to storage account endpoint were blocked due to insufficient permission in the oAuth token presented 

<!--issueDescription-->
Some requests to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** were blocked as the permissions presented in oAuth bearer token were not sufficient for the operation performed between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** and **<!--$EndTime-->[EndTime]<!--/$EndTime-->**.
<!--/issueDescription-->

Sample list of requests that were blocked:**<!--$RequestUrl-->[RequestUrl]<!--/$RequestUrl-->**

There may be more client IPs for which requests were blocked. To view the full list, review the [storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging).

## **Recommended Steps** 

Storage requests using RBAC to authenticate should pass an oAuth token with the correct permissions to perform the intended operation. You can find the current permission and the required permission for the user (OID) in the failure description. 

1. Your Azure AD admin would be able to map the OID (GUID representing the user) to either of the following:

    * The person (firstname,lastname) 
    * The virtual machine with MSI 

2. Your account admin needs to provide the required permissions to the user by referring the links below:

   * [Manage access rights to Azure Blob and Queue data with RBAC](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac)
   * [Authenticate with Azure Active Directory from an application for access to blobs and queues](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-app)
   
