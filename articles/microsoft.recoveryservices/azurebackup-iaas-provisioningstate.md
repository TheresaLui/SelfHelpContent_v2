<properties
	pageTitle="Diagnose and resolve issues with Windows Azure virtual machine ProvisioningStateFailed"
	description="Diagnose and resolve issues with Windows Azure virtual machine ProvisioningStateFailed"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684548"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="baa7233f-a514-4b71-aa34-096a5f6ab0c5"
	ownershipId="StorageMediaEdge_Backup"
/>

# Diagnose and resolve issues with Windows Azure ProvisioningStateFailed

## **Recommended Steps**

**START HERE**:  To **self-resolve** common VM extension issues, follow these [step-by-step](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-3-check-azure-vm-extension-health) instructions
- Azure Backup service uses VMSnapshot extension to take VM backup, **Ensure the VMSnapshot extension is healthy by following the prechecks/requirements mentioned in this [section](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-4-check-azure-backup-vm-extension-health)**
- [How to troubleshoot Azure VM extension issues](https://docs.microsoft.com/azure/virtual-machines/extensions/overview#troubleshoot-extensions)?

**Common error codes**

- My backup operation failed with error [*UserErrorVmProvisioningStateFailed - The VM is in failed provisioning state*](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorvmprovisioningstatefailed---the-vm-is-in-failed-provisioning-state)
- My backup operation failed with error [*GuestAgentSnapshotTaskStatusError - Could not communicate with the VM agent for snapshot status*](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#guestagentsnapshottaskstatuserror---could-not-communicate-with-the-vm-agent-for-snapshot-status)
- My backup operation failed with error [*ExtensionSnapshotFailedNoNetwork - Snapshot operation failed due to no network connectivity on the virtual machine*](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#ExtensionSnapshotFailedNoNetwork-snapshot-operation-failed-due-to-no-network-connectivity-on-the-virtual-machine)
- My backup operation failed with error [*ExtensionFailedVssWriterInBadState - Snapshot operation failed because VSS writers were in a bad state*](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#extensionfailedvsswriterinbadstate---snapshot-operation-failed-because-vss-writers-were-in-a-bad-state)


**Additional reference**
- [Complete list of supported, unsupported and know limitations](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas) for Azure VM backup
- Review the [best practices before you enable Azure VM backup](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#best-practices)


## **Recommended Documents**

- [Common configuration errors and how to troubleshoot them](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot)
- [Troubleshooting Azure VM extension and Guest Agent issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout)
- Azure VM backup - [Frequently asked questions](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq)
