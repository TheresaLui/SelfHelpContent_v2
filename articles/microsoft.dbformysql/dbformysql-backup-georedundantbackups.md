<properties
    pageTitle="Backups and restore options for Azure Database for MySQL"
    description="Backups and restore options for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="150"
    selfHelpType="generic"
    supportTopicIds="32640059"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec, Mooncake"
    articleId="9ff641ce-1994-4202-873f-a1d0aedb4bd6"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Backups and restore options for Azure Database for MySQL

Geo-redundant backups can be configured at the time an Azure Database for MySQL server is created. If configured, the last known good backup is geo-redundantly store and a new server can be created in a different Azure region. Geo-restore does not allow you to chose a point in time, but rather always restores to the last known good state. Restoring individual databases within a server is not supported.

**NOTE**: **This functionality is currently only supported in Azure Database for MySQL Single server**

## Moving from locally redundant backup storage to geo-redundant storage
Configuring locally redundant or geo-redundant storage for backup is only allowed during server create. Once the server is provisioned, you cannot change the backup storage redundancy option. The only way to move an existing server from locally redundant storage is by recreating a server and migrating the data using [dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore) from old server to new server. Support team cannot migrate the server and migration has to performed by end user using [dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore).


## **Recommended Steps**

* If you try to restore a server in a different region and you are not seeing backups to restore from, make sure that the source server was created with geo-redundant backups turned on
* Review the [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/concepts-business-continuity) to understand estimated restore times and restore point objectives
* Review the [Azure Database for MySQL backup and restore concepts](https://docs.microsoft.com/azure/mysql/concepts-backup) to understand supported functionality and regional coverage
* [How to export MySQL database using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench)

## **Recommended Documents**

* [How to restore a MySQL server using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal)<br>
* [How to restore a MySQL server using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
