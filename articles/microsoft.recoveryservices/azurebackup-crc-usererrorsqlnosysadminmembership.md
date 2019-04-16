<properties
	pageTitle="usererrorsqlnosysadminmembership"
	description="usererrorsqlnosysadminmembership"
	infoBubbleText="Azure Backup service creates a service account “NTService\ AzureWLBackupPluginSvc” for all operations and this account needs SQL sysadmin privilege."
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
	cloudEnvironments="public"
/>

# UserErrorSQLNoSysadminMembership We identified that your backup operation failed because the SQL sysadmin privilege is not assigned to this service account **NTService\AzureWLBackupPluginSvc**

<!--issueDescription-->
## **Azure Backup service creates a service account NTService\ AzureWLBackupPluginSvc for all operations and this account needs SQL sysadmin privilege**
<!--/issueDescription-->

## **Recommended Steps**

To check and set the sysadmin permission for the **NT Service\AzureWLBackupPluginSvc** user, perform the below:

* Open the **SQL Server Management Studio**, in the **Object Explorer** expand the **Security** folder.
* Select **Logins** folder, a list of users are displayed.
* Right-click **AzureWLBackupPluginSvc**, select **Property** and then select **Server Role** to view the roles.
* If the **sysadmin** role not assigned then select the **sysadmin** option and click **OK**.

If the service and user have the necessary permissions, and you're still facing the same issue then perform the below steps:

**Steps 1**: Drop the user AzureWLBackupPluginSvc

In the **SQL Management Server Studio** right-click on <parent node> and run the below query:

` DROP LOGIN [NT SERVICE\AzureWLBackupPluginSvc] `

**Steps 2**: Create the AzureWLBackupPluginSvc

To create the AzureWLBackupPluginSvc user, run the below query

` CREATE LOGIN [NT Service\AzureWLBackupPluginSvc] FROM WINDOWS WITH DEFAULT_DATABASE=[master] `

**Steps 3**: Assign the sysdmin role

To alter the server role to sysadmin, run the below query

` ALTER SERVER ROLE [sysadmin] ADD MEMBER [NT Service\AzureWLBackupPluginSvc]  `

## **Recommended Document**
To fix SQL sysadmin permissions section, see [article](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#fix-sql-sysadmin-permissions)
