<properties
	pageTitle="UserErrorBCMUnsupportedDiskCount"
	description="UserErrorBCMUnsupportedDiskCount"
	infoBubbleText="Number of data disks attached to the virtual machine exceeded the supported limit."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorbcmunsupporteddiskcount"
	diagnosticScenario="azurebackup-crc-usererrorbcmunsupporteddiskcount"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorBCMUnsupportedDiskCount

<!--issueDescription-->
We have identified that the number of data disks attached to the Virtual Machine has exceeded the supported limit.
<!--/issueDescription-->

## **Recommended Steps**

* To resolve this issue, review the limitations of [data disks attached to a Virtual Machine](https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#are-there-size-limits-for-data-backup)
* Detach some data disks from this virtual machine
* Retry the operation
