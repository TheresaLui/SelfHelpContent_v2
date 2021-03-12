<properties
  pagetitle="Issues connecting to a newly restored server"
  description="Issues connecting to a newly restored server"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="bahusse, jtoland"
  selfhelptype="Generic"
  supporttopicids="32788629"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="2aac1e28-d2e0-4932-bbec-311ed1fbb980"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Issues connecting to a newly restored Azure Database for MySQL server

Many users resolve related issues by leveraging the following guidance.

## Fix it yourself

* **Successful restore, but still seeing current data in the restored server?**
  
  At times, users report that their point in time restores show recent (current) data in the restored server. This occurs because of an incorrect connection string when connecting to the restored server. For more details, see [Point in Time Restore in Azure database for MySQL and Azure Database for PostgreSQL](https://techcommunity.microsoft.com/t5/azure-database-support-blog/point-in-time-restore-in-azure-database-for-mysql-and-azure/ba-p/772655)

* **Experiencing a user access issue for the restored server/ Access denied?**
  
  If you are encountering this issue, consult the following guides:

  * [Azure MySQL migration best practices](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online)
  * [Export and import MySQL users and privileges to Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/export-and-import-mysql-users-and-privileges-to-azure-database/ba-p/916995)
  * [Tips and Tricks in using mysqldump and mysql restore to Azure Database for MySQL](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/tips-and-tricks-in-using-mysqldump-and-mysql-restore-to-azure/ba-p/916912)

## **Recommended documents**

* Azure Database for MySQL business continuity overview for [Single server](https://docs.microsoft.com/azure/mysql/concepts-business-continuity) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-business-continuity)
* Azure Database for MySQL backup and restore concepts for [Single Server](https://docs.microsoft.com/azure/mysql/concepts-backup) and [Flexible Servers](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-backup-restore)
* How-to restore a MySQL server using the Azure portal [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-portal) and [Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-restore-server-portal)
* How-to restore a MySQL server using the Azure CLI [Single server](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
* [How to restore a MySQL server using the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-restore-server-cli)
