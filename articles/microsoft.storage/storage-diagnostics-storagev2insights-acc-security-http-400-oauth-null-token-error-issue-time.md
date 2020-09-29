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
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Connections to storage account endpoint were blocked due to Null oAuth token
<!--issueDescription-->
Some connections to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** were blocked between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** and **<!--$EndTime-->[EndTime]<!--/$EndTime-->** as they had a Null oAuth bearer token.

Sample list of requests were blocked:

**<!--$RequestUrl-->[RequestUrl]<!--/$RequestUrl-->**
<!--/issueDescription-->

There may be more requests that were blocked. To get the exhaustive list, see the [storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging).

Storage requests using RBAC to authenticate should pass a valid oAuth token with right permissions to perform the intended operation.

## **Recommended Steps** 

Find the current permission and the required permission for the user (OID) in the failure description above. 

1. Your Azure AD admin is able to map the OID (GUID representing the user) to the the person (firstname,lastname) or virtual machine with MSI
2. Your account admin needs to provide the required permissions to the user by referring the links below:

   * [Manage access rights to Azure Blob and Queue data with RBAC](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac)
   * [Authenticate with Azure Active Directory from an application for access to blobs and queues](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-app)
   
