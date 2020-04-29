<properties
	pageTitle="UserErrorWAEnabledDisksNotSupported"
	description="UserErrorWAEnabledDisksNotSupported"
	infoBubbleText="Generic SQL User Correctable Error."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorwaenableddisksnotsupported"
	diagnosticScenario="azurebackup-crc-usererrorwaenableddisksnotsupported"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorWAEnabledDisksNotSupported

<!--issueDescription-->
We have identified that your VM has a Write Accelerator enabled disk, which is currently not supported by Azure Backup.  
<!--/issueDescription-->

## **Recommended Documents**

* Azure Backup [automatically excludes disks with Write Accelerator enabled during backup](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas#vm-storage-support)
