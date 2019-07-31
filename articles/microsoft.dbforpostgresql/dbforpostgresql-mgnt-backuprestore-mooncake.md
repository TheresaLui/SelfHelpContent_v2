<properties
	pageTitle="Backups and restore options for Azure Database for PostgreSQL"
	description="Backups and restore options for Azure Database for PostgreSQL"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32639968, 32639993, 32639984, 32640011"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="MoonCake"
	articleId="7b83315e-3c52-4fbe-a8f3-ae2c6b5e2976"
/>

# Backups and restore options for Azure Database for PostgreSQL

Azure Database for PostgreSQL supports point-in-time restore and geo-restore of a given server. The backups required to support this functionality are taken automatically in the background. Customers do not have direct access to backups taken by the service. To enable geo-restore capabilities, a server must be created with geo-backups enabled.

## **Recommended Documents**

* [Azure Database for PostgreSQL business continuity overview](https://docs.azure.cn/postgresql/concepts-business-continuity)
* [Azure Database for PostgreSQL backup and restore concepts](https://docs.azure.cn/postgresql/concepts-backup)
* [How-to restore a PostgreSQL server using the Azure portal](https://docs.azure.cn/postgresql/howto-restore-server-portal)
* [How-to restore a PostgreSQL server using the Azure CLI](https://docs.azure.cn/postgresql/howto-restore-server-cli)
