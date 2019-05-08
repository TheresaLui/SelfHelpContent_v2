<properties
	pageTitle="Troubleshooting Azure File dropped or terminated connections"
	description="Troubleshooting Azure File dropped or terminated connections problems"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="jeffpatt24"
	ms.author="jeffpatt"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602759"
	resourceTags=""
	productPesIds="16460"
	cloudEnvironments="public,MoonCake"
	articleId="0fe3cd1e-3520-4156-8657-b26992ff7597"
/>

# Troubleshooting Azure File: Dropped or Terminated Connections

## **Recommended Steps**

- Run [troubleshooting script for mounting errors](https://support.microsoft.com/help/4022301/troubleshooter-for-azure-files-shares)<br>
- Check if you hit [quota error when trying to open a file](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-1816-not-enough-quota-is-available-to-process-this-command-when-you-copy-to-an-azure-file-share)<br>

**Windows Client Problems**

- [Error 5 when attempting to mount an Azure File Share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-5-when-you-mount-an-azure-file-share)<br>
- [Error 53, Error 67, or Error 87 when attempting to mount an Azure File Share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-53-error-67-or-error-87-when-you-mount-or-unmount-an-azure-file-share)<br>
- [Net use was successful but I don’t see the Azure file share mounted in Windows Explorer](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#no-folder-with-a-drive-letter-in-my-computer)<br>
- [My storage account contains "/" and the net use command fails](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#net-use-command-fails-if-the-storage-account-contains-a-forward-slash)<br>
- [My application/service cannot access mounted Azure Files drive](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#application-or-service-cannot-access-a-mounted-azure-files-drive)<br>

**Linux Client Problems**

- ["Mount error(13): Permission denied" when you attempt to mount an Azure file share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-linux-file-connection-problems#mount-error13-permission-denied-when-you-mount-an-azure-file-share)
- ["Host is down" error on existing file shares, or the shell hangs when doing list commands on the mount point](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-linux-file-connection-problems#mount-error115-operation-now-in-progress-when-you-mount-azure-files-by-using-smb-30)<br>
- ["Mount error(115): Operation now in progress" when you attempt to mount an Azure file share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-linux-file-connection-problems#mount-error115-operation-now-in-progress-when-you-mount-azure-files-by-using-smb-30)<br>

