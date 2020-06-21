<properties
    pageTitle="Backups and restore options for Azure Database for MariaDB"
    description="Backups and restore options for Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="160"
    selfHelpType="generic"
    supportTopicIds="32640149"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="eb1cfd84-8c36-4b22-84c9-5a27fb7cd5b4"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Backups and restore options for Azure Database for MariaDB

Azure Database for MariaDB generally does not support restoring dropped servers. When a server is dropped, the operation cascades to the backups shortly after the server drop operation was initiated.

## **Recommended Steps**

* If you accidentally dropped a server, immediately issue a point-in-time restore request using our [REST API](https://docs.microsoft.com/rest/api/mariadb/servers/create#create-a-database-as-a-point-in-time-restore) to a point in time just before the time the server was dropped. You can issue this request within 7 days of accidentally dropping a server. This may enable you to recover the deleted server.

## **Recommended Documents**

* [Azure Database for MariaDB business continuity overview](https://docs.microsoft.com/azure/mariadb/concepts-business-continuity)
