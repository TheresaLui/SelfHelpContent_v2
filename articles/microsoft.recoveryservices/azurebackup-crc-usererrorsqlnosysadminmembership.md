<properties
	pageTitle="usererrorsqlnosysadminmembership"
	description="usererrorsqlnosysadminmembership"
	infoBubbleText="Azure Backup service creates a service account “NTService\AzureWLBackupPluginSvc” for all operations and this account needs SQL sysadmin privilege."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorsqlnosysadminmembership"
	diagnosticScenario="azurebackup-crc-usererrorsqlnosysadminmembership"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorSQLNoSysadminMembership

<!--issueDescription-->
We identified that your backup operation failed because the SQL sysadmin privilege is not assigned to this service account. Azure Backup service creates a service account called "NTService\AzureWLBackupPluginSvc" for all operations, and this account requires SQL sysadmin privileges.
<!--/issueDescription-->

## **Recommended Steps**

To check and set the sysadmin permission for the **NT Service\AzureWLBackupPluginSvc** user, perform the below:

* Open the **SQL Server Management Studio** in the **Object Explorer** and expand the **Security** folder
* Select **Logins** folder - a list of users is displayed
* Right-click **AzureWLBackupPluginSvc**, select **Property**, and select **Server Role** to view the roles
* If the **sysadmin** role not assigned, select the **sysadmin** option and click **OK**

If the service and user have the necessary permissions and you're still facing the same issue, perform the below steps:

1. Drop the user "AzureWLBackupPluginSvc"

	* In the **SQL Management Server Studio**, right-click on <parent node> and run the query `DROP LOGIN [NT SERVICE\AzureWLBackupPluginSvc]`

2. Create the "AzureWLBackupPluginSvc" user

	* To create the AzureWLBackupPluginSvc user, run the query `CREATE LOGIN [NT Service\AzureWLBackupPluginSvc] FROM WINDOWS WITH DEFAULT_DATABASE=[master]`

3. Assign the sysadmin role

	* Change the server role to sysadmin with the query `ALTER SERVER ROLE [sysadmin] ADD MEMBER [NT Service\AzureWLBackupPluginSvc]`

## **Recommended Documents**

* [SQL sysadmin permissions](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#fix-sql-sysadmin-permissions)
