<properties
	pageTitle="Diagnose and resolve issues for Azure Virtual Machine Backup and Restore"
	description="Diagnose and resolve issues for Azure Virtual Machine Backup and Restore"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32783169"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="4cea27ca-0a1a-4382-838f-02a2ed10855d"
	ownershipId="StorageMediaEdge_Backup"
/>

# Diagnose and resolve issues for Azure Virtual Machine Backup and Restore

Most users can diagnose and resolve Azure VM backup and restore issues by using the following information.

## **Recommended Steps**

- [What are the guidance/best practices to improve backup performance?](https://docs.microsoft.com/azure/backup/guidance-best-practices)

**Vault**<br>
- [How do I change my vault storage replication type from **GRS to LRS**?](https://docs.microsoft.com/azure/backup/backup-create-rs-vault#how-to-change-from-grs-to-lrs-after-configuring-backup)<br>
- **How to move an Azure VM** across a [Resource Group or Vault](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#how-do-i-move-a-vm-backed-up-by-azure-backup-to-a-different-resource-group)<br>
- **How to move a Vault** across [Resource Group](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-different-resource-group) or across a [Subscription](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#use-azure-portal-to-move-recovery-services-vault-to-a-different-subscription)<br>
- Moving Recovery points across a Vault or Subscription is not supported. <br>

**Backup**<br>
- [Why is initial backup is taking a long time to complete?](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#why-initial-backup-is-taking-lot-of-time-to-complete)
- [How to backup an **Encrypted Azure VM**](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption)<br>
- How to enable backup using [Azure CLI](https://docs.microsoft.com/azure/backup/quick-backup-vm-cli) / [PowerShell?](https://docs.microsoft.com/azure/backup/quick-backup-vm-powershell)<br>
- Unsupported backup and restore configurations: ***Shared disk***, ***Temp drive***, ***Deduplicated Disk***, ***Ultra disk*** and ***disk with write Accelerator enabled***. [Learn more](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#vm-storage-support).<br>
- [What are application-consistent and crash-consistent snapshots?](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#snapshot-consistency)<br>
- [Backup policies/retention and recovery points behavior](https://docs.microsoft.com/azure/backup/manage-recovery-points)

**Restore**<br>

- [What are the possible or best **restore options available**?](https://docs.microsoft.com/azure/backup/about-azure-vm-restore#restore-scenarios)<br>
- [How to restore an unmanaged disk as managed](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restoring-unmanaged-vms-and-disks-as-managed)<br>
- [How to **restore an Encrypted VM**](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#restore-an-encrypted-vm)?<br>
- [How to create a VM from restored disks using Azure PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks)<br>
- How to restore VM to an [alternate location](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#create-a-vm) or [replace my original VM](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#replace-existing-disks)?<br>
- Restore VM with special configurations: [Dynamic disks](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#dynamic-disks), [Windows storage spaces](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#windows-storage-spaces), [LVM/Raid arrays](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#lvmraid-arrays)<br>


## **Recommended Documents**
- [Complete list of supported and unsupported scenarios and known limitations](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas)
- How to restore from an [existing Azure backup](https://docs.microsoft.com/azure/backup/about-azure-vm-restore) or [restore from Azure portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms)?<br>
- [How to troubleshoot permission issues while configuring protection](https://docs.microsoft.com/azure/backup/backup-rbac-rs-vault)
- [FAQ for Azure VM backup](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq)
- Troubleshoot [common backup failures](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot) and [VM guest Agent and Extension issues](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout) on Azure virtual machines
