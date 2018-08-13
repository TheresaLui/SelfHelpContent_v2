<properties
pageTitle="Troubleshoot Azure Files mounting errors on Linux"
description="Unsupported Linux version"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_files_mount_linuxVersion"
diagnosticScenario="Unsupported Linux version for Azure Files"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="linux"
productPesIds=""
cloudEnvironments="public"
/>

# Unsupported Linux version for Azure File

<!--issueDescription-->
Azure File mount is not supported for **<!--$LinuxVersion-->[LinuxVersion]<!--/$LinuxVersion-->**  when **<!--$ServerLocation-->[ServerLocation]<!--/$ServerLocation-->**. Azure Files can be mounted in an Azure VM within the same region as the file share only via [secure protocols SMB 2.1 or SMB 3.0](https://docs.microsoft.com/windows-server/storage/file-server/smb-security). Please see [prerequisites for mounting an Azure File Share on Linux](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-linux#prerequisites-for-mounting-an-azure-file-share-with-linux-and-the-cifs-utils-package) for more details on supported environment versions and upgrade your VM to a supported OS version in order to mount Azure File.
<!--/issueDescription-->
