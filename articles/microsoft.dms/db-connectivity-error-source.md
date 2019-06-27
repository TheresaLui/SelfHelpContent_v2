<properties
	pageTitle="Error when connecting to source database"
	description="Troubleshooting connectivity issues to source database"
	infoBubbleText=""
	service="microsoft.dms"
	resource="virtualmachines"
	authors="radjaram"
	ms.author="rradjou"
	displayOrder="1"
	articleId="db-connectivity-error-source"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32673582"
	resourceTags=""
	productPesIds="16307"
	cloudEnvironments="public"
/>

# <-- Errors you may encounter when connecting to source database for migration and recommended steps --> 

### SQL Server as source

* **Error**: "SQL connection failed. A network-related or instance-specific error occurred while establishing a connection to SQL Server. The server was not found or was not accessible. Verify that the instance name is correct and that SQL Server is configured to allow remote connections."

	* **Recommended documents**: 

		[Error connecting to source SQL Server when using dynamic port or named instance](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms#error-connecting-to-source-sql-server-when-using-dynamic-port-or-named-instance)


* **Error**: Error 53 - SQL connection failed. (The other codes are -1, 2, 5, 53, 233, 258, 1225, 11001).

	* **Recommended documents**: 

		[Interactive user guide to troubleshoot the connectivity issue](https://support.microsoft.com/help/4009936/solving-connectivity-errors-to-sql-server)
		
		[Prerequisites for migrating SQL Server to Azure SQL Database](https://docs.microsoft.com/azure/dms/pre-reqs#prerequisites-for-migrating-sql-server-to-azure-sql-database)

		[Prerequisites for migrating SQL Server to an Azure SQL Database managed instance](https://docs.microsoft.com/azure/dms/pre-reqs#prerequisites-for-migrating-sql-server-to-an-azure-sql-database-managed-instance)


* **Error 4060 - Login failed**

	Authentication has failed with the target database. Review user actions in [Authentication Errors Page](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error?view=sql-server-2017), and update authentication settings.


## **Recommended Documents**

* [Solving Connectivity errors to SQL Server](https://support.microsoft.com/help/4009936/solving-connectivity-errors-to-sql-server)
