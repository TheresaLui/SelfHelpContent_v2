<properties
	pageTitle="Azure AAD DS authentication over SMB"
	description="Azure AAD DS authentication over SMB"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	ms.author="passap"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629551"
	resourceTags=""
	productPesIds="16460"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest"
	articleId="9142F58A-99B0-4C8D-88A8-09F0805308E1"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# Azure AAD DS authentication over SMB

Most users are able to resolve their Azure AD DS authentication over SMB issue using the steps below.

## **Recommended Steps**    
Ensure that the following steps are completed to enable AAD DS Authentication feature on your storage account:
1. Have you ran through the [prerequisites to enable Azure AD DS authentication over SMB](https://docs.microsoft.com/azure/storage/files/storage-files-active-directory-enable#prerequisites)?
2. Is the virtual machine you used to mount Azure Files using AAD credentials domain joined to AAD DS? 
3. Have you [granted share level permissions](https://docs.microsoft.com/azure/storage/files/storage-files-active-directory-enable#assign-access-permissions-to-an-identity) to the target user through RBAC?
4.	Have you [granted file/directory level permissions (NTFS ACLs)](https://docs.microsoft.com/azure/storage/files/storage-files-active-directory-enable#configure-ntfs-permissions-over-smb) to the target user through file explorers or icacls? 

