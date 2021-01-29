<properties
	pageTitle="Authorization Permission Mismatch Error"
	description="Authorization Permission Mismatch Error"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="521a773a-dc6d-4828-8da9-2d7b12273565"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Authorization Permission Mismatch Error

1. Customer is attempting to migrate data from one storage account to another in the same subscription and encounter an error stating 'Authorization Permission Mismatch'. 
2. Insufficient permissions to access data abstraction. 
3. Grant requisite RBAC permissions for data access on the source and destination storage accounts. This applies to blob, file, and queues. 

### Recommended Documents

1. [Overview of Azure Files identity-based authentication support for SMB access](https://docs.microsoft.com/en-us/azure/storage/files/storage-files-active-directory-overview)
2. [Use the Azure portal to assign an RBAC role for access to blob and queue data](https://docs.microsoft.com/en-us/azure/storage/common/storage-auth-aad-rbac-portal)
3. [Choose how you'll provide authorization credentials](https://docs.microsoft.com/en-us/azure/storage/common/storage-use-azcopy-v10#choose-how-youll-provide-authorization-credentials)
4. [Internal Wiki](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/313994/Azure_Storage_TSG_AzCopy-v10-AuthorizationPermissionMismatch-Error)

