<properties
    pageTitle="Backups and restore options for Azure Database for MySQL"
    description="Backups and restore options for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="160"
    selfHelpType="generic"
    supportTopicIds="32640087"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="baebc228-20af-4d96-9dcf-9f5663257124"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Backups and restore options for Azure Database for MySQL

Azure Database for MySQL generally does not support restoring dropped servers. When a server is dropped, the operation cascades to the backups shortly after the server drop operation was initiated.

## **Recommended Steps**

* If you accidentally dropped a server, immediately issue a point-in-time restore request using our [REST API](https://docs.microsoft.com/rest/api/mysql/servers/create#create-a-database-as-a-point-in-time-restore) to a point in time just before the time the server was dropped. You can issue this request within 7 days of accidentally dropping a server. This may enable you to recover the deleted server.


## **Recommended Documents**

* [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/concepts-business-continuity)
