<properties
    pageTitle="Azure Database for MySQL server stuck in restart, startup or recovery"
    description="Azure Database for MySQL server stuck in restart, startup or recovery"
    service="microsoft.dbformysql"
    resource="servers"
    ms.author="bahusse, jtoland"
    displayOrder="40"
    selfHelpType="generic"
    supportTopicIds="32788646"
    resourceTags="servers, databases"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="376daae7-c67c-4fb9-9081-78728c17759e"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Azure Database for MySQL server stuck in restart, startup, or recovery

The time it takes to restore or recover an Azure Database for MySQL server relates directly to the recency of your backup checkpoint.

As a transactional database, MySQL keeps a record of all DML operations and transactions such as Update, Insert, and Delete in InnoDB. During crash recovery, the InnoDB engine looks for a check point label in the log files, as all database modifications before the label are present in the disk image of the database. The InnoDB engine then scans the log files forward from the checkpoint, applying the logged modifications to the database. This process is known as recovery, and the longer it has been since a check point was created, the longer it will take for the server to recover.

## **Recommended documents**

* [Troubleshoot common connectivity issues to Azure Databases for MySQL](https://docs.microsoft.com/azure/mysql/howto-troubleshoot-common-connection-issues)
* [Tutorial: Creating and connecting to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/tutorial-design-database-using-portal)
