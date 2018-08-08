<properties
pageTitle="Troubleshoot Azure Files mounting errors on Linux"
description="Unsupported Linux version"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_files_mount_linuxVersion_onPrem"
diagnosticScenario="Unsupported Linux version for Azure Files"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="linux"
productPesIds=""
cloudEnvironments="public"
/>

# Unsupported Linux version for Azure Files

<!--issueDescription-->
Azure file mount is not supported for **<!--$LinuxVersion-->[LinuxVersion]<!--/$LinuxVersion-->**  when **<!--$ServerLocation-->[ServerLocation]<!--/$ServerLocation-->**. For connections coming from clients on-premises or in other Azure regions, Azure Files will only allow connections using [encrypted SMB 3.0 protocol](https://docs.microsoft.com/windows-server/storage/file-server/smb-security#smb-encryption). SMB 3.0 encryption support was introduced in Linux kernel version 4.11 and has been backported to older kernel versions for popular Linux distributions. Please see [prerequisites for mounting an Azure File Share on Linux](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-linux#prerequisites-for-mounting-an-azure-file-share-with-linux-and-the-cifs-utils-package) for more details on supported environment versions.
<!--/issueDescription-->
