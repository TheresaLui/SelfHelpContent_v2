<properties
pageTitle="Troubleshoot Azure Files mount error 115 on Linux"
description="How to troubleshoot Azure Files Linux mount error 115"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_files_mount_linux_error115"
diagnosticScenario="Troubleshoot Azure Files mounting errors on Linux"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# "Mount error(115): Operation now in progress" when you mount Azure Files by using SMB 3.0

<!--issueDescription-->
If your Azure file share mount fails with the following error: "Mount error(115): Operation now in progress", please follow the recommended steps below to troubleshoot the problem.
<!--/issueDescription-->

## **Recommended Steps**
### **Cause**
Some Linux distributions don't yet support encryption features in SMB 3.0. Users might receive a "115" error message if they try to mount Azure Files by using SMB 3.0 because of a missing feature. SMB 3.0 with full encryption is supported only when you're using Ubuntu 16.04 or later.

### **Solution**
The encryption feature for SMB 3.0 for Linux was introduced in the 4.11 kernel. This feature enables mounting of an Azure file share from on-premises or from a different Azure region. This functionality is included in the Linux distributions listed in [Minimum recommended versions with corresponding mount capabilities (SMB version 2.1 vs SMB version 3.0)](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-linux#minimum-recommended-versions-with-corresponding-mount-capabilities-smb-version-21-vs-smb-version-30). Other distributions require kernel 4.11 and later versions.

If your Linux SMB client doesn't support encryption, mount Azure Files by using SMB 2.1 from an Azure Linux VM that's in the same datacenter as the file share. Verify that the [Secure transfer required]( https://docs.microsoft.com/azure/storage/common/storage-require-secure-transfer) setting is disabled on the storage account. 


## **Recommended Documents**

- [Troubleshoot Azure Files problems in Linux](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-linux-file-connection-problems)
- [AzFileDiagnostics - Troubleshooting tool for Azure Files mounting errors on Linux or MacOS](https://gallery.technet.microsoft.com/Troubleshooting-tool-for-02184089)
- [Minimum recommended versions with corresponding mount capabilities (SMB version 2.1 vs SMB version 3.0)](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-linux#minimum-recommended-versions-with-corresponding-mount-capabilities-smb-version-21-vs-smb-version-30)
- [Secure transfer required]( https://docs.microsoft.com/azure/storage/common/storage-require-secure-transfer)

