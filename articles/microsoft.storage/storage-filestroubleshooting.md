<properties
    pageTitle="Troubleshooting Azure File issues"
    description="Troubleshoot most common problems related to connecting, mapping, and mounting Azure Files shares"
    service="microsoft.storage"
    resource="storageaccounts"
    authors="jeffpatt24"
	ms.author="jeffpatt"
    displayOrder="7"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds="16460"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="84a62987-f85c-4757-b671-0d2a30280fba"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# Troubleshooting Azure Files issues

## **Recommended Steps**

### **Troubleshooting Mounting Errors**

* [Step by step guided walkthrough for mounting errors on Windows and Linux](https://support.microsoft.com/help/4022301/troubleshooter-for-azure-files-shares)
* [Download and run troubleshooting tool for mounting errors on Windows](https://gallery.technet.microsoft.com/Troubleshooting-tool-for-a9fa1fe5)
* [Download and run troubleshooting tool for mounting errors on Linux](https://gallery.technet.microsoft.com/Troubleshooting-tool-for-02184089)

### **General Problems (Windows and Linux clients)**

- [Quota error when trying to open a file](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-1816-not-enough-quota-is-available-to-process-this-command-when-you-copy-to-an-azure-file-share)
- [Slow performance when you access Azure File storage from Windows or from Linux](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#slow-file-copying-to-and-from-azure-files-in-windows)
- [Error “Access denied” when browsing to an Azure file share in the portal](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-access-denied-when-browsing-to-an-azure-file-share-in-the-portal)

### **Windows Client Problems**

- [Error 5 when attempting to mount an Azure File Share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-5-when-you-mount-an-azure-file-share)<br>
- [Error 53, Error 67, or Error 87 when attempting to mount an Azure File Share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-53-error-67-or-error-87-when-you-mount-or-unmount-an-azure-file-share)<br>
- [Net use was successful but I don’t see the Azure file share mounted in Windows Explorer](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#no-folder-with-a-drive-letter-in-my-computer)<br>
- [My storage account contains "/" and the net use command fails](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#net-use-command-fails-if-the-storage-account-contains-a-forward-slash)<br>
- [My application/service cannot access mounted Azure Files drive](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#application-or-service-cannot-access-a-mounted-azure-files-drive)

### **Linux Client Problems**

- ["Mount error(13): Permission denied" when you attempt to mount an Azure file share](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-linux-file-connection-problems#mount-error13-permission-denied-when-you-mount-an-azure-file-share)
- [Error "You are copying a file to a destination that does not support encryption" when uploading/copying files to Azure Files](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#error-you-are-copying-a-file-to-a-destination-that-does-not-support-encryption)
- ["Host is down" error on existing file shares, or the shell hangs when doing list commands on the mount point](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-linux-file-connection-problems#mount-error115-operation-now-in-progress-when-you-mount-azure-files-by-using-smb-30)
- [Mount error 115 when attempting to mount Azure Files on the Linux VM](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-linux-file-connection-problems#mount-error115-operation-now-in-progress-when-you-mount-azure-files-by-using-smb-30)
- [Linux VM experiencing random delays in commands like "ls"](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-linux-file-connection-problems#slow-performance-on-an-azure-file-share-mounted-on-a-linux-vm)

## **Recommended Documents**

- [Troubleshooting Azure File storage problems](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems)
- [Azure Files FAQ](https://docs.microsoft.com/azure/storage/files/storage-files-faq)
