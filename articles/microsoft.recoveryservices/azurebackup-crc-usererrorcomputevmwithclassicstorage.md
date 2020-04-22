<properties
	pageTitle="UserErrorComputeVmWithClassicStorage"
	description="UserErrorComputeVmWithClassicStorage"
	infoBubbleText="Configuring backup failed due to unsupported VM configuration."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorcomputevmwithclassicstorage"
	diagnosticScenario="azurebackup-crc-usererrorcomputevmwithclassicstorage"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorComputeVmWithClassicStorage

<!--issueDescription-->
We have identified that your backup operation failed because the VM configuration is using an unsupported Classic Storage account.
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, perform the below:

* Move the disks to a Resource Manager storage account and retry the backup operation
* Migrate the VM and storage account from Azure Service Management to Azure Resource Manager

## **Recommended Document**

* [Migrate a storage account from ASM to ARM](https://docs.microsoft.com/azure/virtual-machines/windows/migration-classic-resource-manager-ps?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json#step-62-migrate-a-storage-account)
