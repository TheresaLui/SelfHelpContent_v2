<properties
	pageTitle="AzureIaaSVMBackupPerfMoreBackupQueueTime"
	description="AzureIaaSVMBackupPerfMoreBackupQueueTime"
	infoBubbleText="the restore operation is taking long time to complete because of high data churn on the VM"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-azureiaasvmbackupperfmorebackupqueuetime"
	diagnosticScenario="azurebackup-crc-azureiaasvmbackupperfmorebackupqueuetime"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error AzureIaaSVMBackupPerfMoreBackupQueueTime

<!--issueDescription-->
We have identified that your backup operation is taking longer to complete because of high data churn on the VM.
<!--/issueDescription-->

## **Recommended Steps**

This error occurs if backup queue time is greater than 120 minutes at the time of the backup. Consider the following guidelines:

- Check if the backup is scheduled during application production time. If yes, consider moving the backup schedule to non-peak hours.
- Ensure that the previous backup operation is complete before starting a new backup. If you start the backup while the previous backup is in progress, the new backup might fail.
- If data churn onthe VM is more than 2 to 5 percent of original disk size, then backups can be slow.
