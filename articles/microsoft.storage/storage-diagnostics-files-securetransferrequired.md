<properties
pageTitle="SMB 2.1 and SMB 3.0 clients that do not support encryption will be unable to access Azure file shares"
description="SMB clients that do not support encryption will be unable to access Azure file shares"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="jeffpatt24"
ms.author="jeffpatt"
displayOrder=""
articleId="Files_SecureTransferRequired"
diagnosticScenario="Secure transfer required setting is enabled on storage account"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# SMB clients that do not support encryption will be unable to access Azure file shares

<!--issueDescription-->
The **Secure transfer required** setting is enabled on storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. SMB 2.1 and SMB 3.0 clients that do not support encryption will be unable to access Azure file shares.
<!--/issueDescription-->

## **Recommended Steps**

* Disable the **Secure transfer required** setting on storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** if SMB clients do not support encryption

## **Recommended Documents**

* [Troubleshoot Azure Files problems in Windows](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems)
* [Troubleshoot Azure Files problems in Linux](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-linux-file-connection-problems)
* [Require secure transfer in Azure Storage](https://docs.microsoft.com/azure/storage/common/storage-require-secure-transfer)
