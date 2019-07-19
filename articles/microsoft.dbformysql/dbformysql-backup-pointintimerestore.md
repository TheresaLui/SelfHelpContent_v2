<properties
    pageTitle="Backups and restore options for Azure Database for MySQL"
    description="Backups and restore options for Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="30"
    selfHelpType="resource"
    supportTopicIds="32640083"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="53cc541f-c3de-406e-93cf-cab3a0842fce"
/>

# Backups and restore options for Azure Database for MySQL

Azure Database for MySQL supports point-in-time restore to any point within the configured backup retention period for a server. The default retention period is 7 days and can be increased to 35 days. The backups required to support this functionality are taken automatically. Because transaction log backups are taking every 5 minutes, restore to a point in time within the last 5 minutes might only be available 5 minutes after the point in time you want to restore to.

## **Recommended Steps**

* Azure that you try to restore to a point in time that is within you configured retention period. Note that we do not backfill the backups if you increase the retention period.
* If you are trying to restore to a point in time within the last 5 minutes and the backup is not yet available, wait for up to 5 minutes and try to restore again

## **Recommended Documents**

* [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/concepts-business-continuity)<br>
* [Azure Database for MySQL backup and restore concepts](https://docs.microsoft.com/azure/mysql/concepts-backup)<br>
* [How-to restore a MySQL server using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal)<br>
* [How-to restore a MySQL server using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
