<properties
	pageTitle="SQL Database create database from backup"
	description="SQL Database create database from backup"
	service="microsoft.sql"
	resource="servers"
	authors="andikshi"
    ms.author="andikshi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32689884"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="sql-createordropresources-createdatabasefrombackup"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# Issues while creating a database from backup

### Creating database from other platforms

You can import a SQL Server database into a database in Azure SQL Database using a BACPAC file. You can import the data from a BACPAC file stored in Azure Blob storage (standard storage only) or from local storage in an on-premises location. To maximize import speed by providing more and faster resources, scale your database to a higher service tier and compute size during the import process. You can then scale down after the import is successful.

* [Exporting a bacpac](https://docs.microsoft.com/azure/sql-database/sql-database-export)<br>
* [Importing a bacpac](https://docs.microsoft.com/azure/sql-database/sql-database-import?tabs=azure-powershell)

### Using Azure SQL Database backups

Azure SQL Database automatically creates the database backups that are kept for the duration of the configured retention period. It uses Azure read-access geo-redundant storage (RA-GRS) to ensure the backups are preserved even if the datacenter is unavailable.

* [Automated backups](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups?tabs=single-database)<br>
* [Recovery using backups](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups)<br>
* [Long-term backup retention](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-retention)

### Limitations

Importing to a database in elastic pool isn't supported. You can import data into a single database and then move the database to an elastic pool.<br>
Creating database from .bak files to Azure SQL PAAS is not supported, you need to create a .Bacpac or .Dacpac file.


## **Recommended Documents**

* [Discussion of the entire SQL Server database migration process, including performance recommendations](https://docs.microsoft.com/azure/sql-database/sql-database-single-database-migrate)<br>

