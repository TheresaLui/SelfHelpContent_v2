<properties
	pageTitle="Backup of Azure virtual machine fails"
	description="Backup of Azure virtual machine fails"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="15"
	selfHelpType="resource"
	supportTopicIds="32637320"
	resourceTags="linux"
	productPesIds="15571,15797,16470,16454"
	cloudEnvironments="MoonCake"
	articleId="ce3059e1-dea9-432e-8d74-f16235e18dd6"
/>

# Azure Backup - Backup is failing for my VM

## **Recommended Steps**

- [Ensure your Linux VM agent is up to date before troubleshooting further](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-agent-installed-in-the-vm-is-out-of-date-for-linux-vms)
- [Ensure there is connectivity between VM and Azure Storage endpoints](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-vm-has-no-internet-access)
- [If your Linux OS/Kernel version is not listed here, then it is not supported](https://docs.azure.cn/backup/backup-support-matrix-iaas#operating-system-support-linux)
- [For Snapshot extension issues, uninstall extensions to force reload & retry backup](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-backup-extension-fails-to-update-or-load)
- [If your issue is still not resolved, check VM Backup troubleshooting guide](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-backup-extension-fails-to-update-or-load)

## **Recommended Documents**

- [UserErrorGuestAgentStatusUnavailable - VM agent unable to communicate with Azure Backup](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#UserErrorGuestAgentStatusUnavailable-vm-agent-unable-to-communicate-with-azure-backup)
- [UserErrorBackupOperationInProgress/SystemBackupOperationInProgress - Unable to initiate backup as another backup operation is currently in progress](https://www.microsoft.com/?ref=aka)
- [UserErrorUnsupportedDiskSize - Currently Azure Backup does not support disk sizes greater than 4095GB](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorunsupporteddisksize---currently-azure-backup-does-not-support-disk-sizes-greater-than-1023gb)
- [ExtensionSnapshotFailedNoNetwork - Snapshot operation failed due to no network connectivity on the virtual machine](https://docs.azure.cn/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#ExtensionSnapshotFailedNoNetwork-snapshot-operation-failed-due-to-no-network-connectivity-on-the-virtual-machine)
- [GuestAgentSnapshotTaskStatusError - Could not communicate with the VM agent for snapshot status](https://www.microsoft.com/?ref=aka)
- [UserErrorRpCollectionLimitReached - The Restore Point collection max limit has reached](https://www.microsoft.com/?ref=aka)
- [UserErrorKeyvaultPermissionNotConfigured - Backup doesn't have sufficient permissions to the key vault for backup of encrypted VMs](https://docs.azure.cn/backup/backup-azure-vms-encryption#troubleshooting-errors)
- [ExtentionOperationFailed - VMSnapshot extension operation failed](https://www.microsoft.com/?ref=aka)
- [BackUpOperationFailed / BackUpOperationFailedV2 - Backup fails, with an internal error](https://www.microsoft.com/?ref=aka)
