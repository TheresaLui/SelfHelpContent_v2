<properties
	pageTitle="UserErrorBackupFailedDBGuidChanged"
	description="UserErrorBackupFailedDBGuidChanged"
	infoBubbleText="Azure Backup service is not able to connect to the SQL instance"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorbackupfaileddbguidchanged"
	diagnosticScenario="azurebackup-crc-usererrorbackupfaileddbguidchanged"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error UserErrorBackupFailedDBGuidChanged

<!--issueDescription-->
We have identified that your Log/Differential backup failed because database GUID has changed since the last successful Full backup. 
<!--/issueDescription-->

## **Recommended Document**
To resolve this issue follow steps listed below:

* If scheduled Differential/Log backups fails with this issue Azure Backup uses auto-heal to trigger a remedial full backup. not further action is required.
* If adhoc Differential/Log backups fails with this issue, then ensure Full backup is taken else, all subsequent adhoc Diff/Log backup will continue to fail with this error code.
