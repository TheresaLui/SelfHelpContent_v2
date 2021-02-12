<properties
	pageTitle="Azure Linux VM Restore Limitations"
	description="Limitations when restoring an Azure VM from backup"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="9"
	selfHelpType="generic"
	supportTopicIds="32553297"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9344f1ee-97c8-459c-8a55-58c514b4d2ef"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Linux VM Restore Limitations

## **Recommended Steps**

**Restore scenarios**
- [What are the possible or best **restore options available**?](https://docs.microsoft.com/azure/backup/about-azure-vm-restore#restore-scenarios)<br>
- Steps to restore using [**Cross Region Restore**](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#cross-region-restore)
- [How to restore disks](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-disks) and create a new VM using [ARM templates](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#use-templates-to-customize-a-restored-vm), [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#create-a-vm-from-restored-disks), or [Azure CLI](https://docs.microsoft.com/azure/backup/tutorial-restore-disk)
- How to restore: [selective disk](https://docs.microsoft.com/azure/backup/selective-disk-backup-restore#selective-disk-restore), [encrypted Azure VM](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#restore-an-encrypted-vm), [selective files and folders](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#mount-the-volume-and-copy-files)
- [Guidelines for restoring VM with large disk size (>4TB) and disk count (>16 disks)](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#file-recovery-from-virtual-machine-backups-having-large-disks)
- If you can't find the file or disk to restore, check unsupported restore configurations to see if the disks are backed up: **Temp drive**, **Deduplicated Disk**, **Shared disk** and **Disk with write Accelerator enabled**. [Learn more].(https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#vm-storage-support).
- How to restore to latest or specific recovery point using [the Azure portal](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#select-a-restore-point) or [PowerShell](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-an-azure-vm)
- [How to restore an encrypted VM when KEK (Key Encryption Key) and BEK (BitLocker Encryption Key) do not exist in the key vault](https://docs.microsoft.com/azure/backup/backup-azure-restore-key-secret)
- [Restore a Domain Controller VM](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-vms-with-special-configurations)<br>


**Restore Files**
- [Recovering files from an encrypted Azure VM is currently not supported](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#support-for-file-level-restore). Alternatively, you can [restore disk of the encrypted VM](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#restore-an-encrypted-vm) and copy the required files
- [How to restore files from Azure VM backup](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm)
- Special restore configuration requirements for [cynamic disks, LVM/RAID arrays](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#lvmraid-arrays-for-linux-vms)

**Common restore issues**

- [Permissions and RBAC roles](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#before-you-start) required before performing a restore
- [How to stop or cancel an ongoing restore job](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#restore)

**Restore error codes**
- [UserErrorSkuNotAvailable](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#usererrorskunotavailable---vm-creation-failed-as-vm-size-selected-is-not-available)
- [UserErrorMarketPlaceVMNotSupported](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#usererrormarketplacevmnotsupported---vm-creation-failed-due-to-market-place-purchase-request-being-not-present)
- UserErrorInvalidManagedDiskOperation - Restore failed due to lack of quota. [Learn more](https://docs.microsoft.com/azure/azure-portal/supportability/resource-manager-core-quotas-request).

## **Recommended Documents**

- [Supported and unsupported scenarios for restoring a VM with management configuration changes](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#support-for-vm-management). Example: DC, availability set, V-Net
- [Post restore guidelines, for example, set up static IP, availability set](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#post-restore-steps)
- [Configure static IP address to restored VM](https://docs.microsoft.com/previous-versions/azure/virtual-network/virtual-networks-reserved-private-ip#how-to-add-a-static-internal-ip-to-an-existing-vm)<br>
- Attach an existing NIC to the restored VM:
	- Step 1: [Remove from original VM](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#remove-a-network-interface-from-a-vm)<br>
	- Step 2: [Attach to restored VM](https://docs.microsoft.com/azure/virtual-network/virtual-network-network-interface-vm#vm-add-nic)<br>
- We recommend using SSH-based authentication for Linux VMs. If you are using password-based authentication on the backed up VM, you need to [reset the password](https://docs.microsoft.com/previous-versions/azure/virtual-machines/linux/classic/reset-access-classic) after restore, using the VM Access extension <br>
- [Azure Virtual Machine restore troubleshooting guide](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#restore)<br>
- [Azure VM backup FAQ](https://docs.microsoft.com/azure/backup/backup-azure-vm-backup-faq#restore)
