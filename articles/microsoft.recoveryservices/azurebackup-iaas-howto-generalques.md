<properties
	pageTitle="IaaS VM Backup How-to and general questions"
	description="IaaS VM Backup How-to and general questions"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32612993"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>
# Advisory questions related to IaaS VM Backup and Restore

## **Recommended documents**
**Common Questions**<br>
- [Support matrix](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#supported-operating-systems-for-backup) for Azure IAAS VM backup<br>
- How to: [Backup VM?](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#create-a-recovery-services-vault-for-a-vm), [Restore VM?](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms), [Restore files from VM?](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-files-from-an-azure-vm-backup), [Restore VM to alternate location](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-backed-up-disks), [Create VM from restored disks](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks)<br>
- How much time will it take to: [Backup?](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#total-vm-backup-time) [Restore?](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#total-restore-time)<br>
- How to stop/cancel backup job using [PowerShell?](https://docs.microsoft.com/powershell/module/azurerm.backup/stop-azurermbackupjob?view=azurermps-5.1.1)<br>
- How to get the list of the Rolls (RBAC) assigned to a user using [powershell?](https://docs.microsoft.com/azure/active-directory/role-based-access-control-manage-access-powershell)<br>
- [Port and URLs required for file restore](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#mount-the-volume-and-copy-files)<br>
- [How to delete recovery service vault](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault)<br>
- Best backup solution for file server backup in azure VM is VM level backups.[Refer to the article](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction)<br>
- [How to restore azure backed-up VM in different Vnet but should be in same subscription and region](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#create-a-new-vm-from-a-restore-point)<br>
- [How to Configure Backup report using PowerBI?](https://docs.microsoft.com/azure/backup/backup-azure-configure-reports)<br>
- [How to restore environment using GRS copy of backup data in case of complete site goes down?](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-a-vm-during-an-azure-datacenter-disaster)<br>
- "UserErrorBackupOperationInProgress" will not trigger the backup alert<br>
