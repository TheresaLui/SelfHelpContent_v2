<properties
	  pageTitle="Customer is facing a data plane issue."
	  description="Customer is facing a data plane issue."
      service="Microsoft.Storage"
      resource="Microsoft.Storage/storageAccounts,Microsoft.ClassicStorage/storageAccounts"
	  authors="yagohel23"
	  ms.author="yagohel"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds="32679285,32679299,32679292,32678715"
	  resourceTags=""
	  productPesIds="16459,16461,15629,16598"
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="7070f14f-844e-4fda-9bca-327a9c333187"
	  ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Customer is facing a data plane issue.

**Data Plane** issues will happen if the user does not have appropriate data plane permissions on the storage account or on the container they are trying to access. Depending on the operation user is trying to perform on the blob object, we have several [built-in roles](https://docs.microsoft.com/azure/storage/common/storage-auth-aad#azure-built-in-roles-for-blobs-and-queues) which the customers can assign to a particular user/identity. 

- [Storage Blob Data Owner](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#storage-blob-data-owner): Use to set ownership and manage POSIX access control for Azure Data Lake Storage Gen2. For more information, see [Access control in Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-access-control).
- [Storage Blob Data Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#storage-blob-data-contributor): Use to grant read/write/delete permissions to Blob storage resources.
- [Storage Blob Data Reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#storage-blob-data-reader): Use to grant read-only permissions to Blob storage resources.
- [Storage Blob Delegator](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#storage-blob-delegator): Get a user delegation key to use to create a shared access signature that is signed with Azure AD credentials for a container or blob.
- [Storage Queue Data Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#storage-queue-data-contributor): Use to grant read/write/delete permissions to Azure queues.
- [Storage Queue Data Reader](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#storage-queue-data-reader): Use to grant read-only permissions to Azure queues.
- [Storage Queue Data Message Processor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#storage-queue-data-message-processor): Use to grant peek, retrieve, and delete permissions to messages in Azure Storage queues.
- [Storage Queue Data Message Sender](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#storage-queue-data-message-sender): Use to grant add permissions to messages in Azure Storage queues.

They can also create their own [custom roles](https://docs.microsoft.com/azure/role-based-access-control/custom-roles) depending on the types of permissions they want to provide to a particular user. Details regarding Storage Built-in roles definition can be [found here](https://docs.microsoft.com/azure/role-based-access-control/role-definitions#management-and-data-operations). [This public document](https://docs.microsoft.com/rest/api/storageservices/authorize-with-azure-active-directory#permissions-for-calling-blob-and-queue-data-operations) also provides details regarding data plane permissions needed for each of the blob/queue storage operation. 


In order to resolve permission issue, verify if the user in question has appropriate data plane permissions on the storage account. Using the failure you found in dgrep, identify the user identity using the **UserObjectID** column. Once you know the objectID of the user, use ASC to verify if the user has appropriate control plane permission.

1. Navigate to customer's storage account in ASC Resource Explorer
2. Navigate to **Access Control** tab and plug in user's ObjectID in the **Check Access** option and run it.
3. You will be able to see user's RBAC permissions on that particular storage account. For each of the role assignment you see in there, please make sure the scope of the role assignment is properly specified.
4. Verify if the user has appropriate data plane role assigned to them or have a custom role assigned to them which provides appropriate data plane permission.
5. If the user does not have required permission, please ask them to work with the owner of their storage account to get it. That should help resolve the issue. 
6. If the user has appropriate permissions but they still face permission issues, please escalate the ticket to the TA.

