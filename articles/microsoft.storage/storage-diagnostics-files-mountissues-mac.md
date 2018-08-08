<properties
pageTitle="Troubleshoot Azure Files mounting errors on macOS"
description="Unsupported macOS version"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_files_mount_macOSVersion"
diagnosticScenario="Unsupported macOS version for Azure Files"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="macOS"
productPesIds=""
cloudEnvironments="public"
/>

# Unsupported macOS version for Azure Files

<!--issueDescription-->
Azure File mount is not supported for **<!--$macOSVersion-->[macOSVersion]<!--/$macOSVersion-->**. Azure file shares can only be mounted with [encrypted SMB 3.0 protocol](https://docs.microsoft.com/windows-server/storage/file-server/smb-security#smb-encryption) that is available on macOS El Capitan 10.11+. Please see [prerequisites for mounting an Azure File Share on Windows](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-windows) for more details on supported environment versions and upgrade your VM to a supported OS version.
<!--/issueDescription-->
