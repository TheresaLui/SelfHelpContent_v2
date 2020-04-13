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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorLogBackupFailedAsRecoveryModelChanged

<!--issueDescription-->
We have identified that the log backup failed because the data source of the recovery model has changed since the last successful backup.
<!--/issueDescription-->

## **Recommended Steps**

* If this error occur during scheduled backup, Azure Backup service will Autoheal this issue with a full backup
* In case of on-demand backup, trigger a full backup
* Retry the operation
