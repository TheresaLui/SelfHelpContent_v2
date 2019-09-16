<properties
    pageTitle="Dropped server in Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: deleted server"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="170"
    selfHelpType="generic"
    supportTopicIds="32640015"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="d5bcb730-39d9-4889-9dce-0777c7f3c778"
/>

# Restoring a deleted server

Azure Database for PostgreSQL generally does not support restoring a deleted server. When a server is deleted, the operation cascades to the backups shortly after the server delete operation is initiated.

## **Recommended Steps**

* If you accidentally drop a server, immediately issue a point-in-time restore request using our [REST API](https://docs.microsoft.com/rest/api/postgresql/servers/create#create-a-database-as-a-point-in-time-restore) to a point in time just before the time the server was dropped. This may enable you to recover the deleted server.

## **Recommended Documents**

* [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity)
