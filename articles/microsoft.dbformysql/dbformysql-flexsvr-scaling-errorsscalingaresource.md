<properties
  pagetitle="Error while scaling a resource in Azure Database for MySQL Flexible Server&#xD;"
  description="Error while scaling a resource in Azure Database for MySQL Flexible Server"
  service="microsoft.dbformysql"
  resource="flexibleservers"
  ms.author="andrela,jtoland"
  selfhelptype="Generic"
  supporttopicids="32747613"
  resourcetags="servers,databases"
  productpesids="17344"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="98ed92cb-eb30-45ae-b80c-bd02f711fa39"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Error while scaling a resource in Azure Database for MySQL Flexible Server

In Azure Database for MySQL Flexible Server, you can scale both compute and storage resources. Scaling compute resources (across compute tiers or vCores) requires a server restart. Scaling storage is an online operation that does not require a restart.

Most users can resolve their issues by considering the following points.

### Considerations

* **Connections are dropped and no new connections can be established while vCores are scaled.**

  vCore scaling requires a server restart. When new connections can't be established, the time it takes for the window to appear varies, but in most cases, it is under a minute. We recommend you implement retry logic so that your application can seamlessly reconnect to the MySQL server after the scale operation is completed. Storage scaling does not cause a restart.

* **Can't scale up the master server when a replica exists, or can't scale down a replica.**

  Before you update a master server configuration with new values, update the replica configuration using equal or greater values. This action ensures the replica can keep up with any changes made to the master.

* The Azure Monitor auto-scale feature is not supported in Azure Database for MySQL. However, you can configure auto-scaling using Azure run books and Python. See [How to auto-scale an Azure Database for MySQL/PostgreSQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177)

## **Recommended documents**

* [Azure Database for MySQL Flexible Server documentation](https://docs.microsoft.com/azure/mysql/flexible-server)
* [Azure Database for MySQL Flexible Server - Compute + storage](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage)
* [Manage Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-manage-portal)