<properties
	pageTitle="usererrorolrnotsupportedonrpwithdisksexcluded"
	description="usererrorolrnotsupportedonrpwithdisksexcluded"
	infoBubbleText="This RP had some disks excluded during backup, original location restore from such RPs is not supported"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorolrnotsupportedonrpwithdisksexcluded"
	diagnosticScenario="azurebackup-crc-usererrorolrnotsupportedonrpwithdisksexcluded"
	selfHelpType="diagnostics"
	supportTopicIds="32553276"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorOlrNotSupportedOnRpWithDisksExcluded

<!--issueDescription-->
We have identified that your restore operation failed because you have a VM with write accelerator disks, this is an unsupported scenario and the disk has been excluded from backup
<!--/issueDescription-->

## **Recommended Steps**

- Check if your VM is having disk with write accelerator enabled, on Portal > VM > Settings > Disk > [HOST CACHING](https://docs.microsoft.com/azure/virtual-machines/how-to-enable-write-accelerator#enabling-write-accelerator-using-the-azure-portal)
- Check if the VM disk host catching has write accelerator enabled. If it is enabled, then OLR (original location restore) is not supported
- Please review [restore scenarios](https://docs.microsoft.com/azure/backup/about-azure-vm-restore#concepts) and use alternate method to [restore disk](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-disks) as a workaround
