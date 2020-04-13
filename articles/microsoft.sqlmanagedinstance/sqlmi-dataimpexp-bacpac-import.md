<properties
	pageTitle="data import, export, sync, replication/Import BACPAC to Managed Instance"
	description="data import, export, sync, replication/Import BACPAC to Managed Instance to BACPAC"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
    ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637268"
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="ccf5c838-b5b3-4d04-b811-a9f0b9ac19c8"
	ownershipId="AzureData_AzureSQLMI"
/>

# Bacpac import

Managed Instance enables you to import data from a `BACPAC` file.

## **Recommended Steps**

If you are experiencing the issues with BACPAC functionality in Managed instance, try some of the following steps:

- Note that BACPAC import can be done with client tools such as [SQL Server Data Tools](https://docs.microsoft.com/sql/ssdt/download-sql-server-data-tools-ssdt) or [sqlpackage.exe](https://docs.microsoft.com/azure/sql-database/sql-database-import#import-from-a-bacpac-file-using-sqlpackage). There is no portal feature that can import a database.
- For bigger databases over 200 GBs, we recommend using [Native restore](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-get-started-restore) from a blob storage or built-in cross instance point-in-time restore to move a database to another instance.
- Make sure that you are using the latest version of the tools that include the latest bug fixes.
- Check is there some [known issue](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#Issues) that might cause the problem that you are experiencing.

## **Recommended Documents**

- [Import a BACPAC using SQL Server Management Studio](https://docs.microsoft.com/sql/relational-databases/data-tier-applications/import-a-bacpac-file-to-create-a-new-user-database)
- [Import a BACPAC using SQLPackage](https://docs.microsoft.com/azure/sql-database/sql-database-import#import-from-a-bacpac-file-using-sqlpackage)
