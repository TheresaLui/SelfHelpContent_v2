<properties
	pageTitle="Azure IAAS VM File recovery"
	description="Azure IAAS VM File recovery"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32783171"
	resourceTags=""
	productPesIds="15207"
	articleId="f31a72cd-6317-43b9-87db-e74cfecc7a7d"
	cloudEnvironments="public, fairfax, usnat, ussec"
		ownershipId="StorageMediaEdge_Backup"
/>

# Recover files from Azure virtual machine backup

Most users can resolve issues concerning recovering files from Azure virtual machine backup by using the following information.

## **Recommended Documents**

### Common errors

- **Unable to view or mount disk/volume/drives to copy files**
    - Review the [list of unsupported backup/restore configurations:](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#vm-storage-support) Shared disk, Temp drive, Deduplicated Disk, Ultra disk, and disk with write Accelerator enabled
    - [If the backed-up VM has large disks or large number of disk, ensure that they meet all the requirements](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#virtual-machine-backups-having-large-disks)
    - [Choose the correct machine](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#step-2-ensure-the-machine-meets-the-requirements-before-executing-the-script) and make sure it meets the [OS requirements](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#step-3-os-requirements-to-successfully-run-the-script) and [access requirements](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#step-4-access-requirements-to-successfully-run-the-script) to run the ILR script
    - Review the requirements for special restore configurations: [LVM/RAID arrays for Linux VM](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#lvmraid-arrays-for-linux-vms)

- **Exception caught while connecting to target**
    - [Review this article](https://docs.microsoft.com/azure/backup/backup-azure-vm-file-recovery-troubleshoot#exception-caught-while-connecting-to-target)

### Other errors
- [The target has already been logged in via an iSCSI session](https://docs.microsoft.com/azure/backup/backup-azure-vm-file-recovery-troubleshoot#the-target-has-already-been-logged-in-via-an-iscsi-session)
- [iSCSI_TCP module can???t be loaded (or) iSCSI_TCP_module not found](https://docs.microsoft.com/azure/backup/backup-azure-vm-file-recovery-troubleshoot#iscsi_tcp-module-cant-be-loaded-or-iscsi_tcp_module-not-found)
- [Cannot download the ILR script](https://docs.microsoft.com/azure/backup/backup-azure-vm-file-recovery-troubleshoot#you-cant-download-the-script)
- [ILR script failed to run](https://docs.microsoft.com/azure/backup/backup-azure-vm-file-recovery-troubleshoot#the-script-downloads-successfully-but-fails-to-run)


## **Recommended Documents**

- [Step-by-step instructions to **restore individual files/folders** from VM backup](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm)<br>
- Ensure that you have what's required for:
  -  [User permissions](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#mount-recovery-volume-who-can-run-script)
  -  [OS requirements](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#step-3-os-requirements-to-successfully-run-the-script) 
  -  [Access requirements](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#step-4-access-requirements-to-successfully-run-the-script) 

- [Recovering files from an encrypted Azure VM is currently not supported](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#support-for-file-level-restore).    Alternatively, you can [restore disk of the encrypted VM](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#restore-an-encrypted-vm) and copy the required files
- Recover files from VM backups with large disks:
   - [**Windows**](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#for-windows)
   - [**Linux**](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#for-linux) 

- [**UserErrorUnableToOpenMount**](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#step-6-closing-the-connection). Ensure that the previous connection to the backup service is closed after the files are restored.
