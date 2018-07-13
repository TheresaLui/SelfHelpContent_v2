<properties
	pageTitle="Troubleshooting Azure File dropped or terminated connections"
	description="Troubleshooting Azure File dropped or terminated connections problems"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602759"
	resourceTags=""
	productPesIds="16460"
	cloudEnvironments="public,MoonCake"
/>

# Troubleshooting Azure File dropped or terminated connections

## **Recommended steps**

- Run [troubleshooting script for mounting errors](https://support.microsoft.com/help/4022301/troubleshooter-for-azure-files-shares)<br>
- Check if you hit [quota error when trying to open a file](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-1816-not-enough-quota-is-available-to-process-this-command-when-you-copy-to-an-azure-file-share)<br>

**Windows client problems**

- Check if [location or network change caused the connection to Azure File Share to terminate](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-53-error-67-or-error-87-when-you-mount-or-unmount-an-azure-file-share)<br>
- Ensure [user account running the application has mounted the File Share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#application-or-service-cannot-access-a-mounted-azure-files-drive)<br>

**Linux client problems**

- Troubleshoot ["Host is down" error on existing file shares, or the shell hangs when doing list commands on the mount point](https://docs.microsoft.com/en-us/azure/storage/files/storage-troubleshoot-linux-file-connection-problems#mount-error112-host-is-down-because-of-a-reconnection-time-out)<br>

