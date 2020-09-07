<properties
pageTitle="Troubleshoot Azure Files mount error 87 on Windows"
description="How to troubleshoot Azure Files Windows mount error 87"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_files_mount_windows_error87"
diagnosticScenario="Troubleshoot Azure Files mounting errors on Windows"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure Files - Windows mount error 87

<!--issueDescription-->
If your Azure file share mount fails with the following error: "System error 87 has occurred. The parameter is incorrect", please follow the recommended steps below to troubleshoot the problem.
<!--/issueDescription-->

## **Recommended Steps**

### **Cause: NTLMv1 is enabled**

System error 87 can occur if NTLMv1 communication is enabled on the client. Azure Files supports only NTLMv2 authentication. Having NTLMv1 enabled creates a less-secure client. Therefore, communication is blocked for Azure Files. 

To determine whether this is the cause of the error, verify that the following registry subkey is set to a value of 3:

**HKLM\SYSTEM\CurrentControlSet\Control\Lsa > LmCompatibilityLevel**

For more information, see the [LmCompatibilityLevel](https://technet.microsoft.com/library/cc960646.aspx) topic on TechNet.

### **Solution**

Revert the **LmCompatibilityLevel** value to the default value of 3 in the following registry subkey:

**HKLM\SYSTEM\CurrentControlSet\Control\Lsa**

## **Recommended Documents**

- [Troubleshoot Azure Files problems in Windows](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems)
- [AzFileDiagnostics - Troubleshooting tool for Azure Files mounting errors on Windows](https://gallery.technet.microsoft.com/Troubleshooting-tool-for-a9fa1fe5)
- [LmCompatibilityLevel](https://technet.microsoft.com/library/cc960646.aspx)
