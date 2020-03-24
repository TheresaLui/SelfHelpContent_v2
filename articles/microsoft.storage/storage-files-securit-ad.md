<properties
	pageTitle="Azure AAD DS authentication over SMB"
	description="Azure AAD DS authentication over SMB"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	ms.author="passap"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32689882"
	resourceTags=""
	productPesIds="16460"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest"
	articleId="5f176206-d6ca-49a4-9c7e-ca93b463b298"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# Azure AAD DS authentication over SMB
Most users are able to resolve their AD authentication over SMB issue using the steps below. These solutions are written by Azure engineers, and will solve most common issues.

## **Recommended Steps**    
Ensure that the following steps are completed to enable AD Authentication feature on your storage account:
1.	Have you ran through the [prerequisites to enable AD authentication over SMB](https://docs.microsoft.com/azure/storage/files/storage-files-identity-auth-active-directory-enable#prerequisites)?
2.	Is the virtual machine you used to mount Azure Files using AD credentials domain joined to AD?
3.	Is your storage account deployed to [an region where AD Authentication is available](https://docs.microsoft.com/azure/storage/files/storage-files-identity-auth-active-directory-enable#regional-availability)?
4.	Have you [registered your storage account against your AD environment](https://docs.microsoft.com/azure/storage/files/storage-files-identity-auth-active-directory-enable#enable-ad-authentication-for-your-account)? 
5.	Have you [granted share level permissions](https://docs.microsoft.com/azure/storage/files/storage-files-identity-auth-active-directory-enable#assign-access-permissions-to-an-identity) to the target user through RBAC?
6.	Have you [granted file/directory level permissions (NTFS ACLs)](https://docs.microsoft.com/azure/storage/files/storage-files-identity-auth-active-directory-enable#configure-ntfs-permissions-over-smb) to the target user through file explorers or icacls?

