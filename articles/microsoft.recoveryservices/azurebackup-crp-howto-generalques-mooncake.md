<properties
	pageTitle="Azure backup - howto and general questions"
	description="Azure backup - howto and general questions"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="14"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags="windows"
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="azurebackup-crp-howto-generalques-mooncake"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure backup - howto and general questions

## **Recommended Steps**

- [Changing storage replication type from GRS to LRS is not supported](https://docs.azure.cn/backup/backup-azure-backup-faq#can-i-change-from-grs-to-lrs-after-a-backup)
- [Support matrix](https://docs.azure.cn/backup/backup-support-matrix-iaas) for Azure Virtual Machine backup
- How much time will it take to [Backup](https://docs.azure.cn/backup/backup-azure-vms-introduction#backup-performance) or [Restore](https://docs.azure.cn/backup/backup-azure-vms-introduction#restore-considerations)?
- How to stop/cancel backup job using [PowerShell](https://docs.microsoft.com/powershell/module/azurerm.backup/stop-azurermbackupjob?view=azurermps-6.13.0&viewFallbackFrom=azurermps-5.1.1)?
- To configure Alert/Notification on successful backup jobs use query [all successful Azure VMs backup jobs](https://docs.azure.cn/backup/backup-azure-monitoring-use-azuremonitor#all-successful-azure-vm-backup-jobs) while defining [alert condition](https://docs.azure.cn/backup/backup-azure-monitoring-use-azuremonitor#alert-condition) in Log Analytics
- You can also use [Activity Logs](https://docs.azure.cn/backup/backup-azure-monitoring-use-azuremonitor#using-rs-vaults-activity-logs) to get notifications for events such as backup success for Azure VMs, read [recommendations](https://docs.azure.cn/backup/backup-azure-monitoring-use-azuremonitor#recommendation) before configuring notification using Activity Logs
- [Frequently asked questions](https://docs.azure.cn/backup/backup-azure-vm-backup-faq)


## **Recommended Documents**

* [Configure Azure VMs Backup in Recovery Services vault](https://docs.azure.cn/backup/backup-azure-arm-vms-prepare#create-a-vault)
* [Enable Backup during VM creation](https://docs.azure.cn/backup/backup-during-vm-creation)
* [Enable Backup from VM blade](https://docs.azure.cn/backup/backup-during-vm-creation)
* [Restore VM](https://docs.azure.cn/backup/backup-azure-arm-restore-vms)
* [Restore files from VM backup](https://docs.azure.cn/backup/backup-azure-restore-files-from-vm)
* [Restore VM to alternate location](https://docs.azure.cn/backup/backup-azure-arm-restore-vms#choose-a-vm-restore-configuration)
* [Create VM from restored disks](https://docs.azure.cn/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks)
* Monitor [Alerts and Jobs](https://docs.azure.cn/backup/backup-azure-monitoring-built-in-monitor#backup-jobs-in-recovery-services-vault) through Recovery Services vault
* [Configure Notifications](https://docs.azure.cn/backup/backup-azure-monitoring-built-in-monitor#notification-for-backup-alerts) for backup Alerts through Recovery Services vault
* [Monitor Azure Backup](https://docs.azure.cn/backup/backup-azure-monitoring-use-azuremonitor#using-log-analytics-workspace) and [create Alerts](https://docs.azure.cn/backup/backup-azure-monitoring-use-azuremonitor#create-alerts-using-log-analytics) using Log Analytics
* [Stop protecting virtual machines](https://docs.azure.cn/backup/backup-azure-manage-vms#stop-protecting-a-vm)
* [Delete Backup data](https://docs.azure.cn/backup/backup-azure-manage-vms#delete-backup-data)
* [Delete Recovery Services vault](https://docs.azure.cn/backup/backup-azure-delete-vault)
