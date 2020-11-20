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

- [What are the guidance/best practices to improve backup performance?](https://docs.microsoft.com/en-us/azure/backup/guidance-best-practices)


**Vault**<br>
- [How do I change my vault storage replication type from **GRS to LRS**?](https://docs.microsoft.com/azure/backup/backup-create-rs-vault#how-to-change-from-grs-to-lrs-after-configuring-backup)<br>
- **How to move Azure VM** across [Resource Group/Vault](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#how-do-i-move-a-vm-backed-up-by-azure-backup-to-a-different-resource-group)<br>
- **How to move Vault** across [Resource Group](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-different-resource-group) (or) across [Subscription](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-a-different-subscription)<br>
- Moving Recovery points across Vaults/Subscription is not supported. <br>

**Backup**<br>
- [Why Initial backup is taking lot of time to complete?](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#why-initial-backup-is-taking-lot-of-time-to-complete)
- [How to backup an **Encrypted Azure VM**?](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption)<br>
- How to enable Backup using [Azure CLI](https://docs.microsoft.com/azure/backup/quick-backup-vm-cli) / [PowerShell?](https://docs.microsoft.com/azure/backup/quick-backup-vm-powershell)<br>
- Unsupported Backup/restore configurations: ***Shared disk***, ***Temp drive***, ***Deduplicated Disk***, ***Ultra disk*** and ***disk with write Accelerator enabled***. [Learn more](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#vm-storage-support)<br>
- [What are application-consistent and crash-consistent snapshots?](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#snapshot-consistency)<br>
- [Backup policies/retention and recovery points behaviour](https://docs.microsoft.com/azure/backup/manage-recovery-points)

**Restore**<br>

- [What are the possible/best **restore options available** for me?](https://docs.microsoft.com/azure/backup/about-azure-vm-restore#restore-scenarios)<br>
- [How to restore an unmanaged disk as managed?](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restoring-unmanaged-vms-and-disks-as-managed)<br>
- [How to **restore an Encrypted VM**](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#restore-an-encrypted-vm)?<br>
- [How to create a VM from restored disks using Azure PowerShell?](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks)<br>
- How to restore VM to ['alternate location'](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#create-a-vm) or ['replace my original VM'](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#replace-existing-disks)?<br>
- Restore VM with special configurations - [Dynamic disks](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#dynamic-disks), [Windows storage spaces](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#windows-storage-spaces), [LVM/Raid arrays](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#lvmraid-arrays)<br>


## **Recommended Documents**
- [Complete list of supported, unsupported and know limitations](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas)
- How to restore from an [existing Azure backup](https://docs.microsoft.com/azure/backup/about-azure-vm-restore) or [restore from Azure portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms)?<br>
- [How to troubleshoot permission issues during configure protection?](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault)
- [Complete list of Frequently Asked Questions](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq)
- Troubleshoot [common backup failures](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot) and [VM guest Agent and Extension issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout) on Azure virtual machines
