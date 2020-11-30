<properties
	pageTitle="Backup of Linux Azure virtual machine fails"
	description="Linux VM Snapshot issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32553276"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="493a4d5a-add2-4831-abc4-7352a51b60d2"
	ownershipId="StorageMediaEdge_Backup"
/>

# Backup of Linux Azure Virtual Machine fails

## **Recommended Steps**

For common backup failure issues, follow these [step-by-step instructions](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-by-step-guide-to-troubleshoot-backup-failures)
- Review the supported and unsupported [Linux distributions and dependent Python versions](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#operating-system-support-linux)

**VM/Guest agent error codes**

- [**UserErrorGuestAgentStatusUnavailable**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#UserErrorGuestAgentStatusUnavailable-vm-agent-unable-to-communicate-with-azure-backup) means that the VM agent is unable to communicate with Azure Backup
- [**GuestAgentSnapshotTaskStatusError**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#guestagentsnapshottaskstatuserror---could-not-communicate-with-the-vm-agent-for-snapshot-status) meanst that the VM agent could not be reached for snapshot status
- [**UserErrorVmProvisioningStateFailed**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorvmprovisioningstatefailed---the-vm-is-in-failed-provisioning-state) means that the VM is in failed provisioning state
- [**ExtensionInstallationFailedMDTC/ExtensionSnapshotFailedCOM/ExtensionInstallationFailedCOM** ](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#extensionsnapshotfailedcom--extensioninstallationfailedcom--extensioninstallationfailedmdtc---extension-installationoperation-failed-due-to-a-com-error) means that the backup operation failed due to an issue with the Windows service COM+ System application

**Common error codes**
- [**UserErrorRpCollectionLimitReached**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorrpcollectionlimitreached---the-restore-point-collection-max-limit-has-reached) means that the Restore Point collection max limit has been reached
- [**UserErrorKeyVaultPermissionsNotConfigured**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorkeyvaultpermissionsnotconfigured---backup-doesnt-have-sufficient-permissions-to-the-key-vault-for-backup-of-encrypted-vms) means that backup doesn't have sufficient permissions to the key vault for backup of encrypted VMs
- [**UserErrorRequestDisallowedByPolicy**](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#usererrorrequestdisallowedbypolicy---an-invalid-policy-is-configured-on-the-vm-which-is-preventing-snapshot-operation) means that an invalid policy is configured on the VM, which is preventing the snapshot operation
- [**UserErrorUnableToOpenMount**](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#step-6-closing-the-connection) means that you need to ensure that a previous connection to the backup service is closed after the files are restored


**Other error codes**
- [**ExtensionOperationFailedForManagedDisks**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#ExtensionOperationFailed-vmsnapshot-extension-operation-failed) means that the VMSnapshot extension operation failed
- [**UserErrorCrpReportedUserError**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorcrpreportedusererror---backup-failed-due-to-an-error-for-details-see-job-error-message-details) means that backup failed due to an error. For details, see Job Error Message details.


**Additional references**
- [Complete list of supported and unsupported scenarios and actions, and known limitations](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas) for Azure VM backup
- Review the [best practices before you enable Azure VM backup](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#best-practices)
- How to [configure](https://docs.microsoft.com/azure/backup/backup-azure-linux-app-consistent#steps-to-configure-pre-script-and-post-script) and [troubleshoot](https://docs.microsoft.com/azure/backup/backup-azure-linux-app-consistent#troubleshooting) pre-script and post-script in order to take application-consistent snapshots


## **Recommended Documents**

- [Common configuration errors and how to troubleshoot them](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot)
- [Troubleshooting Azure VM extension and Guest Agent issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout)
- [Azure VM backup FAQ](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq)
