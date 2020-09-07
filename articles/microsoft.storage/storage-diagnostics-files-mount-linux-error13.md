<properties
pageTitle="Troubleshoot Azure Files mount error 13 on Linux"
description="How to troubleshoot Azure Files Linux mount error 13"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_files_mount_linux_error13"
diagnosticScenario="Troubleshoot Azure Files mounting errors on Linux"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# "Mount error(13): Permission denied" when you mount an Azure file share

<!--issueDescription-->
If your Azure file share mount fails with the following error: "Mount error(13): Permission denied", please follow the recommended steps below to troubleshoot the problem.
<!--/issueDescription-->

## **Recommended Steps**

### **Cause 1: Unencrypted communication channel**

For security reasons, connections to Azure file shares are blocked if the communication channel isn't encrypted and if the connection attempt isn't made from the same datacenter where the Azure file shares reside. Unencrypted connections within the same datacenter can also be blocked if the [Secure transfer required](https://docs.microsoft.com/azure/storage/common/storage-require-secure-transfer) setting is enabled on the storage account. An encrypted communication channel is provided only if the user's client OS supports SMB encryption.

To learn more, see [Prerequisites for mounting an Azure file share with Linux and the cifs-utils package](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-linux#prerequisites-for-mounting-an-azure-file-share-with-linux-and-the-cifs-utils-package). 

### Solution for cause 1

1. Connect from a client that supports SMB encryption or connect from a virtual machine in the same datacenter as the Azure storage account that is used for the Azure file share
2. Verify the [Secure transfer required](https://docs.microsoft.com/azure/storage/common/storage-require-secure-transfer) setting is disabled on the storage account if the client does not support SMB encryption

### **Cause 2: Virtual network or firewall rules are enabled on the storage account**

If virtual network (VNET) and firewall rules are configured on the storage account, network traffic will be denied access unless the client IP address or virtual network is allowed access.

### Solution for cause 2

Verify virtual network and firewall rules are configured properly on the storage account. To test if virtual network or firewall rules is causing the issue, temporarily change the setting on the storage account to **Allow access from all networks**. To learn more, see [Configure Azure Storage firewalls and virtual networks](https://docs.microsoft.com/azure/storage/common/storage-network-security).


## **Recommended Documents**

- [Troubleshoot Azure Files problems in Linux](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-linux-file-connection-problems)
- [AzFileDiagnostics - Troubleshooting tool for Azure Files mounting errors on Linux or MacOS](https://gallery.technet.microsoft.com/Troubleshooting-tool-for-02184089)
- [Prerequisites for mounting an Azure file share with Linux and the cifs-utils package](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-linux#prerequisites-for-mounting-an-azure-file-share-with-linux-and-the-cifs-utils-package)
- [Secure transfer required](https://docs.microsoft.com/azure/storage/common/storage-require-secure-transfer)
- [Configure Azure Storage firewalls and virtual networks](https://docs.microsoft.com/azure/storage/common/storage-network-security)
