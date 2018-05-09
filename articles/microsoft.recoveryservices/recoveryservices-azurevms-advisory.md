<properties
	pageTitle="IaaS VM Backup Advisory"
	description="IaaS VM Backup Advisory"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553270"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Advisory questions related to IaaS VM Backup and Restore

## **Recommended Steps**
- [Support matrix](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#supported-operating-systems-for-backup) for Azure IAAS VM backup<br>
- How to: [Backup VM?](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#create-a-recovery-services-vault-for-a-vm), [Restore VM?](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms), [Restore files from VM?](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-files-from-an-azure-vm-backup), [Restore VM to alternate location](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-backed-up-disks)<br>
- How much time will it take to: [Backup?](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#total-vm-backup-time) [Restore?](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#total-restore-time) <br>
- How to stop/cancel backup job using [PowerShell](https://docs.microsoft.com/powershell/module/azurerm.backup/stop-azurermbackupjob?view=azurermps-5.1.1)?<br>
- [Limitation] More than 1 backup job per day is currently not supported for IaaS VM<br>

**Common Issues**<br>
- [VM agent can't communicate with Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#vm-agent-unable-to-communicate-with-azure-backup)<br>
- [Snapshot operation fails because the virtual machine isn't connected to the network](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#snapshot-operation-failed-due-to-no-network-connectivity-on-the-virtual-machine)<br>
- [VMSnapshot extension operation fails](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#vmsnapshot-extension-operation-failed)<br>
- [Backup fails because the VM agent is unresponsive](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#backup-fails-because-the-vm-agent-is-unresponsive)<br>
- [Backup fails, with an internal error](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#backup-fails-with-an-internal-error)<br>
- [Disk configuration is not supported](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#disk-configuration-is-not-supported)<br>
- [Snapshot task delay on VMs with SQL Server](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#troubleshoot-vm-snapshot-issues)<br>
