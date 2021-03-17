<properties
	pageTitle="Diagnose and resolve issues with Azure Virtual Machine Windows Guest Agent"
	description="Diagnose and resolve issues with Azure Virtual Machine Windows Guest Agent"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32684549"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1f35691a-9c9f-4176-add6-52866f441644"
	ownershipId="StorageMediaEdge_Backup"
/>

# Diagnose and resolve issues with Azure Virtual Machine Windows Guest Agent

## **Recommended Steps**

**START HERE**:  To **self-resolve** common VM Guest agent issues, follow these [step-by-step](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#step-2-check-azure-vm-guest-agent-service-health) instructions
- Ensure *Azure VM Guest Agent* service is up and running on the latest version, [for Windows](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows#manual-installation), [for Linux](https://docs.microsoft.com/azure/virtual-machines/extensions/update-linux-agent)
- A manual installation of the [Windows VM Guest Agent](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-windows#manual-installation) or [Linux VM Agent](https://docs.microsoft.com/azure/virtual-machines/extensions/agent-linux#installation) may be necessary when you create a custom VM image that is deployed to Azure.
-  Review the supported/not supported [Linux Operating System and dependent *Python version*](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#operating-system-support-linux)
- Review the supported/not supported [Windows Operating System](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#operating-system-support-windows)


**Common error codes**
- [**UserErrorGuestAgentStatusUnavailable** - VM agent unable to communicate with Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#UserErrorGuestAgentStatusUnavailable-vm-agent-unable-to-communicate-with-azure-backup)
- [**GuestAgentSnapshotTaskStatusError** - Could not communicate with the VM agent for snapshot status](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#guestagentsnapshottaskstatuserror---could-not-communicate-with-the-vm-agent-for-snapshot-status)
- [**UserErrorVmNotInDesirableState** - VM is not in a state that allows backups](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#usererrorvmnotindesirablestate---vm-is-not-in-a-state-that-allows-backups)

**Additional reference**
- [Complete list of supported, unsupported and know limitations](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas) for Azure VM backup
- Review the [best practices before you enable Azure VM backup](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#best-practices)

## **Recommended Documents**

- [Common configuration errors and how to troubleshoot them](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot)
- [Troubleshooting Azure VM extension and Guest Agent issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout)
- Azure VM backup - [Frequently asked questions](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq)
