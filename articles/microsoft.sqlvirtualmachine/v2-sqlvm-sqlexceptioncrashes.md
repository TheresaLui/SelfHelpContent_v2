<properties
	pageTitle="SQL Server exceptions, crashes, dumps"
	description="SQL Server exceptions, crashes, dumps"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740096"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="761cce48-2167-4785-a8b7-bd1c70d0e2ab"
	ownershipId="AzureData_AzureSQLVM"
/>

# SQL Server exceptions, crashes, dumps

Among other reasons, server crashes and dumps can happen if the SQL Server or the operating system is not updated or if there are corruption in the databases.

To avoid such crashes and dumps, please ensure that: 
- SQL Server and its components are [up to date to the latest build](https://support.microsoft.com/help/321185/how-to-determine-the-version-edition-and-update-level-of-sql-server-an)
- Ensure that all databases are [corruption free](https://docs.microsoft.com/sql/relational-databases/maintenance-plans/check-database-integrity-task-maintenance-plan?view=sql-server-ver15)
- Windows operating system and its components like .NET framework are up to date to the latest build

<br>If you do decide to open a service request, **please share the latest SQL dumps (*.mdmp files) and logs** with Microsoft. 

## **Recommended Documents**
* [Where to find information about the latest SQL Server builds](https://support.microsoft.com/help/957826/where-to-find-information-about-the-latest-sql-server-builds)
* [How to use the Sqldumper.exe utility to generate a dump file in SQL Server](https://support.microsoft.com/help/917825/use-the-sqldumper-exe-utility-to-generate-a-dump-file-in-sql-server)
* [Database Engine Error List](https://docs.microsoft.com/sql/relational-databases/errors-events/database-engine-events-and-errors?view=sql-server-ver15)
