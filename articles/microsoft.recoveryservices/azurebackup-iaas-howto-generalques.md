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

Before filing a support ticket you can find answers to many common questions:<br>

**Vault**<br>
[How to change my vault storage replication type from **GRS to LRS**?](https://docs.microsoft.com/azure/backup/backup-create-rs-vault#how-to-change-from-grs-to-lrs-after-configuring-backup)<br>
How to move:  [Azure VM across Resource Group/Vault](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#how-do-i-move-a-vm-backed-up-by-azure-backup-to-a-different-resource-group); Vault across [Resource Group](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-different-resource-group)/[Subscription](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-a-different-subscription)<br>
Moving Recovery points across Vaults/Subscription is not supported <br>

**Backup**<br>
[Can I **exclude disks** that I do not want to backup?](https://azure.microsoft.com/updates/excludediskpreview/)<br>
[How do I **cleanup/extend the retention period** of Recovery points?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#manage-backup-policy-for-a-vm)<br>
[What happens to the existing recovery points if I change the policy?](https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#what-happens-when-i-change-my-backup-policy)<br>
[How do I take **multiple backups per day**? ](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#run-an-on-demand-backup)<br>
[What are application-consistent and crash-consistent snapshots?](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#snapshot-consistency)<br>

**Restore**<br>
[How to **restore individual files** from VM backup](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm)<br>
[How to **restore an Encrypted VM**](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#restore-an-encrypted-vm)?<br>
[How to create a VM from restored disks using Azure PowerShell?](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks)<br>
How to restore VM to ['alternate location'](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#create-a-vm) or ['replace my original VM'](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#replace-existing-disks)?<br>
[How to enable **cross region restore**?](https://docs.microsoft.com/azure/backup/backup-create-rs-vault#set-cross-region-restore)<br>
Restore VM with special configurations - [Dynamic disks](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#dynamic-disks), [Windows storage spaces](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#windows-storage-spaces), [LVM/Raid arrays](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#lvmraid-arrays)<br>
[Guidance for recovering files from VM backups with large disks](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#file-recovery-from-virtual-machine-backups-having-large-disks)<br>
[What are the available options to restore an Azure VM with managed/unmanaged (or) encrypted/un-encrypted configurations?](https://docs.microsoft.com/azure/backup/about-azure-vm-restore#restore-scenarios)<br>

**Delete backups**<br>
[How to delete VM that is in **soft delete state**?](https://docs.microsoft.com/azure/backup/backup-azure-security-feature-cloud)<br>
[How to **stop protecting a virtual machine** with retain data (or) delete data?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#stop-protecting-a-vm)<br>
[How to delete Backup data?](https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#delete-backup-data)<br>
[How to delete a Recovery Services vault?](https://docs.microsoft.com/azure/backup/backup-azure-delete-vault)<br>

**Backup Reports/Alerts**<br>
[How to **check backup data size** for backup items?](https://docs.microsoft.com/azure/backup/configure-reports)<br>
Understanding Azure Backup [**pricing**](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#backup-costs) and [charges](https://azure.microsoft.com/pricing/details/backup/)<br>
[Configure](https://docs.microsoft.com/azure/backup/configure-reports) and [view](https://docs.microsoft.com/azure/backup/configure-reports#what-happened-to-the-power-bi-reports) Backup report using Power BI<br>
[Configure Notifications](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-built-in-monitor#notification-for-backup-alerts) for backup Alerts through Recovery Services vault <br>
[Monitor Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#using-log-analytics-workspace) and [create Alerts](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#create-alerts-by-using-log-analytics) using Log Analytics<br>
Monitor [Alerts and Jobs](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-built-in-monitor#backup-jobs-in-recovery-services-vault) through Recovery Services vault<br>

## **Recommended Documents**
- [Complete list of supported, unsupported and know limitations](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas)
- [How to configure Azure VM Backup in Recovery Services vault](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#create-a-vault)<br>
- [Enable Backup during VM creation](https://docs.microsoft.com/azure/backup/backup-during-vm-creation)<br>
- [How to restore from an existing Azure backup?](https://docs.microsoft.com/azure/backup/about-azure-vm-restore)<br>
- [How to restore Azure VM data in Azure portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms)?<br>
- [How to troubleshoot permission issues during configure protection?](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault)
- [Complete list of Frequently Asked Questions](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq)
- Troubleshoot [common backup failures](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot) and [VM guest Agent and Extension issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout) on Azure virtual machines




