<properties
	pageTitle="UserErrorPermissionDenied"
	description="UserErrorPermissionDenied"
	infoBubbleText="Our backup account AzureWLBackupPluginSvc was denied permission on this datasource."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorpermissiondenied"
	diagnosticScenario="azurebackup-crc-usererrorpermissiondenied"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorPermissionDenied

<!--issueDescription-->
We have identified that backup operation failed because the backup account AzureWLBackupPluginSvc was denied the required permission on the Data Source.
<!--/issueDescription-->

## **Recommended Steps**

* [Ensure the backup account has the required SysAdmin permissions](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#fix-sql-sysadmin-permissions) 
* Trigger an inquiry (perform [Discover DBs](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#set-permissions-for-non-marketplace-sql-vms) operation from portal) to confirm that the issue is resolved
* Retry the backup operation
