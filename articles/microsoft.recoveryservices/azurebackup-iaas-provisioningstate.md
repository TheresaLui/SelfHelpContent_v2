<properties
	pageTitle="Diagnose and resolve issues with Windows Azure virtual machine ProvisioningStateFailed"
	description="Diagnose and resolve issues with Windows Azure virtual machine ProvisioningStateFailed"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32783167"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="baa7233f-a514-4b71-aa34-096a5f6ab0c5"
	ownershipId="StorageMediaEdge_Backup"
/>

# Diagnose and resolve issues with Windows Azure ProvisioningStateFailed

## **Recommended Steps**

- To resolve common VM extension issues, follow these [step-by-step instructions](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-3-check-azure-vm-extension-health). 
- Azure Backup service uses VMSnapshot extension. To do a VM backup, **first ensure that the VMSnapshot extension is healthy** by following [these prechecks and requirements](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-4-check-azure-backup-vm-extension-health)**
- [How to troubleshoot Azure VM extension issues](https://docs.microsoft.com/azure/virtual-machines/extensions/overview#troubleshoot-extensions)

**Common error codes**

- My backup operation failed with error [*UserErrorVmProvisioningStateFailed - The VM is in failed provisioning state*](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorvmprovisioningstatefailed---the-vm-is-in-failed-provisioning-state)
- My backup operation failed with error [*GuestAgentSnapshotTaskStatusError - Could not communicate with the VM agent for snapshot status*](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#guestagentsnapshottaskstatuserror---could-not-communicate-with-the-vm-agent-for-snapshot-status)
- My backup operation failed with error [*ExtensionSnapshotFailedNoNetwork - Snapshot operation failed due to no network connectivity on the virtual machine*](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#ExtensionSnapshotFailedNoNetwork-snapshot-operation-failed-due-to-no-network-connectivity-on-the-virtual-machine)
- My backup operation failed with error [*ExtensionFailedVssWriterInBadState - Snapshot operation failed because VSS writers were in a bad state*](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#extensionfailedvsswriterinbadstate---snapshot-operation-failed-because-vss-writers-were-in-a-bad-state)


**Additional references**
- [A complete list of supported, unsupported, and known limitations](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas) for Azure VM backup
- Before you enable Azure VM backup, review the [best practices](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#best-practices)

## **Recommended Documents**

- [Common configuration errors and how to troubleshoot them](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot)
- [Troubleshooting Azure VM extension and Guest Agent issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout)
- [Azure VM backup FAQ](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq)
