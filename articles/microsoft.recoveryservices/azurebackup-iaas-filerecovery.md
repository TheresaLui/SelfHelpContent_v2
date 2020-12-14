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

## **Recommended Documents**

- [Step-by-step instructions to **restore individual files/folders** from VM backup](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm)<br>
- Ensure that you have all the required [user permissions](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#mount-recovery-volume-who-can-run-script); [OS requirements](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#step-3-os-requirements-to-successfully-run-the-script); and [access requirements](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#step-4-access-requirements-to-successfully-run-the-script) to run the script for file recovery
- [Recovering files from an encrypted Azure VM is currently not supported](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#support-for-file-level-restore). Alternatively, you can [restore disk of the encrypted VM](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#restore-an-encrypted-vm) and copy the required files
- Special restore configuration requirements for [**LVM/RAID arrays for Linux VM**](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#lvmraid-arrays-for-linux-vms)
- Guidance for recovering files from VM backups with large disks: [for **Windows**](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#for-windows); [for **Linux**](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#for-linux)<br>
- [**UserErrorUnableToOpenMount**](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#step-6-closing-the-connection). Ensure that the previous connection to the backup service is closed after the files are restored.


## **Recommended Documents**

- [What are the possible and the best **restore options available**?](https://docs.microsoft.com/azure/backup/about-azure-vm-restore#restore-scenarios)<br>
