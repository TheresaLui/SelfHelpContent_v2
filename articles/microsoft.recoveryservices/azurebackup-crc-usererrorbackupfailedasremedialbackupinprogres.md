<properties
	pageTitle="UserErrorBackupFailedAsRemedialBackupInProgress"
	description="UserErrorBackupFailedAsRemedialBackupInProgress"
	infoBubbleText="Backup failed because a remedial backup is in progress for this database. Backups on this database will not succeed until the remedial backup is complete"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorbackupfailedasremedialbackupinprogress"
	diagnosticScenario="azurebackup-crc-usererrorbackupfailedasremedialbackupinprogress"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# UserErrorBackupFailedAsRemedialBackupInProgress 

<!--issueDescription-->
We have identified that your backup operation failed because there is already another remedial full backup is in progress.
<!--/issueDescription-->

## **Recommended Steps**

- If you trigger a backup while another full backup is still running it will cause a mismatch of the previous log backup to the current log backup
- Verify if multiple backups have been triggered from HANA native clients. Wait for the remedial backup job to complete before triggering another backup
