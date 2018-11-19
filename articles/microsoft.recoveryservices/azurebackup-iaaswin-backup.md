<properties
	pageTitle="Backup of Windows Azure virtual machine fails"
	description="Top issues causing Windows Azure virtual machine backup failures"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds="32553277"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Backup of Windows Azure virtual machine fails

## **Recommended steps**
- [UserErrorGuestAgentStatusUnavailable - VM agent unable to communicate with Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#UserErrorGuestAgentStatusUnavailable-vm-agent-unable-to-communicate-with-azure-backup) <br>
- [GuestAgentSnapshotTaskStatusError - Could not communicate with the VM agent for snapshot status](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#guestagentsnapshottaskstatuserror---could-not-communicate-with-the-vm-agent-for-snapshot-status) <br>
- [UserErrorStandardSSDNotSupported - Currently Azure Backup does not support Standard SSD disks](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorstandardssdnotsupported---currently-azure-backup-does-not-support-standard-ssd-disks) <br>
- [UserErrorUnsupportedDiskSize - Currently Azure Backup does not support disk sizes greater than 1023GB](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorunsupporteddisksize---currently-azure-backup-does-not-support-disk-sizes-greater-than-1023gb) <br>
- [UserErrorRpCollectionLimitReached - The Restore Point collection max limit has reached](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorrpcollectionlimitreached---the-restore-point-collection-max-limit-has-reached) <br>
- [UserErrorKeyvaultPermissionNotConfigured - Backup doesn't have sufficient permissions to the key vault for backup of encrypted VMs](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#troubleshooting-errors) <br>
- [ExtentionOperationFailed - VMSnapshot extension operation failed](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#ExtentionOperationFailed-vmsnapshot-extension-operation-failed) <br>
- [BackUpOperationFailed / BackUpOperationFailedV2 - Backup fails, with an internal error](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#backupoperationfailed--backupoperationfailedv2---backup-fails-with-an-internal-error) <br>
- [ExtensionSnapshotFailedNoNetwork - Snapshot operation failed due to no network connectivity on the virtual machine](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#ExtensionSnapshotFailedNoNetwork-snapshot-operation-failed-due-to-no-network-connectivity-on-the-virtual-machine) <br>

## **Recommended documents**
- [Ensure your Windows VM agent is up to date before troubleshooting further](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows#manual-installation) <br>
- [Ensure there is connectivity between VM and Azure Storage endpoints](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-vm-has-no-internet-access) <br>
- [For Snapshot extension issues, uninstall extensions to force reload & retry backup](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#the-backup-extension-fails-to-update-or-load) <br>
- [OS Versions older than Windows Server 2008 R2 are not supported for Backup](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#supported-operating-systems-for-backup) <br>
