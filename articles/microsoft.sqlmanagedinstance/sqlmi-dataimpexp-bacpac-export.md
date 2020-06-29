<properties
	pageTitle="data import, export, sync, replication/export from Managed Instance to BACPAC"
	description="data import, export, sync, replication/export from Managed Instance to BACPAC"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
    ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637261"
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="39ddd5e1-c060-449a-bc13-f16a7ac3ff77"
	ownershipId="AzureData_AzureSQLMI"
/>

# Bacpac export

Managed Instance enables you to export data to a `BACPAC` file.

## **Recommended Steps**

If you are experiencing the issues with BACPAC functionality in Managed instance, try some of the following steps:

- Note that BACPAC export can be done with client tools such as [SQL Server Data Tools](https://docs.microsoft.com/sql/ssdt/download-sql-server-data-tools-ssdt) or [sqlpackage.exe](https://docs.microsoft.com/azure/sql-database/sql-database-export#export-to-a-bacpac-file-using-the-sqlpackage-utility). There is no portal feature that can export a database.
- For bigger databases over 200 GBs, we recommend using [Native COPY_ONLY backups](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Native-database-backup-in-Azure-SQL-Managed-Instance/ba-p/386154) to blob storage or built-in cross instance point-in-time restore to move database to another instance.
- Make sure that you are using the latest version of the tools that include the latest bug fixes.
- Check is there some [known issue](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#Issues) that might cause the problem that you are experiencing.

## **Recommended Documents**

- [Export to BACPAC using SQL Server Management Studio](https://docs.microsoft.com/sql/relational-databases/data-tier-applications/export-a-data-tier-application)
- [Export to BACPAC using SQLPackage](https://docs.microsoft.com/azure/sql-database/sql-database-export#export-to-a-bacpac-file-using-the-sqlpackage-utility/)

