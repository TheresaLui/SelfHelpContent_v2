<properties
pageTitle="Troubleshoot Azure Files mount error 5 on Windows"
description="How to troubleshoot Azure Files Windows mount error 5"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_files_mount_windows_error5"
diagnosticScenario="Troubleshoot Azure Files mounting errors on Windows"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure Files - Windows mount error 5

<!--issueDescription-->
If your Azure file share mount fails with the following error: "System error 5 has occurred. Access is denied", please follow the recommended steps below to troubleshoot the problem.
<!--/issueDescription-->

## **Recommended Steps**
### **Cause 1: Unencrypted communication channel**

For security reasons, connections to Azure file shares are blocked if the communication channel isn't encrypted and if the connection attempt isn't made from the same datacenter where the Azure file shares reside. Unencrypted connections within the same datacenter can also be blocked if the [Secure transfer required](https://docs.microsoft.com/azure/storage/common/storage-require-secure-transfer) setting is enabled on the storage account. An encrypted communication channel is provided only if the user's client OS supports SMB encryption.

Windows 8, Windows Server 2012, and later versions of each system negotiate requests that include SMB 3.0, which supports encryption.

### [Solution for cause 1](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#solution-for-cause-1)

### **Cause 2: Virtual network or firewall rules are enabled on the storage account**

If virtual network (VNET) and firewall rules are configured on the storage account, network traffic will be denied access unless the client IP address or virtual network is allowed access.

### [Solution for cause 2](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#solution-for-cause-2)


## **Recommended Documents**

- [Troubleshoot Azure Files problems in Windows](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems)
- [Troubleshooting tool for Azure Files mounting errors on Windows](https://github.com/Azure-Samples/azure-files-samples/tree/master/AzFileDiagnostics/Windows)
- [Secure transfer required](https://docs.microsoft.com/azure/storage/common/storage-require-secure-transfer)
- [Configure Azure Storage firewalls and virtual networks](https://docs.microsoft.com/azure/storage/common/storage-network-security)
