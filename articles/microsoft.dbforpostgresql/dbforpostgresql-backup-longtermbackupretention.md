<properties
    pageTitle="Long term retention of backups for Azure Database for PostgreSQL"
    description="Backups and restore options for Azure Database for PostgreSQL: Long term retention"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="130"
    selfHelpType="resource"
    supportTopicIds="32639993"
    resourceTags="servers, databases"
    productPesIds="16222"
    cloudEnvironments="public"
    articleId="7a6c959f-0671-48c4-9435-8051e7298f9d"
/>

# Long term retention of backups

Long term retention of backups (longer than 35 days) are currently not natively supported by the service. You have the option to use *pg_dump* to take backups and store them for long term retention. Third party solutions are available.

Native support for long term retention backups is currently being worked on by the Azure engineering team.

## **Recommended Documents**

* [Azure Database for PostgreSQL business continuity overview](https://docs.microsoft.com/azure/postgresql/concepts-business-continuity)<br>
* [Azure Database for PostgreSQL backup and restore concepts](https://docs.microsoft.com/azure/postgresql/concepts-backup)<br>
* [Migrate your PostgreSQL database using dump and restore](https://docs.microsoft.com/azure/postgresql/howto-migrate-using-dump-and-restore)
