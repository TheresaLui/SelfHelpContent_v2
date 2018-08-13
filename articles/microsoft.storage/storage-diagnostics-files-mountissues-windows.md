<properties
pageTitle="Troubleshoot Azure Files mounting errors on Windows"
description="Unsupported Windows version"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_files_mount_windowsVersion"
diagnosticScenario="Unsupported Windows version for Azure Files"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="public"
/>

# Unsupported Windows version for Azure Files

<!--issueDescription-->
Azure file mount is not supported for **<!--$WindowsVersion-->[WindowsVersion]<!--/$WindowsVersion-->**  when **<!--$ServerLocation-->[ServerLocation]<!--/$ServerLocation-->**. Azure Files can be mounted in an Azure VM within the same region as the file share only via [secure protocols SMB 2.1 or SMB 3.0](https://docs.microsoft.com/windows-server/storage/file-server/smb-security). Please see [prerequisites for mounting an Azure File Share on Windows](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-windows) for more details on supported environment versions.
<!--/issueDescription-->

