<properties
	pageTitle="Azure Backup - Backup is failing for my VM"
	description="Azure Backup - Backup is failing for my VM"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="18"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="azurebackup-crp-windowsbackupfailure-mooncake"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Backup - Backup is failing for my VM

## **Recommended Steps**

- [Ensure your Windows VM agent is up to date before troubleshooting further](https://docs.azure.cn/virtual-machines/extensions/agent-windows#manual-installation)
- [Ensure there is connectivity between VM and Azure Storage endpoints](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-vm-has-no-internet-access)
- [For Snapshot extension issues, uninstall extensions to force reload & retry backup](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-backup-extension-fails-to-update-or-load)
- [OS Versions older than Windows Server 2008 R2 are not supported for Backup](https://docs.azure.cn/backup/backup-support-matrix-iaas#operating-system-support-windows)

## **Recommended Documents**

- [UserErrorGuestAgentStatusUnavailable - VM agent unable to communicate with Azure Backup](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#UserErrorGuestAgentStatusUnavailable-vm-agent-unable-to-communicate-with-azure-backup)
- [UserErrorStandardSSDNotSupported - Currently Azure Backup does not support Standard SSD disks](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorstandardssdnotsupported---currently-azure-backup-does-not-support-standard-ssd-disks)
- [UserErrorBackupOperationInProgress/SystemBackupOperationInProgress - Unable to initiate backup as another backup operation is currently in progress](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorbackupoperationinprogress---unable-to-initiate-backup-as-another-backup-operation-is-currently-in-progress)
- [UserErrorUnsupportedDiskSize - Currently Azure Backup does not support disk sizes greater than 4095GB](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorunsupporteddisksize---currently-azure-backup-does-not-support-disk-sizes-greater-than-1023gb)
- [ExtensionSnapshotFailedNoNetwork - Snapshot operation failed due to no network connectivity on the virtual machine](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#ExtensionSnapshotFailedNoNetwork-snapshot-operation-failed-due-to-no-network-connectivity-on-the-virtual-machine)
- [GuestAgentSnapshotTaskStatusError - Could not communicate with the VM agent for snapshot status](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#guestagentsnapshottaskstatuserror---could-not-communicate-with-the-vm-agent-for-snapshot-status)
- [UserErrorRpCollectionLimitReached - The Restore Point collection max limit has reached](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorrpcollectionlimitreached---the-restore-point-collection-max-limit-has-reached)
- [UserErrorKeyvaultPermissionNotConfigured - Backup doesn't have sufficient permissions to the key vault for backup of encrypted VMs](https://docs.azure.cn/backup/backup-azure-vms-encryption#troubleshooting-errors)
- [ExtentionOperationFailed - VMSnapshot extension operation failed](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#ExtensionOperationFailed-vmsnapshot-extension-operation-failed)
- [BackUpOperationFailed / BackUpOperationFailedV2 - Backup fails, with an internal error](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#backupoperationfailed--backupoperationfailedv2---backup-fails-with-an-internal-error)
