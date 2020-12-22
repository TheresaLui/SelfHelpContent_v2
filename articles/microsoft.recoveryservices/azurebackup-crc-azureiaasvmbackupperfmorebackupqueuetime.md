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

This error occurs if backup queue time is greater than 120 min at the time of backup. Consider the following guidelines:

- Check if the backup is scheduled during application production time. If yes, consider moving the backup schedule to non-peak hours
- Ensure the previous backup operation is complete before triggering a new backup, if the backup is triggered while the other backup is in progress then the backup might fail
- If data churn on VM is more than 2-5 % of original disk size, then backups can be slow
