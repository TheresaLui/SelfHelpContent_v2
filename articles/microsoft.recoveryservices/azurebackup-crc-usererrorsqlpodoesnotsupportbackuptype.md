<properties
  pageTitle="UserErrorSQLPODoesNotSupportBackupType"
	description="UserErrorSQLPODoesNotSupportBackupType"
	infoBubbleText="This SQL database does not support the requested backup type"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorsqlpodoesnotsupportbackuptype"
	diagnosticScenario="azurebackup-crc-usererrorsqlpodoesnotsupportbackuptype"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error UserErrorSQLPODoesNotSupportBackupType

<!--issueDescription-->
We have identified that your backup operation failed because the database recovery model doesn't allow the requested backup type.
<!--/issueDescription-->

## **Recommended Steps**
To resolve UserErrorSQLPODoesNotSupportBackupType issue change the database recovery model.  

This error can happen in the following situations: <br/>

* A database using a simple recovery model does not allow log backup.<br/>
* Differential and log backups are not allowed for a Master database. 

To resolve this issue following [this](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorsqlpodoesnotsupportbackuptype) troubleshooting steps.
