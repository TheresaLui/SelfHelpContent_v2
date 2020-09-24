<properties
    pageTitle="Backups and restore options for Azure Database for MySQL Flexible Server"
    description="Backups and restore options for Azure Database for MySQL Flexible Server"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="150"
    selfHelpType="generic"
    supportTopicIds="32747615"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec, Mooncake"
    articleId="8d7a7037-6804-4673-8fe9-75855a4cbeb3"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Backups and restore options for Azure Database for MySQL Flexible Server

Geo-redundant backups are currently **not support** for flexible server. You can enable local redundant backup which can be configured for within region data redundancy. The backup created can be retained for a period of 1 - 35 days (default of 7 days). The retention window is the similar to the window of how far back in time can be server be restored.

## **Recommended Steps**

*   Geo-redundant backups are not currently supported for Azure Database for MySQL Flexible Server
*   Review the [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-business-continuity) to understand estimated restore times and restore point objectives
*   Review the [Azure Database for MySQL backup and restore concepts](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-backup) to understand supported functionality and regional coverage
*   [How to export MySQL database using MySQL Workbench](https://docs.microsoft.com/azure/mysql/concepts-migrate-import-export#import-and-export-by-using-mysql-workbench)

## **Recommended Documents**

*   [How to restore a MySQL server using the Azure portal](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-restore-mysql-server-portal)
