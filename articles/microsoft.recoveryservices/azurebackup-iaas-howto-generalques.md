<properties
	pageTitle="Diagnose and resolve issues for Azure Virtual Machine Backup and Restore"
	description="Diagnose and resolve issues for Azure Virtual Machine Backup and Restore"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32612993"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="4cea27ca-0a1a-4382-838f-02a2ed10855d"
	ownershipId="StorageMediaEdge_Backup"
/>

# Diagnose and resolve issues for Azure Virtual Machine Backup and Restore

## **Recommended Steps**
Before filing a support ticket you can find answers to many common questions:
- [How do I change my vault storage replication type from GRS to LRS?](https://docs.microsoft.com/azure/backup/backup-create-rs-vault#how-to-change-from-grs-to-lrs-after-configuring-backup)<br>
- [How do I move an Azure VM to a different Resource Group/Vault while retaining the existing backup?](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#how-do-i-move-a-vm-backed-up-by-azure-backup-to-a-different-resource-group)
- [How to delete VM that is in soft delete state?](https://docs.microsoft.com/azure/backup/backup-azure-security-feature-cloud)
- [How can I modify the retention period in backup policy?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#manage-backup-policy-for-a-vm)
- [What happens to the existing recovery points if I change the retention policy?](https://docs.microsoft.com/azure/backup/backup-architecture#backup-policy-essentials)
- [*Scheduled backup* is limited to one per day, how do I take multiple backups?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#run-an-on-demand-backup)
- [How to enable cross region restore?](https://docs.microsoft.com/azure/backup/backup-create-rs-vault#set-cross-region-restore)
- [Can I exclude disks that I do not want to backup?](https://azure.microsoft.com/updates/excludediskpreview/)
- [How to check backup data size for backup items?](https://docs.microsoft.com/azure/backup/configure-reports)
- Understanding the [cost incurred during Azure backup](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#backup-costs) and [Azure backup pricing calculator](https://azure.microsoft.com/pricing/details/backup/)
- [How to troubleshoot permission issues during configure protection?](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault)
- [Complete list of Frequently Asked Questions](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq)

**Additional References**
- [Complete list of supported, unsupported and know limitations](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas)
- [Azure VM restore scenarios](https://docs.microsoft.com/azure/backup/about-azure-vm-restore)
- [Stop protecting virtual machines](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#stop-protecting-a-vm)
- Troubleshoot [common backup failures](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot) and [VM guest Agent and Extension issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout) on Azure virtual machines
- [Types of Azure VM backup](https://docs.microsoft.com/azure/backup/backup-overview)

## **Recommended Documents**

* [Configure Azure VM Backup in Recovery Services vault](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#create-a-vault)
* [Enable Backup during VM creation](https://docs.microsoft.com/azure/backup/backup-during-vm-creation)
* [How to restore Azure VM data in Azure portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms)?
* [Restore Individual files from VM backup](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm)
* How do I restore entire VM to ['Alternate location than my original VM'](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#create-a-vm) or ['Replacing my original VM'](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#replace-existing-disks)?
* Restore VM Special configurations - [Dynamic disks](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#dynamic-disks), [Windows storage spaces](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#windows-storage-spaces), [LVM/Raid arrays](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#lvmraid-arrays)
* [Guidance for recovering files from VM backups with large disks](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#file-recovery-from-virtual-machine-backups-having-large-disks)
* [How do I restore Encrypted VM](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#restore-an-encrypted-vm)?
* [How to create VM from restored disks using Azure PowerShell?](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks)
* [Configure](https://docs.microsoft.com/azure/backup/configure-reports) and [view](https://docs.microsoft.com/azure/backup/configure-reports#what-happened-to-the-power-bi-reports) Backup report using Power BI
* Monitor [Alerts and Jobs](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-built-in-monitor#backup-jobs-in-recovery-services-vault) through Recovery Services vault
* [Configure Notifications](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-built-in-monitor#notification-for-backup-alerts) for backup Alerts through Recovery Services vault
* [Monitor Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#using-log-analytics-workspace) and [create Alerts](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#create-alerts-by-using-log-analytics) using Log Analytics
* [Delete Backup data](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#delete-backup-data)
* [Delete Recovery Services vault](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault)
*-* How do I move recovery service vault between [resource groups](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-different-resource-group) and [subscriptions?](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-a-different-subscription)
* [What are application-consistent and crash-consistent snapshots?](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#snapshot-consistency)
