<properties
	pageTitle="SalLowDiskSpace"
	description="SalLowDiskSpace error"
	service="microsoft.recoveryservices"
	infoBubbleText="Backup failed due to insufficient space in the cache volume"
	resource="backup"
	authors="srinathv"
 	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-sallowdiskspace"
	diagnosticScenario="azurebackup-crc-sallowdiskspace"
	selfHelpType="diagnostics"
	supportTopicIds="32553276,32553277"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# SalLowDiskSpace error

<!--issueDescription-->
**Backup failed due to insufficient space in the cache volume**

<!--/issueDescription-->

## **Recommended Steps**

To resolve the SalLowDiskSpace issue, complete the below troubleshooting steps and retry the backup operation.

* Ensure VM has the latest backup agent installed
* Ensure that the cache volume has free space corresponding to 5-10 percentage of the backup data size or at least 2.5GB, whichever is greater. If required, switch to a new cache location that meets the specified space requirements.
* If WSB backup is also enabled with MARS backup, ensure there is extra 35 GB of space available in the cache location in addition to above condition

## **Recommended Documents**

* [Azure Backup - switch cache locations](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#backup)
