<properties
	pageTitle="SQL Service startup or configuration"
	description="SQL Service startup or configuration"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740089"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="590dc858-f3e3-459e-9224-7100e0dff53d"
	ownershipId="AzureData_AzureSQLVM"
/>

# SQL Service startup or configuration
To troubleshoot SQL Server Service startup issues, please check following:

- Is there anything related to the issue in the [SQL error log](https://docs.microsoft.com/sql/tools/configuration-manager/viewing-the-sql-server-error-log?view=sql-server-ver15)? For SQL agent startup issues, you can check [SQL agent logs](https://docs.microsoft.com/sql/ssms/agent/sql-server-agent-error-log?view=sql-server-ver15) as well.
- Are you able to [start the service from command prompt](https://docs.microsoft.com/sql/database-engine/configure-windows/start-stop-pause-resume-restart-sql-server-services?view=sql-server-ver15#CommandPrompt)?
- Does SQL Server Service accounts have [required permissions](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-windows-service-accounts-and-permissions?view=sql-server-ver15)?

## **Recommended Documents**

* [Configure  Service Accounts and Permissions](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-windows-service-accounts-and-permissions?view=sql-server-ver15)