﻿<properties
pageTitle="SMB 2.1 and SMB 3.0 clients that do not support encryption will be unable to access Azure file shares"
description="SMB clients that do not support encryption will be unable to access Azure file shares"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="jeffpatt"
displayOrder=""
articleId="Files_SecureTransferRequired"
diagnosticScenario="Secure transfer required setting is enabled on storage account"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# SMB clients that do not support encryption will be unable to access Azure file shares 

<!--issueDescription-->
The **Secure transfer required** setting is enabled on storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. SMB 2.1 and SMB 3.0 clients that do not support encryption will be unable to access Azure file shares. To learn more about the impact of having the **Secure transfer required** setting enabled, see [Require secure transfer in Azure Storage](https://docs.microsoft.com/en-us/azure/storage/common/storage-require-secure-transfer).
<!--/issueDescription-->

## Recommended steps**

Disable the **Secure transfer required** setting on storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** if SMB clients do not support encryption.

If you continue to experience issues accessing an Azure file share, see [Troubleshoot Azure Files problems in Windows](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems) or [Troubleshoot Azure Files problems in Linux](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-linux-file-connection-problems).
