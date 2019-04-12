<properties
	pageTitle="SalLowDiskSpace"
	description="SalLowDiskSpace"
	service="microsoft.recoveryservices"
	infoBubbleText="Backup failed due to insufficient space in the cache volume"
	service="microsoft.recoveryservices"
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
	cloudEnvironments="public"
/>

# SalLowDiskSpace

<!--issueDescription-->
## **Backup failed due to insufficient space in the cache volume**

<!--/issueDescription-->

## **Recommended Steps**
We identified that your backup operation failed due to insufficient space in the cache volume. To resolve this issue, complete the below troubleshooting steps and retry your backup operation.

* Ensure VM has the latest backup agent installed.
* Ensure that the cache volume has free space corresponding to 5-10 percentage of the backup data size or at least 2.5GB, whichever is greater. If required, switch to a new cache location that meets the specified space requirements.
* If WSB backup is also enabled with MARS backup, ensure there is extra 35 GB of space available in the cache location in addition to above condition.

## **Recommended Document**
 To learn more about how to switch cache locations, see [article](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#backup).
