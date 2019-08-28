<properties
	pageTitle="How-To: Azure SQL Database Management"
	description="How-To: Azure SQL Database Management"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa, johirsch"
    ms.author="emlisa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630418"
	productPesIds="13491"
	cloudEnvironments="public"
	articleId="29427fe7-6a8b-46fc-aa6d-8d3fd5176098"
/>

# How-To: Azure SQL Database Management

### Shrink database by clearing up unused space

To free up space and shrink log files, use [these console commands](https://docs.microsoft.com/sql/t-sql/database-console-commands/dbcc-shrinkdatabase-transact-sql).

### Trouble dropping a database through Azure Portal

Often, when dropping a database using Azure Portal fails, dropping the database using SQL Server Management Studio will work more reliably. To do this, run "DROP [database name](https://docs.microsoft.com/azure/sql-database/sql-database-connect-query-ssms)" from SSMS. 

### Database not visible in Azure Portal, name still in use, database cannot be deleted

If you cannot recreate a database because the intended name is apparently in use on an existing database but that database is not visible in Azure Portal and cannot be deleted, this usually means that the database does exist but isn't visible in Azure Portal because of the Azure Resource Manager cache becoming desynchronized. When you file your ticket, request an ARM cache resync. We're currently working on detecting and resolving cache synchronization issues automatically so that this won't continue to be an issue.

### Trouble creating a database in Central Australia

Subscription whitelisting is required for provisioning new databases in the Central Australia region. File a request for whitelisting [here](https://azure.microsoft.com/global-infrastructure/australia/contact/).

## **Recommended Documents**

* [Change database name, edition, size and other options](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630418/)<br>
* [Managing Azure SQL Databases using the Azure portal](https://azure.microsoft.com/documentation/articles/sql-database-manage-portal?WT.mc_id=pid:13491:sid:32630418/)
