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
	cloudEnvironments="public, fairfax, usnat, ussec"
		ownershipId="StorageMediaEdge_Backup"
/>

# Unable to Configure Backup for Azure Virtual Machines

## **Recommended Documents**

- [How can I modify the retention period?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#manage-backup-policy-for-a-vm)
- [What happens to the existing recovery points if I change the retention policy?](https://docs.microsoft.com/azure/backup/backup-architecture#backup-policy-essentials)
- [How do I take multiple backups on the same day?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#run-an-on-demand-backup). **Scheduled backup** is limited to one per day, for multiple backups use on-demand backup as workaround.  
- [Can I exclude disks that I do not want to backup?](https://azure.microsoft.com/updates/excludediskpreview/)
- [How long will the backup data be retained after I stop backup?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#stop-protecting-a-vm)
- [How to stop backup on my VM and delete all the recovery points?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#stop-protecting-a-vm)
- [How to troubleshoot permission issues during configure protection?](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault)
- [How to enable cross region restore?](https://docs.microsoft.com/azure/backup/backup-create-rs-vault#set-cross-region-restore)
- How to configure protection through [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation) and [Azure automation](https://docs.microsoft.com/azure/backup/backup-rm-template-samples)
- [Common configuration errors and how to troubleshoot them](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot)
- [Troubleshooting Azure VM extension and Guest Agent issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout)

### **Additional References**

- [Complete list of supported, unsupported and know limitations](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas) for Azure VM backup
- [How to configure backup of Azure VM from a Recovery Service vault?](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare)
- [How to enable backup during VM creation?](https://docs.microsoft.com/azure/backup/backup-during-vm-creation)
- [How to enable backup after creating a VM?](https://docs.microsoft.com/azure/backup/backup-during-vm-creation#start-a-backup-after-creating-the-vm)
- [Configure](https://docs.microsoft.com/azure/backup/configure-reports) and [view](https://docs.microsoft.com/azure/backup/configure-reports#what-happened-to-the-power-bi-reports) Backup reports using Power BI
* Monitor [Alerts and Jobs](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-built-in-monitor#backup-jobs-in-recovery-services-vault) through Recovery Service vault
* [Configure notifications](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-built-in-monitor#notification-for-backup-alerts) for backup alerts through Recovery Service vault
* [Monitor Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#using-log-analytics-workspace) and [create alerts](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#create-alerts-by-using-log-analytics) using Log Analytics
* [How to delete Backup data?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#delete-backup-data)<br>
* [How to delete Recovery Services vault?](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault)<br>
* Azure VM backup - [Frequently asked questions](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq)
