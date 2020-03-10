<properties
    pageTitle="Troubleshooting Azure File connectivity issue on Windows"
    description="Troubleshooting Azure File connectivity issue on Windows"
    service="microsoft.storage"
    resource="storageaccounts"
    authors="jeffpatt24"
    ms.author="jeffpatt"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32642181"
    resourceTags=""
    productPesIds="16460"
    cloudEnvironments="public,MoonCake,FairFax,BlackForest"
    articleId="F16A06F5-DD5D-42DB-805F-90DDC48198B1"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# Troubleshooting Azure Files: Connectivity issue on Windows

## **Recommended Steps**

1. Run [troubleshooting script for mounting errors](https://support.microsoft.com/help/4022301/troubleshooter-for-azure-files-shares)<br>
2. Check whether you hit [quota error when trying to open a file](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-1816-not-enough-quota-is-available-to-process-this-command-when-you-copy-to-an-azure-file-share)

### Windows Client Problems

* [Error 5 when attempting to mount an Azure File Share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-5-when-you-mount-an-azure-file-share)<br>
* [Error 53, Error 67, or Error 87 when attempting to mount an Azure File Share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-53-error-67-or-error-87-when-you-mount-or-unmount-an-azure-file-share)<br>
* [Net use was successful but I don’t see the Azure file share mounted in Windows Explorer](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#no-folder-with-a-drive-letter-in-my-computer)<br>
* [My storage account contains "/" and the net use command fails](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#net-use-command-fails-if-the-storage-account-contains-a-forward-slash)<br>
* [My application/service cannot access mounted Azure Files drive](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#application-or-service-cannot-access-a-mounted-azure-files-drive)

## **Recommended Documents**

* [Azure file share – failed to delete files from Azure file share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-cannot-delete-files-azure-file-share)