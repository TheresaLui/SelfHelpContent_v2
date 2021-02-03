<properties
  pagetitle="Commons Issues with using Azure Database Migration Services&#xD;"
  description="Commons Issues with using Azure Database Migration Services"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="sumuth,bahusse"
  selfhelptype="Generic"
  supporttopicids="32747556"
  resourcetags="servers,databases"
  productpesids="17343"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="f4dcad6d-caa7-462c-b670-c4c51ac2adf2"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Commons Issues with using Azure Database Migration Services

You can do online and offline migrations using Azure database migration services (DMS). Follow the steps below to resolve common issues.

## **Recommended Steps**

* If you get error 1 from storage engine, see [Can't restore database with error "Got error 1 from storage engine"](https://techcommunity.microsoft.com/t5/azure-database-support-blog/azure-database-for-mysql-8211-can-t-restore-database-with-error/ba-p/368896)
* See [Common known issues with DMS](https://docs.microsoft.com/azure/dms/known-issues-azure-mysql-online)
* If you're migrating databases from RDS MySQL instance to Azure Database for MySQL, verify the steps by using [this example for how to migrate from RDS to Single server](https://docs.microsoft.com/azure/dms/tutorial-rds-mysql-server-azure-db-for-mysql-online)
* If you're migrating from on-premises MySQL instance to Azure Database for MySQL Single Server, verify the steps by using [this example for online migration with MySQL](https://docs.microsoft.com/azure/dms/tutorial-mysql-azure-mysql-online)

## **Recommended Documents**

* [Troubleshoot error when connecting to source database](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms-source-connectivity)<br>
* [Common Issues with DMS](https://docs.microsoft.com/azure/dms/known-issues-troubleshooting-dms)
