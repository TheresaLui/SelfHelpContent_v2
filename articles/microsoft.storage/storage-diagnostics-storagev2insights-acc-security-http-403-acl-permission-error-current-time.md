<properties
pageTitle="Requests to storage account endpoint were blocked due to insufficient ACL permission"
description="Requests to storage account endpoint were blocked due to insufficient ACL permission"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_acc_security_http_403_acl_permission_error_current_time"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Requests to storage account failed authorization due to insufficient ACL permission
<!--issueDescription-->
 Between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** and **<!--$EndTime-->[EndTime]<!--/$EndTime-->**, we didn't find any requests that failed authorization due to an insufficient **Access Control List (ACL)** associated with the user (service principal). However, we found a recent occurrence of ACL failures around the **<!--$CurrentTimestamp-->[CurrentTimestamp]<!--/$CurrentTimestamp-->**.
<!--/issueDescription-->

## **Recommended Steps**

The following table shows details of the failed requests with the operation type `Get(Read)` or `Put/Post(Write)`, along with the folder or file path and user. For successful authorization, the user (service principal) should have the following ACLs:

- **For the folder path** - Provide **Execute**(**X**) and **Read**(**R**) permissions for the relevant folder and **Execute**(**X**) permission for all the parent folders up to the root folder.<br>
- **For the file path** - Provide **Read**(**R**) or **Write**(**W**) permission, depending on the operation on the file, and **Execute**(**X**) permission for all the parent folders up to the root folder.

To learn more about ACLs, see [Manage Access control lists (ACLs) in Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-access-control?WT.mc_id=Portal-Microsoft_Azure_Support).

**Note:** There may be more client IPs with blocked requests that are not shown here. For the complete list, see the **[storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging)**.

Sample list of requests that failed ACL authorization:<br><!--$RequestUrl-->[RequestUrl]<!--/$RequestUrl-->
