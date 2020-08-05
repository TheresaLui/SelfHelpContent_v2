<properties
	pageTitle="AzCopy Synchronize Files"
	description="AzCopy Synchronize Files"
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
	articleId="cf0d2835-1ee5-4eb4-9ccd-9e6f4d5083b4"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# AzCopy Synchronize Files

1. You can use AzCopy to synchronize files between a local file system and a blob container. This feature is supported only for Non-ADLSGen2 accounts and is one way operation. 
2. Compares files names and last modified time stamps 
3. To prevent accidental deletions, make sure you request the customers to enable the [soft delete](httpsdocs.microsoft.comen-usazurestorageblobsstorage-blob-soft-delete) feature before they use the --delete-destination=prompttrue flag.

### Upload a container with changes to a local file system

1. In this case, the container is the destination, and the local file system is the source.
2. Syntax azcopy sync local-directory-path httpsstorage-account-name.blob or dfs.core.windows.netcontainer-name --recursive

### Update a local file system with changes to a container

1. Syntax azcopy sync httpsstorage-account-name.blob or dfs.core.windows.netcontainer-name CmyDirectory --recursive

### Sync Command Guide

1. AzCopy offers a convenient sync command to save on costs when transferring large amount of data. It enumerates both the source and destination directories, and compare the last modified times of the source and destination files, to see if they need to be transferred. [Link to Sync commmand guide](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/333098/Azure_Storage_TSG_AzCopy-v10-Sync-command-guide)
