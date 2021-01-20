<properties
pageTitle="Requests to storage account endpoint were blocked due to insufficient ACL permission"
description="Requests to storage account endpoint were blocked due to insufficient ACL permission"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_acc_security_http_403_acl_permission_error_issue_time"
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
 Between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** and **<!--$EndTime-->[EndTime]<!--/$EndTime-->** requests to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** failed authorization due to insufficient **Access Control List (ACL)** associated with the user(service principal).
<!--/issueDescription-->

## **Recommended Steps**
Below table shows details of the failed requests with operation type Get(Read) or Put/Post(Write) along with the folder or file path and user. For successful authorization the user(service principal) should posses the following ACL.

- **For folder path** - Please provide **Execute**(**X**) and **Read**(**R**) permission on the concerned folder and **Execute**(**X**) permission on all the parent folders till root.<br>
- **For file path** - Please provide **Read**(**R**) or **Write**(**W**) depending on the operation on the file and **Execute**(**X**) permission on all the parent folders till root.

Please refer [Manage Access control lists (ACLs) in Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-access-control?WT.mc_id=Portal-Microsoft_Azure_Support) to learn more about ACLs.

**Note:** There may be more client IPs for which requests were blocked which we are not able to display here. To view the full list, review the **[storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging)**.

Sample list of requests that failed ACL authorization:<br><!--$RequestUrl-->[RequestUrl]<!--/$RequestUrl-->