<properties
	pageTitle="Tools/SQL Server Management Studio"
	description="Tools/SQL Server Management Studio"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
	ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637308,32637289,32637253"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="8d88d916-123d-4da3-bdf4-56a7854fecb4"
	ownershipId="AzureData_AzureSQLMI"
/>

# SQL Server Management Studio an tools

You can use the SQL Server Management Studio and other tools to connect to Managed Instance.

## Recommended Steps

- Make sure you are using the latest version of SQL Server Management Studio. Version must be [18.0 or higher](https://docs.microsoft.com/sql/ssms/download-sql-server-management-studio-ssms).
- Check are you using the latest version of [SQLManagementObjects](https://www.nuget.org/packages/Microsoft.SqlServer.SqlManagementObjects) - version 150 or higher is required.
- Check are you using the latest version of [DacFx Framework](https://www.microsoft.com/download/details.aspx?id=57784&WT.mc_id=rss_alldownloads_all) (18 or higher).
- Make sure that you can reach Managed Instance from the computer where you are running queries. Try to test connectivity with the commands like `tns <managed-instance> -1433`.
- Make sure that you are using some of the [supported versions of client libraries](https://docs.microsoft.com/azure/sql-database/sql-database-connect-query#libraries).
- Make sure that you are using correct [connection parameters](https://docs.microsoft.com/azure/sql-database/sql-database-connect-query#tls-considerations-for-sql-database-connectivity).
- Check are there any [known issues](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#Issues) that are reported.

## **Recommended Documents**

- [Quick-start: Use SQL Server Management Studio to connect and query an Azure SQL database](https://docs.microsoft.com/azure/sql-database/sql-database-connect-query-ssms)
