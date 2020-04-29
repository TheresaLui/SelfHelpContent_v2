<properties
	pageTitle="UserErrorMarketPlaceVMNotSupported"
	description="UserErrorMarketPlaceVMNotSupported"
	infoBubbleText="VM creation failed due to Market Place purchase request being not present"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrormarketplacevmnotsupported"
	diagnosticScenario="azurebackup-crc-usererrormarketplacevmnotsupported"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorMarketPlaceVMNotSupported

<!--issueDescription-->
We have identified that your **Restore VM** operation failed because the backed up VM's image (which was originally used to create the VM) no longer exists (no longer supported) in Azure Market Place.
<!--/issueDescription-->

## **Recommended Document**
To resolve this issue use the **Restore Disk** operation using the steps listed in this [article](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#restore-disks).<br/>
Additionally you can use [template](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#use-templates-to-customize-a-restored-vm) to customize a restored VM as per the current plan offering on Azure.
