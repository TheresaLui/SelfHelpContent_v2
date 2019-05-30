<properties
	pageTitle="UserErrorLogBackupFailedAsRecoveryModelChanged"
	description="UserErrorLogBackupFailedAsRecoveryModelChanged"
	infoBubbleText="Make sure the node that can take the requested backup type is reachable, and has the extension services running."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorlogbackupfailedasrecoverymodelchanged"
	diagnosticScenario="azurebackup-crc-usererrorlogbackupfailedasrecoverymodelchanged"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error UserErrorLogBackupFailedAsRecoveryModelChanged

<!--issueDescription-->
We have identified that the log backup failed because the data source's of the  recovery model has changed since the last successful backup.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue perform the below steps based on the type of backup and retry the operation.

* If this error occur during scheduled backup then Azure Backup service will Autoheal this issue with a full backup. 
* In case of on-demand back, trigger a full backup.
