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

**START HERE**:  To **self-resolve** common backup failure issues, follow these [step-by-step](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-by-step-guide-to-troubleshoot-backup-failures) instructions
- Review the supported/not supported [Linux Operating System and dependent *Python version*](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#operating-system-support-linux)

**Common error codes**

- [**UserErrorGuestAgentStatusUnavailable**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#UserErrorGuestAgentStatusUnavailable-vm-agent-unable-to-communicate-with-azure-backup) - VM agent unable to communicate with Azure Backup
- [**UserErrorVmProvisioningStateFailed**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorvmprovisioningstatefailed---the-vm-is-in-failed-provisioning-state) - The VM is in failed provisioning state
- [**GuestAgentSnapshotTaskStatusError**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#guestagentsnapshottaskstatuserror---could-not-communicate-with-the-vm-agent-for-snapshot-status) -Could not communicate with the VM agent for snapshot status
- [**ExtensionInstallationFailedMDTC/ExtensionSnapshotFailedCOM/ExtensionInstallationFailedCOM** ](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#extensionsnapshotfailedcom--extensioninstallationfailedcom--extensioninstallationfailedmdtc---extension-installationoperation-failed-due-to-a-com-error) - The Backup operation failed due to an issue with Windows service COM+ System application
- [**UserErrorCrpReportedUserError**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorcrpreportedusererror---backup-failed-due-to-an-error-for-details-see-job-error-message-details) - Backup failed due to an error. For details, see Job Error Message Details
- [**UserErrorRequestDisallowedByPolicy**](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#usererrorrequestdisallowedbypolicy---an-invalid-policy-is-configured-on-the-vm-which-is-preventing-snapshot-operation) - An invalid policy is configured on the VM which is preventing Snapshot operation
- [**ExtensionOperationFailedForManagedDisks**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#ExtensionOperationFailed-vmsnapshot-extension-operation-failed) - VMSnapshot extension operation failed
- [**UserErrorKeyVaultPermissionsNotConfigured**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorkeyvaultpermissionsnotconfigured---backup-doesnt-have-sufficient-permissions-to-the-key-vault-for-backup-of-encrypted-vms) - Backup doesn't have sufficient permissions to the key vault for backup of encrypted VMs
- [**UserErrorRpCollectionLimitReached**](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorrpcollectionlimitreached---the-restore-point-collection-max-limit-has-reached) - The Restore Point collection max limit has reached

**Additional reference**
- [Complete list of supported, unsupported and know limitations](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas) for Azure VM backup
- Review the [best practices before you enable Azure VM backup](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#best-practices)
- How to [configure](https://docs.microsoft.com/azure/backup/backup-azure-linux-app-consistent#steps-to-configure-pre-script-and-post-script) and [troubleshoot](https://docs.microsoft.com/azure/backup/backup-azure-linux-app-consistent#troubleshooting) pre-script and post-script to take application consistent snapshot.
- [Can I exclude disks that I do not want to backup?](https://azure.microsoft.com/updates/excludediskpreview/)


## **Recommended Documents**

- [Common configuration errors and how to troubleshoot them](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot)
- [Troubleshooting Azure VM extension and Guest Agent issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout)
- Azure VM backup - [Frequently asked questions](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq)
