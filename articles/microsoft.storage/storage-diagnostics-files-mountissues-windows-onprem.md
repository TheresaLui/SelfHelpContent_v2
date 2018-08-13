<properties
pageTitle="Troubleshoot Azure Files mounting errors on Windows"
description="Unsupported Windows version"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_files_mount_windowsVersion_onPrem"
diagnosticScenario="Unsupported Windows version for Azure Files"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# Unsupported Windows version for Azure Files

<!--issueDescription-->
Azure file mount is not supported for **<!--$WindowsVersion-->[WindowsVersion]<!--/$WindowsVersion-->**  when **<!--$ServerLocation-->[ServerLocation]<!--/$ServerLocation-->**. In order to use an Azure file share outside of the Azure region it is hosted in, such as on-premises or in a different Azure region, the OS must support [encrypted SMB 3.0 protocol](https://docs.microsoft.com/windows-server/storage/file-server/smb-security#smb-encryption). Please see [prerequisites for mounting an Azure File Share on Windows](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-windows) for more details on supported environment versions.
<!--/issueDescription-->
