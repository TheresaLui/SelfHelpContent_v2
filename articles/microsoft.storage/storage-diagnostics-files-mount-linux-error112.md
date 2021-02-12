<properties
pageTitle="Troubleshoot Azure Files mount error 112 on Linux"
description="How to troubleshoot Azure Files Linux mount error 112"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_files_mount_linux_error112"
diagnosticScenario="Troubleshoot Azure Files mounting errors on Linux"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# "Mount error(112): Host is down" when you mount an Azure file share

<!--issueDescription-->
If your Azure file share mount fails with the following error: "Mount error(112): Host is down", please follow the recommended steps below to troubleshoot the problem.
<!--/issueDescription-->

## **Recommended Steps**
### **Cause**
A "112" mount error occurs on the Linux client when the client has been idle for a long time. After an extended idle time, the client disconnects and the connection times out.  

The connection can be idle for the following reasons:

-	Network communication failures that prevent re-establishing a TCP connection to the server when the default "soft" mount option is used
-	Recent reconnection fixes that are not present in older kernels

### **Solution**

This reconnection problem in the Linux kernel is now fixed as part of the following changes:

- [Fix reconnect to not defer smb3 session reconnect long after socket reconnect](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/fs/cifs?id=4fcd1813e6404dd4420c7d12fb483f9320f0bf93)
- [Call echo service immediately after socket reconnect](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/commit/?id=b8c600120fc87d53642476f48c8055b38d6e14c7)
- [CIFS: Fix a possible memory corruption during reconnect](https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=53e0e11efe9289535b060a51d4cf37c25e0d0f2b)
- [CIFS: Fix a possible double locking of mutex during reconnect (for kernel v4.9 and later)](https://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=96a988ffeb90dba33a71c3826086fe67c897a183)

However, these changes might not be ported yet to all the Linux distributions. This fix and other reconnection fixes can be found in the [Minimum recommended versions with corresponding mount capabilities (SMB version 2.1 vs SMB version 3.0)](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-linux#minimum-recommended-versions-with-corresponding-mount-capabilities-smb-version-21-vs-smb-version-30) section of the [Use Azure Files with Linux](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-linux) article. You can get this fix by upgrading to one of these recommended kernel versions.

### **Workaround**

You can work around this problem by specifying a hard mount. A hard mount forces the client to wait until a connection is established or until it's explicitly interrupted. You can use it to prevent errors because of network time-outs. However, this workaround might cause indefinite waits. Be prepared to stop connections as necessary.

If you can't upgrade to the latest kernel versions, you can work around this problem by keeping a file in the Azure file share that you write to every 30 seconds or less. This must be a write operation, such as rewriting the created or modified date on the file. Otherwise, you might get cached results, and your operation might not trigger the reconnection.


## **Recommended Documents**

- [Troubleshoot Azure Files problems in Linux](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-linux-file-connection-problems)
- [AzFileDiagnostics - Troubleshooting tool for Azure Files mounting errors on Linux or MacOS](https://github.com/Azure-Samples/azure-files-samples/tree/master/AzFileDiagnostics/Linux)
- [Minimum recommended versions with corresponding mount capabilities (SMB version 2.1 vs SMB version 3.0)](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-linux#minimum-recommended-versions-with-corresponding-mount-capabilities-smb-version-21-vs-smb-version-30)
