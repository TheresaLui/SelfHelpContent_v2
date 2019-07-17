<properties
	pageTitle="UserErrorParentFullBackupMissing"
	description="UserErrorParentFullBackupMissing"
	infoBubbleText=" First full backup is missing for this datasource."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorparentfullbackupmissingremedial"
	diagnosticScenario="azurebackup-crc-usererrorparentfullbackupmissingremedial"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error UserErrorParentFullBackupMissing

<!--issueDescription-->
We have identified that an adhoc/scheduled backup was triggered before the first ever full backup for the database.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, perform the below steps:

* If scheduled Differential/Log backups fails with this issue, then Azure Backup uses auto-heal to trigger a remedial full backup and no further action is required as it is auto corrected
* If adhoc Differential/Log backups fails with this issue, then ensure full backup is taken else, all the subsequent adhoc Diff/Log backup will continue to fail with this error code
