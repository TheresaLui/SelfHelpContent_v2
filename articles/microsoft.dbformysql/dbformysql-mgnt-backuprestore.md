<properties
	pageTitle="Backups and restore options for Azure Database for MySQL"
	description="Backups and restore options for Azure Database for MySQL"
	service="microsoft.dbformysql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="21"
	selfHelpType="resource"
	supportTopicIds="32628381"
	resourceTags="servers, databases"
	productPesIds="16221"
	cloudEnvironments="public"
	articleId="6593edfc-3e01-44e4-a125-8c47e7748b7b"
/>

# Backups and restore options for Azure Database for MySQL

Azure Database for MySQL supports point-in-time restore and geo-restore of a given server. The backups required to support this functionality are taken automatically in the background. Customers do not have direct access to backups taken by the service. To enable geo-restore capabilities, a server must be created with geo-backups enabled.

## **Recommended Documents**

* [Azure Database for MySQL business continuity overview](https://docs.microsoft.com/azure/mysql/concepts-business-continuity)<br>
* [Azure Database for MySQL backup and restore concepts](https://docs.microsoft.com/azure/mysql/concepts-backup)<br>
* [How-to restore a MySQL server using the Azure portal](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal)<br>
* [How-to restore a MySQL server using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
