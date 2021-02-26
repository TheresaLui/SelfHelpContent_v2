<properties
    pageTitle="Backups and restore options for Azure Database for MySQL"
    description="Backups and restore options for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="bahusse"
    displayOrder="120"
    selfHelpType="generic"
    supportTopicIds="32640067"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="be30fc87-a22e-47e3-b1b5-7a80dc1b3a12"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Long term backup retention for Azure Database for MySQL

**Retention less than 7 days or beyond 35 days?** 

The default [backup retention](https://docs.microsoft.com/azure/mysql/concepts-backup) period is 7 days and can be increased up to 35 days. In Azure MySQL Single server, you can't set retention for less than 7 days or beyond 35 days. But you can [Automate backups of your Azure Database for MySQL server to azure storage for longer term retention](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/automate-backups-of-your-azure-database-for-mysql-server-to/ba-p/1791157). For Azure Database for MySQL Flexible servers, you can reduce the backup period to minimum 1 day.

Long-term retention backups are currently not natively supported by the service. You have the option to use `mysqldump` to take backups and store them for long-term retention. Third-party solutions are available. The Azure engineering team is currently working on native support for long-term retention backups.

**Exporting Azure Database for MySQL database using MySQL Workbench?** 

Read [How to export MySQL database using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench)

**Backing up Azure Database for MySQL to Blog Storage?** 

If you want to back up Azure Database for MySQL to a Blob storage, see [Backup Azure Database for MySQL to a Blob Storage](https://techcommunity.microsoft.com/t5/Azure-Database-for-MySQL/Backup-Azure-Database-for-MySQL-to-a-Blob-Storage/ba-p/803830)

## **Recommended Documents**

* [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/concepts-business-continuity)
* [Azure Database for MySQL backup and restore concepts](https://docs.microsoft.com/azure/mysql/concepts-backup)
