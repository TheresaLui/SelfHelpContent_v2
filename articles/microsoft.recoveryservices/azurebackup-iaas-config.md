<properties
	pageTitle="Azure IAAS VM Backup Configure Protection"
	description="Azure IAAS VM Backup Configure Protection failures"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="kasparks"
	ms.author="kasparks"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553285"
	resourceTags=""
	productPesIds="15207"
	articleId="95333929-5668-4cb5-bed3-3855436ddbf7"
	cloudEnvironments="public"
	
/>

# Unable to Configure Backup for Azure Virtual Machines

## **Recommended Steps**

- [UserErrorGuestAgentStatusUnavailable - VM agent unable to communicate with Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#UserErrorGuestAgentStatusUnavailable-vm-agent-unable-to-communicate-with-azure-backup) <br>
- [UserErrorStandardSSDNotSupported - Currently Azure Backup does not support Standard SSD disks](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorstandardssdnotsupported---currently-azure-backup-does-not-support-standard-ssd-disks) <br>
- [UserErrorBackupOperationInProgress/SystemBackupOperationInProgress - Unable to initiate backup as another backup operation is currently in progress](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorbackupoperationinprogress---unable-to-initiate-backup-as-another-backup-operation-is-currently-in-progress) <br>
- [UserErrorUnsupportedDiskSize - Currently Azure Backup does not support disk sizes greater than 1023GB](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorunsupporteddisksize---currently-azure-backup-does-not-support-disk-sizes-greater-than-1023gb) <br>
- [ExtensionSnapshotFailedNoNetwork - Snapshot operation failed due to no network connectivity on the virtual machine](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#ExtensionSnapshotFailedNoNetwork-snapshot-operation-failed-due-to-no-network-connectivity-on-the-virtual-machine) <br>
- [GuestAgentSnapshotTaskStatusError - Could not communicate with the VM agent for snapshot status](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#guestagentsnapshottaskstatuserror---could-not-communicate-with-the-vm-agent-for-snapshot-status) <br>
- [UserErrorRpCollectionLimitReached - The Restore Point collection max limit has reached](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorrpcollectionlimitreached---the-restore-point-collection-max-limit-has-reached) <br>
- [UserErrorKeyvaultPermissionNotConfigured - Backup doesn't have sufficient permissions to the key vault for backup of encrypted VMs](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#troubleshooting-errors) <br>
- [ExtentionOperationFailed - VMSnapshot extension operation failed](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#ExtentionOperationFailed-vmsnapshot-extension-operation-failed) <br>
- [BackUpOperationFailed / BackUpOperationFailedV2 - Backup fails, with an internal error](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#backupoperationfailed--backupoperationfailedv2---backup-fails-with-an-internal-error) <br>

## **Recommended Documents**

* [Azure virtual machine backup troubleshooting guide](https://azure.microsoft.com/documentation/articles/backup-azure-vms-troubleshoot/)
